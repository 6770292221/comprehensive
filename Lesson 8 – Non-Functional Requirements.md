# ⚙️ Lesson 8 – Non-Functional Requirements (NFRs)
**Software Requirements Engineering – Chulalongkorn University**  
Instructor: นครทิพย์ พร้อมพูล  

---

## 🎯 Objectives
- เข้าใจความแตกต่างระหว่าง **Functional Requirements (FRs)** และ **Non-Functional Requirements (NFRs)**  
- จำแนกประเภทของ NFRs: Product, Process, External  
- อธิบายปัญหาในการกำหนดและวัดค่า NFR  
- สามารถ **derive NFRs จาก user needs / system goals**  
- เข้าใจ **metrics** สำหรับการประเมิน NFR  
- วิเคราะห์ **conflicts และ trade-off** ระหว่าง NFRs  
- อ้างอิงมาตรฐาน **ISO/IEC/IEEE 29148, ISO/IEC 9126, ISO/IEC 25010 (SQuaRE)**  

---

## 🧠 Concept Overview

> **Functional Requirements (FRs)**: “ระบบต้องทำอะไร”  
> **Non-Functional Requirements (NFRs)**: “ระบบต้องดีแค่ไหน” หรือ “ควรทำอย่างไร”

| Aspect | Functional | Non-Functional |
|---------|-------------|----------------|
| Focus | พฤติกรรม / ฟังก์ชันของระบบ | คุณภาพและข้อจำกัดของระบบ |
| Example | “ระบบต้องสามารถบันทึกข้อมูลผู้ใช้ได้” | “ระบบต้องบันทึกข้อมูลภายใน 2 วินาที” |
| Type | Feature-based | Constraint / Quality-based |
| Relation | FRs ถูกกำหนดในขั้นวิเคราะห์ | NFRs มักเกิดขึ้นในขั้นออกแบบ / ทดสอบ |

---

## 🧩 Classification of NFRs (ตาม Sommerville)
| Type | Description | Example |
|------|--------------|----------|
| **Product Requirements** | กำหนดคุณภาพของระบบที่พัฒนา | Performance, Usability, Reliability, Portability |
| **Process Requirements** | กำหนดวิธีการพัฒนา | “ต้องพัฒนาโดยใช้ ISO 12207”, “ใช้ CASE Tool XYZ” |
| **External Requirements** | มาจากสภาพแวดล้อม / กฎหมาย / องค์กร | ISO 27034-3, PDPA, WHO report rule |

> ⚠️ NFRs บางข้ออาจอยู่ได้หลายหมวด เช่น Security เป็นได้ทั้ง Product & External:contentReference[oaicite:1]{index=1}

---

## 🧮 Examples of Product NFRs

| Type | Example |
|-------|----------|
| **Reliability** | “ระบบต้องมี availability 99.8%” |
| **Performance** | “ตอบสนองต่อคำขอไม่เกิน 2 วินาที” |
| **Space** | “ขนาด executable ต้องไม่เกิน 512 KB” |
| **Portability** | “ระบบต้องทำงานได้บน Windows และ macOS” |
| **Security** | “เข้ารหัสข้อมูลทั้งหมดด้วย RSA” |

---

## 🧱 Process NFRs
- ข้อจำกัดของกระบวนการพัฒนา เช่น  
  - “ต้องใช้มาตรฐาน ISO 12207”  
  - “ต้องจัดทำรายงาน effort ทุก 2 สัปดาห์”  
  - “ต้องจัดทำแผน Disaster Recovery ของการพัฒนา”

---

## 🌐 External NFRs
- ข้อจำกัดจากสภาพแวดล้อม กฎหมาย หรือองค์กร เช่น  
  - ระบบ E-Commerce ต้องมี OTP สำหรับการยืนยัน  
  - ระบบ การแพทย์ ต้องใช้รหัส ICD-10 ของ WHO  
  - ข้อมูลส่วนบุคคลต้องได้รับการรับรองจาก Data Protection Officer  

---

## 🧭 Approaches to Derive NFRs

### 1. Product-Process-External (Sommerville)
- พิจารณาเป้าหมายของผู้ใช้ / องค์กร / กฎหมาย แล้วระบุข้อจำกัดตามประเภท

### 2. Goal Decomposition (Loucopoulos & Karakostas, 1995)
- แปลง **Enterprise Goal → Sub-Goal → NFR → Quantitative Metric**
- เช่น  
  Goal: Visualize Air Traffic → NFR: “Display radar data in real time” → Metric: < 0.165 sec:contentReference[oaicite:2]{index=2}

### 3. Concerns Decomposition (Sommerville)
- วิเคราะห์ “ความกังวลหลัก” เช่น Safety → Detect Excess Speed → Requirement “System must avoid excess speed”  

---

## ⚠️ Problems of Expressing NFRs
1. บาง constraint ขึ้นอยู่กับ design ที่ยังไม่รู้ตอน requirements  
2. บางข้อ subjective (เช่น Usability / Learnability)  
3. FR & NFR มี dependency สูง แยกยาก  
4. NFRs มัก conflict กันเอง (เช่น Security vs Usability)  
5. ไม่มีเกณฑ์แน่ชัดว่าควร “พอแล้ว” เมื่อไหร่  

---

## 🧩 Attributes of a Good NFR
| Attribute | Description |
|------------|-------------|
| **Objective** | ต้องไม่เป็นความคิดเห็นหรือความปรารถนา |
| **Testable** | ต้องสามารถทดสอบได้ด้วย metric ที่ชัดเจน |

---

## 📏 Example of Measurable Metrics

| Category | Metrics |
|-----------|----------|
| **Performance** | Transactions/sec, Response time |
| **Reliability** | ROCOF (rate of failure), MTTF |
| **Availability** | Probability of failure on demand |
| **Usability** | Time to learn 80% functions, Error rate |
| **Robustness** | Time to recover after failure |
| **Portability** | Number of target platforms |

---

## 🧩 Commonly Considered NFRs

| Category | Example |
|-----------|----------|
| **Reliability** | Availability 99.8%, MTTF ≥ 500 hrs |
| **Performance** | Response ≤ 2 s, ≥ 10 TPS |
| **Security** | Encrypted data, Access control roles |
| **Usability** | Learn time ≤ 2 hrs, Error rate < 3% |

---

## ⚔️ Conflicts Between NFRs

| Conflict | Description |
|-----------|-------------|
| **Security vs Usability** | การยืนยันตัวตนหลายชั้นทำให้ใช้งานช้า |
| **Safety vs Availability** | Fail-safe อาจลด availability |
| **Performance vs Reliability** | การตรวจสอบระบบมาก → ช้าลง |

> 💡 **แนวแก้:** ใช้ Trade-off analysis → พิจารณาความสำคัญและผลกระทบ ต่อ system goals:contentReference[oaicite:3]{index=3}

---

## 🧱 Trade-off Analysis Steps
1. ระบุคู่ NFR ที่ขัดแย้ง  
2. ประเมินผลกระทบต่อ System Goal  
3. ให้ Weight ของ แต่ละ NFR ตาม Stakeholder Priority  
4. วิเคราะห์ผลลัพธ์รวม (net benefit)  
5. กำหนด compromise ที่เหมาะสม  

---

## 🧩 ISO/IEC 9126 → ISO/IEC 25010 (SQuaRE)
**3 มิติคุณภาพหลัก:**

| Quality Dimension | Focus |
|-------------------|--------|
| **Quality in Use** | Effectiveness, Productivity, Safety, Satisfaction |
| **External Quality** | คุณสมบัติของ final product ที่ผู้ใช้เห็น (Reliability, Usability, Efficiency) |
| **Internal Quality** | คุณภาพที่นักพัฒนาเห็น (Maintainability, Portability, Testability) |

---

## 📘 Example – NFR Integration with FR
| FR | Related NFR | Metric |
|----|--------------|--------|
| User login | Security – Encrypted Password | SHA-256 + Salt |
| Upload file | Performance – Upload < 3 s | Response time test |
| Display dashboard | Usability – Learn time < 10 min | UAT survey score ≥ 4/5 |

---

## 🧾 Example Question Bank

### 🟦 Multiple Choice
- NFR ใดเป็นประเภท Product Requirement  
- ข้อใดเป็น metric ที่ใช้วัด Reliability  
- “ระบบต้องเข้ารหัสข้อมูล” คือ NFR ประเภทใด  
- ข้อใดเป็น conflict ระหว่าง NFR  

### 🟨 Short Answer
- อธิบาย Product / Process / External Requirements  
- ยกตัวอย่าง Goal → NFR → Metric  
- NFR ที่สำคัญใน E-Commerce มีอะไรบ้าง  

### 🟥 Analytical
- จาก FR “Make Appointment” ระบุ NFR ที่เกี่ยวข้อง และ metrics  
- วิเคราะห์ trade-off ระหว่าง Usability และ Security  
- เขียน ตาราง Product vs Process vs External ของ ระบบ ของคุณ  

---

## 💡 Summary Flashcards
- **NFR = คุณภาพ (“ilities”) เช่น reliability, usability, security**  
- **FR = ทำ อะไร / NFR = ทำ อย่างไร**  
- **3 ประเภทหลัก:** Product | Process | External  
- **NFR ดีต้อง objective และ testable**  
- **ใช้ metric ชัดเจน → MTTF, TPS, Error Rate**  
- **Trade-off จำเป็น เมื่อ NFRs ขัดกัน**  
- **มาตรฐานสำคัญ:** ISO 29148, ISO 9126 → 25010 (SQuaRE)  

---

## 📚 References
- ISO/IEC/IEEE 29148:2018 – Requirements Engineering  
- ISO/IEC 9126 & ISO/IEC 25010 (SQuaRE)  
- Kotonya & Sommerville, *Requirements Engineering Processes and Techniques*, 1997  
- Dennis et al., *Systems Analysis and Design with UML (5th Ed.)*, 2015  
- Mairiza et al., *SAC 2010 – Investigation into the Notion of NFRs*  
- นครทิพย์ พร้อมพูล, *Lesson 8 – Non-Functional Requirements (2024)*:contentReference[oaicite:4]{index=4}

---

✍️ *Prepared by Aphirak P. for RE Lesson 8 – Non-Functional Requirements*
