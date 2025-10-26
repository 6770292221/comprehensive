# 🚦 Requirements — Smart Transportation & Safety

## 1) ระบบ Smart Bus Request & Scheduling (ระบบ "ขอส่ง" + จัดตารางเดินรถ)

### 1.1 Functional Requirements (FR) — ระบบต้องทำอะไร
- **FR-01 (Request Bus):** ผู้โดยสารส่งคำขอรถผ่านแอปได้ (ตำแหน่ง, จุดหมาย, จำนวนคน)
- **FR-02 (ETA):** ระบบคำนวณและแสดงเวลารถจะมาถึง (ETA) แบบเรียลไทม์
- **FR-03 (Routing):** ระบบจัดเส้นทางอัตโนมัติรวมคำขอที่ใกล้กัน (ride pooling)
- **FR-04 (Assignment):** จัดคันรถ/คนขับให้เหมาะสมตามความจุและระยะทาง
- **FR-05 (Driver App):** คนขับรับงาน, ดูเส้นทาง, แจ้งสถานะ “กำลังไป/ถึงแล้ว/รับผู้โดยสารแล้ว”
- **FR-06 (Stop Management):** เพิ่ม/ลบ/ย้ายจุดรับ-ส่งชั่วคราวได้ตามสภาพจราจร
- **FR-07 (Notification):** แจ้งเตือนผู้โดยสารเมื่อรถใกล้ถึง/เมื่อมีการเปลี่ยนเส้นทาง
- **FR-08 (Payment/Verify):** รองรับตรวจบัตร/จ่ายค่าโดยสาร (ถ้ามี) และยืนยันผู้โดยสารขึ้นรถ
- **FR-09 (Incident Report):** แจ้งเหตุฉุกเฉิน/พฤติกรรมเสี่ยงจากผู้โดยสารหรือคนขับได้
- **FR-10 (Ops Dashboard):** ศูนย์ควบคุมดูแผนที่รถ, ปริมาณคำขอ, KPI เดินรถ, ปัญหาหน้างาน
- **FR-11 (Maintenance):** บันทึกสภาพรถ/อุปกรณ์ และสร้างแจ้งเตือนบำรุงรักษาตามรอบ
- **FR-12 (Data Export):** ส่งออกสถิติการเดินรถ/การใช้บริการเป็น CSV/PDF

### 1.2 Non-Functional Requirements (NFR) — ต้องดีแค่ไหน/อย่างไร
- **Performance**
  - **NFR-P1:** 95% ของคำขอ ETA ต้องคำนวณเสร็จภายใน **2 วินาที**
  - **NFR-P2:** อัปเดตตำแหน่งรถทุก **5–10 วินาที** (end-to-end latency ≤ **3 วินาที**)
- **Availability/Reliability**
  - **NFR-R1:** Uptime ระบบศูนย์กลาง ≥ **99.8%/เดือน**
  - **NFR-R2:** รองรับผู้ใช้พร้อมกันอย่างน้อย **5,000 concurrent** โดย throughput ≥ **200 req/s**
- **Scalability**
  - **NFR-S1:** เพิ่มจำนวนรถ/พื้นที่บริการได้โดย **ไม่ต้องหยุดระบบ** และไม่ให้ p95 latency > **3 วินาที**
- **Security/Privacy**
  - **NFR-SEC1:** เข้ารหัสข้อมูลระหว่างส่ง **TLS 1.2+**, ข้อมูลส่วนบุคคลเข้ารหัสที่พักด้วย **AES-256**
  - **NFR-SEC2:** แยกเก็บพิกัดแบบ **tokenization/anonymization** เมื่อทำ analytics
  - **NFR-SEC3:** ล็อกอิน 2-FA สำหรับแอดมิน/โอเปอร์เรเตอร์
- **Usability/Accessibility**
  - **NFR-U1:** ผู้ใช้ใหม่ต้องสร้างคำขอแรกได้ภายใน **< 60 วินาที**
  - **NFR-U2:** แอปรองรับ **ภาษาไทย/อังกฤษ** และหน้าจอ **WCAG AA** (ขนาดฟอนต์/คอนทราสต์)
- **Maintainability/Operability**
  - **NFR-M1:** deploy เวอร์ชันใหม่แบบ **zero-downtime**
  - **NFR-M2:** มี **health check + alerting** (MTTR < **30 นาที**)
- **Compliance**
  - **NFR-C1:** ดำเนินการตาม **PDPA** (ขอความยินยอม, สิทธิ์ลบข้อมูล, วัตถุประสงค์การใช้)

---

## 2) ระบบ AI Road Safety Monitoring (ตรวจจับพฤติกรรมเสี่ยง/ความเร็ว/ง่วงนอน)

### 2.1 Functional Requirements (FR)
- **FR-01 (In-Vehicle Sensing):** กล้อง/เซนเซอร์ในรถตรวจจับง่วง, ใช้โทรศัพท์, ไม่คาดเข็มขัด
- **FR-02 (Roadside Sensing):** กล้องริมถนนตรวจจับความเร็วเกิน/ฝ่าไฟแดง
- **FR-03 (Event Scoring):** AI ให้คะแนนความเสี่ยงเหตุการณ์ (risk score) ต่อคัน/ต่อคนขับ
- **FR-04 (Real-time Alert):** แจ้งเตือนเสียง/จอในรถ และแจ้งศูนย์เมื่อเสี่ยงสูง
- **FR-05 (Evidence Clip):** เก็บวิดีโอ snapshot 10–20 วินาทีก่อน–หลังเหตุการณ์
- **FR-06 (Ops Console):** เจ้าหน้าที่รีวิวเหตุการณ์, ยืนยัน/ยกเลิก (human-in-the-loop)
- **FR-07 (Enforcement Link):** ส่งต่อเคสยืนยันไปยังงานบังคับใช้/ประกันภัย (ตามสิทธิ์)
- **FR-08 (Analytics):** แผนที่จุดเสี่ยง, heatmap เวลา–สถานที่, เทรนด์ลดอุบัติเหตุ
- **FR-09 (Policy Config):** ตั้งค่าเกณฑ์ความเร็ว, ช่วงเวลาเฝ้าระวัง, รายการพฤติกรรมที่ตรวจจับ
- **FR-10 (Audit Trail):** บันทึกการเข้าถึง/แก้ไข/อนุมัติทุกรายการ

### 2.2 Non-Functional Requirements (NFR)
- **AI Performance/Quality**
  - **NFR-AI1:** สำหรับเหตุ “ใช้โทรศัพท์ขณะขับ” → **Precision ≥ 0.95**, **Recall ≥ 0.90**
  - **NFR-AI2:** p95 inference latency **≤ 200 ms** ต่อเฟรม/เหตุ
  - **NFR-AI3:** มี **bias audit** รายไตรมาส + รายงาน fairness
- **Safety & Governance**
  - **NFR-G1:** ทุกการออกใบเตือน/ปรับ ต้องผ่าน **human review** เว้นเหตุฉุกเฉิน (override policy)
  - **NFR-G2:** เก็บหลักฐานวิดีโอสูงสุด **90 วัน** แล้วทำ **secure purge**
- **Security/Privacy**
  - **NFR-SEC1:** เข้ารหัสสตรีมวิดีโอแบบ **end-to-end**, จำกัดสิทธิ์แบบ **RBAC**
  - **NFR-SEC2:** หน้ากาก/เบลอใบหน้า (privacy masking) ในมุมมองสาธารณะตามกฎหมาย
- **Reliability/Availability**
  - **NFR-R1:** ระบบตรวจจับทำงานแม้เน็ตติดขัด (buffer/edge cache อย่างน้อย **60 นาที**)
  - **NFR-R2:** Uptime ≥ **99.9%** สำหรับศูนย์กลาง (NOC)
- **Interoperability**
  - **NFR-I1:** รองรับ **ONVIF/RTSP** กล้อง, ส่งออกเหตุการณ์เป็น **Webhook/JSON** มาตรฐาน
- **Maintainability**
  - **NFR-M1:** hot-swap โมดูล AI ได้ (model registry + versioning), rollback ได้ใน **< 10 นาที**

---

## 3) ตารางจับคู่ FR ↔ NFR (ตัวอย่าง Mapping ใช้ตอบข้อสอบได้)

| FR | คำอธิบายย่อ | NFR ที่เกี่ยวข้อง (ตัวอย่างวัดได้) |
|----|--------------|-------------------------------------|
| FR-01 (Request Bus) | ส่งคำขอรถ | NFR-P1 (≤2s), NFR-U1 (<60s to first request), NFR-SEC1 |
| FR-03 (Routing) | รวมคำขอ/จัดเส้นทาง | NFR-P2 (update ≤3s), NFR-S1 (scale w/out downtime) |
| FR-07 (Notification) | แจ้งเตือนใกล้ถึง | NFR-P1 (≤2s), NFR-R1 (99.8%) |
| FR-05 AI Alert | แจ้งเตือนพฤติกรรมเสี่ยง | NFR-AI2 (≤200ms), NFR-G1 (human review) |
| FR-06 Evidence | เก็บคลิปเหตุ | NFR-G2 (retention 90 วัน), NFR-SEC1 (E2E encryption) |
| FR-08 Analytics | สถิติความเสี่ยง | NFR-I1 (JSON/Webhook), NFR-SEC2 (masking/anonymize) |

---

## 4) Template (คัดลอกไปกรอกเพิ่มสำหรับโปรเจกต์ของคุณ)
### 4.1 Functional Requirements (เติมตามบริบท)
- **FR-01:** …  
- **FR-02:** …  
- **FR-03:** …  
- **FR-04:** …  
- **FR-05:** …

### 4.2 Non-Functional Requirements (กำหนดให้ “วัดได้” เสมอ)
- **Performance:** p95 latency ≤ … s, update interval … s, throughput ≥ … req/s  
- **Availability/Reliability:** uptime ≥ …%, MTTR < … นาที  
- **Security/Privacy:** TLS …, AES-256 at rest, RBAC, retention … วัน, masking/anonymization  
- **Usability/Accessibility:** time-to-task < … วินาที, รองรับภาษา …, WCAG …  
- **Scalability:** รองรับ concurrent ≥ … โดย p95 latency ไม่เกิน … s  
- **AI Quality (ถ้ามี):** Precision ≥ …, Recall ≥ …, Bias audit ราย … , human-in-the-loop  
- **Compliance:** PDPA / มาตรฐานที่เกี่ยวข้อง …

