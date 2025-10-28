# 📘 Chapter 8: Project Quality Management

> แหล่งที่มา: *Information Technology Project Management (9th Edition)*  
> โดย Kathy Schwalbe / Twittie Senivongse (ed.)  
> “Quality is not an act, it is a habit.” – Aristotle

---

## 🎯 Learning Objectives

1. เข้าใจแนวคิดของ Project Quality Management และความสัมพันธ์กับ IT Projects  
2. อธิบายกระบวนการ Plan – Manage – Control Quality  
3. รู้จักเครื่องมือ 7 ประการของการควบคุมคุณภาพ (Seven Basic Tools of Quality)  
4. อธิบายหลักการ Lean, Kaizen, Kanban, Benchmarking และ Quality Audit  
5. เข้าใจแนวคิด Six Sigma, Cost of Quality, และ Testing  
6. อธิบายการประยุกต์ใช้ Software และ Agile กับ Quality Management:contentReference[oaicite:1]{index=1}

---

## 🧩 ความหมายของ “Quality”

| มาตรฐาน | ความหมาย |
|-----------|------------|
| **ISO 8042 (1994)** | Totality of characteristics that satisfy needs |
| **ISO 9000 (2000)** | Degree to which inherent characteristics fulfil requirements |

**นิยามทั่วไป**
- **Conformance to requirements** → ผลิตภัณฑ์ตรงตามข้อกำหนด  
- **Fitness for use** → ใช้งานได้ตามวัตถุประสงค์:contentReference[oaicite:2]{index=2}

---

## ⚙️ กระบวนการหลักของ Project Quality Management

| ลำดับ | Process | คำอธิบาย | Output |
|--------|----------|-----------|---------|
| 1️⃣ | **Plan Quality Management** | ระบุมาตรฐานคุณภาพที่เกี่ยวข้อง | Quality Management Plan |
| 2️⃣ | **Manage Quality** | ดำเนินกิจกรรมเพื่อให้ได้คุณภาพตามแผน | Quality Reports, Process Improvements |
| 3️⃣ | **Control Quality** | ตรวจสอบและประเมินผลผลิตจริง | Quality Metrics, Validated Deliverables |

---

## 🧱 1️⃣ Plan Quality Management

แนวทางการป้องกันข้อบกพร่อง (Prevention over Inspection)
- เลือกวัสดุที่เหมาะสม  
- ฝึกอบรมบุคลากรด้านคุณภาพ  
- วางแผนกระบวนการที่ให้ผลลัพธ์ที่ถูกต้องตั้งแต่แรก  

### 📋 ปัจจัยที่มีผลต่อคุณภาพ
| ด้าน | ตัวอย่าง |
|------|-----------|
| Functionality | ระบบติดตามยอดขายได้ครบถ้วน |
| Features | GUI ที่ใช้งานง่าย มี online help |
| Performance | ทำงานได้รวดเร็ว |
| Reliability | ใช้งานได้ต่อเนื่อง ไม่ล่มบ่อย |
| Maintainability | ซ่อมบำรุงได้ง่าย |

### 🧩 มาตรฐานสำคัญ
- **ISO 9000** – มาตรฐานระบบคุณภาพองค์กร  
- **ISO/IEC 25010 (SQuaRE)** – คุณภาพของระบบและซอฟต์แวร์  
- **IEEE 730** – มาตรฐานกระบวนการประกันคุณภาพซอฟต์แวร์:contentReference[oaicite:3]{index=3}

---

## 🧭 2️⃣ Manage Quality

รวมกิจกรรม **Quality Assurance (QA)** และ **Continuous Improvement**

### 🧠 แนวคิดหลัก
| แนวคิด | ความหมาย |
|----------|-----------|
| **Lean** | ลดของเสีย (Waste) เพิ่มคุณค่าให้ลูกค้า |
| **Kaizen** | ปรับปรุงอย่างต่อเนื่อง โดยให้ทุกคนมีส่วนร่วม |
| **Kanban** | ระบบกระดานแสดงสถานะงานแบบ Visual Workflow |
| **Benchmarking** | เปรียบเทียบกับองค์กรอื่นเพื่อปรับปรุงมาตรฐาน |
| **Quality Audit** | ตรวจสอบคุณภาพโดยทีมภายใน/ภายนอก เพื่อระบุจุดปรับปรุง:contentReference[oaicite:4]{index=4}

---

### 💡 ตัวอย่าง Waste (ของเสีย) ใน Lean
| ประเภท | ตัวอย่าง |
|----------|-----------|
| Information Waste | ป้อนข้อมูลซ้ำ, ข้อมูลผิดพลาด, ฟอร์แมตไม่ตรงกัน |
| Process Waste | Rework, Waiting, Overprocessing |
| People Waste | Multitasking, Role ไม่ชัดเจน, ขาดการฝึกอบรม |

---

## 🧾 3️⃣ Control Quality

ตรวจสอบผลลัพธ์ของโครงการให้ตรงตามมาตรฐานคุณภาพ

### Output สำคัญ
- **Acceptance Decisions** → ผ่าน / ไม่ผ่าน  
- **Rework** → การแก้ไขงานที่ไม่ผ่านมาตรฐาน  
- **Process Adjustments** → ปรับกระบวนการป้องกันข้อผิดพลาดในอนาคต:contentReference[oaicite:5]{index=5}

---

## 🔍 Tools & Techniques for Quality Control

### 🧰 Seven Basic Tools of Quality

| ลำดับ | เครื่องมือ | จุดประสงค์ |
|--------|--------------|--------------|
| 1️⃣ | **Cause-and-Effect Diagram (Fishbone)** | หา “Root Cause” ของปัญหา |
| 2️⃣ | **Control Chart** | ตรวจเสถียรภาพของกระบวนการ (ดูว่าอยู่ใน Control Limit หรือไม่) |
| 3️⃣ | **Checksheet** | เก็บข้อมูลเหตุการณ์ เช่น จำนวน Defect |
| 4️⃣ | **Scatter Diagram** | แสดงความสัมพันธ์ระหว่างตัวแปร |
| 5️⃣ | **Histogram** | แสดงการกระจายของข้อมูล |
| 6️⃣ | **Pareto Chart (80/20 Rule)** | เน้นสาเหตุหลักที่กระทบมากที่สุด |
| 7️⃣ | **Flowchart / Run Chart** | วิเคราะห์ขั้นตอนของกระบวนการและแนวโน้มเวลา:contentReference[oaicite:6]{index=6}

---

## 📊 Statistical Sampling

> ใช้สุ่มตัวอย่างเพื่อตรวจสอบคุณภาพโดยไม่ต้องตรวจทั้งหมด  

📘 **สูตรประมาณขนาดตัวอย่าง (Cochran’s Formula):**
\[
n = \frac{(Z^2)(0.25)}{E^2}
\]

| ระดับความมั่นใจ | Z (Certainty Factor) | Margin of Error | ขนาดตัวอย่าง (n) |
|--------------------|--------------------|-----------------|--------------------|
| 99% | 2.576 | 0.01 | 16,589 |
| 95% | 1.96 | 0.05 | 384 |
| 90% | 1.645 | 0.10 | 68 |
| 80% | 1.281 | 0.20 | 10 |

---

## 🧮 Six Sigma

### ความหมาย
ชุดเครื่องมือและหลักการเพื่อ **ลดความแปรปรวน (Variation)** และ **ข้อบกพร่อง (Defects)**  
- เป้าหมาย: **3.4 Defects ต่อ 1,000,000 โอกาส**  
- ใช้หลักการ **±6σ** จากค่าเฉลี่ยใน Control Chart:contentReference[oaicite:7]{index=7}

| ระดับ Sigma | ความแม่นยำ (%) | DPMO |
|--------------|------------------|------|
| 3σ | 99.73% | 66,800 |
| 4σ | 99.9937% | 6,210 |
| 5σ | 99.999943% | 230 |
| 6σ | 99.9999998% | 3.4 |

### วิธีการ
- **DMAIC** → ใช้ปรับปรุงกระบวนการ (Define – Measure – Analyze – Improve – Control)  
- **DMADV** → ใช้สร้างกระบวนการใหม่ (Define – Measure – Analyze – Design – Verify)

---

## 🔹 Six 9s of Quality

- หมายถึงคุณภาพระดับ **99.9999% (fault = 1 ต่อ 1,000,000)**  
- เช่น โทรคมนาคม uptime = 99.9999% → downtime ~30 วินาที/ปี:contentReference[oaicite:8]{index=8}

---

## 🧪 Testing

- ต้องทำทุกเฟสของ SDLC (ไม่ใช่เฉพาะตอนท้าย)  
| ประเภทการทดสอบ | จุดประสงค์ |
|------------------|-------------|
| **Unit Testing** | ตรวจโค้ดแต่ละโมดูล |
| **Integration Testing** | ตรวจความเชื่อมโยงของระบบย่อย |
| **System Testing** | ตรวจระบบรวมทั้งหมด |
| **User Acceptance Testing (UAT)** | ตรวจโดยผู้ใช้ก่อนรับมอบระบบ:contentReference[oaicite:9]{index=9}

---

## 🧠 Modern Quality Management

หลักการสำคัญ:
- เน้น **Customer Satisfaction**
- เน้น **Prevention มากกว่า Inspection**
- ผู้บริหารต้องรับผิดชอบคุณภาพโดยตรง:contentReference[oaicite:10]{index=10}

---

## 💵 Cost of Quality

| ประเภทต้นทุน | คำอธิบาย |
|---------------|-----------|
| **Prevention Cost** | ค่าใช้จ่ายเพื่อป้องกันข้อผิดพลาด (Training, Planning) |
| **Appraisal Cost** | ค่าใช้จ่ายในการตรวจประเมินคุณภาพ |
| **Internal Failure Cost** | ค่าแก้ไขข้อผิดพลาดก่อนส่งมอบ |
| **External Failure Cost** | ค่าเสียหายหลังส่งมอบลูกค้า |
| **Measurement Cost** | ค่าทดสอบและเครื่องมือวัดคุณภาพ:contentReference[oaicite:11]{index=11}

---

## 🧩 Maturity Models

| โมเดล | จุดเด่น |
|--------|----------|
| **SQFD** | เน้นการแปลงความต้องการผู้ใช้เป็นคุณลักษณะซอฟต์แวร์ |
| **CMMI** | ระดับ 1–5: Incomplete → Optimizing |
| **OPM3** | มาตรฐาน PMI เพื่อวัดระดับความเป็นผู้ใหญ่ด้านการบริหารโครงการ:contentReference[oaicite:12]{index=12}

---

## ⚙️ Agile Quality Considerations

- ตรวจสอบคุณภาพในทุก Iteration  
- ใช้ Retrospective เพื่อปรับปรุงต่อเนื่อง  
- มี **Definition of Done (DoD)** ชัดเจนที่รวมเกณฑ์คุณภาพ  
- ทดสอบโดยผู้ใช้ในแต่ละรอบ:contentReference[oaicite:13]{index=13}

---

# 🧩 แบบทดสอบท้ายบท

1. Project Quality Management มีกี่กระบวนการ  
   - [ ] 2  
   - [X] 3  
   - [ ] 4  
   - [ ] 5  

2. ข้อใดคือมาตรฐานระบบคุณภาพองค์กร  
   - [X] ISO 9000  
   - [ ] IEEE 802.11  
   - [ ] ISO/IEC 27001  
   - [ ] ISO 25010  

3. แนวคิด Lean มุ่งเน้นสิ่งใด  
   - [ ] เพิ่มขั้นตอนการทำงาน  
   - [ ] เพิ่มคนทำงาน  
   - [X] ลดของเสีย เพิ่มคุณค่าให้ลูกค้า  
   - [ ] ทำงานให้เสร็จเร็วที่สุด  

4. Kanban คืออะไร  
   - [ ] ตารางค่าใช้จ่าย  
   - [ ] ระบบสำรองข้อมูล  
   - [X] Visual Workflow สำหรับบริหารงาน  
   - [ ] ระบบจัดเก็บเอกสาร  

5. Kaizen หมายถึง  
   - [X] การปรับปรุงอย่างต่อเนื่อง  
   - [ ] การตรวจสอบคุณภาพ  
   - [ ] การวิเคราะห์สาเหตุ  
   - [ ] การวางแผนต้นทุน  

6. Pareto Chart ใช้หลักการอะไร  
   - [ ] 60/40 Rule  
   - [ ] Fishbone Rule  
   - [X] 80/20 Rule  
   - [ ] Normal Rule  

7. ถ้าพบว่า Process อยู่ “Out of Control” หมายถึงอะไร  
   - [ ] อยู่ในขอบเขตมาตรฐาน  
   - [X] มีความแปรปรวนผิดปกติ ต้องปรับกระบวนการ  
   - [ ] ผลิตภัณฑ์ได้คุณภาพดี  
   - [ ] ควรหยุดการตรวจสอบ  

8. ข้อใดไม่ใช่ต้นทุนคุณภาพ (Cost of Quality)  
   - [ ] Prevention Cost  
   - [ ] Appraisal Cost  
   - [X] Marketing Cost  
   - [ ] Internal Failure Cost  

9. ระดับ Sigma ที่ได้คุณภาพสูงสุดคือ  
   - [ ] 4σ  
   - [ ] 5σ  
   - [X] 6σ  
   - [ ] 3σ  

10. ใน Agile Project “Definition of Done” ควรมีอะไร  
    - [ ] ขอบเขตงานเท่านั้น  
    - [ ] งบประมาณ  
    - [X] เกณฑ์คุณภาพที่ชัดเจน  
    - [ ] กำหนดเวลาอย่างเดียว  

---

## ✅ เฉลยท้ายบท

| ข้อ | คำตอบ | หมายเหตุ |
|-----|--------|-----------|
| 1 | ✅ 3 | Plan – Manage – Control |
| 2 | ✅ ISO 9000 | มาตรฐานระบบคุณภาพ |
| 3 | ✅ ลดของเสีย | Lean Principle |
| 4 | ✅ Visual Workflow | Kanban |
| 5 | ✅ ปรับปรุงต่อเนื่อง | Kaizen |
| 6 | ✅ 80/20 Rule | Pareto Principle |
| 7 | ✅ Out of Control | ความแปรปรวนผิดปกติ |
| 8 | ✅ Marketing Cost | ไม่อยู่ใน Cost of Quality |
| 9 | ✅ 6σ | สูงสุดใน Six Sigma |
| 10 | ✅ Quality Criteria | Agile DoD |

---

> 💡 **Tips สำหรับสอบ**
> - จำ 3 ขั้นตอน: Plan → Manage → Control  
> - 7 Tools of Quality = Fishbone, Control Chart, Checksheet, Scatter, Histogram, Pareto, Flowchart  
> - Lean ลด Waste, Kaizen ปรับปรุงต่อเนื่
