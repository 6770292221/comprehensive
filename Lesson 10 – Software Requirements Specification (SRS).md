# 🧩 Lesson 10: Software Requirements Specification (SRS)
> Subject: Software Requirements Engineering (2110623)  
> Lecturer: N. Prompoon, Chulalongkorn University (2024)

---

## 🎯 บทสรุปเนื้อหา
**SRS (Software Requirements Specification)** คือเอกสารที่กำหนดรายละเอียดความต้องการของซอฟต์แวร์  
ทั้ง **Functional Requirements (FRs)** และ **Non-Functional Requirements (NFRs)**  
โดยอ้างอิงจากมาตรฐาน  
- ISO/IEC/IEEE 29148 – Requirements Engineering  
- IEEE 830 – Recommended Practice for SRS  

**วัตถุประสงค์ของ SRS**
- ใช้เป็นข้อตกลงระหว่างผู้ว่าจ้างและผู้พัฒนา  
- เป็นฐานข้อมูลสำหรับ Design / Implementation / Testing  
- ป้องกัน scope creep และลดความเข้าใจผิดในทีม  

---

## 🧱 โครงสร้างของ SRS

| หมวด | เนื้อหา |
|-------|----------|
| **1. Identification & Front Matter** | ชื่อ, เวอร์ชัน, วันที่, TOC, Definition, References |
| **2. Purpose & Scope** | จุดประสงค์และขอบเขตของระบบ |
| **3. Product Overview** | ความสัมพันธ์กับระบบอื่น, interfaces, user, limitations, assumptions |
| **4. Specific Requirements** | รายละเอียด FR / NFR ของระบบ |
| **5. Verification** | วิธีตรวจสอบความถูกต้องของความต้องการ |
| **6. Supporting Information** | ตัวอย่าง, ข้อมูลสนับสนุน, ผลการสำรวจ, packaging ฯลฯ |

---

## ⚙️ Product Overview Details

### Product Perspective
- System interfaces  
- User interfaces (UI layout, error message style)  
- Hardware / Software / Communication interfaces  
- Memory constraints  
- Operation & backup modes  
- Site adaptation requirements

### Product Functions
สรุปฟังก์ชันหลักของระบบ (ไม่ลงรายละเอียดขั้นตอน)

### User Characteristics
- ระดับการศึกษา, ประสบการณ์, ความพิการ, ความเชี่ยวชาญ  
→ มีผลต่อ **Usability**

### Limitations
ข้อจำกัด เช่น
- Regulation, Hardware, Parallel Operation, Safety, Audit, Language

### Assumptions & Dependencies
ปัจจัยภายนอกที่ส่งผลต่อ requirement  
> เช่น “ระบบจะรันบน Windows 11”

### Apportioning of Requirements
การแบ่ง requirement ไปยัง subsystem/module  
> ใช้ Cross-Reference Table แสดง Function ↔ Module

---

## 🧠 Specific Requirements

### Functional Requirements (FR)
- สิ่งที่ระบบต้องทำ  
- ต้องระบุ **Input, Output, Function**  
- มี Unique ID และ Cross-Reference

### External Interface Requirements
- ชื่อ / คำอธิบาย / แหล่งที่มา / หน่วย / รูปแบบข้อมูล  
- Timing, Valid Range, Accuracy, Format (Screen / Window / Data)

### Non-Functional Requirements (NFR)
1. **Usability** – ความง่ายและประสิทธิภาพในการใช้งาน  
2. **Performance** – ตัวเลขเชิงปริมาณ เช่น  
   > 95% ของธุรกรรมต้องเสร็จภายใน 1 วินาที  
3. **Logical Database Requirements** – Entity, Relationship, Data Integrity  
4. **Design Constraints** – กฎ มาตรฐาน หรือข้อจำกัดของโครงการ  
5. **Standards Compliance** – Audit trace, Report format, Accounting rules  
6. **Software Attributes**  
   - Reliability (เชื่อถือได้)  
   - Availability (พร้อมใช้งาน)  
   - Security (ปลอดภัย)  
   - Maintainability (ดูแลแก้ไขง่าย)  
   - Portability (ย้าย Platform ได้ง่าย)

---

## 🔍 Verification & Supporting Info

| ส่วน | รายละเอียด |
|------|--------------|
| **Verification** | ระบุวิธีตรวจสอบว่า software ตรงตาม SRS หรือไม่ เช่น Testing, Simulation |
| **Supporting Info** | ตัวอย่าง Input/Output, User Survey, Cost Analysis, Packaging |

---

## 🧾 แนวข้อสอบยอดนิยม

### หมวด 1: ความเข้าใจพื้นฐาน
**Q1.** อธิบายความหมายของ SRS  
> เอกสารที่รวบรวมรายละเอียดความต้องการของระบบทั้ง FR/NFR เพื่อใช้เป็นสัญญาอ้างอิงระหว่างผู้พัฒนาและผู้ว่าจ้าง

**Q2.** ต่างจาก Requirements Definition อย่างไร  
> Definition = สรุปคร่าว ๆ ของสิ่งที่ระบบต้องทำ  
> SRS = เอกสารอย่างเป็นทางการพร้อมข้อจำกัดและรายละเอียดครบถ้วน

---

### หมวด 2: โครงสร้างและองค์ประกอบ
**Q3.** Product Overview มีองค์ประกอบใดบ้าง  
> Perspective, Functions, User Characteristics, Limitations, Assumptions, Apportioning

**Q4.** Specific Requirements ต้องระบุอะไรบ้าง  
> Input, Output, Function (และ Cross-Reference)

**Q5.** ตัวอย่าง Non-Functional Requirement  
> “ระบบต้องตอบสนองภายใน 3 วินาที” (Performance)

---

### หมวด 3: Software Attributes
| Attribute | ความหมาย | ตัวอย่าง |
|------------|-----------|-----------|
| Reliability | ระบบทำงานถูกต้อง | ระบบต้อง uptime 99.9% |
| Availability | ความพร้อมใช้งาน | ใช้งานได้ 24 ชม./วัน |
| Security | ป้องกันการเข้าถึง | ใช้การเข้ารหัส AES-256 |
| Maintainability | แก้ไขง่าย | แยก module อิสระ |
| Portability | ย้าย platform ได้ | ทำงานได้ทั้ง Windows / Linux |

---

### หมวด 4: ข้อสอบวิเคราะห์/จับคู่
**Q6.** ข้อใดไม่ใช่องค์ประกอบของ Product Overview  
> ง. Test Case ✅ (อยู่ใน Verification)

**Q7.** อธิบายความแตกต่างระหว่าง “Assumption” และ “Constraint”  
| ประเภท | ความหมาย | ตัวอย่าง |
|----------|------------|-----------|
| Assumption | สมมติฐานภายนอก | ระบบรันบน Windows 11 |
| Constraint | ข้อจำกัดที่ต้องปฏิบัติตาม | ต้องใช้ Oracle DB เท่านั้น |

---

### หมวด 5: คำถามเขียนตอบยาว
**Q8.** ทำไมต้องเขียน SRS?  
> เพื่อเป็น baseline อ้างอิง ใช้ในการออกแบบ ทดสอบ และสื่อสารกับลูกค้าอย่างชัดเจน

**Q9.** ถ้าระบบไม่ทำงานตรงตาม SRS เป็นปัญหาในขั้นใด?  
> Verification – “เราสร้างถูกต้องตามเอกสารหรือไม่”

**Q10.** ยกตัวอย่างตาราง Apportioning of Requirements  
| Function | Subsystem | Module |
|-----------|------------|--------|
| Login | Authentication | Auth Module |
| Display Report | Dashboard | UI Module |
| Store Data | Database | DB Service |

---

## 🧩 สรุปท้ายบท

| หัวข้อ | เนื้อหาสำคัญ |
|---------|---------------|
| **SRS คืออะไร** | เอกสารระบุความต้องการระบบแบบเป็นทางการ |
| **มาตรฐานอ้างอิง** | ISO/IEC/IEEE 29148, IEEE 830 |
| **องค์ประกอบหลัก** | Purpose, Scope, Overview, Requirements, Verification |
| **FR/NFR** | สิ่งที่ระบบทำ + คุณภาพของระบบ |
| **Software Attributes** | Reliability, Availability, Security, Maintainability, Portability |

---

📘 **Tip สำหรับสอบ:**  
- ท่อง 5 Attributes (R-A-S-M-P)  
- จำลำดับ Section ของ SRS  
- เขียนตัวอย่าง FR/NFR ได้อย่างน้อย 2 ข้อ  
- เข้าใจความแตกต่างระหว่าง *Requirement*, *Assumption*, *Constraint*  

---
