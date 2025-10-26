# 📘 Lesson 6: Structural Modeling – UML Class Diagram  
**รายวิชา:** 2110623 – วิศวกรรมความต้องการซอฟต์แวร์ (Software Requirements Engineering)  
**ผู้สอน:** ผศ. ดร. นครทิพย์ พร้อมพูล  
**ภาควิชา:** วิศวกรรมคอมพิวเตอร์ จุฬาลงกรณ์มหาวิทยาลัย  

---

## 🎯 วัตถุประสงค์ของบทเรียน
- เข้าใจกฎและแนวทางการสร้าง **Class Diagram (UML)**  
- เข้าใจกระบวนการสร้างโมเดลเชิงโครงสร้าง (Structural Model)  
- สามารถระบุและสร้างความสัมพันธ์ระหว่างคลาส  
- เข้าใจความเชื่อมโยงระหว่างโมเดลเชิงโครงสร้าง (Structural) และโมเดลเชิงฟังก์ชัน (Functional)

---

## 🧩 ความหมายของ Structural Model
- **Structural Model** หรือ **Conceptual Model** คือแบบจำลองที่อธิบาย *โครงสร้างข้อมูล* ที่รองรับกระบวนการทางธุรกิจขององค์กร  
- เป็นวิธีการทางการ (Formal Way) ในการแทนวัตถุ (Objects) ที่ถูกใช้และสร้างโดยระบบธุรกิจ  
- ตัวอย่างวัตถุ (Objects):  
  - คน (Person, Member)  
  - สถานที่ (Office, Museum)  
  - สิ่งของหรือเหตุการณ์ (Transaction, Reservation)

**หมายเหตุ:** โมเดลเชิงโครงสร้างถูกสร้างแบบ *iterative* — จาก conceptual → design model

---

## 🧱 Class Diagram คืออะไร
- เป็น **Static Model** ที่แสดง “คลาส” และ “ความสัมพันธ์ระหว่างคลาส”  
- ใช้ในการเก็บและจัดการข้อมูล (attributes + operations) ของระบบ  
- ในขั้น **Analysis**: เน้นโครงสร้างเชิงตรรกะของข้อมูล  
- ในขั้น **Design**: พัฒนาให้เป็นรูปแบบเชิงเทคนิค เช่น Database หรือ GUI Components

---

## 🧠 องค์ประกอบของ Class Diagram

| องค์ประกอบ | ความหมาย |
|--------------|------------|
| **Class** | แบบแผนของวัตถุ เช่น Person, Book, Reservation |
| **Attribute** | คุณสมบัติของคลาส เช่น name, age, id |
| **Operation (Method)** | การกระทำหรือฟังก์ชันที่คลาสสามารถทำได้ |
| **Visibility** | การกำหนดสิทธิ์เข้าถึง: + public, - private, # protected |
| **Relationship** | ความสัมพันธ์ระหว่างคลาส (Generalization, Aggregation, Association) |
| **Multiplicity** | จำนวนของวัตถุที่เชื่อมโยง เช่น 1..1, 0..*, 1..* |

---

## ⚙️ ประเภทของคลาส (Class Types)
1. **Concrete Class** – คลาสที่สามารถสร้างวัตถุจริงได้ เช่น `Customer`, `Employee`  
2. **Abstract Class** – คลาสเชิงแนวคิด ไม่สามารถสร้างวัตถุได้โดยตรง เช่น `Person`  
3. **Domain Class** – คลาสในบริบทธุรกิจ (focus หลักในขั้น analysis)  
4. **UI / File / Document / Data Structure Class** – ใช้ในขั้น design

---

## 🧮 ประเภทของ Relationship

| ประเภท | ความหมาย | ตัวอย่าง |
|----------|-----------|-----------|
| **Generalization** | ความสัมพันธ์ “เป็นชนิดของ (is-a-kind-of)” | Employee → Person |
| **Aggregation** | ความสัมพันธ์ “เป็นส่วนหนึ่งของ (has-a / part-of)” | Department → Employee |
| **Composition** | ความสัมพันธ์เชิงกายภาพ ถ้า whole หาย part หายด้วย | Car → Engine |
| **Association** | ความสัมพันธ์ทั่วไป “เชื่อมโยงกัน” | Patient ↔ Appointment |
| **Association Class** | ความสัมพันธ์ที่มีข้อมูลเฉพาะของความเชื่อมโยง | Student–Course → Grade |

---

## 🔗 Generalization / Inheritance / Specialization
- **Generalization:** รวมคลาสย่อยที่คล้ายกันขึ้นเป็นคลาสแม่ (Superclass)  
- **Specialization:** แตกคลาสแม่ออกเป็นคลาสลูก (Subclass)  
- **Inheritance:** คลาสลูกสืบทอด Attribute และ Operation จากคลาสแม่  
- ใช้หลัก **Substitutability Principle** → Subclass ต้องแทนที่ Superclass ได้ทุกกรณี  

---

## 🧱 Aggregation vs Composition
| ประเภท | สัญลักษณ์ | ความหมาย | ตัวอย่าง |
|----------|-------------|-----------|-----------|
| **Aggregation** | ◇ (diamond โปร่ง) | ความสัมพันธ์แบบตรรกะ ส่วนหนึ่งของ แต่แยกได้ | Department ◇→ Employee |
| **Composition** | ◆ (diamond ทึบ) | ความสัมพันธ์แบบกายภาพ หาก Whole ตาย Part ก็ตายด้วย | Car ◆→ Engine |

---

## 🔍 Multiplicity (Cardinality)
ใช้ระบุจำนวนวัตถุที่สัมพันธ์กัน เช่น  
- `1..1` = ต้องมีหนึ่งเดียว  
- `0..*` = อาจไม่มีหรือมีได้หลายรายการ  
- `1..*` = ต้องมีอย่างน้อยหนึ่งรายการ  

---

## 🧰 วิธีระบุคลาส (Object Identification)

### 1️⃣ Textual Analysis
วิเคราะห์จาก Use Case Description  
- **Nouns (คำนาม)** → Class / Attribute  
- **Verbs (คำกริยา)** → Operation / Association  
- **Adjective (คำคุณศัพท์)** → Attribute  
- **Modal Verb (must, should)** → Constraint  

**เช่น:**  
> “A patient makes an appointment with a doctor.”  
→ Patient, Appointment, Doctor = Classes  
→ make appointment = Operation  
→ Relationship = Association

---

### 2️⃣ Common Object List
กลุ่มของวัตถุที่พบบ่อยในโดเมนธุรกิจ  
- **Physical things:** Book, Desk, Equipment  
- **Incidents:** Meeting, Flight, Accident  
- **Roles:** Doctor, Nurse, Patient  
- **Interactions:** Appointment, Payment  
- **Places:** Branch, Office  
- **Business Records:** Invoice, Contract  

---

### 3️⃣ Pattern-based Identification
ใช้ **Design/Analysis Patterns** เพื่อระบุโครงสร้างคลาสที่ใช้ซ้ำได้  
เช่น  
- **Party–Product–Transaction Pattern** (Martin Fowler)  
- **Entity–Control–Boundary (ECB) Pattern**

---

## 🧮 Entity–Control–Boundary (ECB) Pattern

| ประเภท | หน้าที่ |
|----------|----------|
| **Entity** | แทนข้อมูลถาวรในระบบ เช่น Customer, Order |
| **Boundary** | รับอินพุตจากผู้ใช้ / ติดต่อระบบภายนอก |
| **Control** | จัดการลำดับเหตุการณ์และตรรกะของ Use Case |

**แนวคิด:**  
- 1 Use Case → 1 Control Class  
- Control ควบคุม Entity และ Boundary ให้ทำงานร่วมกัน  
- อายุของ Control Object = ตลอดอายุ Use Case

---

## 🧱 ขั้นตอนการสร้าง Structural Model (5 Steps)
1. **Perform Object Identification**  
   - ใช้ Textual Analysis + Brainstorm + Common Object List  
2. **Create Class Diagram**  
   - วาดคลาส + ความสัมพันธ์ + Multiplicity + Visibility  
3. **Review Diagram**  
   - ตรวจสอบกับ Use Case ให้สอดคล้อง  
4. **Incorporate Patterns**  
   - เพิ่ม/ลบคลาสตาม Pattern ที่เหมาะสม  
5. **Validate Model**  
   - ตรวจสอบความถูกต้องและสอดคล้องกับ Use Case เดิม  

---

## ✅ การตรวจสอบและยืนยันโมเดล (Verification & Validation)

| ขั้นตอน | เนื้อหา |
|----------|----------|
| **Verification** | ตรวจว่าโมเดล “ถูกต้องตามสเปก” |
| **Validation** | ตรวจว่าโมเดล “ตรงกับความต้องการผู้ใช้” |

### 🔹 กฎพื้นฐานในการตรวจสอบ Class Diagram
1. Object Type ที่เป็นคลาส → ต้องใช้ Association (ไม่ใช่ Attribute)  
2. Relationships ต้องถูกต้อง (Generalization, Aggregation, Composition, Association)  
3. ใช้ Association Class เมื่อความสัมพันธ์มี Attribute เฉพาะ  
4. Diagram ต้องไม่ละเมิด Syntax ของ UML (เช่น Class เป็น Subclass ของตัวเองไม่ได้)

---

## 🧩 วิธีทำ Class Diagram ให้อ่านง่าย (Simplification)
1. แสดงเฉพาะ **Concrete Classes**  
2. ใช้ **View Mechanism**  
   - Use Case View → แสดงคลาสเฉพาะของ Use Case  
   - Relationship View → แสดงเฉพาะประเภทของความสัมพันธ์  
3. แสดงเฉพาะบางส่วนของข้อมูล เช่น ชื่อคลาส + Attribute เท่านั้น  
4. ใช้ **Packages** รวมคลาสที่เกี่ยวข้องในกลุ่มเดียวกัน  

---

## 🧱 ตัวอย่าง Pattern สำคัญ

| Pattern | แนวคิด | ตัวอย่าง |
|----------|----------|-----------|
| **Sale Order Contract** | ทุกธุรกรรมมักมี Party, Product, Transaction | Order–Item–Customer |
| **Account Pattern** | ต้องบันทึกทุกการเปลี่ยนแปลงของค่า (entry) | Bank Account, Inventory Record |
| **Accounting Transaction** | การเคลื่อนไหวระหว่างบัญชีต้องสมดุล | Transfer, Double Entry |
| **Entity–Control–Boundary (ECB)** | แยกชั้นข้อมูล–ควบคุม–อินเตอร์เฟซ | MarketingCampaign, Control, BudgetSystem |

---

## 🧠 แนวคำถาม–คำตอบ (พร้อมเฉลย)

| # | คำถาม | เฉลย |
|---|--------|-------|
| 1 | Structural Model คืออะไร | แบบจำลองโครงสร้างข้อมูลที่สนับสนุนกระบวนการทางธุรกิจ |
| 2 | Class Diagram แสดงอะไร | แสดงคลาสและความสัมพันธ์ระหว่างคลาส |
| 3 | Attribute กับ Operation ต่างกันอย่างไร | Attribute = ข้อมูล, Operation = การกระทำของคลาส |
| 4 | Visibility มีแบบใดบ้าง | + public, - private, # protected |
| 5 | Concrete Class คืออะไร | คลาสที่สามารถสร้างวัตถุจริงได้ |
| 6 | Abstract Class คืออะไร | คลาสแนวคิดที่ไม่สามารถสร้างวัตถุได้โดยตรง |
| 7 | Generalization หมายถึงอะไร | ความสัมพันธ์แบบ “is-a-kind-of” |
| 8 | Aggregation กับ Composition ต่างกันอย่างไร | Aggregation = แยกได้, Composition = ผูกติดกัน |
| 9 | Association Class คืออะไร | คลาสที่แทนความสัมพันธ์ที่มีข้อมูลเฉพาะ เช่น Grade |
| 10 | Multiplicity ใช้ทำอะไร | ระบุจำนวนของวัตถุที่เชื่อมโยงกัน |
| 11 | Textual Analysis ใช้ทำอะไร | ระบุคลาส/แอตทริบิวต์จากคำใน Use Case |
| 12 | Common Object List มีประโยชน์อย่างไร | ช่วยระบุวัตถุที่พบบ่อยในโดเมนธุรกิจ |
| 13 | Entity–Control–Boundary คืออะไร | Pattern แบ่งคลาสตามบทบาท: ข้อมูล–ควบคุม–อินเตอร์เฟซ |
| 14 | Verification vs Validation ต่างกันอย่างไร | Verification = ตรวจสเปก, Validation = ตรวจความต้องการ |
| 15 | วิธีลดความซับซ้อนของ Class Diagram คืออะไร | ใช้ View, แสดงเฉพาะคลาสหลัก, รวมเป็น Package |
| 16 | Patterns มีประโยชน์อะไร | ใช้ซ้ำ ลดเวลา สร้างโมเดลที่ครบถ้วนและมาตรฐาน |
| 17 | 5 ขั้นตอนสร้าง Structural Model คืออะไร | Identify → Create → Review → Incorporate → Validate |
| 18 | Relationship หลักมีกี่แบบ | 3 แบบ: Generalization, Aggregation, Association |
| 19 | Inheritance คืออะไร | การสืบทอดคุณสมบัติจากคลาสแม่ไปยังคลาสลูก |
| 20 | ใช้ Association Class เมื่อใด | เมื่อความสัมพันธ์มี Attribute หรือ Operation เฉพาะตัว |

---

## 💡 เคล็ดจำก่อนสอบ
| หัวข้อ | เทคนิคจำ |
|---------|------------|
| ความสัมพันธ์หลัก | **G–A–C–As** → Generalization, Aggregation, Composition, Association |
| การตรวจสอบโมเดล | **V&V Rule 4 ข้อ** |
| การระบุคลาส | **T–C–P** → Textual, Common Object List, Pattern |
| ประเภทคลาส | **C–A–D** → Concrete, Abstract, Domain |
| ความแตกต่างหลัก | Aggregation (◇) vs Composition (◆) |

---

## 📚 แหล่งอ้างอิง
- Dennis, Wixom, & Tegarden (2015), *Systems Analysis and Design with UML, 5th Ed.*  
- Martin Fowler (1997), *Analysis Patterns: Reusable Object Models*  
- Sommerville (2015), *Software Engineering*  
- ISO/IEC/IEEE 29148: Systems and Software Requirements  
- เอกสารบรรยาย 2110623 – Software Requirements Engineering, จุฬาฯ  

---

> 💬 **Tips:**  
> - จำโครงสร้าง Class Diagram + Relationship 3 แบบ  
> - จำขั้นตอนสร้าง Structural Model 5 ขั้น  
> - จำ Pattern ECB และความต่างระหว่าง Aggregation / Composition  
> ✅ ข้อสอบมักถามตรงเรื่อง “ประเภท Relationship”, “การระบุคลาส”, “Verification Rules”
