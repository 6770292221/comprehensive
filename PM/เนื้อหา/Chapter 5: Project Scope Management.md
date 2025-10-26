# 📘 บทที่ 5: การจัดการขอบเขตของโครงการ (Project Scope Management)  
จาก *Information Technology Project Management, 9th Edition*:contentReference[oaicite:0]{index=0}

---

## 🎯 วัตถุประสงค์ของบท (Learning Objectives)
1. อธิบายเหตุผลว่าทำไมการจัดการขอบเขตของโครงการ (Scope Management) จึงสำคัญ  
2. เข้าใจกระบวนการวางแผน การเก็บรวบรวม และการควบคุมขอบเขต  
3. อธิบายวิธีการสร้าง **Work Breakdown Structure (WBS)**  
4. เข้าใจความแตกต่างระหว่างการตรวจสอบ (Validate) และควบคุม (Control) ขอบเขต  
5. วิเคราะห์วิธีลด Scope Creep และใช้ซอฟต์แวร์ช่วยในการจัดการขอบเขต  
6. อธิบายแนวทางการจัดการขอบเขตในสภาพแวดล้อมแบบ Agile  

---

## 🧩 1. ความหมายของ Project Scope Management
- **Scope** คือ งานทั้งหมดที่จำเป็นต่อการสร้าง “ผลิตภัณฑ์หรือบริการ” ของโครงการ  
- **Deliverable** คือ สิ่งที่เกิดจากการทำงานของโครงการ (อาจเป็นเอกสาร ระบบ หรือซอฟต์แวร์)  
- การจัดการขอบเขต คือ การ “กำหนดและควบคุมว่าอะไรอยู่ในโครงการ และอะไรไม่อยู่”  
- เป้าหมายหลักคือให้ทีมและผู้มีส่วนได้ส่วนเสียเข้าใจขอบเขตของงานตรงกัน:contentReference[oaicite:1]{index=1}

---

## ⚙️ 2. กระบวนการหลักของการจัดการขอบเขต (Scope Management Processes)
| ลำดับ | กระบวนการ | คำอธิบาย |
|--------|-------------|-----------|
| 1️⃣ | **Planning Scope Management** | กำหนดวิธีการบริหารขอบเขตและข้อกำหนด |
| 2️⃣ | **Collecting Requirements** | เก็บรวบรวมและบันทึกความต้องการของผู้มีส่วนได้ส่วนเสีย |
| 3️⃣ | **Defining Scope** | สร้างเอกสารขอบเขต (Scope Statement) |
| 4️⃣ | **Creating WBS** | แยกงานออกเป็นส่วนย่อย ๆ ที่จัดการได้ |
| 5️⃣ | **Validating Scope** | ตรวจสอบและยืนยันผลงานที่ส่งมอบ |
| 6️⃣ | **Controlling Scope** | ควบคุมการเปลี่ยนแปลงของขอบเขต |

---

## 🧭 3. การวางแผนการจัดการขอบเขต (Planning Scope Management)
เอกสารสำคัญ 2 ฉบับที่ต้องจัดทำ:
1. **Scope Management Plan** – อธิบายวิธีสร้าง/อนุมัติ WBS และการยอมรับผลงาน  
2. **Requirements Management Plan** – ระบุวิธีเก็บ รวบรวม วิเคราะห์ และติดตามข้อกำหนด  

**เนื้อหาที่ควรรวมในแผนขอบเขต:**  
- วิธีสร้างและรักษา WBS  
- วิธีอนุมัติ Deliverables  
- วิธีควบคุมการเปลี่ยนแปลงของ Scope  

**ข้อควรจำ:**  
> “Requirement” คือ ความสามารถหรือเงื่อนไขที่จำเป็นในผลิตภัณฑ์หรือบริการหนึ่ง ๆ:contentReference[oaicite:2]{index=2}

---

## 📋 4. การเก็บรวบรวมความต้องการ (Collecting Requirements)
การเก็บ Requirement อย่างไม่รอบคอบจะทำให้เกิด **Rework** และเพิ่มต้นทุนในภายหลัง  

**เทคนิคที่นิยมใช้:**
- การสัมภาษณ์ (Interviews)  
- การจัดเวิร์กช็อป / Focus Group  
- แบบสอบถาม (Surveys)  
- การสังเกตการทำงาน (Observation)  
- การวิเคราะห์เอกสาร (Document Analysis)  
- การสร้างต้นแบบ (Prototyping)  
- การเปรียบเทียบมาตรฐาน (Benchmarking)  

**ผลลัพธ์ของขั้นตอนนี้:**  
- **Requirements Documentation** – แบ่งเป็น Functional / Non-Functional  
- **Requirements Traceability Matrix (RTM)** – ตารางเชื่อมโยงแต่ละ Requirement กับแหล่งที่มาและสถานะ เช่นใน IT Upgrade Project:contentReference[oaicite:3]{index=3}

---

## 🧱 5. การกำหนดขอบเขต (Defining Scope)
**Project Scope Statement** ประกอบด้วย:
- Product Description  
- Acceptance Criteria  
- รายละเอียด Deliverables  
- ขอบเขตและข้อจำกัด (Boundaries & Constraints)  
- สมมติฐานและเอกสารอ้างอิง  

**ตัวอย่างพัฒนา Scope Statement:**  
เวอร์ชันแรกพูดถึง “การอัปเกรดเซิร์ฟเวอร์” โดยยังไม่ชัดเจน  
เวอร์ชันที่สองระบุชัดว่า “ต้องซื้อ 10 เครื่องใหม่ ใช้ Virtualization และแนบเอกสารแนวทางในภาคผนวก”:contentReference[oaicite:4]{index=4}

---

## 🧩 6. การสร้าง Work Breakdown Structure (Creating the WBS)
> **WBS** = การแบ่งงานของโครงการออกเป็นโครงสร้างลำดับชั้น เพื่อให้เห็นภาพรวมทั้งหมดของงาน:contentReference[oaicite:5]{index=5}

- **Decomposition:** การแตกงานใหญ่ให้ละเอียดขึ้น  
- **Work Package:** งานที่เล็กที่สุดที่สามารถประมาณเวลาและต้นทุนได้  
- ใช้ **คำนาม (Nouns)** สำหรับชื่อรายการใน WBS  

**แนวทางการสร้าง WBS:**
| วิธี | รายละเอียด |
|------|-------------|
| **Guidelines** | ใช้แนวทางขององค์กร เช่น DOD WBS Manual |
| **Analogy** | เทียบกับโครงการเดิมที่คล้ายกัน |
| **Top-down** | เริ่มจากภาพรวม แตกย่อยลงไป |
| **Bottom-up** | เริ่มจากรายละเอียด รวมเป็นภาพใหญ่ |
| **Mind Mapping** | ใช้ภาพแผนผังแนวคิดเพื่อช่วยระดมความคิด |

**WBS Dictionary:**  
เอกสารอธิบายรายละเอียดของแต่ละรายการใน WBS เช่น เป้าหมาย ผู้รับผิดชอบ และลำดับงาน:contentReference[oaicite:6]{index=6}

---

## ✅ 7. การตรวจสอบขอบเขต (Validating Scope)
- เป็นการตรวจสอบและรับรองผลงานที่เสร็จแล้วอย่างเป็นทางการ  
- มักใช้วิธี “การตรวจสอบ (Inspection)” หรือ “การลงนามรับรอง (Sign-off)” จากลูกค้า  
- ผลลัพธ์อาจเป็น **Accepted Deliverables** หรือ **Change Requests**  

> ปัญหาที่พบบ่อยคือ “Scope Creep” — การขยายขอบเขตงานโดยไม่ได้รับอนุมัติ:contentReference[oaicite:7]{index=7}

---

## 🔄 8. การควบคุมขอบเขต (Controlling Scope)
เป้าหมายคือ **ป้องกันการเปลี่ยนแปลงโดยไม่จำเป็น** และรักษา Scope ให้ตรงกับเป้าหมายโครงการ  

**เครื่องมือ:** Variance Analysis (วิเคราะห์ความต่างระหว่างแผนกับผลจริง)  
**แนวทางควบคุม:**
- จัดประชุมผู้ใช้สม่ำเสมอ  
- ให้ผู้ใช้มีส่วนร่วมในทีมโครงการ  
- ทำเอกสาร Requirement ให้เป็นลายลักษณ์อักษร  
- ใช้เทคนิค **Prototyping / Use Case / JAD (Joint Application Development)**  
- สร้างระบบ **Requirements Database** เพื่อควบคุมการเปลี่ยนแปลง:contentReference[oaicite:8]{index=8}

---

## 💻 9. ซอฟต์แวร์ช่วยในการจัดการขอบเขต
| ประเภท | ตัวอย่างการใช้งาน |
|----------|-------------------|
| Word / Excel | เขียนเอกสารและติดตาม Requirement |
| Mind Mapping Tools | ใช้ระดมความคิดและสร้าง WBS |
| Project Management Software | ใช้สร้าง Gantt Chart, WBS และ Scope Baseline |
| Requirements Tools | เช่น Jira, Confluence, IBM DOORS – จัดเก็บและติดตามข้อกำหนด:contentReference[oaicite:9]{index=9}

---

## 🧠 10. ขอบเขตในสภาพแวดล้อม Agile / Adaptive
- ผู้มีส่วนได้ส่วนเสียจะกำหนดขอบเขต “ก่อนเริ่มแต่ละ Iteration”  
- ผลิตภัณฑ์ (Deliverable) จะถูกส่งมอบได้จริงในแต่ละรอบ  
- Scope จะค่อย ๆ ชัดเจนขึ้นตาม Feedback จากลูกค้า:contentReference[oaicite:10]{index=10}

---

## 📚 สรุปท้ายบท
- Project Scope Management มี 6 กระบวนการหลัก  
- ช่วยให้ทีมโฟกัสเฉพาะงานที่ “จำเป็นและมีคุณค่า”  
- เอกสารสำคัญ: **Scope Statement**, **WBS**, **WBS Dictionary**, **RTM**  
- ปัญหาสำคัญคือ **Scope Creep** ต้องป้องกันด้วยกระบวนการควบคุมที่ชัดเจน  

---

## 🧾 แนวข้อสอบแบบกากบาท (Multiple Choice)

1. Scope หมายถึงอะไรในโครงการ  
   - A) ทรัพยากรที่ใช้ในโครงการ  
   - ✅ B) งานทั้งหมดที่เกี่ยวข้องกับการสร้างผลิตภัณฑ์ของโครงการ  
   - C) ระยะเวลาในการทำโครงการ  
   - D) ขอบเขตของงบประมาณ  

2. ข้อใด “ไม่ใช่” กระบวนการของ Scope Management  
   - A) Defining Scope  
   - B) Validating Scope  
   - ✅ C) Managing Schedule  
   - D) Controlling Scope  

3. เอกสาร “Requirements Traceability Matrix (RTM)” ใช้ทำอะไร  
   - ✅ A) เชื่อมโยงความต้องการกับการพัฒนาและทดสอบ  
   - B) แสดงแผนการใช้ทรัพยากร  
   - C) แสดงงบประมาณของโครงการ  
   - D) ใช้วิเคราะห์ความเสี่ยง  

4. เครื่องมือหลักของการสร้าง WBS คืออะไร  
   - A) Simulation  
   - ✅ B) Decomposition  
   - C) Brainstorming  
   - D) Forecasting  

5. ข้อใด “ไม่ใช่” วิธีการพัฒนา WBS  
   - A) Top-down  
   - B) Bottom-up  
   - ✅ C) Waterfall Mapping  
   - D) Mind Mapping  

6. Scope Validation ใช้วิธีการใด  
   - A) Earned Value  
   - ✅ B) Inspection และ Sign-off จากลูกค้า  
   - C) Benchmarking  
   - D) Statistical Control  

7. ปัญหา “Scope Creep” หมายถึงอะไร  
   - ✅ A) การขยายขอบเขตงานโดยไม่อนุมัติ  
   - B) การตรวจสอบงานไม่ละเอียด  
   - C) การเปลี่ยนทีมงานกลางโครงการ  
   - D) การลดคุณภาพงาน  

8. WBS Dictionary ใช้เพื่ออะไร  
   - ✅ A) อธิบายรายละเอียดของแต่ละรายการใน WBS  
   - B) ระบุเวลาในการทำงาน  
   - C) คำนวณต้นทุนรวม  
   - D) สรุปคุณภาพงาน  

9. เครื่องมือ “Variance Analysis” ใช้เพื่อ  
   - A) วิเคราะห์ต้นทุนจริง  
   - ✅ B) ตรวจสอบความต่างระหว่างงานตามแผนกับผลลัพธ์จริง  
   - C) ควบคุมเวลาโครงการ  
   - D) วัดความพึงพอใจลูกค้า  

10. ใน Agile Scope จะถูกกำหนดอย่างไร  
    - A) กำหนดทั้งหมดตั้งแต่เริ่มโครงการ  
    - ✅ B) กำหนดรายละเอียดก่อนเริ่มแต่ละ Iteration  
    - C) ปรับหลังปิดโครงการเท่านั้น  
    - D) ไม่กำหนด Scope ชัดเจนเลย  

---

📖 **คำแนะนำสำหรับการอ่านสอบ**
- จำ 6 กระบวนการของ Scope Management ให้ครบ  
- เข้าใจความแตกต่างของ **Scope Statement**, **WBS**, และ **RTM**  
- รู้ว่า “Scope Creep” คือปัญหาหลัก และวิธีป้องกันมัน  
- ทบทวนการใช้เทคนิคต่าง ๆ เช่น Top-down, Mind Mapping, Decomposition  
- รู้ว่า Agile จะค่อย ๆ พัฒนา Scope ผ่าน Iteration  
