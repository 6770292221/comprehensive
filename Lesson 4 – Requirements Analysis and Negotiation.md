# 📘 Lesson 4: Requirements Analysis and Negotiation  
**รายวิชา:** 2110623 – วิศวกรรมความต้องการซอฟต์แวร์ (Software Requirements Engineering)  
**ผู้สอน:** ผศ. ดร. นครทิพย์ พร้อมพูล  
**ภาควิชา:** วิศวกรรมคอมพิวเตอร์ คณะวิศวกรรมศาสตร์ จุฬาลงกรณ์มหาวิทยาลัย  

---

## 🎯 วัตถุประสงค์ของบทเรียน
- เพื่ออธิบายแนวทางและกลยุทธ์ที่ใช้ในกระบวนการ **วิเคราะห์และเจรจาความต้องการ (Requirement Analysis and Negotiation)**  
- เพื่อสามารถเลือกวิธีการวิเคราะห์ที่เหมาะสมกับสถานการณ์ต่าง ๆ ได้อย่างมีเหตุผล  

---

## 🧩 ความหมายและเป้าหมายของ Requirements Analysis
**Requirements Analysis and Negotiation** เป็นขั้นตอนต่อเนื่องจาก Elicitation  
มีจุดประสงค์เพื่อ  
- ตรวจสอบและทำให้ความต้องการที่เก็บมา **ครบถ้วน ชัดเจน และไม่ขัดแย้งกัน**  
- ช่วยให้ทีมพัฒนาเข้าใจขอบเขตของระบบ  
- เจรจาและแก้ไขความต้องการที่ขัดแย้ง เพื่อให้ทุกฝ่ายเห็นพ้องร่วมกัน  

**ผลลัพธ์:** เอกสารความต้องการที่ผ่านการตกลงร่วมกัน (Agreed Requirements Document)

---

## ⚙️ ขั้นตอนของ Requirements Analysis and Negotiation

| ขั้นตอน | คำอธิบาย |
|----------|-----------|
| **Necessity Checking** | ตรวจสอบว่าความต้องการนั้นจำเป็นจริงหรือไม่ |
| **Consistency & Completeness Checking** | ตรวจสอบความสอดคล้องและความครบถ้วน |
| **Feasibility Checking** | ตรวจสอบความเป็นไปได้ของเทคโนโลยีและงบประมาณ |
| **Requirements Discussion** | เปิดการสนทนากับผู้มีส่วนได้ส่วนเสีย |
| **Requirements Prioritization** | จัดลำดับความสำคัญของความต้องการ |
| **Requirements Agreement** | เจรจาจนได้ข้อสรุปที่ทุกฝ่ายยอมรับร่วมกัน |

---

## 🧱 การจัดโครงสร้างความรู้ความต้องการ (Davis’ Three Ways)
1. **Partitioning** – การแบ่งส่วนตามโครงสร้างหรือองค์ประกอบ (Aggregation)  
   > เช่น ระบบจองตั๋วอาจแบ่งเป็น flight, passenger, fare, date  
2. **Abstraction** – ความสัมพันธ์ทั่วไป/เฉพาะ (General–Specific)  
   > เช่น “Passenger” อาจแบ่งเป็น เด็ก ผู้ใหญ่ หรือผู้โดยสารแบบลดราคา  
3. **Projection** – การมองจากหลายมุมมอง (Viewpoints)  
   > เช่น มุมมองของผู้โดยสาร พนักงานเช็กอิน ผู้จัดการสายการบิน  

---

## 📚 การจำแนกประเภทของความต้องการ (Requirements Classification)

| หมายเลข | มิติการจำแนก | คำอธิบาย |
|----------|----------------|-----------|
| 1 | **Functional / Non-functional** | ความต้องการเชิงหน้าที่ vs ไม่เชิงหน้าที่ |
| 2 | **Derived / Imposed / Emergent** | ความต้องการที่สืบเนื่องจากเป้าหมายสูงสุด หรือถูกกำหนดโดย stakeholder |
| 3 | **Product / Process** | ความต้องการของตัวผลิตภัณฑ์ หรือของกระบวนการพัฒนา |
| 4 | **Priority** | ความสำคัญ เช่น Mandatory, Desirable, Optional |
| 5 | **Scope (Global / Narrow)** | ผลกระทบกว้างหรือตรงจุด เช่น requirement ที่กระทบทั้งระบบ |
| 6 | **Volatility / Stability** | ความคงที่หรือความเปลี่ยนแปลงของความต้องการระหว่างวงจรชีวิตระบบ |

---

## 🧮 ตัวอย่าง Functional & Non-functional Requirements

### ✅ Functional Requirements
1. ผู้ป่วยสามารถ **สร้าง / เปลี่ยน / ยกเลิกการนัดหมาย** ได้  
2. ผู้จัดการสามารถ **ตรวจสอบและพิมพ์ตารางนัดรายวัน** ได้  
3. แพทย์สามารถ **อัปเดตตารางการให้บริการ** ได้  

### ⚙️ Non-functional Requirements
| ประเภท | ตัวอย่าง |
|----------|------------|
| **Operational** | ระบบทำงานบน Windows หรือ Web Browser ได้ |
| **Performance** | การค้นหาใช้เวลาไม่เกิน 2 วินาที |
| **Security** | มีการจำกัดสิทธิ์เข้าถึงเฉพาะแพทย์และผู้จัดการ |
| **Cultural & Political** | รองรับภาษาไทยและอังกฤษ / ปฏิบัติตามกฎหมายอุตสาหกรรม |

---

## 🧾 Requirements Analysis Checklist
ใช้เพื่อตรวจสอบความสมบูรณ์และคุณภาพของแต่ละ requirement

| หัวข้อใน Checklist | คำถามตรวจสอบ |
|--------------------|---------------|
| Premature Design | มีรายละเอียดของการออกแบบก่อนเวลาอันควรหรือไม่ |
| Combined Requirements | ความต้องการนี้รวมหลายเรื่องไว้หรือไม่ |
| Unnecessary Requirements | มีสิ่งที่เกินจำเป็นหรือไม่ (Gold Plating) |
| Use of Non-standard Hardware | ใช้เทคโนโลยีที่ไม่เป็นมาตรฐานหรือไม่ |
| Conformance with Business Goals | สอดคล้องกับเป้าหมายธุรกิจหรือไม่ |
| Ambiguity | มีความกำกวม / ตีความได้หลายแบบหรือไม่ |
| Realism | ทำได้จริงตามเทคโนโลยีที่มีหรือไม่ |
| Testability | สามารถทดสอบได้หรือไม่ |

---

## 🔗 Interaction Matrix
ใช้แสดง **ความสัมพันธ์ระหว่างความต้องการ**
- **1** = ขัดแย้ง (Conflict)  
- **1000** = ทับซ้อน (Overlap)  
- **0** = เป็นอิสระ (Independent)

> ช่วยตรวจจับความขัดแย้ง และการซ้ำซ้อนของ requirement ได้อย่างเป็นระบบ

---

## 🧠 Conceptual Modeling
ใช้ในการเข้าใจปัญหาเชิงลึก โดยการสร้าง **แบบจำลองแนวคิด (Model)**  
เช่น  
- Use Case Diagram  
- Class Diagram  
- Activity Diagram  
- Domain Model  

**ปัจจัยในการเลือกแบบจำลอง:**
1. ลักษณะของปัญหา (Problem Type)  
2. ความเชี่ยวชาญของวิศวกรซอฟต์แวร์  
3. ความต้องการของลูกค้าหรือมาตรฐานขององค์กร  

---

## 🏗️ Requirements Allocation
คือการกระจายความต้องการไปยัง **องค์ประกอบทางสถาปัตยกรรม (Architectural Components)**  
เช่น ระบบ Search Engine  
- Query Module → รับคำค้นหา  
- Ranking Module → เรียงลำดับผลลัพธ์  
- Indexing Module → อัปเดตดัชนีข้อมูลทุก 24 ชม.  
- Crawling Module → ดึงข้อมูลจากเว็บไซต์  

---

## 🧮 Formal Analysis
การใช้ **ภาษารูปแบบทางคณิตศาสตร์ (Formal Specification Language)**  
เพื่อเขียนความต้องการให้ **ชัดเจน ไม่กำกวม และพิสูจน์ได้**  
เช่น Z, VDM, B, CSP, Petri Nets, Larch, LOTOS

---

## 💬 Requirements Negotiation
คือกระบวนการ **เจรจาและแก้ไขความขัดแย้ง** ของความต้องการ  
โดยใช้การประชุมร่วม (Brainstorming / Workshop)

### ขั้นตอนของการประชุม
1. **Information Stage:** อธิบายปัญหา  
2. **Discussion Stage:** ถกเถียงแนวทางแก้  
3. **Resolution Stage:** สรุปผลและตกลงการเปลี่ยนแปลง  

**ผู้ดำเนินการประชุม (Facilitator)** ควรเป็นบุคคลกลาง ไม่เกี่ยวข้องโดยตรงกับโครงการ  

---

## 📊 Requirements Prioritization
2 วิธีหลักในการจัดลำดับความสำคัญ:
1. **Cost–Value Approach:**  
   - พิจารณาความคุ้มค่าระหว่าง “ประโยชน์” กับ “ต้นทุน”  
2. **Analytic Hierarchy Process (AHP):**  
   - เปรียบเทียบความต้องการแบบจับคู่ (Pairwise Comparison)  

---

## 🧭 Requirement Analysis Approaches

| แนวทาง | คำอธิบาย | ความเสี่ยง | ผลตอบแทน |
|----------|-----------|-------------|-----------|
| **Business Process Automation (BPA)** | ใช้เทคโนโลยีมาช่วยงานเดิม | ต่ำ | ต่ำ |
| **Business Process Improvement (BPI)** | ปรับปรุงกระบวนการให้มีประสิทธิภาพมากขึ้น | ปานกลาง | ปานกลาง |
| **Business Process Reengineering (BPR)** | ปรับเปลี่ยนกระบวนการทั้งหมดใหม่ | สูงมาก | สูงมาก |

---

## 🧮 Requirements Analysis Strategies

| กลยุทธ์ | คำอธิบาย |
|----------|-----------|
| **Problem Analysis** | เน้นแก้ปัญหาเล็ก ๆ จากระบบเดิม |
| **Root Cause Analysis** | หาสาเหตุที่แท้จริงของปัญหา |
| **Duration Analysis** | วิเคราะห์เวลาในแต่ละขั้นตอนของกระบวนการ |
| **Activity-Based Costing** | วิเคราะห์ต้นทุนของแต่ละกิจกรรม |
| **Benchmarking** | เปรียบเทียบกับองค์กรอื่น (Formal/Informal) |
| **Outcome Analysis** | มองจากมุมมองของผลลัพธ์ที่ผู้ใช้ต้องการ |
| **Technology Analysis** | ศึกษาเทคโนโลยีใหม่ ๆ ที่สามารถปรับใช้ได้ |
| **Activity Elimination** | ทดลองลบกิจกรรมบางอย่างออกเพื่อดูผลลัพธ์ |

---

## 🚫 ข้อผิดพลาดที่พบบ่อยในการวิเคราะห์
- ลดเวลาการวิเคราะห์มากเกินไป  
- ผู้ใช้ระบุความต้องการเกินจำเป็น (User Gold-Plating)  
- นักพัฒนาเพิ่มฟีเจอร์ที่ไม่จำเป็น (Developer Gold-Plating)  
- ขาดการมีส่วนร่วมจากผู้ใช้ (Lack of User Involvement)

---

## 🧠 แนวคำถาม–คำตอบ (พร้อมเฉลย)

| # | คำถาม | เฉลย |
|---|--------|-------|
| 1 | จุดประสงค์ของ Requirements Analysis คืออะไร | ทำให้ความต้องการครบ ชัดเจน ไม่ขัดแย้ง และตกลงร่วมกันได้ |
| 2 | Partitioning, Abstraction, Projection คืออะไร | วิธีการจัดโครงสร้างความรู้ความต้องการ |
| 3 | Requirement Classification มีกี่มิติ | 6 มิติ เช่น Functional/Non-functional, Priority, Volatility |
| 4 | Checklist มีไว้เพื่ออะไร | ตรวจสอบคุณภาพของแต่ละ Requirement |
| 5 | Interaction Matrix คืออะไร | ตารางแสดงความสัมพันธ์ ขัดแย้ง/ซ้ำซ้อนของความต้องการ |
| 6 | Conceptual Modeling ใช้เพื่ออะไร | เข้าใจระบบและแสดงความสัมพันธ์ขององค์ประกอบในโลกจริง |
| 7 | Requirement Allocation คืออะไร | การจัดสรรความต้องการไปยังส่วนประกอบสถาปัตยกรรม |
| 8 | Negotiation มีขั้นตอนอะไรบ้าง | Information → Discussion → Resolution |
| 9 | Cost–Value Approach คืออะไร | การจัดลำดับความสำคัญโดยพิจารณาประโยชน์เทียบต้นทุน |
| 10 | 3 แนวทางหลักของ Analysis คืออะไร | BPA, BPI, BPR |
| 11 | กลยุทธ์ Root Cause Analysis เน้นอะไร | หาสาเหตุรากของปัญหาเพื่อแก้ให้ตรงจุด |
| 12 | Formal Specification Language คืออะไร | ภาษาคณิตศาสตร์ที่ใช้กำหนดความต้องการอย่างชัดเจน |
| 13 | ความต่างของ Efficiency vs Effectiveness คืออะไร | Efficiency = ใช้ทรัพยากรน้อย, Effectiveness = บรรลุเป้าหมายครบถ้วน |
| 14 | ข้อผิดพลาดที่พบบ่อยในการวิเคราะห์คืออะไร | ลดเวลาวิเคราะห์มากไป / Gold Plating / ขาดการมีส่วนร่วมผู้ใช้ |
| 15 | เมื่อใดควรเลือก BPR | เมื่อองค์กรต้องการเปลี่ยนแปลงกระบวนการอย่างสิ้นเชิง |

---

## 💡 สรุปจำง่ายก่อนสอบ

| หัวข้อ | เทคนิคจำ |
|---------|-----------|
| โครงสร้างความรู้ | **P–A–P** → Partitioning, Abstraction, Projection |
| การจำแนกความต้องการ | **6 มิติ** → Func/Nonfunc, Derived, Process, Priority, Scope, Volatility |
| ขั้นตอนวิเคราะห์ | **N–C–F–D–P–A** → Necessity, Consistency, Feasibility, Discussion, Prioritization, Agreement |
| แนวทางหลัก | **BPA–BPI–BPR** |
| กลยุทธ์หลัก | **R–D–C–B–O–T–A** → Root cause, Duration, Costing, Benchmarking, Outcome, Technology, Activity |

---

## 📚 แหล่งอ้างอิง
- SWEBOX V3.0 – Guide to the Software Engineering Body of Knowledge  
- Kotonya & Sommerville (1997), *Requirements Engineering Processes and Techniques*  
- J. Cleland-Huang (2005), *Software Requirements*, IEEE Computer Society  
- Denis A., Wixom, B.H., Tegarden, D. (2015), *Systems Analysis and Design (5th Ed.)*, Wiley  

---
> 💬 **Tips:**  
> เน้นอ่าน “Classification”, “Checklist”, “Negotiation Steps”, “BPA–BPI–BPR” และ “Analysis Strategies” เพราะมักออกข้อสอบบ่อยที่สุด ✅
