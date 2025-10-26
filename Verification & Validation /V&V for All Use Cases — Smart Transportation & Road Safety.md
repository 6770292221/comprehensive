# 🧩 V&V for All Use Cases — Smart Transportation & Road Safety

> ระบบตัวอย่าง: Smart Transportation & Road Safety  
> โมเดลอ้างอิง: Use Case Diagram, Use Case Description, Class Diagram, Sequence Diagram, Behavioral State Machine

---

## 🔑 แนวคิดสั้น ๆ
- **Verification** = ตรวจว่าแบบจำลอง/สเปก “ถูกต้องไหม” (*Build the system right*)  
  - Cross-check: UC ↔ Sequence ↔ Class ↔ Activity/State (ชื่อเมธอด, พารามิเตอร์, ลำดับ, guard/transition, multiplicity)
- **Validation** = ตรวจว่า “ตรงความต้องการผู้ใช้ไหม” (*Build the right system*)  
  - Prototype/UAT/Scenario: ให้ Passenger/Driver/Dispatcher/Police ทดลองตามงานจริง

---

## 📋 ตารางสรุปทั้งระบบ (ภาพรวมเร็ว)

| UC | ชื่อ | Verification (โมเดลต่อโมเดล) | Validation (ทดสอบกับผู้ใช้) | AC (เกณฑ์ยอมรับย่อ) |
|----|------|-------------------------------|------------------------------|----------------------|
| UC1 | Request Ride/Bus | Seq `createRequest()` ↔ Class `RequestSvc.create()`; Activity ตรง UC steps | ผู้โดยสารสร้างคำขอสำเร็จ/แนะนำจุดรับเมื่ออยู่นอกโซน | p95 ≤ 2s, แนะนำจุดรับถูกต้อง |
| UC2 | Track ETA & Notify | Seq update/notify ↔ Class `TrackingSvc.getETA()`, `NotifySvc.push()`; State ไม่เปลี่ยนผิด | ผู้โดยสารเห็นรถขยับ/ETA อัปเดต; แจ้งเตือนเมื่อใกล้ถึง | Update 5–10s, e2e latency ≤ 3s |
| UC3 | Assign & Route | Activity (find→assign→notify) ↔ UC; Class multiplicity vehicle:request ถูก; State `Created→Assigned` | Dispatcher พอใจกับแผน; ไม่มี assign ซ้ำ | Assign ≤ 5s/รอบ, no double-assign |
| UC4 | Driver Accept & Navigate | Seq `acceptJob()`/`updateStatus()` ↔ Class DriverApp; State `Assigned→Going→Arrived` | คนขับกดรับงาน, นำทางถึงจุดรับ | ETA drift ≤ ±15% |
| UC5 | Verify Boarding/Payment | Seq `scanQR()`/`charge()` ↔ Class; State `Arrived→OnBoard` เฉพาะจ่ายสำเร็จ | สแกนสำเร็จ→OnBoard; จ่ายล้มเหลวไม่ขึ้น OnBoard | Pay success ≥ 99.5% |
| UC6 | Report Incident/SOS | Seq `createCase()` ↔ Class Case; State Case `New→Open→Resolved` | ผู้โดยสาร/คนขับกด SOS แล้วศูนย์รับเคสภายในเวลา | TTA (time-to-ack) ≤ 30s |
| UC7 | AI Detect Risky Driving | Seq AI `POST /events`; State Event `Created→InReview` | โมเดลแจ้งเตือนถูกกาลเทศะ; false positive ยอมรับได้ | Prec ≥ 0.95, Rec ≥ 0.90 |
| UC8 | Human Review & Enforcement | Seq reviewer decision; State `InReview→(Confirmed|Rejected)→(Enforced|Closed)` | 100% เคสที่บังคับใช้ผ่าน human review | Zero bypass to Enforced |
| UC9 | Manage Stops/Zones | Seq `upsertStop()`; Impact ไป UC1/3; Schema constraint | โซน/จุดรับอัปเดตสะท้อนในแอปและการจัดสรร | Propagation ≤ 1 min |
| UC10 | Ops Dashboard & Analytics | Seq `getLiveMap()`/`export()` ↔ Class; ไม่แก้สถานะโดยไม่ตั้งใจ | Dispatcher เห็นสด/รายงานตรง | Live map lag ≤ 5s |
| UC11 | Maintenance & Health | Seq `createWorkOrder()`; State Vehicle `Active→OutOfService→Active` | แจ้งเสีย→ถอดจากการจัดสรรทันที | Removal from pool ≤ 30s |

> หมายเหตุ: ตัวเลข AC (Acceptance Criteria) เป็นค่าแนะนำ สามารถปรับตาม SLA ของโครงการจริง

---

## 🧪 V&V ราย Use Case (เต็มทุก UC)

### UC1 — Request Ride/Bus
- **Verification**
  - Seq: `RequestController.create(origin,dest,qty)` → Class: `RequestService.create(req)` มีจริง และ param ตรง
  - Activity ของ UC1 มี step ตรงกับ Use Case Description (เลือกจุดรับ→ตรวจโซน→คำนวณ ETA→ยืนยัน)
  - Constraint: ถ้าอยู่นอกโซน ต้องมี branch “Suggest nearest stop”
- **Validation**
  - UAT ให้ผู้โดยสาร 10 คนลอง: ในโซน/นอกโซน/เน็ตช้า → ผลลัพธ์ตรง Use Case
  - KPI: time-to-first-request < 60s (usability)
- **AC**: p95 `POST /requests` ≤ 2s; แนะนำจุดรับถูกต้อง ≥ 95%

---

### UC2 — Track ETA & Notify
- **Verification**
  - Seq: `TrackingSvc.getETA(tripId)` และ `NotifySvc.push(topic)` ต้องมีใน Class Diagram
  - State Trip ไม่ควรเปลี่ยนเพียงเพราะติดตาม (read-only)
- **Validation**
  - Simulate รถขยับทุก 5–10s → ETA/UI อัปเดตลูกค้า + แจ้งเตือนเมื่อใกล้ถึง
- **AC**: Update interval 5–10s; e2e latency ≤ 3s; Notify ใกล้ถึงในระยะ X เมตร

---

### UC3 — Assign & Route Optimization
- **Verification**
  - Activity: find→assign→notify ตรง UC steps
  - Class multiplicity: `Request 0..1 — 1..1 AssignedVehicle` ชั่วขณะ / `Vehicle 1 — 0..* Assignments`
  - State Trip: `Created→Assigned` ก่อน UC4
  - OCL-like: `Request.assignedVehicle->size() <= 1`, `Vehicle.currentLoad <= capacity`
- **Validation**
  - Simulation 50 คำขอ/10 รถ: ไม่มี double-assign; plan มี ETA ที่มีเหตุผล
- **AC**: รอบ assign ≤ 5s; no double-assign; plan utilization ≥ target

---

### UC4 — Driver Accept & Navigate
- **Verification**
  - Seq: `DriverApp.accept(jobId)`/`updateStatus(Going,Arrived)` ↔ Class
  - State Trip: `Assigned→Going→Arrived`
- **Validation**
  - คนขับจริงทดลอง: รับงาน→นำทางถึงจุดรับ→สถานะ Arrived แสดงฝั่งศูนย์/ผู้โดยสาร
- **AC**: ETA drift ≤ ±15%; status propagation ≤ 2s

---

### UC5 — Verify Boarding/Payment
- **Verification**
  - Seq: `scanQR()` → `PaymentSvc.charge()` → `Trip.setOnBoard()`
  - State Trip: `Arrived→OnBoard` เฉพาะ payment success; failure stay `Arrived`
- **Validation**
  - Case จ่ายสำเร็จ/ล้มเหลว/timeout: UI และสถานะถูกต้อง; ไม่มีทางลัดขึ้น OnBoard เมื่อจ่ายไม่ผ่าน
- **AC**: Payment success ≥ 99.5%; zero false OnBoard

---

### UC6 — Report Incident / SOS
- **Verification**
  - Seq: `SOSController.createCase()` ↔ Class `CaseService.create()`
  - State Case: `New→Open→(Escalated|Resolved)→Closed`
- **Validation**
  - ผู้โดยสาร/คนขับกด SOS → ศูนย์รับแจ้งและติดต่อกลับภายในเกณฑ์
- **AC**: Time-to-ack ≤ 30s; time-to-dispatch ≤ 2 min

---

### UC7 — AI Detect Risky Driving
- **Verification**
  - Seq: AI `POST /events {evidence,score}` → Event State: `Created`
  - State Event: `Created→InReview` เท่านั้นโดยอัตโนมัติ (ไม่มี Enforced ตรง ๆ)
- **Validation**
  - Offline eval: Precision/Recall ตามเกณฑ์; Online shadow test: alarm ไม่ล้น
- **AC**: Precision ≥ 0.95, Recall ≥ 0.90; inference p95 ≤ 200ms

---

### UC8 — Human Review & Enforcement
- **Verification**
  - Seq: `Reviewer.decide(confirm/reject)`; ถ้า confirm&severe → `sendToPolice()`
  - State Event: `InReview→(Confirmed|Rejected)→(Enforced|Closed)`
  - Rule: ห้าม transition Created→Enforced โดยตรง (ต้องผ่าน InReview+Confirmed)
- **Validation**
  - Reviewer ทดลอง 20 เคส: 100% ที่ “Enforced” ต้องมี reviewer + audit log
- **AC**: Zero bypass human review; audit completeness = 100%

---

### UC9 — Manage Stops / Zones
- **Verification**
  - Seq: `ZoneAdmin.upsertStop()`/`upsertZone()` ↔ Class
  - Impact: UC1 ตรวจโซนใหม่; UC3 ใช้แผนใหม่
  - Schema: geometry valid; uniqueness constraints
- **Validation**
  - เพิ่ม/แก้ stop แล้ว client เห็นผลและ assign ใช้ข้อมูลใหม่
- **AC**: Propagation to clients/optimizer ≤ 1 min

---

### UC10 — Ops Dashboard & Analytics
- **Verification**
  - Seq: `Dashboard.getLiveMap()`/`getKPIs()`/`exportReport()` ↔ Class
  - Read-only: ไม่มี side-effect เปลี่ยน state โดยไม่ตั้งใจ
- **Validation**
  - Dispatcher ใช้งานจริง: แผนที่สด lag ต่ำ; รายงานตัวเลขถูก
- **AC**: Live map lag ≤ 5s; export ≤ 10s; KPI accuracy ≥ 99%

---

### UC11 — Maintenance & Health Check
- **Verification**
  - Seq: `Maintenance.createWorkOrder()`/`Vehicle.setOutOfService()` ↔ Class
  - State Vehicle: `Active→OutOfService→Active`; Trip pool เคารพ state
- **Validation**
  - แจ้งเสียแล้วรถหายจากการจัดสรรทันที; ปิดงานคืนเข้า pool
- **AC**: Removal from pool ≤ 30s; return-to-pool ≤ 60s

---

## 🔗 RTM (Traceability Matrix) — ตัวอย่างย่อ

| UC | FR/NFR อ้างอิง | Class/Op | Sequence Msg | State/Activity | Test |
|----|-----------------|----------|--------------|----------------|------|
| UC1 | FR-01, NFR-p95≤2s | RequestSvc.create | POST /requests | Act: check zone | TC-REQ-001 |
| UC5 | FR-05, NFR-pay99.5 | PaymentSvc.charge | scanQR→charge | Arrived→OnBoard | TC-PAY-004 |
| UC7 | FR-07, NFR-Prec/Rec | EventSvc.create | POST /events | Created→InReview | TC-AI-005 |
| UC8 | FR-08, NFR-audit | ReviewSvc.decide | POST /decision | InReview→… | TC-REVIEW-007 |

---

## 🧰 วิธีตรวจ (Verification How-to)
- **Model Consistency Checklist**
  - [ ] ชื่อ **message** ใน Sequence ↔ **operation** ใน Class ตรงกัน  
  - [ ] **พารามิเตอร์/ชนิดข้อมูล** ตรงกับลายเซ็น  
  - [ ] **Activity steps** ตรงกับ UC Description (ไม่มี/ไม่ตก)  
  - [ ] **State transitions** ครบ, มี guard ที่จำเป็น, ไม่มีทางลัดผิดตรรกะ  
  - [ ] **Multiplicity/Constraints** ป้องกันสถานะผิด เช่น double-assign

## 🧪 วิธีทดสอบ (Validation How-to)
- **Scenario/UAT**
  - ตั้ง **เคสใช้งานจริง** ต่อ UC (ปกติ/ทางเลือก/ข้อยกเว้น)  
  - วัด **KPI/AC** ที่วางไว้ (latency, accuracy, success rate)  
  - เก็บ **Feedback Stakeholders** (Passenger/Driver/Dispatcher/Police)

---

## 🧠 สรุปจำง่าย
- พูดถึง “โมเดลไม่ตรงกัน” = **Verification**  
- พูดถึง “ผู้ใช้ลองแล้วไม่ตรงใจ” = **Validation**  
- ครอบคลุมทุก UC ด้วยเกณฑ์วัด (AC) + การเชื่อมโยง (RTM) = ได้คะแนนเต็ม

---
