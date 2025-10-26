# 🧩 Verification & Validation for All Use Cases — README (Simple → Complex)

> รวมตัวอย่างการทำ Verification & Validation (V&V) สำหรับระบบหลากหลายระดับ  
> ไล่จากระบบง่าย → ปานกลาง → ซับซ้อน  
> ครอบคลุม Use Case, Functional / Non-Functional Requirements, Verification, Validation, และ Acceptance Criteria  

---

## 🧱 System 1: To-Do List (Easy)

**System Overview:**  
ระบบช่วยจัดการงานประจำวัน ผู้ใช้สามารถเพิ่ม แก้ไข ทำเครื่องหมายเสร็จ และดูรายการงานทั้งหมดได้

```
[User]
  |-- (Add Task)
  |-- (Mark Done)
  '-- (View All Tasks)
```

- **Functional Requirements (FR):**  
  - FR1: เพิ่ม / ลบ / แก้ไขงานได้  
  - FR2: ทำเครื่องหมายว่างานเสร็จแล้ว  
  - FR3: แสดงรายการงานทั้งหมดเรียงตามเวลา  

- **Non-Functional Requirements (NFR):**  
  - Response time ≤ 300 ms  
  - Availability ≥ 99%  
  - UI ใช้งานง่ายภายใน 3 คลิก  

| Category | Description |
|-----------|--------------|
| **Verification** | ตรวจว่า Sequence Diagram มี `addTask()`, `completeTask()` และปรากฏใน Class Diagram; Activity ครบทุกขั้นตอน |
| **Validation** | ผู้ใช้จริงเพิ่มงานและทำเครื่องหมายเสร็จภายใน 30 วินาที โดยไม่เกิด error |
| **Acceptance Criteria (AC)** | Task ถูกบันทึกทุกครั้ง, เวลาเฉลี่ยเพิ่มงาน ≤ 2 วินาที |

---

## 📚 System 2: Library Borrowing System (Medium)

**System Overview:**  
ระบบห้องสมุดออนไลน์สำหรับค้นหา ยืมคืน และจัดการค่าปรับโดยอัตโนมัติ

```
[Member] ------ (Search Book)
   |             (Reserve)
   |
[Librarian] --- (Borrow / Return)
                 (Collect Fine)
```

- **FR:**  
  - FR1: ค้นหาหนังสือด้วยชื่อหรือ ISBN  
  - FR2: ยืม–คืนหนังสือโดยอัตโนมัติ  
  - FR3: คำนวณค่าปรับกรณีคืนช้า  

- **NFR:**  
  - Search latency ≤ 1 s  
  - Data consistency 100%  
  - Log retention ≥ 180 วัน  

| Category | Description |
|-----------|-------------|
| **Verification** | ตรวจว่ามี method `borrow()`, `returnBook()` ใน Class Diagram และปรากฏใน Sequence Diagram; ตรวจ state `Available → Borrowed → Returned` ถูกต้อง |
| **Validation** | จำลองการยืมจริง: due date และค่าปรับคำนวณถูกต้อง; ผู้ใช้เข้าใจหน้าจอ |
| **AC** | ยืมได้ ≤ 5 เล่มต่อคน, ค่าปรับคำนวณถูกต้องทุกกรณี |

---

## 🍔 System 3: Food Delivery Platform (Medium → Complex)

**System Overview:**  
แพลตฟอร์มสั่งอาหารที่เชื่อมต่อระหว่างลูกค้า ร้านอาหาร คนส่ง และระบบจ่ายเงิน

```
[Customer] → (Place Order) → [Restaurant] → (Prepare)
    ↓                                   ↓
 (Track Order)                      [Courier] (Deliver)
    ↓
 [Payment] (Charge)
```

- **FR:**  
  - FR1: สั่งอาหารและชำระเงินออนไลน์  
  - FR2: ร้านรับออเดอร์และอัปเดตสถานะ  
  - FR3: ระบบติดตามตำแหน่งของคนส่ง  

- **NFR:**  
  - p95 API ≤ 2 s  
  - Tracking latency ≤ 3 s  
  - TLS 1.2+, PDPA compliant  

| Category | Description |
|-----------|-------------|
| **Verification** | ตรวจว่า `PaymentService.charge()` อยู่ใน Class Diagram และ message `DeliverOrder()` ตรงกับ Activity |
| **Validation** | ทดสอบสั่งอาหารจริง: ETA ต่างจากจริง ≤ ±10% และผู้ใช้ให้คะแนน ≥ 8/10 |
| **AC** | Delivery success ≥ 99%, ราคาในใบเสร็จตรงกับเมนู |

---

## 🏥 System 4: Clinic Appointment (Moderate)

**System Overview:**  
ระบบจองคิวแพทย์ — ผู้ป่วยสามารถจองคิว ดูตารางหมอ และรับการแจ้งเตือนอัตโนมัติ

```
[Patient] -- (Book Appointment)
     |              |
     |              v
     |         (Receive Notification)
[Staff] ---- (Manage Slots)
[Doctor] --- (Consult & Record)
```

- **FR:**  
  - FR1: ผู้ป่วยจองคิวแพทย์ได้  
  - FR2: ระบบแจ้งเตือนล่วงหน้า 24 ชม.  
  - FR3: แพทย์สามารถบันทึกผลตรวจและใบสั่งยา  

- **NFR:**  
  - Booking time ≤ 2 นาที  
  - Data encrypted (Health data)  
  - Uptime ≥ 99.5%  

| Category | Description |
|-----------|-------------|
| **Verification** | Class `Appointment` มี attributes `date`, `doctor`, `patient`; ตรวจ state `Booked → Checked-In → Completed` |
| **Validation** | ทดสอบจริง: ผู้ป่วยได้รับแจ้งเตือนล่วงหน้าและหมอเห็นรายชื่อถูกต้อง |
| **AC** | แจ้งเตือนถูกต้อง ≥ 95%, Double booking = 0 |

---

## 🅿️ System 5: Smart Parking (Complex)

**System Overview:**  
ระบบที่ตรวจจับป้ายทะเบียน คิดค่าจอด และเปิดไม้กั้นโดยอัตโนมัติ

```
[Driver] ---- (Enter via ANPR)
     |              |
     |              v
     |         (Pay Fee)
     |              |
     |              v
     |         (Exit)
[Cashier] -- (Assist Manually)
```

- **FR:**  
  - FR1: กล้องอ่านป้ายทะเบียน (ANPR)  
  - FR2: ระบบคิดค่าจอดและส่วนลด  
  - FR3: เปิดไม้กั้นเมื่อจ่ายเงินสำเร็จ  

- **NFR:**  
  - ANPR Accuracy ≥ 98%  
  - Gate open ≤ 1 s after payment  
  - Data retention ≥ 30 days  

| Category | Description |
|-----------|-------------|
| **Verification** | ตรวจว่า Sequence Diagram มี `calculateFee()` ↔ Class `ParkingService`; ตรวจ state `Ticket Created → Paid → Closed` |
| **Validation** | ทดสอบจ่ายจริง: ไม้กั้นเปิด ≤ 1 s; ใบเสร็จออกถูกต้อง |
| **AC** | Payment success ≥ 99.5%, Zero false gate open |

---

## 🚍 System 6: Smart Transportation & Road Safety (Advanced)

**System Overview:**  
ระบบจัดการการเดินทางอัจฉริยะที่รวมผู้โดยสาร คนขับ ศูนย์ควบคุม AI และตำรวจเพื่อเพิ่มความปลอดภัย

```
[Passenger] --- (Request Ride)
     |               |
     v               v
(Track ETA)      (Board & Pay)
     |               |
[Dispatcher] -- (Assign Vehicle)
[Driver] ----- (Accept / Navigate)
[AI] --------- (Detect Risky Driving)
[Police] ----- (Enforce)
```

- **FR:**  
  - FR1: ขอรถ / จัดสรร / นำทาง / ชำระเงิน  
  - FR2: AI ตรวจจับพฤติกรรมขับเสี่ยง  
  - FR3: ศูนย์ควบคุมตรวจสอบและบังคับใช้  

- **NFR:**  
  - API latency ≤ 2 s, Tracking ≤ 3 s  
  - AI Precision ≥ 0.95, Recall ≥ 0.90  
  - Availability ≥ 99.8%, Audit 100%, PDPA compliant  

| Category | Description |
|-----------|-------------|
| **Verification** | ตรวจว่า Use Case ↔ Sequence ↔ Class ตรง (`scanQR()`, `charge()`, `assignVehicle()`); State Trip `Assigned → Arrived → OnBoard`; Event `Created → InReview → (Confirmed|Rejected)` |
| **Validation** | ทดสอบ Pilot จริง 2 สัปดาห์: pickup ตรงเวลา ≥ 95%, cancel rate < 5%, AI แจ้งเตือนแม่นยำ (FP < 5%) |
| **AC** | p95 request latency ≤ 2 s, AI accuracy ตามเกณฑ์, 100% review ก่อน enforce |

---

## ✅ Summary Table

| System | Verification (Model) | Validation (Real Test) |
|--------|----------------------|------------------------|
| To-Do List | Method ↔ Class ตรง | ผู้ใช้เพิ่มงานสำเร็จ < 30 s |
| Library | UC↔Seq↔State ครบ | ยืมคืนถูกต้อง + Fine คำนวณถูก |
| Food Delivery | Payment/Deliver match | ETA ต่างจริง ±10% |
| Clinic | Appointment class/state | ผู้ป่วยได้แจ้งเตือนถูกเวลา |
| Parking | Fee calc + state Ticket | Gate เปิดใน 1 s หลังจ่าย |
| Transport | Trip + AI event transition ครบ | Pilot ตรง SLA + AI FP ต่ำ |

---

> 🧠 **จำง่ายในข้อสอบ:**  
> Verification = Build the system right.  
> Validation = Build the right system.  
> (โมเดลตรงสเปก ↔ ระบบตรงใจผู้ใช้)

