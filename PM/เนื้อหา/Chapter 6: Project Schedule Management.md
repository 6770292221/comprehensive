# 📘 บทที่ 6: การจัดการกำหนดการของโครงการ (Project Schedule Management)  
จาก *Information Technology Project Management, 9th Edition*:contentReference[oaicite:0]{index=0}

---

## 🎯 วัตถุประสงค์ของบท
1. อธิบายความสำคัญของการจัดการกำหนดการโครงการ  
2. เข้าใจกระบวนการ 6 ขั้นของ Schedule Management  
3. ใช้เครื่องมือวางแผน เช่น Gantt Chart, Network Diagram, CPM, PERT  
4. วิเคราะห์การย่นระยะเวลา (Crashing, Fast Tracking)  
5. ใช้แนวคิด Critical Chain และ Buffer เพื่อควบคุมทรัพยากร  
6. ควบคุมและติดตามตารางเวลาให้เป็นไปตามแผน  
7. อธิบายการจัดการกำหนดการใน Agile/Adaptive Environment  

---

## 🧩 1. ความสำคัญของกำหนดการโครงการ
- เวลาเป็นทรัพยากรที่ยืดหยุ่นน้อยที่สุด — ผ่านไปไม่หยุดรอ  
- ผู้จัดการโครงการส่วนใหญ่ยอมรับว่า “การส่งงานตรงเวลา” คือความท้าทายหลัก  
- ความแตกต่างทางวัฒนธรรม (เช่น วันหยุด, ชั่วโมงทำงาน) ส่งผลต่อความเข้าใจเรื่องเวลา  
- การจัดการกำหนดการที่ดีช่วยลดความขัดแย้งและเพิ่มประสิทธิภาพในการทำงาน:contentReference[oaicite:1]{index=1}

---

## ⚙️ 2. กระบวนการของ Project Schedule Management  
| ลำดับ | ชื่อกระบวนการ | คำอธิบาย |
|--------|----------------|-----------|
| 1️⃣ | **Planning Schedule Management** | วางแผนวิธีควบคุมและรายงานตารางเวลา |
| 2️⃣ | **Defining Activities** | แยกกิจกรรมจาก Deliverables ใน WBS |
| 3️⃣ | **Sequencing Activities** | จัดลำดับกิจกรรมและระบุความสัมพันธ์ |
| 4️⃣ | **Estimating Activity Durations** | ประมาณระยะเวลาในการทำแต่ละกิจกรรม |
| 5️⃣ | **Developing the Schedule** | สร้างตารางเวลาจริง เช่น Gantt Chart |
| 6️⃣ | **Controlling the Schedule** | ตรวจสอบ ติดตาม และปรับแก้เมื่อมีการเปลี่ยนแปลง |

---

## 🧭 3. การวางแผนการจัดการกำหนดการ (Planning Schedule Management)
- กำหนดระดับความละเอียด, หน่วยเวลา (วัน, ชั่วโมง)  
- ระบุวิธีวัดผลการทำงาน (% ความคืบหน้า)  
- ตั้งค่าค่าเบี่ยงเบนที่ยอมรับได้ (เช่น ±10%)  
- ระบุรูปแบบรายงานและความถี่ในการอัปเดต  
- พัฒนา **Schedule Model** = Model + Calendar Dates:contentReference[oaicite:2]{index=2}

---

## 🧱 4. การกำหนดกิจกรรม (Defining Activities)
- แยกงานจาก **WBS** ออกมาเป็น **Activity List**  
- **Activity Attributes**: Predecessor, Successor, Resource, Lead/Lag  
- **Milestone**: เหตุการณ์สำคัญ (ไม่มีระยะเวลา) เช่น Sign-off หรือการส่งมอบผลลัพธ์  

🔹 **Lead:** กิจกรรมต่อไปเริ่มก่อนกิจกรรมก่อนหน้าเสร็จ  
🔹 **Lag:** ต้องรอเวลาหลังจากกิจกรรมก่อนหน้าเสร็จ:contentReference[oaicite:3]{index=3}

---

## 🔄 5. การจัดลำดับกิจกรรม (Sequencing Activities)
- ระบุความสัมพันธ์ (Dependencies)  
| ประเภท | คำอธิบาย |
|----------|-----------|
| **Mandatory (Hard Logic)** | ต้องทำตามลำดับ เช่น ต้องทดสอบหลังพัฒนาเสร็จ |
| **Discretionary (Soft Logic)** | ทีมกำหนดเอง เช่น รอการอนุมัติ |
| **External** | พึ่งพากิจกรรมนอกโครงการ เช่น รอซัพพลายเออร์ |
| **Internal** | อยู่ภายใต้การควบคุมของทีม เช่น Unit Test → System Test |

- ใช้ **Network Diagram** เพื่อแสดงลำดับ เช่น **ADM (Activity-on-Arrow)** และ **PDM (Activity-on-Node)**:contentReference[oaicite:4]{index=4}

---

## ⏱ 6. การประมาณระยะเวลา (Estimating Activity Durations)
- **Duration ≠ Effort**  
  (เช่น ใช้แรงงาน 20 ชั่วโมง แต่กระจายทำใน 2 เดือน)
- ผู้ทำงานควรมีส่วนร่วมในการประมาณเวลา  
- ใช้ข้อมูลจากโครงการเก่า / ผู้เชี่ยวชาญ  
- **Three-Point Estimate (PERT):**  
  \[
  t_e = \frac{O + 4M + P}{6}
  \]  
  โดย O = Optimistic, M = Most likely, P = Pessimistic:contentReference[oaicite:5]{index=5}

---

## 📅 7. การพัฒนากำหนดการ (Developing the Schedule)
รวมข้อมูลจากกระบวนการก่อนหน้าเพื่อสร้าง “แผนเวลาโครงการจริง”  
เครื่องมือที่นิยมใช้:  
- **Gantt Chart**  
- **Critical Path Method (CPM)**  
- **PERT**  
- **Critical Chain Scheduling**  

---

### 🗓 Gantt Chart  
- แสดงกิจกรรมในรูปแบบปฏิทิน  
- **Diamond** = Milestone  
- **Thick bar** = Summary task  
- **Thin bar** = Duration  
- **Arrow** = ความสัมพันธ์ของงาน  

**Tracking Gantt Chart** ใช้เปรียบเทียบ Planned vs Actual  
- แสดง Baseline Start/Finish  
- ใช้ประเมินความคืบหน้าและเบี่ยงเบน:contentReference[oaicite:6]{index=6}

---

### 🧮 Critical Path Method (CPM)
> เส้นทางวิกฤติ = เส้นทางที่ยาวที่สุดใน Network Diagram และมี Float = 0

- กิจกรรมบน Critical Path หากล่าช้า → ทั้งโครงการล่าช้า  
- **Slack / Float:** เวลาที่สามารถเลื่อนโดยไม่กระทบกำหนดการ  
- คำนวณโดยใช้  
  - **ES (Early Start)**, **EF (Early Finish)**  
  - **LS (Late Start)**, **LF (Late Finish)**  
  - **TS (Total Slack)**, **FS (Free Slack)**:contentReference[oaicite:7]{index=7}

---

### 🧩 PERT (Program Evaluation and Review Technique)
ใช้เมื่อมี “ความไม่แน่นอนสูง” ในเวลาแต่ละกิจกรรม  
- ใช้สมการแบบ Probabilistic Estimate  
- ช่วยประเมินความเสี่ยงด้านเวลา  
- ใช้ร่วมกับ CPM ได้:contentReference[oaicite:8]{index=8}

---

### ⚡ เทคนิคการย่นเวลา (Schedule Compression)
| เทคนิค | รายละเอียด |
|---------|--------------|
| **Crashing** | เพิ่มทรัพยากร เช่น จ้างพนักงานเพิ่ม หรือทำ OT |
| **Fast Tracking** | ทำกิจกรรมบางอย่าง “ซ้อนกัน” หรือ “ขนานกัน” |
| **Reallocation** | ย้ายทรัพยากรจากกิจกรรมที่มี Slack > 0 ไปยัง Critical Path |

---

## 🧠 8. Critical Chain Scheduling
- อิงแนวคิด **Theory of Constraints (TOC)** – จุดอ่อนคือสิ่งที่จำกัดประสิทธิภาพระบบ  
- พิจารณาทรัพยากรจำกัดและลด Multitasking  
- ใช้ **Buffer (ตัวกันเวลา)** เพื่อป้องกันความล่าช้า  
  | ประเภท | บทบาท |
  |----------|--------|
  | **Project Buffer** | ปลาย Critical Chain ป้องกันกำหนดส่ง |
  | **Feeding Buffer** | ระหว่าง Non-critical Chain กับ Critical Chain |
  | **Resource Buffer** | สำรองคนหรือเครื่องมือที่จำเป็น |
- แก้ปัญหา “Parkinson’s Law” และ “Student Syndrome”:contentReference[oaicite:9]{index=9}

---

## 📉 9. การควบคุมตารางเวลา (Controlling the Schedule)
- ตรวจสอบสถานะตารางและจัดการเมื่อมีการเปลี่ยนแปลง  
- เครื่องมือที่ใช้:  
  - **Earned Value Analysis (EVA)**  
  - **Burndown Chart (ใน Agile)**  
  - **Resource Leveling**  
  - **Schedule Compression (Crashing / Fast Tracking)**:contentReference[oaicite:10]{index=10}

---

## 📊 10. การจัดการใน Agile / Adaptive Environment
- ไม่จำเป็นต้องกำหนดระยะเวลากิจกรรมล่วงหน้า  
- ใช้ **Iteration / Sprint Planning**  
- ลูกค้า (Product Owner) จะกำหนด “งานที่ต้องการ” ในแต่ละรอบ  
- ใช้ **Story Points** เพื่อประมาณความพยายาม  
- มุ่งเน้น **การส่งมอบที่ใช้งานได้จริงทุก Iteration**:contentReference[oaicite:11]{index=11}

---

## 📚 สรุปท้ายบท
- การจัดการเวลาเป็นหนึ่งในปัจจัยความสำเร็จหลักของโครงการ  
- มีกระบวนการ 6 ขั้นตอน ตั้งแต่การวางแผนจนถึงควบคุม  
- เครื่องมือสำคัญ: Gantt Chart, Network Diagram, CPM, PERT  
- ใช้ Critical Chain เพื่อลดความล่าช้าและเพิ่มประสิทธิภาพ  
- Agile มุ่งเน้นการส่งมอบเป็นรอบ ๆ มากกว่าการคาดคะเนระยะยาว  

---

## 🧾 แนวข้อสอบแบบกากบาท (Multiple Choice)

1. เส้นทางวิกฤติ (Critical Path) หมายถึงอะไร  
   - A) เส้นทางที่ใช้เวลาสั้นที่สุด  
   - ✅ B) เส้นทางที่ยาวที่สุดและมี Float = 0  
   - C) เส้นทางที่ขึ้นอยู่กับ Resource  
   - D) เส้นทางที่เปลี่ยนแปลงได้ตามต้องการ  

2. ความแตกต่างระหว่าง Duration และ Effort คืออะไร  
   - A) Duration = ชั่วโมงทำงานทั้งหมด  
   - ✅ B) Effort คือจำนวนชั่วโมงงานจริง ส่วน Duration คือเวลาที่ใช้รวมทั้งหมด  
   - C) Duration หมายถึงเวลาพัก  
   - D) ไม่มีความแตกต่าง  

3. Lead หมายถึง  
   - ✅ A) งานต่อไปเริ่มก่อนงานก่อนหน้าจบ  
   - B) งานต่อไปต้องรอก่อนเริ่ม  
   - C) งานเสร็จช้ากว่ากำหนด  
   - D) งานถูกเลื่อนเพราะ Resource  

4. Schedule Compression แบบใดที่ “เพิ่มทรัพยากร” เพื่อเร่งเวลา  
   - A) Fast Tracking  
   - ✅ B) Crashing  
   - C) Leveling  
   - D) Floating  

5. Critical Chain ต่างจาก Critical Path อย่างไร  
   - ✅ A) พิจารณาทรัพยากรและใช้ Buffer เพื่อรองรับความล่าช้า  
   - B) ใช้เฉพาะใน Agile Project  
   - C) ไม่สนใจ Resource Constraints  
   - D) ใช้คำนวณ Float เท่านั้น  

6. PERT ใช้สำหรับกรณีใด  
   - ✅ A) เมื่อมีความไม่แน่นอนสูงเกี่ยวกับระยะเวลา  
   - B) เมื่อโครงการสั้นและ Simple  
   - C) เมื่อ Resource มีเพียงพอ  
   - D) ใช้เฉพาะใน Agile  

7. Tracking Gantt Chart ใช้เพื่ออะไร  
   - ✅ A) เปรียบเทียบ Planned vs Actual Schedule  
   - B) แสดงงบประมาณที่ใช้  
   - C) แสดง Risk Register  
   - D) บันทึกคุณภาพงาน  

8. Slack = 0 หมายถึง  
   - ✅ A) งานอยู่ใน Critical Path  
   - B) งานไม่สำคัญ  
   - C) งานเสร็จเร็ว  
   - D) งานรออนุมัติ  

9. Buffer ประเภทใดอยู่ท้าย Critical Chain  
   - A) Feeding Buffer  
   - ✅ B) Project Buffer  
   - C) Resource Buffer  
   - D) Slack Buffer  

10. Agile Project จัดการเวลาอย่างไร  
    - A) ใช้ PERT คำนวณเวลาทุกกิจกรรม  
    - ✅ B) กำหนดงานเป็น Iteration และส่งมอบเป็นรอบ  
    - C) ใช้ Gantt Chart อย่างละเอียด  
    - D) ไม่มีการวางแผนเวลาเลย  

---

📖 **คำแนะนำก่อนสอบ**
- จำ 6 กระบวนการหลักของ Schedule Management  
- เข้าใจความแตกต่างของ CPM, PERT, และ Critical Chain  
- ฝึกวาด Gantt Chart และคำนวณ Float  
- เข้าใจคำศัพท์สำคัญ (ES, EF, LS, LF, TS, FS)  
- รู้วิธีย่นเวลา (Crashing vs Fast Tracking)  
- เข้าใจแนวคิด Buffer และการจัดการเวลาใน Agile  
