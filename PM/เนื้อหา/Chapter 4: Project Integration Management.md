# 📘 บทที่ 4: การบูรณาการการจัดการโครงการ  
(*Chapter 4: Project Integration Management*)  
จาก *Information Technology Project Management, Ninth Edition*:contentReference[oaicite:0]{index=0}

---

## 🎯 วัตถุประสงค์การเรียนรู้
- เข้าใจภาพรวมของ **Project Integration Management** และความสัมพันธ์กับ **Project Life Cycle**  
- อธิบายขั้นตอนการสร้าง **Project Charter** และ **Project Management Plan**  
- อธิบายการดำเนินงาน การควบคุม และการปิดโครงการ  
- เข้าใจแนวคิด **Change Control System** และการจัดการความรู้ (Knowledge Management)  
- วิเคราะห์การใช้ซอฟต์แวร์เพื่อช่วยในการบริหารและแนวทาง **Agile / Adaptive Environment**  

---

## 🧩 1. ความหมายของ Project Integration Management
> เป็นกระบวนการสำคัญที่ “เชื่อมโยงทุกองค์ความรู้ (Knowledge Areas)” เข้าด้วยกันตลอดวงจรชีวิตของโครงการ:contentReference[oaicite:1]{index=1}

### ✅ กระบวนการหลัก (ตาม PMBOK 6th Edition)
1. **Develop Project Charter**  
2. **Develop Project Management Plan**  
3. **Direct and Manage Project Work**  
4. **Manage Project Knowledge**  
5. **Monitor and Control Project Work**  
6. **Perform Integrated Change Control**  
7. **Close Project or Phase**

---

## 🧭 2. การวางแผนเชิงกลยุทธ์ (Strategic Planning)
- จุดเริ่มต้นของการบริหารโครงการคือ “การเลือกว่าจะทำโครงการใด”  
- ใช้การวิเคราะห์ **SWOT (Strengths, Weaknesses, Opportunities, Threats)** เพื่อประเมินความเหมาะสมของโครงการ  

---

## ⚙️ 3. วิธีการคัดเลือกโครงการ (Project Selection Methods)
องค์กรจะใช้หลายวิธีร่วมกัน เช่น:
| วิธี | รายละเอียด |
|------|-------------|
| **1. Broad Organizational Needs** | พิจารณาจาก “Need, Funding, Will” |
| **2. Categorizing IT Projects** | แบ่งเป็น Problems, Opportunities, Directives, Timing, Priority |
| **3. Financial Analysis** | วิเคราะห์ **NPV**, **ROI**, **Payback Period** |
| **4. Weighted Scoring Model** | ให้คะแนนและน้ำหนักแต่ละปัจจัย ก่อนคำนวณคะแนนรวม |

### 💰 ตัวอย่างการวิเคราะห์ทางการเงิน
- **NPV (Net Present Value):** คำนวณมูลค่าปัจจุบันของกระแสเงินสดทั้งหมด  
- **ROI (Return on Investment):**  
  \[
  ROI = \frac{(ผลประโยชน์ - ต้นทุน)}{ต้นทุน} \times 100
  \]
- **Payback Period:** ระยะเวลาที่ผลตอบแทนครอบคลุมเงินลงทุนทั้งหมด  

---

## 🧾 4. การพัฒนาเอกสารหลักของโครงการ

### 🔹 4.1 Project Charter  
- เอกสารที่ “รับรองการมีอยู่ของโครงการ” อย่างเป็นทางการ  
- ระบุวัตถุประสงค์ เป้าหมาย และอำนาจของ Project Manager  
- ต้องได้รับการอนุมัติจากผู้บริหาร (Sponsor)  

**Output:** Project Charter, Assumption Log

---

### 🔹 4.2 Project Management Plan  
- เอกสารที่รวมแผนย่อยทั้งหมดเข้าด้วยกัน  
- มีทั้ง **Management Plan** (Scope, Schedule, Risk ฯลฯ) และ **Technical Plan** (Tools, Infrastructure, QA)  
- มาตรฐานอ้างอิง: *IEEE 1058 Software Project Management Plan (SPMP)*  

**หัวข้อหลัก:**  
1. Overview & Purpose  
2. Project Organization  
3. Managerial Process Plans  
4. Technical Process Plans  
5. Supporting Process Plans (QA, Config Mgmt, Reviews)

---

## 🚀 5. การดำเนินการและการควบคุม (Execution & Control)
### 🔸 Directing and Managing Project Work
- บริหารทีมงานและผู้มีส่วนได้ส่วนเสีย  
- ใช้ **Project Information Systems** และการประชุมเพื่อติดตามงาน  

### 🔸 Managing Project Knowledge
- ความรู้มี 2 ประเภท:
  - **Explicit:** เอกสาร, แผน, คู่มือ  
  - **Tacit:** ประสบการณ์, ความเชื่อ, ความเข้าใจเฉพาะตัว  
- ใช้ **Lessons-Learned Repository** เพื่อเก็บองค์ความรู้ตลอดโครงการ  

### 🔸 Monitoring and Controlling Project Work
- ตรวจสอบความคืบหน้าโดยใช้ Baseline และ Key Performance Indicators  
- **Output:** Status Report, Forecasts, Change Requests  

---

## 🔄 6. การควบคุมการเปลี่ยนแปลง (Integrated Change Control)
> “Change is inevitable” — การเปลี่ยนแปลงหลีกเลี่ยงไม่ได้ ต้องจัดการอย่างมีระบบ:contentReference[oaicite:2]{index=2}

### 💼 ระบบ Change Control ประกอบด้วย:
| องค์ประกอบ | รายละเอียด |
|--------------|-------------|
| **Change Control Board (CCB)** | กลุ่มผู้มีอำนาจอนุมัติ / ปฏิเสธการเปลี่ยนแปลง |
| **Configuration Management** | ควบคุมและตรวจสอบเวอร์ชันของเอกสารและโค้ด |
| **Communication Process** | แจ้งการเปลี่ยนแปลงแก่ผู้เกี่ยวข้องอย่างเป็นทางการ |

### 🔹 แนวคิดใหม่  
- เดิม: ทำตามแผนให้ตรงที่สุด  
- ปัจจุบัน: เปลี่ยนแปลงได้ “หากเพิ่มคุณค่าและสอดคล้องกับเป้าหมายองค์กร”  

---

## 🏁 7. การปิดโครงการ (Closing Project or Phase)
- ตรวจสอบงานทั้งหมดเสร็จสมบูรณ์  
- ส่งมอบผลผลิต (Deliverables)  
- จัดทำเอกสารสำคัญ เช่น:
  - **Final Report**
  - **Lessons Learned**
  - **Post-Implementation Review**
  - **Project Closure Form**  

---

## 💻 8. การใช้ซอฟต์แวร์ช่วยในการบริหาร
- Word / Excel → สร้างเอกสารและติดตามงบประมาณ  
- Project Management Software (เช่น MS Project, ProjectPlan365) → แสดง Gantt Chart, Baseline  
- Communication Tools → Email, Slack, Teams, Zoom  

---

## 🧠 9. Agile / Adaptive Integration
- ผู้จัดการโครงการยังคงต้องทำหน้าที่บูรณาการ (Integration)  
- แต่เปิดให้ทีมเป็นผู้วางแผนและส่งมอบรายละเอียดเองในแต่ละ Sprint  
- เน้น **Collaboration, Transparency, Adaptability**  

---

## 📚 สรุปท้ายบท
- การบูรณาการเป็นหัวใจของการบริหารโครงการ  
- ต้องเชื่อมโยงทุกองค์ความรู้เข้าด้วยกัน  
- มี 7 กระบวนการหลักจาก Initiation → Closing  
- การเปลี่ยนแปลงต้องได้รับการจัดการอย่างมีระบบผ่าน **Change Control System**  
- ความรู้และบทเรียนจากโครงการควรถูกบันทึกเพื่อปรับปรุงในอนาคต  

---

## 🧾 แนวข้อสอบแบบกากบาท (Multiple Choice)

1. Project Integration Management หมายถึงอะไร  
   - A) การควบคุมการเปลี่ยนแปลงของโครงการ  
   - ✅ B) การบูรณาการองค์ความรู้ทั้งหมดในวงจรชีวิตโครงการ  
   - C) การจัดสรรทรัพยากรบุคคล  
   - D) การสร้างแผนงานเท่านั้น  

2. เอกสารใดใช้รับรองการมีอยู่ของโครงการ  
   - A) Risk Register  
   - ✅ B) Project Charter  
   - C) Scope Statement  
   - D) Lessons Learned  

3. ขั้นตอนใดมีการอนุมัติ Change Request  
   - A) Planning  
   - ✅ B) Perform Integrated Change Control  
   - C) Execution  
   - D) Closing  

4. Project Management Plan ตามมาตรฐาน IEEE 1058 ประกอบด้วยอะไรบ้าง  
   - ✅ A) Overview, Organization, Managerial, Technical, Supporting Plans  
   - B) Cost, Schedule, Risk, Communication, Stakeholder  
   - C) Charter, Report, Procurement, QA, HR  
   - D) Planning, Monitoring, Closing, Review  

5. การควบคุมการเปลี่ยนแปลง (Change Control System) ต้องมีอะไร  
   - ✅ A) CCB, Configuration Management, Communication  
   - B) WBS, Scope, Budget  
   - C) Sprint, Burndown, Backlog  
   - D) Stakeholder Mapping  

6. องค์กรควรเลือกโครงการที่มีลักษณะใด  
   - A) ต้องการเทคโนโลยีใหม่  
   - ✅ B) มีความจำเป็น, งบประมาณ, และความมุ่งมั่น (Need, Funding, Will)  
   - C) ใช้เวลาสั้นที่สุด  
   - D) เสี่ยงต่ำที่สุด  

7. Explicit Knowledge หมายถึงอะไร  
   - ✅ A) ความรู้ที่อธิบายได้ด้วยคำพูดและตัวเลข  
   - B) ความเข้าใจที่เกิดจากประสบการณ์ส่วนตัว  
   - C) ความคิดเห็นของผู้บริหาร  
   - D) ความลับขององค์กร  

8. ใครเป็นผู้มีอำนาจอนุมัติการเปลี่ยนแปลงในโครงการ  
   - A) Project Sponsor  
   - ✅ B) Change Control Board (CCB)  
   - C) Project Analyst  
   - D) Team Leader  

9. เอกสาร Lessons Learned ควรถูกจัดทำในขั้นตอนใด  
   - A) Initiation  
   - B) Planning  
   - C) Execution  
   - ✅ D) Closing  

10. ในบริบท Agile ผู้จัดการโครงการควรมุ่งเน้นอะไร  
    - A) ควบคุมรายละเอียดทุกงาน  
    - ✅ B) สร้างสภาพแวดล้อมให้ทีมร่วมตัดสินใจและตอบสนองต่อการเปลี่ยนแปลง  
    - C) กำหนดเวลาแน่นอนให้ทุก Sprint  
    - D) ทำแผนแบบละเอียดก่อนเริ่มงาน  

---

📖 **คำแนะนำก่อนสอบ**
- จำลำดับ 7 กระบวนการหลักของ Integration ให้ได้ครบ  
- เข้าใจความแตกต่างระหว่าง **NPV, ROI, Payback Period**  
- รู้หน้าที่ของ **CCB** และ **Configuration Management**  
- ทบทวนความหมายของ **Explicit vs Tacit Knowledge**  
- เข้าใจบทบาทของ Project Manager ใน **Agile Context**  
