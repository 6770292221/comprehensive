# 🧾 Lesson 11 – Requirements Validation & Requirements Management  
**Software Requirements Engineering (2110623)**  
Instructor: *Assoc. Prof. Nakornthip Phromphoo*  
Department of Computer Engineering, Chulalongkorn University  
Source: RE_Lesson_11_RE_ValidationAndMGT.pdf :contentReference[oaicite:0]{index=0}

---

## 🎯 Learning Objectives
- เข้าใจหลักการพื้นฐานของ **Requirements Validation**  
  - Review, Prototyping, Model Validation, Acceptance Testing  
- ฝึกปฏิบัติการตรวจสอบความถูกต้องของ Requirement  
- เข้าใจหลักการของ **Requirements Management**  
  - Change Management, Tracing, Measuring, Attributes  

---

# 🧩 PART I — REQUIREMENTS VALIDATION

> **Requirements Validation** คือกระบวนการตรวจสอบว่า  
> “Requirement ที่ได้มานั้นตรงกับความต้องการจริงของผู้ใช้หรือไม่”  
> และ “เป็นระบบที่ถูกต้องที่ผู้ใช้คาดหวังหรือไม่”

---

## 🔹 Validation vs Verification

| แนวคิด | Validation | Verification |
|---------|-------------|--------------|
| คำถามหลัก | “Are we building the right system?” | “Are we building the system right?” |
| เป้าหมาย | ตรวจสอบความถูกต้องของความต้องการ | ตรวจสอบการทำงานตามเอกสารและมาตรฐาน |
| ระยะเวลา | ระหว่างขั้นตอน Requirements | ระหว่าง Design / Implementation |
| ตัวอย่าง | User review, prototype testing | Static analysis, code inspection |

---

## ⚙️ ขั้นตอนหลักของ Requirements Validation

1. **Requirements Review**  
2. **Prototyping**  
3. **Model Validation**  
4. **Acceptance Testing**

---

### 🧠 1. Requirements Review
> วิธีที่พบบ่อยที่สุดในการตรวจสอบข้อกำหนด  

**ลักษณะสำคัญ**
- จัดทำโดยกลุ่มผู้มีส่วนได้ส่วนเสีย (Stakeholders) ทั้งจากฝั่งผู้ใช้และผู้พัฒนา  
- ตรวจสอบ:  
  - ความถูกต้อง (Correctness)  
  - ความชัดเจน (Clarity)  
  - ความสอดคล้อง (Consistency)  
  - ความสมบูรณ์ (Completeness)  
- มักใช้ **Checklist** และ **Review Report Template**

**Review Summary Report ควรมี**  
- วัตถุประสงค์และขอบเขต  
- รายชื่อผู้เข้าร่วม  
- วันเวลา  
- นิยามประเภทข้อบกพร่อง  
- ผลการตรวจสอบ (เช่น ตาราง 2 มิติ: Checklist × Item)  
- รายการปัญหาที่ยังเปิดอยู่ + ผู้รับผิดชอบแก้ไข  

---

### 🧩 2. Prototyping
> ใช้สร้างแบบจำลอง (mockup / interactive UI) เพื่อให้ผู้ใช้เข้าใจระบบจริงมากขึ้น  

**ข้อดี**
- ช่วยให้ผู้ใช้และนักพัฒนาทำความเข้าใจตรงกัน  
- ลดความผันผวนของ Requirement (Volatility)  
- เหมาะกับระบบที่มี **User Interface, Dynamic behavior, หรือ Safety-critical features**

**ข้อเสีย**
- ผู้ใช้อาจมองข้ามฟังก์ชันหลัก  
- อาจเข้าใจผิดว่า Prototype คือระบบจริง  

---

### ⚙️ 3. Model Validation
> ตรวจสอบความถูกต้องของโมเดล (Functional / Structural / Behavioral / Architectural)  

**ตัวอย่างในเชิง UML**
- ตรวจสอบว่ามี **Communication path** ระหว่าง objects ครบหรือไม่  
- ตรวจสอบว่า **Use Case ↔ Activity ↔ Sequence Diagram** มีความสอดคล้องกัน  

**Rules for Model Verification & Validation**
1. ทุก Action ใน Activity Diagram ต้องมี Event ใน Use Case Description  
2. ลำดับใน Use Case ต้องตรงกับ Activity Diagram  
3. Actor ทั้งหมดใน Use Case Description ต้องปรากฏใน Use Case Diagram  
4. Diagram ทุกแบบต้องสอดคล้องกัน (Consistency)  

---

### 🧾 4. Acceptance Testing
> คือการทดสอบเพื่อยืนยันว่า “ระบบที่พัฒนาแล้วตรงตาม Requirement ทั้งหมด”  

**หลักการสำคัญ**
- ทุก Requirement ต้องสามารถตรวจสอบได้ (Verifiable)  
- กำหนด **Acceptance Criteria** ไว้ตั้งแต่เริ่มต้น  
- ทดสอบทั้ง Functional และ Non-functional  
- NFR ต้องแปลงให้วัดได้เชิงปริมาณก่อน เช่น  
  - Response ≤ 2s  
  - Accuracy ≥ 95%  

---

# 🧩 PART II — REQUIREMENTS MANAGEMENT

> **Requirements Management** คือการบันทึก, ควบคุม, และจัดการ Requirement ที่เปลี่ยนแปลงอยู่ตลอดวงจรชีวิตของโครงการ

---

## 🧠 แนวคิดพื้นฐาน
- เก็บรักษา Requirement และบริบท (Context & History)  
- ควบคุม Baseline ของ Requirement แต่ละระดับ  
- สอดคล้องกับมาตรฐาน **ISO/IEC 15288** และ **ISO/IEC 12207**  
- ระบุ Requirement ที่คาดว่าจะ “เปลี่ยนแปลง” และสื่อสารล่วงหน้า  
- ต้องมีนโยบายการจัดการเวอร์ชัน (Version Control)  

---

## 🔄 Change Management
> การบริหารการเปลี่ยนแปลงของ Requirement  

**หลักการ**
- ยอมรับว่าการเปลี่ยนแปลงเป็นสิ่ง “หลีกเลี่ยงไม่ได้”  
- ใช้ขั้นตอน Impact Analysis → Review → Approval  
- ใช้เครื่องมือเช่น **Requirement Management Tool (RM Tool)**  
- ควบคุมการเปลี่ยนโดยใช้ **Baseline**

**ประเภทของ Baseline**
| ประเภท | ความหมาย |
|----------|-----------|
| **Functional Baseline** | เอกสาร System Requirement + External Interfaces |
| **Allocated Baseline** | เอกสาร System Element Requirement + Interface Spec |
| **Developmental Baseline** | สถานะของระบบระหว่างพัฒนา |
| **Product Baseline** | ระบบที่เสร็จสมบูรณ์ (Final Version) |

---

### 🔹 ตัวอย่างแหล่งที่มาของ Change Request
- Bug Reports  
- User Enhancement Requests  
- Changes from other projects (system interface)  
- OS / Software updates  
- Organization Strategy Change  

---

## 🧭 Requirements Tracing
> การเชื่อมโยง (Traceability) ระหว่าง Requirement → Design → Implementation → Test  

**หลักการ**
- **Backward Traceability:**  
  จาก Software Requirement → System Requirement → Stakeholder  
- **Forward Traceability:**  
  จาก Requirement → Design Entity → Code Module → Test Case  

**เครื่องมือ**
- **Traceability Matrix** (ตารางเชื่อมโยง Req ID ↔ Test Case ↔ Module)  
- ต้องอัปเดตอยู่เสมอ เพื่อให้ Impact Analysis มีความน่าเชื่อถือ  

---

## 📏 Measuring Requirements
> ใช้ประเมิน “ขนาดและความซับซ้อน” ของ Requirements  

**แนวทางที่นิยม**
- **Function Point (FP)** – นับจำนวนฟังก์ชันทางธุรกิจ  
- **Use Case Point (UCP)** – ประเมิน effort จากจำนวน use case  
- ใช้ในการประเมิน Cost, Effort, และผลกระทบของ Change  

---

## 🧱 Requirements Attributes
> ข้อมูลประกอบของ Requirement ที่ต้องบันทึกและอัปเดตเสมอ  

| Attribute | ตัวอย่าง / ความหมาย |
|------------|----------------------|
| **ID** | หมายเลขเฉพาะ (Unique Identifier) |
| **Description** | คำอธิบาย Requirement |
| **Source** | ที่มาของ Requirement |
| **Rationale** | เหตุผลที่ต้องมี Requirement นี้ |
| **Verification Method** | วิธีตรวจสอบ เช่น Test / Review |
| **Priority** | ความสำคัญ |
| **Risk Level** | ความเสี่ยงถ้า Requirement ผิดพลาด |
| **Dependency** | ความสัมพันธ์กับ Requirement อื่น |
| **Change History** | วันที่และผู้แก้ไขล่าสุด |

---

## 🧾 Summary
- **Requirements Validation** → ตรวจสอบความถูกต้องของ Requirement  
  - Review, Prototype, Model Validation, Acceptance Test  
- **Requirements Management** → ดูแล Requirement ตลอดอายุโครงการ  
  - Change Management, Traceability, Measurement, Attribute  

---

# 💬 แนวข้อสอบออกบ่อย

### 🟦 ปรนัย
- ข้อใดเป็นขั้นตอนของ Requirement Validation  
- Change Management มีวัตถุประสงค์ใด  
- Baseline แบบใดใช้หลังจากระบบเสร็จสมบูรณ์  
- Requirement Attribute ข้อใดสำคัญที่สุด  

### 🟨 อัตนัย / วิเคราะห์
- อธิบายความแตกต่างระหว่าง Verification และ Validation  
- ยกตัวอย่างการตรวจสอบ Requirement โดยใช้ Prototype  
- เขียนอธิบายหลักการของ Requirements Tracing พร้อมตัวอย่าง  
- ยกตัวอย่าง Requirement Attribute อย่างน้อย 5 รายการและอธิบายความสำคัญ  
- อธิบายผลกระทบของ “Requirements Creep”  

---

## 🧩 Summary Table – Validation vs Management

| หมวด | Validation | Management |
|-------|-------------|-------------|
| เป้าหมาย | ตรวจสอบว่าถูกต้อง | บันทึกและควบคุม |
| เครื่องมือ | Review, Prototype, Model, Test | RM Tool, Trace Matrix |
| ผู้เกี่ยวข้อง | User, Analyst, QA | PM, Dev, QA |
| ผลลัพธ์ | Requirement ที่ยืนยันแล้ว | Requirement ที่จัดการได้ตลอดอายุระบบ |

---

📚 **References**
- ISO/IEC/IEEE 29148:2011 – *Systems and Software Engineering — Requirements Engineering*  
- ISO/IEC 12207 – *Software Life Cycle Processes*  
- *Guide to the Software Engineering Body of Knowledge (SWEBOK 3.0)*  
- Nakornthip Phromphoo, *Lesson 11 – Requirements Validation & Management (2024)*:contentReference[oaicite:1]{index=1}

✍️ *Prepared by Aphirak P. — Comprehensive README for Exam Review and Project Documentation*

# 📘 Lesson 11 — Requirements Validation & Management
## 🎯 ตัวอย่างแนวข้อสอบ & วิธีวิเคราะห์คำตอบ

---

## 🧩 Part A: Conceptual / Short Essay

### ❓ Q1. อธิบายความแตกต่างระหว่าง “Verification” และ “Validation”
**แนวตอบ:**
- **Verification:** ตรวจสอบว่าระบบถูกต้องตามสเปก → *“Build the system right”*  
  เช่น ตรวจ UML, Review เอกสาร, Unit Test  
- **Validation:** ตรวจสอบว่าระบบตอบโจทย์ผู้ใช้จริง → *“Build the right system”*  
  เช่น UAT, Prototype, Scenario-based Testing  
**เคล็ดลับ:** เขียนตารางเปรียบเทียบพร้อมยกตัวอย่าง 1 use case จะได้คะแนนเต็ม

---

### ❓ Q2. ยกตัวอย่าง “Requirements Validation Technique” อย่างน้อย 3 วิธี
**แนวตอบ:**
1. **Requirements Review** – ให้ทีม cross-functional ตรวจความครบถ้วน/ขัดแย้ง  
2. **Prototyping** – ทำต้นแบบเพื่อให้ผู้ใช้ยืนยัน  
3. **Model Validation** – ตรวจ consistency ระหว่าง Use Case, Class, Sequence  
4. **Acceptance Test** – ตรวจว่าระบบจริงทำงานตาม SRS  
(เลือก 3 ใน 4 ก็เพียงพอ)

---

### ❓ Q3. คุณสมบัติของ “Good Requirement” มีอะไรบ้าง (Validation Criteria)
**แนวตอบ (ใช้จำแบบ C-C-C-F-V-C):**
- Correctness  
- Completeness  
- Consistency  
- Feasibility  
- Verifiability  
- Clarity  
**เทคนิคจำ:** "C³FVC"

---

### ❓ Q4. อธิบายกระบวนการ Requirements Change Management
**แนวตอบ:**
1. ผู้ใช้เสนอ Change Request (CR)  
2. ทีมประเมินผลกระทบ (Impact Analysis)  
3. CCB (Change Control Board) อนุมัติหรือปฏิเสธ  
4. อัปเดต SRS, RTM, และแจ้ง QA / Dev  
5. ติดตามผลหลังการเปลี่ยนแปลง  
**คำสำคัญที่ต้องมี:** *impact, approval, update baseline, traceability*

---

### ❓ Q5. อธิบายความสำคัญของ Requirement Traceability Matrix (RTM)
**แนวตอบสั้น:**
- ใช้เชื่อมโยง Requirement → Design → Code → Test → Deployment  
- ช่วยติดตามผลกระทบเมื่อ requirement เปลี่ยน  
- เป็นเครื่องมือหลักใน Verification & Validation

---

## 🧠 Part B: Scenario-based / Analytical

### 🧭 Q6. (วิเคราะห์สถานการณ์)
> ในระบบ “Online Parking System”  
> พบว่าใน Use Case Diagram มี Use Case “Check-in” และ “Pay Fee”  
> แต่ใน Sequence Diagram ไม่มี message ที่อ้างถึงการ “คำนวณค่าจอด”  
>  
> **ถาม:** คุณจะตรวจพบปัญหานี้ได้ในขั้นตอนใดของ V&V?  
> และจะอธิบายว่าเป็น “Verification” หรือ “Validation”?

**แนววิเคราะห์คำตอบ:**
- ปัญหานี้เป็นเรื่อง *ความไม่สอดคล้องของแบบจำลอง (model inconsistency)*  
  → ตรวจพบในขั้นตอน **Verification**  
- วิธีตรวจ: Cross-check Use Case กับ Sequence Diagram  
- ถ้า Use Case มีแต่ Sequence ไม่มี → ต้องปรับ Sequence หรืออัปเดต UC  

**สรุปตอบ:**  
> “ตรวจพบในขั้นตอน Verification โดยใช้ Model Consistency Check”

---

### 🧭 Q7. (Use Case Validation)
> Use Case “Borrow Book” ของระบบห้องสมุด  
> ระบุ Postcondition ว่า “ระบบอัปเดตจำนวนหนังสือคงเหลือ”  
> แต่ Prototype ที่ทดสอบจริง ไม่มีฟังก์ชันนี้  
>  
> **ถาม:** ปัญหานี้เป็น Verification หรือ Validation? และควรทำอย่างไร?

**แนววิเคราะห์คำตอบ:**
- เป็น **Validation Error** (ระบบไม่ตรงตามสิ่งที่ผู้ใช้คาดหวัง / SRS)  
- วิธีแก้: แจ้งทีม Dev และ QA เพื่อปรับปรุง prototype ให้สอดคล้อง  
- ใช้ RTM ตรวจว่า FR-03 “Update remaining book count” ถูกทดสอบหรือยัง

---

### 🧭 Q8. (Change Management Case)
> ลูกค้าขอเพิ่มฟีเจอร์ “แจ้งเตือนการชำระผ่าน LINE” หลัง SRS ถูกอนุมัติแล้ว  
>  
> **ถาม:** ขั้นตอนการจัดการควรทำอย่างไรตามหลัก Requirements Management?

**แนววิเคราะห์คำตอบ:**
1. สร้าง Change Request (CR)  
2. ทำ Impact Analysis → UI, API, Cost, Schedule  
3. เสนอ CCB พิจารณา  
4. ถ้าอนุมัติ → Update SRS + RTM + Test Cases  
5. แจ้งทีมที่เกี่ยวข้อง  

---

## ⚙️ Part C: Model-based V&V

### 🔍 Q9. (Model Verification Example)
> จาก Use Case “Make Payment”  
> ตรวจพบว่าใน Sequence Diagram มีการเรียก `PaymentGateway.pay()`  
> แต่ใน Class Diagram ไม่มี method ดังกล่าว  
>  
> **ถาม:** ปัญหานี้คืออะไร และอยู่ในขั้นตอนใดของ V&V?

**แนววิเคราะห์คำตอบ:**
- ปัญหา: *Inconsistency between Sequence & Class Diagram*  
- ขั้นตอน: **Verification** (เพราะตรวจโมเดลกับโมเดล ไม่เกี่ยวผู้ใช้)  
- วิธีแก้: เพิ่ม method `pay()` ในคลาส `PaymentGateway` หรือปรับ Sequence ให้ถูกต้อง

---

### 🔍 Q10. (Model Validation Example)
> จาก Use Case “Track Bus” ของระบบ Smart Transport  
> Prototype แสดงเวลา ETA ผิดจากสถานการณ์จริงมาก  
>  
> **ถาม:** จะตรวจพบใน Verification หรือ Validation?

**แนววิเคราะห์คำตอบ:**
- ปัญหานี้ตรวจพบเมื่อผู้ใช้ทดสอบต้นแบบจริง → เป็น **Validation Error**  
- วิธีแก้: ทบทวน algorithm คำนวณ ETA / GPS Update Rate  
- สรุป: Validation = ตรวจว่าระบบตอบโจทย์ “ของจริง”

---

## 🧾 Part D: Essay – Analytical & Integration

### 🧮 Q11. “อธิบายวิธีทำ Model Verification & Validation 3 แบบ”
**แนวตอบสั้น:**
1. **Use Case → Sequence Consistency Check**  
   ตรวจว่า event ทุกตัวใน UC มีใน Sequence และเรียงถูกลำดับ  
2. **Class ↔ Sequence Structural Check**  
   ตรวจ method/parameter ตรงกัน  
3. **State Machine Validation**  
   ตรวจ state ครบทุกกรณีและสอดคล้องกับ flow จริงของผู้ใช้  

---

### 🧮 Q12. “อธิบายความสัมพันธ์ระหว่าง Requirements Validation กับ Requirements Management”
**แนวตอบ:**
- Validation ทำให้แน่ใจว่า requirement ถูกต้องตั้งแต่ต้น  
- Management ช่วยดูแลความถูกต้องนั้นให้คงอยู่แม้มีการเปลี่ยนแปลง  
> ทั้งสองทำงานร่วมกันเพื่อให้ระบบยังตอบโจทย์ผู้ใช้ แม้ requirement evolve ไปเรื่อย ๆ  

---

## 🎓 เคล็ดลับการตอบข้อสอบ

- เขียนคำตอบให้มี “คีย์เวิร์ด” ชัด เช่น *consistency, completeness, stakeholder review, prototype, traceability*  
- ยกตัวอย่างระบบที่เข้าใจ (Library, Transport, Clinic, Food Delivery)  
- ถ้าเป็นโจทย์โมเดล → พยายามระบุว่าเป็น “Verification (model-to-model)” หรือ “Validation (user-to-model)”  
- ใช้ตารางเปรียบเทียบถ้าข้อสอบถาม V vs V (ได้คะแนนแน่นอน)

---

## 🔖 สรุปจำง่ายใน 1 บรรทัด

| Concept | คำจำสั้น |
|----------|------------|
| **Verification** | Build the system right |
|
