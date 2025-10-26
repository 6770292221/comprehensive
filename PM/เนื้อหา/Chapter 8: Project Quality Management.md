# 📘 บทที่ 8: การจัดการคุณภาพของโครงการ (Project Quality Management)
จาก *Information Technology Project Management, Ninth Edition*:contentReference[oaicite:0]{index=0}

---

## 🎯 วัตถุประสงค์ของบทเรียน (Learning Objectives)
1. อธิบายความหมายของ “คุณภาพ” และความสัมพันธ์กับโครงการ IT  
2. เข้าใจกระบวนการหลักของ Project Quality Management  
3. อธิบายเครื่องมือควบคุมคุณภาพ เช่น **Seven Basic Tools**, **Six Sigma**, **Statistical Sampling**, และ **Testing**  
4. วิเคราะห์แนวคิดสมัยใหม่ เช่น **Lean**, **Kaizen**, **Kanban**, และ **Benchmarking**  
5. อธิบายบทบาทของผู้นำและ “ต้นทุนของคุณภาพ (Cost of Quality)”  
6. เข้าใจแนวคิดคุณภาพในสภาพแวดล้อมแบบ Agile  

---

## 🧩 1. ความหมายของ “คุณภาพ” (What is Quality)
> “คุณภาพ” คือระดับที่ผลิตภัณฑ์หรือบริการสามารถตอบสนองความต้องการที่กำหนดไว้ได้:contentReference[oaicite:1]{index=1}

| แนวคิด | ความหมาย |
|----------|-------------|
| **Conformance to Requirements** | ผลิตภัณฑ์ตรงตามข้อกำหนด |
| **Fitness for Use** | ผลิตภัณฑ์ใช้งานได้ตามวัตถุประสงค์ |
| **ISO 9000 (2000)** | ระดับของคุณลักษณะที่สนองความต้องการโดยธรรมชาติ |

---

## ⚙️ 2. กระบวนการหลักของ Project Quality Management
| ลำดับ | กระบวนการ | จุดประสงค์ |
|--------|-------------|-------------|
| 1️⃣ | **Planning Quality Management** | ระบุมาตรฐานและวิธีตรวจสอบคุณภาพ |
| 2️⃣ | **Managing Quality (Quality Assurance)** | ดำเนินการและปรับปรุงกระบวนการคุณภาพ |
| 3️⃣ | **Controlling Quality (Quality Control)** | ตรวจสอบและวัดผลผลิตให้ตรงตามมาตรฐาน |

---

## 🧱 3. การวางแผนคุณภาพ (Planning Quality Management)
### หลักคิดสำคัญ
- มุ่งเน้น **การป้องกันข้อบกพร่องมากกว่าการตรวจจับ (Prevention over Inspection)**  
- สร้างคุณภาพ “ตั้งแต่การออกแบบ (Design-In Quality)”  
- ปรับสมดุลระหว่าง **คุณภาพ-เวลา-ต้นทุน-ขอบเขต**

### ปัจจัยที่เกี่ยวข้องกับคุณภาพ
- **Functionality:** ระบบทำงานได้ครบตามที่ต้องการ  
- **Performance:** ความเร็วและประสิทธิภาพของระบบ  
- **Reliability:** การทำงานได้อย่างคงที่  
- **Maintainability:** ซ่อมบำรุงได้ง่าย  
- **Features:** ฟีเจอร์ที่เพิ่มคุณค่าแก่ผู้ใช้  

### มาตรฐานสากลที่เกี่ยวข้อง
| มาตรฐาน | รายละเอียด |
|----------|-------------|
| **ISO 9000** | ระบบบริหารคุณภาพ |
| **ISO/IEC 25010** | โมเดลคุณภาพซอฟต์แวร์ (SQuaRE) |
| **IEEE 730** | มาตรฐานกระบวนการประกันคุณภาพซอฟต์แวร์ |

---

## 🧭 4. การบริหารคุณภาพ (Managing Quality)
### 🔹 แนวคิดสำคัญ
การประกันคุณภาพ (Quality Assurance) คือกระบวนการเพื่อให้มั่นใจว่าโครงการจะปฏิบัติตามมาตรฐานคุณภาพที่กำหนด

---

### 🔸 Lean
> “ทำให้ลูกค้าได้รับคุณค่ามากที่สุด โดยลดความสูญเปล่า (Waste)”:contentReference[oaicite:2]{index=2}

**ประเภทของ Waste**
- **Information waste:** การป้อนข้อมูลซ้ำ, ข้อมูลไม่ใช้, ฟอร์แมตไม่ตรงกัน  
- **Process waste:** Defects, Rework, Overproduction  
- **People waste:** ขาดการฝึกอบรม, มอบหมายงานไม่ชัด, การทำงานหลายอย่างพร้อมกัน  

---

### 🔸 Kaizen
> ปรัชญาญี่ปุ่นแปลว่า “การปรับปรุงอย่างต่อเนื่อง”:contentReference[oaicite:3]{index=3}

- ใช้การปรับปรุงเล็ก ๆ อย่างต่อเนื่องโดยทุกคนในองค์กร  
- เน้นการสร้างมาตรฐานและลดความสูญเปล่า  
- ยึดหลัก “Continuous Improvement”  

---

### 🔸 Kanban
> ระบบกระดานแสดงสถานะงาน “To-Do → In Progress → Validate → Done”:contentReference[oaicite:4]{index=4}

- ควบคุมงานที่กำลังทำ (**WIP Limit**) เพื่อป้องกันคอขวด  
- ใช้ใน Agile ร่วมกับ Scrum ได้  
- ไม่มีรอบ Sprint → เน้น Flow ต่อเนื่อง  

---

### 🔸 Benchmarking & Quality Audit
| เครื่องมือ | จุดประสงค์ |
|-------------|--------------|
| **Benchmarking** | เปรียบเทียบกระบวนการกับองค์กรอื่น |
| **Quality Audit** | ตรวจสอบคุณภาพภายในหรือภายนอก เพื่อเรียนรู้และปรับปรุง |

---

## 🧾 5. การควบคุมคุณภาพ (Controlling Quality)
**Output หลัก:**
1. **Acceptance Decisions:** ผ่าน/ไม่ผ่านมาตรฐาน  
2. **Rework:** แก้ไขข้อบกพร่องให้ตรงมาตรฐาน  
3. **Process Adjustments:** ปรับปรุงกระบวนการเพื่อป้องกันปัญหาในอนาคต:contentReference[oaicite:5]{index=5}

---

## 🧰 6. เครื่องมือควบคุมคุณภาพ (Tools & Techniques)

### Seven Basic Tools of Quality
| ลำดับ | เครื่องมือ | การใช้งาน |
|--------|-------------|------------|
| 1️⃣ | **Cause-and-Effect Diagram (Fishbone)** | หาสาเหตุรากเหง้าของปัญหา |
| 2️⃣ | **Control Chart** | แสดงเสถียรภาพของกระบวนการ |
| 3️⃣ | **Checksheet** | เก็บข้อมูลอย่างมีระบบ |
| 4️⃣ | **Scatter Diagram** | วิเคราะห์ความสัมพันธ์ระหว่างตัวแปร |
| 5️⃣ | **Histogram** | แสดงการกระจายของข้อมูล |
| 6️⃣ | **Pareto Chart (80/20 Rule)** | ระบุสาเหตุหลักที่ควรแก้ก่อน |
| 7️⃣ | **Flowchart / Run Chart** | แสดงขั้นตอนและแนวโน้มกระบวนการ:contentReference[oaicite:6]{index=6}

---

### 📊 Statistical Sampling
- ใช้ตัวอย่างแทนประชากรทั้งหมด  
- สูตรคำนวณตัวอย่าง (Cochran’s Formula):  
  \[
  n = \frac{Z^2 \times 0.25}{E^2}
  \]
  เช่น ความเชื่อมั่น 95% (Z = 1.96), ขอบผิดพลาด 5% → ต้องใช้ 384 ตัวอย่าง:contentReference[oaicite:7]{index=7}

---

### ⚙️ Six Sigma
> แนวทางลดความแปรปรวนในกระบวนการผลิต เพื่อให้เกิด “Defect ≤ 3.4 ต่อหนึ่งล้านโอกาส”:contentReference[oaicite:8]{index=8}

**แนวคิดหลัก**
- ใช้สถิติวัดและปรับปรุงคุณภาพกระบวนการ  
- กระบวนการ DMAIC (ลดข้อบกพร่อง):  
  **Define → Measure → Analyze → Improve → Control**  
- กระบวนการ DMADV (ออกแบบใหม่):  
  **Define → Measure → Analyze → Design → Verify**  
- ลำดับความเชี่ยวชาญ: **Yellow → Green → Black → Master Black Belt**

---

### 💡 Six 9s of Quality
- หมายถึง **99.9999% ความพร้อมใช้งานของระบบ** (Downtime ~30 วินาที/ปี)  
- ใช้ในอุตสาหกรรมโทรคมนาคมและระบบที่ต้องการเสถียรสูง:contentReference[oaicite:9]{index=9}

---

### 🧪 การทดสอบคุณภาพ (Testing)
| ประเภท | จุดประสงค์ |
|----------|--------------|
| **Unit Test** | ตรวจสอบโมดูลเดี่ยว |
| **Integration Test** | ตรวจสอบการเชื่อมต่อระหว่างโมดูล |
| **System Test** | ตรวจสอบระบบทั้งหมด |
| **User Acceptance Test (UAT)** | ทดสอบโดยผู้ใช้จริงก่อนส่งมอบ:contentReference[oaicite:10]{index=10}  

> *Watts Humphrey* กล่าวไว้ว่า “การทดสอบเพียงอย่างเดียวไม่เพียงพอ ต้องออกแบบกระบวนการที่ลดข้อผิดพลาดตั้งแต่ต้นทาง”

---

## 🌟 7. แนวคิดการจัดการคุณภาพสมัยใหม่ (Modern Quality Management)
- เน้น **Customer Satisfaction**  
- **Prevention > Inspection**  
- ผู้บริหารต้องมีส่วนร่วมในความรับผิดชอบด้านคุณภาพ:contentReference[oaicite:11]{index=11}

---

## 💼 8. การยกระดับคุณภาพในโครงการ IT
### 🔹 Leadership
- ปัญหาคุณภาพส่วนใหญ่เกิดจาก “การจัดการ” ไม่ใช่เทคนิค  
- ผู้นำควรส่งเสริมมาตรฐานคุณภาพและการฝึกอบรมอย่างต่อเนื่อง:contentReference[oaicite:12]{index=12}

### 🔹 Cost of Quality (COQ)
| ประเภทต้นทุน | คำอธิบาย |
|----------------|-----------|
| **Prevention Cost** | ป้องกันข้อผิดพลาด เช่น การฝึกอบรม |
| **Appraisal Cost** | ตรวจสอบคุณภาพ |
| **Internal Failure Cost** | แก้ไขก่อนถึงลูกค้า |
| **External Failure Cost** | แก้ไขหลังลูกค้าใช้งาน |
| **Measurement Cost** | เครื่องมือและอุปกรณ์ที่ใช้ตรวจสอบคุณภาพ:contentReference[oaicite:13]{index=13}

---

## 🧠 9. ปัจจัยเพิ่มเติม
- สภาพแวดล้อมการทำงานที่ดี → เพิ่ม Productivity  
- วัฒนธรรมองค์กรต่างกันส่งผลต่อมาตรฐานคุณภาพ:contentReference[oaicite:14]{index=14}  

---

## 🏗️ 10. โมเดลความเป็นผู้ใหญ่ด้านคุณภาพ (Maturity Models)
| โมเดล | จุดเน้น |
|--------|----------|
| **SQFD** | การแปลงความต้องการผู้ใช้เป็นแผนคุณภาพ |
| **CMMI** | พัฒนาและปรับปรุงกระบวนการ (5 ระดับ: Incomplete → Optimizing) |
| **OPM3 (PMI)** | ความเป็นเลิศด้าน Project, Program, Portfolio Management:contentReference[oaicite:15]{index=15}

---

## 💻 11. ซอฟต์แวร์ที่ช่วยจัดการคุณภาพ
- **Spreadsheet / Chart Tools:** ใช้สร้างกราฟควบคุมคุณภาพ  
- **Statistical Tools:** เช่น Minitab, SPSS  
- **Six Sigma Tools:** ช่วยติดตาม DMAIC และวิเคราะห์ Defect:contentReference[oaicite:16]{index=16}

---

## 🌀 12. การจัดการคุณภาพใน Agile
- มีการตรวจสอบและรีวิวคุณภาพทุก Iteration  
- ใช้ **Retrospective** เพื่อหาสาเหตุของปัญหาและแนวทางปรับปรุง  
- มี **Definition of Done (DoD)** ที่รวมเกณฑ์คุณภาพไว้ด้วย:contentReference[oaicite:17]{index=17}

---

## 📚 สรุปท้ายบท
- Project Quality Management ประกอบด้วย 3 กระบวนการ: **Plan – Manage – Control**  
- เครื่องมือสำคัญ: **Seven Tools**, **Six Sigma**, **Testing**  
- คุณภาพต้องการ **การมีส่วนร่วมจากผู้นำ** และ **การปรับปรุงอย่างต่อเนื่อง (Continuous Improvement)**  
- ใน Agile ต้องมีการตรวจสอบคุณภาพทุก Iteration เพื่อปรับปรุงเร็วขึ้น:contentReference[oaicite:18]{index=18}

---

## 🧾 แนวข้อสอบแบบกากบาท (Multiple Choice)

1. เครื่องมือใดไม่อยู่ใน “Seven Basic Tools of Quality”  
   - A) Histogram  
   - ✅ B) Gantt Chart  
   - C) Control Chart  
   - D) Pareto Chart  

2. แนวคิดของ Kaizen เน้นเรื่องใด  
   - A) การตรวจสอบข้อผิดพลาดภายหลัง  
   - ✅ B) การปรับปรุงอย่างต่อเนื่อง  
   - C) การลดเวลาในกระบวนการ  
   - D) การย่นงบประมาณ  

3. WIP Limit เป็นแนวคิดของ  
   - A) Scrum  
   - ✅ B) Kanban  
   - C) Lean  
   - D) CMMI  

4. กระบวนการ DMAIC ใช้ในบริบทใด  
   - ✅ A) การปรับปรุงกระบวนการเพื่อลดข้อบกพร่อง  
   - B) การพัฒนา Requirement  
   - C) การสร้าง WBS  
   - D) การวิเคราะห์ความเสี่ยง  

5. “Six 9s of Quality” หมายถึง  
   - A) การตรวจสอบ 9 ขั้นตอน  
   - ✅ B) ระบบที่พร้อมใช้งาน 99.9999%  
   - C) ระดับ Sigma 9  
   - D) การวัด Productivity  

6. ข้อใดเป็นตัวอย่างของ Cost of Nonconformance  
   - A) การฝึกอบรมพนักงาน  
   - ✅ B) ค่าแก้ไขเมื่อผลิตภัณฑ์เสียหลังขาย  
   - C) การทดสอบซอฟต์แวร์ก่อนส่งมอบ  
   - D) การวางแผนคุณภาพ  

7. Pareto Chart ช่วยในการ  
   - ✅ A) ระบุสาเหตุหลักของปัญหาที่ส่งผลมากที่สุด  
   - B) แสดงความสัมพันธ์ของสองตัวแปร  
   - C) ตรวจสอบเสถียรภาพของกระบวนการ  
   - D) วัดแนวโน้มของข้อมูลตามเวลา  

8. หน่วยวัดคุณภาพใน Six Sigma คือ  
   - ✅ A) Defects Per Million Opportunities (DPMO)  
   - B) Earned Value  
   - C) Story Points  
   - D) PERT Estimate  

9. Agile ใช้การทดสอบคุณภาพแบบใด  
   - ✅ A) ทดสอบในแต่ละ Iteration ด้วยผู้ใช้จริง (User Testing)  
   - B) ทดสอบตอนจบโครงการเท่านั้น  
   - C) ใช้การทดสอบอัตโนมัติเท่านั้น  
   - D) ไม่มีการทดสอบ  

10. เครื่องมือใดช่วยลด Waste ในกระบวนการพัฒนา  
    - A) Benchmarking  
    - ✅ B) Lean  
    - C) Fishbone  
    - D) PERT  

---

📖 **คำแนะนำก่อนสอบ**
- จำ 3 กระบวนการหลัก: **Plan – Manage – Control**  
- รู้จัก **Seven Tools of Quality**, **DMAIC**, **Cost of Quality**  
- เข้าใจความแตกต่างของ Lean / Kaizen / Kanban  
- จำว่า “Six Sigma → ลด Defect”, “Six 9s → เพิ่ม Availability”  
- Agile ต้องมี **Definition of Done** ที่รวมเกณฑ์คุณภาพไว้เสมอ  
