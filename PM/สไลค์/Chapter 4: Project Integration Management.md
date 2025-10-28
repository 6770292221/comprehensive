# 📘 Chapter 4: Project Integration Management

> แหล่งที่มา: *Information Technology Project Management, 9th Edition* — Kathy Schwalbe / Twittie Senivongse (ed.)

---

## 🎯 Learning Objectives

1. อธิบายกรอบรวมของ Project Integration Management  
2. เข้าใจกระบวนการวางแผนเชิงกลยุทธ์และการคัดเลือกโครงการ  
3. อธิบายความสำคัญของ Project Charter และ Project Management Plan  
4. เข้าใจการดำเนินงาน การจัดการความรู้ การควบคุมการเปลี่ยนแปลง และการปิดโครงการ  
5. เชื่อมโยงกับเครื่องมือ Software และแนวทาง Agile/Adaptive Environment  

---

## 🧩 Concept Overview

**Project Integration Management** คือ การประสานทุกองค์ความรู้ของการบริหารโครงการเข้าด้วยกันตลอดวงจรชีวิตโครงการ  
ประกอบด้วย 7 กระบวนการหลัก (PMBOK® 6th Ed.):contentReference[oaicite:1]{index=1}

| # | Process | Key Output |
|---|----------|-------------|
| 1 | Develop Project Charter | Project Charter |
| 2 | Develop Project Management Plan | PM Plan (รวมแผนย่อยทั้งหมด) |
| 3 | Direct & Manage Project Work | Deliverables |
| 4 | Manage Project Knowledge | Lessons Learned Register |
| 5 | Monitor & Control Project Work | Status Report / Change Request |
| 6 | Perform Integrated Change Control | Approved Change Requests |
| 7 | Close Project or Phase | Final Report, Lessons Learned |

---

## 💡 Strategic Planning & Project Selection

องค์กรต้องเริ่มจาก **Strategic Planning** เพื่อเลือกโครงการที่สอดคล้องกับเป้าหมายระยะยาว  
โดยใช้เครื่องมือดังนี้:

### 🔹 SWOT Analysis
วิเคราะห์ **Strengths / Weaknesses / Opportunities / Threats** เพื่อคาดการณ์โอกาสและความเสี่ยงในตลาด:contentReference[oaicite:2]{index=2}

### 🔹 Project Selection Methods
1. **Organizational Needs** – เน้นความจำเป็น ความพร้อมด้านงบ และความมุ่งมั่น (Need, Funding, Will):contentReference[oaicite:3]{index=3}  
2. **Categorizing Projects** – แบ่งตาม Problems / Opportunities / Directives และลำดับ Priority:contentReference[oaicite:4]{index=4}  
3. **Financial Analysis** – เช่น  
   - **NPV (Net Present Value)** → โครงการที่มี NPV > 0 ควรพิจารณา  
   - **ROI (Return on Investment)** → ยิ่งสูงยิ่งดี  
   - **Payback Period** → ระยะเวลาคืนทุนสั้น = ความเสี่ยงต่ำ  
4. **Weighted Scoring Model** – กำหนดเกณฑ์ให้คะแนนแต่ละโครงการ แล้วรวมคะแนนถ่วงน้ำหนัก:contentReference[oaicite:5]{index=5}

---

## 🏗️ Core Processes of Project Integration

### 1️⃣ Develop Project Charter
- เอกสารที่ยืนยันการอนุมัติโครงการ  
- ระบุวัตถุประสงค์ ผู้รับผิดชอบ และ Sponsor  
- ให้สิทธิ์ PM ใช้ทรัพยากรองค์กรอย่างเป็นทางการ:contentReference[oaicite:6]{index=6}

### 2️⃣ Develop Project Management Plan
- รวมแผนจากทุก Knowledge Area  
- ใช้เป็นแนวทางการดำเนินโครงการ  
- ตามมาตรฐาน IEEE 1058 SPMP แบ่งเป็น 5 หมวดใหญ่ ได้แก่ Overview, Organization, Managerial, Technical, Supporting Plans:contentReference[oaicite:7]{index=7}

### 3️⃣ Direct & Manage Project Work
- ดำเนินงานตามแผน ควบคุมทรัพยากรและการสื่อสาร  
- ใช้เครื่องมือ: Expert Judgment, Meetings, PMIS (Project Management Information System):contentReference[oaicite:8]{index=8}

### 4️⃣ Manage Project Knowledge
- จัดการความรู้ทั้ง **Explicit** (เอกสาร/ตัวเลข) และ **Tacit** (ประสบการณ์/ความเชื่อ)  
- จัดทำ **Lessons Learned Register** ระหว่างและหลังโครงการ:contentReference[oaicite:9]{index=9}

### 5️⃣ Monitor & Control Project Work
- ตรวจสอบความคืบหน้าเทียบกับ Baseline (Scope, Schedule, Cost)  
- ออกรายงาน: Status / Progress / Forecast / Change Requests:contentReference[oaicite:10]{index=10}

### 6️⃣ Perform Integrated Change Control
- จัดการการเปลี่ยนแปลง (Scope-Time-Cost-Quality Trade-off)  
- ใช้ **Change Control System** ที่มีองค์ประกอบ เช่น  
  - **CCB (Change Control Board)** อนุมัติ/ปฏิเสธการเปลี่ยนแปลง  
  - **Configuration Management** → ควบคุมเวอร์ชันและความถูกต้องของเอกสาร/โค้ด:contentReference[oaicite:11]{index=11}  
  - **Communication of Change** → แจ้งข้อมูลการเปลี่ยนให้ผู้เกี่ยวข้อง:contentReference[oaicite:12]{index=12}

### 7️⃣ Close Project or Phase
- ปิดโครงการอย่างเป็นทางการ  
- ผลลัพธ์หลัก: Final Deliverable, Closure Report, Lessons Learned, Post-Implementation Review:contentReference[oaicite:13]{index=13}

---

## 🧠 Software & Agile Integration

| ด้าน | ตัวอย่างเครื่องมือ / แนวทาง |
|------|-------------------------------|
| Software Tools | MS Project, Excel, Word, PowerPoint, Jira, Trello |
| Agile Environment | ทีมเป็นผู้ควบคุมการวางแผนรายละเอียด (Self-Organized) |
| บทบาท PM | สร้างบรรยากาศการตัดสินใจร่วม, ส่งเสริมการเรียนรู้ และตอบสนองต่อการเปลี่ยนแปลง:contentReference[oaicite:14]{index=14} |

---

## 🧾 Chapter Summary

- Integration Management คือหัวใจที่รวมทุก Knowledge Area เข้าด้วยกัน  
- เครื่องมือคัดเลือกโครงการ: SWOT, NPV, ROI, Weighted Scoring  
- กระบวนการหลัก 7 ขั้น ตั้งแต่ Charter → Plan → Execution → Control → Closure  
- การเปลี่ยนแปลงต้องผ่าน CCB / Configuration / Communication System  
- ใน Agile → PM เน้น Facilitation และ Empowerment มากกว่า Control  

---

# 🧩 แบบทดสอบท้ายบท

1. ข้อใดคือจุดประสงค์หลักของ Project Integration Management  
   - [ ] การจัดการเฉพาะ Scope ของโครงการ  
   - [X] การประสานและเชื่อมโยงทุกองค์ความรู้ของการบริหารโครงการ  
   - [ ] การวิเคราะห์เฉพาะความเสี่ยงของโครงการ  
   - [ ] การจัดทำรายงานทางการเงิน  

2. SWOT Analysis ใช้เพื่ออะไร  
   - [ ] ประเมินทีมงาน  
   - [ ] คำนวณ ROI  
   - [X] วิเคราะห์จุดแข็ง จุดอ่อน โอกาส และภัยคุกคาม  
   - [ ] วางแผนกำหนดเวลาโครงการ  

3. NPV (Net Present Value) เป็นเครื่องมือใช้ในกระบวนการใด  
   - [X] การคัดเลือกโครงการ (Project Selection)  
   - [ ] การติดตามโครงการ  
   - [ ] การควบคุมการเปลี่ยนแปลง  
   - [ ] การปิดโครงการ  

4. เอกสารใดเป็นผลลัพธ์ของ Initiating Process  
   - [ ] Project Plan  
   - [X] Project Charter  
   - [ ] Risk Register  
   - [ ] Status Report  

5. ข้อใดไม่ใช่ส่วนหนึ่งของ IEEE SPMP (Software Project Management Plan)  
   - [ ] Overview  
   - [ ] Technical Plan  
   - [X] Change Request  
   - [ ] Supporting Plan  

6. Change Control Board (CCB) มีหน้าที่หลักคืออะไร  
   - [ ] สร้างแผนโครงการใหม่  
   - [X] อนุมัติหรือปฏิเสธการเปลี่ยนแปลงในโครงการ  
   - [ ] ติดตามการใช้จ่ายงบประมาณ  
   - [ ] จัดประชุมเปิดโครงการ  

7. Configuration Management มีจุดประสงค์เพื่ออะไร  
   - [ ] จัดการความรู้ในองค์กร  
   - [ ] สร้างรายงานผลการดำเนินงาน  
   - [X] ควบคุมเวอร์ชันและตรวจสอบความถูกต้องของเอกสารและซอฟต์แวร์  
   - [ ] วิเคราะห์ ROI  

8. ใน Agile Project บทบาทของ Project Manager คือ  
   - [ ] ควบคุมการตัดสินใจทุกอย่าง  
   - [ ] จัดสรรงานตามลำดับชั้น  
   - [X] สร้างบรรยากาศให้ทีมตัดสินใจร่วมและตอบสนองต่อการเปลี่ยนแปลง  
   - [ ] เป็นผู้เขียนโค้ดหลักของทีม  

9. ข้อใดเป็นผลลัพธ์หลักของกระบวนการ Close Project  
   - [ ] Gantt Chart  
   - [ ] Change Request Log  
   - [X] Lessons Learned Report และ Final Acceptance  
   - [ ] Risk Matrix  

10. ข้อใดกล่าวถูกต้องเกี่ยวกับ Integration Management  
    - [X] เป็นศูนย์กลางในการประสาน Knowledge Area ทั้งหมดในโครงการ  
    - [ ] ใช้เฉพาะในโครงการขนาดใหญ่  
    - [ ] เป็นส่วนหนึ่งของ Cost Management  
    - [ ] ใช้เฉพาะใน Waterfall Model  

---

## ✅ เฉลยท้ายบท

| ข้อ | คำตอบ | คำอธิบาย |
|-----|--------|-----------|
| 1 | ✅ Integration รวมทุกด้าน | คือการผสานทุกองค์ความรู้ของ PM |
| 2 | ✅ SWOT | วิเคราะห์กลยุทธ์องค์กร |
| 3 | ✅ NPV | ใช้เลือกโครงการที่มีมูลค่าเพิ่ม |
| 4 | ✅ Project Charter | ผลลัพธ์ของ Initiating |
| 5 | ✅ Change Request | ไม่ใช่ส่วนใน SPMP |
| 6 | ✅ CCB | อนุมัติ/ปฏิเสธการเปลี่ยนแปลง |
| 7 | ✅ Version Control | รักษาความถูกต้องของ config |
| 8 | ✅ Facilitation Role | PM ช่วยทีมตัดสินใจใน Agile |
| 9 | ✅ Lessons Learned | เอกสารสำคัญตอนปิดโครงการ |
| 10 | ✅ Core of PM | Integration = แกนกลางของการบริหารโครงการ |

---

> 💡 **Tips for Exam**
> - “7 ขั้นตอน Integration = Charter → Plan → Execute → Knowledge → Monitor → Change → Close”  
> - จำว่า Change Control = CCB + Config + Communication  
> - Agile → PM = Facilitator ไม่ใช่ Controller  
> - NPV/ROI/Payback = ใช้เลือกโครงการ (Project Selection)
