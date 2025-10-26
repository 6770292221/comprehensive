# 🧩 Model Verification & Validation — Multiple Examples

> จาก Use Case Diagram, Use Case Description, Class Diagram, Sequence Diagram, และ Behavioral (State Machine) Diagram  
> รวมตัวอย่างหลายระบบ: Library, Food Delivery, Transport, Clinic, Parking, Ticketing, Smart Home, Banking

---

## 🎯 Concept Recap

| ประเภท | ความหมาย |
|----------|-----------|
| **Verification** | ตรวจว่าแบบจำลองหรือระบบ "ถูกต้องตามสเปกไหม" (*Build the system right*) |
| **Validation** | ตรวจว่าแบบจำลองหรือระบบ "ตรงความต้องการผู้ใช้ไหม" (*Build the right system*) |

---

## 🧪 Example 1 — Library System (Borrow / Return Book)

### Use Case: UC3 “Borrow Book”
**Actors:** Member, Librarian  
**Goal:** ยืมหนังสือและบันทึกวันครบกำหนด  

| ประเภท | รายละเอียด |
|----------|-------------|
| **Verification** | Sequence Diagram แสดง `Librarian.checkMember()` → `Book.updateStatus("Borrowed")` → `Loan.create()` ต้องมี method เหล่านี้ใน Class Diagram ทุกตัว |
| **Validation** | ทดลองยืมหนังสือจริงใน prototype พบว่าผู้ใช้เข้าใจ flow และระบบคำนวณวันครบกำหนดถูกต้อง |
| **ผลลัพธ์:** | ✅ โมเดลสอดคล้องกัน และระบบตอบโจทย์ผู้ใช้ |

---

## 🧪 Example 2 — Food Delivery System (Place Order)

### Use Case: UC2 “Place Order”
**Actors:** Customer, Restaurant, Payment Gateway  

| Verification | Validation |
|---------------|------------|
| ตรวจว่า message `Customer.placeOrder()` และ `PaymentService.charge()` มีใน Class Diagram | ทดลองสั่งอาหารจริง พบว่า ETA และราคาแสดงถูกต้อง |
| ตรวจ Sequence ↔ Activity: flow ตรงกัน (Create → Pay → Confirm) | ผู้ใช้ยืนยันว่าขั้นตอนเข้าใจง่าย และสามารถสั่งได้จบใน 3 ขั้นตอน |

---

## 🧪 Example 3 — Smart Transportation (Assign Vehicle)

### Use Case: UC3 “Assign & Route Optimization”

| Verification | Validation |
|---------------|------------|
| ตรวจว่า Activity Diagram (Find → Assign → Notify) มี event ตรงกับ Use Case Description | ทดสอบในสถานการณ์จริง 10 คำขอ → ระบบจัดสรรรถถูกต้อง ไม่มีซ้ำ |
| ตรวจ State Machine: `Trip: Created → Assigned → OnBoard` | Dispatcher ยืนยันว่า flow ตรงตามการทำงานจริง |

---

## 🧪 Example 4 — Clinic Appointment System

### Use Case: UC4 “Book Appointment”

| Verification | Validation |
|---------------|------------|
| Class Diagram ต้องมี class `Appointment` พร้อม attribute (date, doctor, patient) | ผู้ป่วยลองจองคิวใน prototype → ยืนยันว่าระบบใช้งานง่าย |
| Sequence Diagram มี `Patient.selectSlot()` → `System.confirm()` → `Doctor.scheduleUpdate()` | การจองถูกบันทึกในฐานข้อมูลจริง และแจ้งเตือนถูกต้อง |

---

## 🧪 Example 5 — Parking System (Check-in / Pay Fee)

### Use Case: UC2 “Pay Parking Fee”

| Verification | Validation |
|---------------|------------|
| ตรวจว่าใน Sequence Diagram มี `Camera.detectPlate()` → `PaymentSystem.calculateFee()` → `Gate.open()` และ method เหล่านี้มีใน Class Diagram | ทดสอบระบบจริง → หลังชำระเงิน ไม้กั้นเปิดภายใน ≤ 1s |
| ตรวจ State Machine: Ticket `Created → Paid → Closed` | ผู้ใช้จริงพอใจความเร็วและค่าจอดคำนวณถูกต้อง |

---

## 🧪 Example 6 — Event Ticketing System (Buy Ticket)

### Use Case: UC2 “Buy Ticket”

| Verification | Validation |
|---------------|------------|
| ตรวจว่าข้อความใน Sequence เช่น `Customer.selectSeat()` → `PaymentService.process()` → `Ticket.generateQR()` ตรงกับ method ใน Class Diagram | ผู้ซื้อทดสอบในระบบจริง → QR ใช้สแกนเข้าหน้างานได้ 100% |
| ตรวจ Activity Diagram มี branch “Cancel / Refund” ตรงกับ Use Case Description | ผู้ใช้ยืนยันว่ากระบวนการขอคืนเงินทำได้จริง |

---

## 🧪 Example 7 — Smart Home (Turn On/Off Device)

### Use Case: UC1 “Control Smart Light”

| Verification | Validation |
|---------------|------------|
| Class Diagram: `SmartLight` ต้องมี method `turnOn()` / `turnOff()` | ผู้ใช้ทดลองใน prototype: กดปุ่มเปิด–ปิดผ่านมือถือแล้วไฟตอบสนองทันที |
| State Machine: Light `OFF → ON → OFF` | สอดคล้องกับพฤติกรรมจริงของอุปกรณ์ |

---

## 🧪 Example 8 — Banking System (Transfer Money)

### Use Case: UC4 “Transfer Funds”

| Verification | Validation |
|---------------|------------|
| ตรวจว่า Sequence Diagram มี `Account.debit()` → `BankAPI.credit()` → `Transaction.log()` และทุก method ปรากฏใน Class Diagram | ทดสอบใน UAT environment พบว่าการโอนสำเร็จและ SMS แจ้งเตือนถูกต้อง |
| ตรวจ State Machine ของ Transaction: `Initiated → Completed → Archived` | ผู้ใช้ยืนยันว่าระบบแสดงสถานะถูกต้องและปลอดภัย |

---

## 📊 Summary Table (รวม 8 ตัวอย่าง)

| ระบบ | Diagram ที่ตรวจ | Verification Focus | Validation Focus |
|------|------------------|--------------------|------------------|
| Library | Use Case ↔ Sequence ↔ Class | Message ↔ Method Consistency | Flow ยืมคืนตรงกับผู้ใช้ |
| Food Delivery | Use Case ↔ Activity ↔ Class | Event ครบในโมเดล | สั่งอาหารจริง Flow ถูก |
| Smart Transport | Use Case ↔ State Machine | Transition ครบ | Dispatcher ยืนยันผลจริง |
| Clinic | Use Case ↔ Sequence ↔ Class | Entity ครบ | ผู้ป่วยเข้าใจขั้นตอนจอง |
| Parking | Sequence ↔ Class ↔ State | Method และ State ตรง | จ่ายเงินแล้วไม้เปิดจริง |
| Ticketing | Activity ↔ Use Case | Branch ครบ | ผู้ใช้พอใจกระบวนการซื้อ |
| Smart Home | Class ↔ State | Method ↔ Behavior | การเปิด–ปิดตรงตามจริง |
| Banking | Use Case ↔ Sequence ↔ State | Message ↔ Operation | ผู้ใช้โอนเงินสำเร็จและปลอดภัย |

---

## 🧠 ข้อคิดสำหรับข้อสอบ

> ถ้าโจทย์พูดถึง “ความไม่สอดคล้องของโมเดล” → คือ **Verification**  
> ถ้าโจทย์พูดถึง “ผู้ใช้ทดสอบจริง / Prototype / UAT” → คือ **Validation**

**ตัวอย่างโจทย์ที่ควรฝึก:**
1. Sequence Diagram มี message ที่ไม่มีใน Class Diagram → Verification  
2. Prototype ไม่แสดงปุ่ม “Confirm Payment” ที่ระบุใน Use Case → Validation  
3. State Machine ข้ามจาก “Created → Completed” โดยไม่มี guard → Verification  
4. ผู้ใช้จริงไม่เข้าใจข้อความแจ้งเตือน → Validation  

---

## ✍️ Quick Template for Answering in Exams

> **Example:**  
> From the “Pay Parking Fee” use case, we verify that all messages in the sequence diagram (detectPlate, calculateFee, openGate) exist as operations in the class diagram.  
> Validation is performed by simulating real user payment at the gate; if the barrier opens within 1 second after payment, the behavior matches the real-world expectation.

---

## 🧩 สรุปจำง่าย (ในข้อสอบเขียน 3–4 บรรทัด)

| หมวด | Verification | Validation |
|-------|---------------|-------------|
| คำถาม | แบบจำลองถูกไหม | ตรงกับผู้ใช้ไหม |
| วิธี | ตรวจโมเดล, Review, Cross-check | Prototype, UAT |
| ตัวอย่าง | UC ↔ Seq ↔ Class consistency | ผู้ใช้ทดสอบจริง |
| คำจำ | *Build the system right* | *Build the right system* |

---
