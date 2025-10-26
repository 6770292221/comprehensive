# 📘 บทที่ 7: การจัดการต้นทุนโครงการ (Project Cost Management)
จาก *Information Technology Project Management, Ninth Edition*:contentReference[oaicite:0]{index=0}

---

## 🎯 วัตถุประสงค์ของบทเรียน
1. เข้าใจเหตุผลและความสำคัญของการจัดการต้นทุนในโครงการ  
2. อธิบายแนวคิดพื้นฐานและคำศัพท์ของการจัดการต้นทุน  
3. อธิบายกระบวนการ 4 ขั้นตอนของการจัดการต้นทุน  
4. รู้จักประเภทของการประมาณค่าใช้จ่ายและเทคนิคการคำนวณ  
5. เข้าใจการประยุกต์ใช้ **Earned Value Management (EVM)**  
6. วิเคราะห์ตัวอย่างการใช้ **COCOMO II** และ **Function Point Analysis (FPA)**  
7. เข้าใจแนวคิดการจัดการต้นทุนในสภาพแวดล้อมแบบ Agile  

---

## 🧩 1. ความสำคัญของการจัดการต้นทุน (Importance of Cost Management)
- โครงการ IT ส่วนใหญ่ **เกินงบประมาณ (Cost Overrun)** เพราะขาดการคาดการณ์ที่แม่นยำ  
- “ต้นทุน” คือทรัพยากรที่ถูกใช้เพื่อให้ได้มาซึ่งวัตถุประสงค์  
- “ผลประโยชน์ (Benefit)” คือมูลค่าที่ได้รับจากสิ่งนั้น เช่น รายได้, การเพิ่มประสิทธิภาพ  
- หากไม่จัดการอย่างเหมาะสม → อาจเกิดความเสียหายต่อทั้งงบและเป้าหมายขององค์กร  

---

## ⚙️ 2. หลักพื้นฐานของการจัดการต้นทุน
| ประเภท | คำอธิบาย | ตัวอย่าง |
|----------|------------|-----------|
| **Tangible Costs/Benefits** | วัดเป็นตัวเงินได้ | เงินเดือน, ค่าซอฟต์แวร์ |
| **Intangible Costs/Benefits** | วัดค่าได้ยาก | ชื่อเสียง, ความพึงพอใจ |
| **Direct Cost** | ต้นทุนที่เกี่ยวข้องโดยตรงกับโครงการ | ค่าแรง, ฮาร์ดแวร์ |
| **Indirect Cost** | ต้นทุนที่เกี่ยวข้องทางอ้อม | ค่าน้ำ ค่าไฟ |
| **Sunk Cost** | ต้นทุนที่จ่ายไปแล้วและไม่ควรนำมาพิจารณาต่อ | งบที่จ่ายไปในโครงการที่ยกเลิก |

**Reserves:**  
- **Contingency Reserve:** ความเสี่ยงที่รู้ว่าอาจเกิด (Known Unknowns)  
- **Management Reserve:** ความเสี่ยงที่คาดไม่ถึง (Unknown Unknowns)  

---

## 🧭 3. กระบวนการจัดการต้นทุน (Cost Management Processes)
| ลำดับ | กระบวนการ | จุดประสงค์ |
|--------|-------------|-------------|
| 1️⃣ | **Planning Cost Management** | วางแผนวิธีการจัดการต้นทุน |
| 2️⃣ | **Estimating Costs** | ประมาณค่าใช้จ่ายของทรัพยากรทั้งหมด |
| 3️⃣ | **Determining Budget** | สร้างงบประมาณและ Cost Baseline |
| 4️⃣ | **Controlling Costs** | ตรวจสอบและควบคุมงบประมาณ |

---

## 🧾 4. การวางแผนการจัดการต้นทุน (Planning Cost Management)
แผนต้นทุนควรรวมถึง:
- **ระดับความแม่นยำ (Level of Accuracy):** เช่น ปัดเศษ ±$100  
- **หน่วยวัด (Units of Measure):** ชั่วโมง / วัน / บาท  
- **Thresholds:** กำหนดขอบเขตการเบี่ยงเบน เช่น ±10%  
- **Reporting Format:** รูปแบบและความถี่ของรายงาน  
- **Performance Rules:** กำหนดว่าตรวจสอบค่าใช้จ่ายบ่อยแค่ไหน  

---

## 💰 5. การประมาณต้นทุน (Cost Estimation)
### 🔹 ประเภทของการประมาณต้นทุน
| ประเภท | ระยะเวลา | ความแม่นยำ |
|----------|------------|-------------|
| **Rough Order of Magnitude (ROM)** | ช่วงต้นโครงการ | -50% ถึง +100% |
| **Budgetary Estimate** | ช่วงวางแผน | -10% ถึง +25% |
| **Definitive Estimate** | ก่อนเริ่มงานจริง | -5% ถึง +10% |

### 🔹 เทคนิคการประมาณต้นทุน
| วิธี | รายละเอียด |
|------|-------------|
| **Analogous (Top-Down)** | ใช้ข้อมูลจากโครงการคล้ายกันในอดีต |
| **Bottom-Up** | รวมค่าประมาณของงานย่อยทั้งหมด |
| **Three-Point (PERT)** | ใช้ค่า Optimistic, Most Likely, Pessimistic |
| **Parametric Estimating** | ใช้สมการทางสถิติ เช่น Function Points, COCOMO |

---

## ⚠️ 6. ปัญหาที่พบบ่อยในการประมาณต้นทุน IT
- เร่งทำประมาณการก่อนเข้าใจ Requirement ชัดเจน  
- ขาดข้อมูลอ้างอิงหรือประสบการณ์  
- ผู้บริหารมัก “อยากได้ตัวเลขที่ต่ำกว่า”  
- มนุษย์มัก **ประเมินต่ำเกินจริง (Underestimate Bias)**:contentReference[oaicite:1]{index=1}

---

## 🧮 7. ตัวอย่างการคำนวณต้นทุนซอฟต์แวร์

### 🔸 การใช้ Lines of Code (LOC)
> สมมติซอฟต์แวร์มี 33,200 LOC, ผลิตภาพ 620 LOC/person-month, ค่าแรง $8,000/เดือน

\[
Cost = \frac{33,200}{620} \times 8000 = \$431,000
\]

---

### 🔸 การใช้ Story Points (Agile)
> งานรวม 200 SP, Velocity = 50 SP/Sprint, ทีม 5 คน, 2 สัปดาห์ต่อ Sprint

\[
Cost = 5 \text{ คน} × 8,000 × 2 \text{ เดือน} = \$80,000
\]

---

### 🔸 Function Point Analysis (FPA)
- วัดขนาดระบบโดยดูจาก 5 องค์ประกอบ:  
  - **EI (External Input)**  
  - **EO (External Output)**  
  - **EQ (External Inquiry)**  
  - **ILF (Internal Logical File)**  
  - **EIF (External Interface File)**  
- ใช้ค่า DET, RET, FTR เพื่อคำนวณ FP และแปลงเป็น LOC ด้วย **Backfiring**

---

### 🔸 COCOMO II (Constructive Cost Model)
\[
PM = A × Size^E × \prod EM_i
\]

โดย:  
- **A** = Effort Coefficient  
- **E** = Scale Factor  
- **EM** = Effort Multipliers (17 ตัว เช่น RELY, CPLX, PCAP, SCED)  
- ใช้ในการคำนวณแรงงาน (Person-Month), เวลา (TDEV), และต้นทุนรวม  

---

## 📊 8. การกำหนดงบประมาณ (Determining the Budget)
- รวมผลการประมาณทั้งหมดเป็น **Cost Baseline**  
- เพิ่ม **Management Reserve** → ได้ “Project Budget”  
- ใช้แนวคิด **Time-Phased Budget** เพื่อควบคุมรายเดือน  

---

## 📉 9. การควบคุมต้นทุน (Controlling Costs)
- ตรวจสอบค่าใช้จ่ายจริงเทียบกับแผน  
- ปรับงบประมาณเมื่อเกิดการเปลี่ยนแปลง  
- ใช้ **Earned Value Management (EVM)** เป็นเครื่องมือวัดผล  

### 🔹 ตัวอย่างคำนวณ
| ตัวแปร | คำอธิบาย | ค่า |
|---------|------------|------|
| **BAC** | งบทั้งหมด | $10,000 |
| **PV** | แผนไว้ (50%) | $5,000 |
| **EV** | งานสำเร็จจริง (40%) | $4,000 |
| **AC** | ค่าใช้จ่ายจริง | $6,000 |

\[
\begin{align*}
CV &= EV - AC = -2000 \\
SV &= EV - PV = -1000 \\
CPI &= EV / AC = 0.67 \\
SPI &= EV / PV = 0.8
\end{align*}
\]

→ เกินงบ 33% และล่าช้า 20%:contentReference[oaicite:2]{index=2}

---

### 🔹 ตัวชี้วัดสำคัญใน EVM
| ชื่อ | สูตร | ความหมาย |
|------|------|------------|
| **CPI (Cost Performance Index)** | EV / AC | ประสิทธิภาพด้านต้นทุน |
| **SPI (Schedule Performance Index)** | EV / PV | ประสิทธิภาพด้านเวลา |
| **EAC (Estimate at Completion)** | BAC / CPI | คาดการณ์งบสิ้นสุด |
| **ETC (Estimate to Complete)** | EAC - AC | งบที่ต้องใช้ต่อจากนี้ |
| **TCPI (To-Complete Performance Index)** | (BAC - EV)/(BAC - AC) | ต้องรักษาความคุ้มค่าที่เหลือในอนาคต |

---

## 💻 10. การใช้ซอฟต์แวร์ช่วยในการบริหารต้นทุน
- **Excel/Google Sheets:** คำนวณและติดตามงบเบื้องต้น  
- **MS Project / Primavera:** สร้าง Baseline และรายงาน EVM  
- **ERP / Jira / Power BI:** วิเคราะห์การใช้งบแบบ Portfolio  

---

## 🌀 11. ต้นทุนใน Agile / Adaptive Environment
- ใช้แนวคิด **AgileEVM** เพื่อคำนวณต้นทุนใน Sprint  
- ใช้ Story Points แทนชั่วโมง  
- วัด Velocity และ Burn Rate เพื่อประเมินงบที่เหลือ  
- การคาดการณ์งบประมาณทำต่อเนื่องทุก Iteration:contentReference[oaicite:3]{index=3}

---

## 📚 สรุปท้ายบท
- การจัดการต้นทุนคือหัวใจของการบริหารโครงการ IT ให้สำเร็จ  
- ต้องเข้าใจทั้งหลักการประมาณ (ROM, Budgetary, Definitive) และการควบคุม (EVM)  
- เครื่องมือช่วย เช่น COCOMO, FPA, Story Point → ใช้สร้างงบประมาณที่แม่นยำขึ้น  
- การติดตาม EVM และ CPI/SPI เป็นตัวชี้วัดความสำเร็จเชิงต้นทุน  

---

## 🧾 แนวข้อสอบแบบกากบาท (Multiple Choice)

1. ข้อใดไม่ใช่กระบวนการของ Project Cost Management  
   - A) Estimating Costs  
   - B) Determining Budget  
   - ✅ C) Planning Schedule Management  
   - D) Controlling Costs  

2. Contingency Reserve ใช้เพื่อ  
   - ✅ A) รองรับความเสี่ยงที่ทราบ (Known Unknowns)  
   - B) รองรับเหตุการณ์ที่ไม่อาจคาดการณ์  
   - C) ปรับปรุงคุณภาพระบบ  
   - D) สำรองงบเผื่อเงินเดือนเพิ่ม  

3. วิธีการประมาณต้นทุนที่อาศัยโครงการเดิมคือ  
   - ✅ A) Analogous Estimating  
   - B) Bottom-up  
   - C) PERT  
   - D) Parametric  

4. หาก CPI < 1 หมายถึงอะไร  
   - ✅ A) ใช้งบเกินจากแผน  
   - B) ใช้งบน้อยกว่าแผน  
   - C) ตรงตามงบประมาณ  
   - D) ไม่มีการใช้จ่าย  

5. เครื่องมือใดใช้ในการวัดประสิทธิภาพด้านเวลาและงบ  
   - ✅ A) Earned Value Management (EVM)  
   - B) Gantt Chart  
   - C) WBS  
   - D) SWOT  

6. การคำนวณ EAC = BAC/CPI หมายถึง  
   - ✅ A) ประมาณงบประมาณใหม่เมื่อทราบประสิทธิภาพจริง  
   - B) ต้นทุนเริ่มต้นของโครงการ  
   - C) งบประมาณที่อนุมัติครั้งแรก  
   - D) ค่าความเบี่ยงเบนของต้นทุน  

7. ใน Agile การคำนวณงบประมาณมักใช้หน่วยใด  
   - A) ชั่วโมงทำงาน (Hours)  
   - ✅ B) Story Points  
   - C) LOC  
   - D) Function Points  

8. FPA ใช้วัดอะไร  
   - ✅ A) ขนาดเชิงตรรกะของซอฟต์แวร์ (Functional Size)  
   - B) ขนาดเชิงกายภาพของโค้ด  
   - C) ความซับซ้อนของอัลกอริทึม  
   - D) จำนวนทีมที่เกี่ยวข้อง  

9. หาก TCPI > 1 หมายถึง  
   - ✅ A) ต้องทำงานให้มีประสิทธิภาพกว่าปัจจุบันเพื่อให้งบเพียงพอ  
   - B) ใช้งบน้อยเกินไป  
   - C) โครงการอยู่ในงบ  
   - D) โครงการเสร็จเร็วเกินแผน  

10. เครื่องมือใดใช้ประเมินต้นทุนซอฟต์แวร์จาก Function Points  
    - A) PERT  
    - ✅ B) COCOMO II  
    - C) EVA  
    - D) Burndown Chart  

---

📖 **คำแนะนำก่อนสอบ**
- จำกระบวนการ 4 ขั้นของ Cost Management  
- เข้าใจสูตร EVM (CV, SV, CPI, SPI, EAC, TCPI)  
- ทบทวนเทคนิคการประมาณ (Analogous, Bottom-up, Parametric)  
- รู้ว่า FPA และ COCOMO ใช้คำนวณต้นทุนซอฟต์แวร์  
- ฝึกอ่านกราฟ EVM และการตีความ CPI/SPI  
