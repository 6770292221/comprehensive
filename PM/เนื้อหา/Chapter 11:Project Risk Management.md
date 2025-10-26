# 📘 บทที่ 11: การจัดการความเสี่ยงของโครงการ (Project Risk Management)
จาก *Information Technology Project Management, Ninth Edition*:contentReference[oaicite:0]{index=0}

---

## 🎯 วัตถุประสงค์ของบทเรียน (Learning Objectives)
1. อธิบายแนวคิดของ “ความเสี่ยง” (Risk) ในบริบทของการบริหารโครงการ  
2. เข้าใจขั้นตอนและองค์ประกอบของการจัดการความเสี่ยง  
3. ระบุและสร้าง **Risk Register** และ **Risk Report**  
4. วิเคราะห์ความเสี่ยงเชิงคุณภาพและเชิงปริมาณ  
5. อธิบายกลยุทธ์การตอบสนองความเสี่ยงทั้งเชิงบวกและเชิงลบ  
6. อธิบายการติดตามความเสี่ยงและการใช้ซอฟต์แวร์ช่วยบริหารความเสี่ยง  
7. เข้าใจแนวทางการจัดการความเสี่ยงในสภาพแวดล้อมแบบ Agile / Adaptive  

---

## 💡 1. ความสำคัญของการบริหารความเสี่ยง (Importance of Risk Management)
- การจัดการความเสี่ยงเป็นทั้ง **ศาสตร์และศิลป์** ของการระบุ วิเคราะห์ และตอบสนองต่อความไม่แน่นอนในโครงการ  
- ช่วยให้:
  - เลือกโครงการที่เหมาะสม
  - กำหนดขอบเขตที่เป็นจริง
  - พัฒนาแผนประมาณการที่แม่นยำขึ้น  
- องค์กรที่บริหารความเสี่ยงได้ดีมักมี “ความสำเร็จของโครงการ” สูงกว่า:contentReference[oaicite:1]{index=1}

---

## ⚙️ 2. ความหมายของ “Risk” และประเภทของความเสี่ยง
- **Risk (ความเสี่ยง):** ความไม่แน่นอนที่ส่งผล **เชิงบวกหรือเชิงลบ** ต่อวัตถุประสงค์ของโครงการ  
- **Negative Risk (Threat):** ความเสี่ยงที่อาจก่อให้เกิดผลเสีย เช่น ล่าช้า งบเกิน  
- **Positive Risk (Opportunity):** ความเสี่ยงที่นำไปสู่ผลลัพธ์ดี เช่น ทำงานได้เร็วหรือประหยัดกว่า:contentReference[oaicite:2]{index=2}

---

## 🧭 3. ระดับความพึงพอใจต่อความเสี่ยง (Risk Utility)
| ประเภท | ลักษณะ | ตัวอย่างพฤติกรรม |
|----------|-----------|----------------|
| **Risk-Averse** | ไม่ชอบความเสี่ยง | ลงทุนในสิ่งที่แน่นอน |
| **Risk-Seeking** | ชอบความเสี่ยง | ยอมเสี่ยงเพื่อผลตอบแทนสูง |
| **Risk-Neutral** | สมดุล | วิเคราะห์ผลตอบแทนต่อความเสี่ยงก่อนตัดสินใจ:contentReference[oaicite:3]{index=3}

---

## 🧩 4. กระบวนการบริหารความเสี่ยงของโครงการ (Project Risk Management Processes)
| ขั้นตอน | รายละเอียด |
|----------|-------------|
| 1️⃣ Planning Risk Management | วางแผนวิธีจัดการความเสี่ยง |
| 2️⃣ Identifying Risks | ระบุความเสี่ยงที่อาจเกิดขึ้น |
| 3️⃣ Performing Qualitative Risk Analysis | วิเคราะห์โอกาสเกิดและผลกระทบ |
| 4️⃣ Performing Quantitative Risk Analysis | ประเมินค่าความเสี่ยงเชิงตัวเลข |
| 5️⃣ Planning Risk Responses | วางแผนการตอบสนองความเสี่ยง |
| 6️⃣ Implementing Risk Responses | ลงมือดำเนินการตามแผน |
| 7️⃣ Monitoring Risks | ติดตามและปรับปรุงการบริหารความเสี่ยง:contentReference[oaicite:4]{index=4}

---

## 📝 5. การวางแผนการจัดการความเสี่ยง (Planning Risk Management)
**Output หลัก:** Risk Management Plan  
**เนื้อหาสำคัญที่ต้องระบุในแผน**:contentReference[oaicite:5]{index=5}  
- วิธีการจัดการความเสี่ยง (Methodology)  
- บทบาทและความรับผิดชอบของทีม  
- งบประมาณและระยะเวลาในการบริหารความเสี่ยง  
- หมวดหมู่ความเสี่ยง (Risk Categories)  
- วิธีประเมินความน่าจะเป็นและผลกระทบ  
- การติดตามและรายงานผลความเสี่ยง  

---

## 🧠 6. การระบุความเสี่ยง (Identifying Risks)
- ต้องทำตั้งแต่เริ่มต้นและทำอย่างต่อเนื่อง  
- ใช้ข้อมูลจาก **WBS, Lessons Learned, Expert Judgment**  
- **Output:**  
  - 🧾 *Risk Register*  
  - 📊 *Risk Report*:contentReference[oaicite:6]{index=6}

### ตัวอย่างแหล่งความเสี่ยงในโครงการ IT
| ประเภท | ตัวอย่าง |
|----------|-----------|
| Market | สินค้าไม่เป็นที่ต้องการของตลาด |
| Financial | ROI ต่ำกว่าเป้า |
| Technology | ใช้เทคโนโลยีใหม่ที่ยังไม่เสถียร |
| People | ขาดบุคลากรที่มีทักษะ |
| Process | ขั้นตอนซับซ้อนหรือเปลี่ยนแปลงบ่อย:contentReference[oaicite:7]{index=7}

---

## 🧰 7. เครื่องมือในการระบุความเสี่ยง (Tools and Techniques)
| วิธี | รายละเอียด |
|------|--------------|
| **Brainstorming** | ระดมสมองภายในทีม แต่ควรมีผู้ดำเนินที่มีประสบการณ์ |
| **Delphi Technique** | ให้ผู้เชี่ยวชาญตอบแบบสอบถามหลายรอบจนได้ข้อสรุปที่เห็นพ้องร่วมกัน |
| **Interviewing** | สัมภาษณ์ผู้มีประสบการณ์ในโครงการคล้ายกัน |
| **SWOT Analysis** | วิเคราะห์จุดแข็ง จุดอ่อน โอกาส และภัยคุกคาม:contentReference[oaicite:8]{index=8}

---

## 📋 8. Risk Register
**เอกสารสำคัญที่สุดในกระบวนการบริหารความเสี่ยง**  
ประกอบด้วย:  
- รหัสความเสี่ยง (Risk ID)  
- ชื่อและคำอธิบายของความเสี่ยง  
- หมวดหมู่ (Category)  
- สาเหตุและสัญญาณเตือน (Root Cause, Trigger)  
- วิธีตอบสนอง (Response Plan)  
- เจ้าของความเสี่ยง (Risk Owner)  
- ความน่าจะเป็น / ผลกระทบ / สถานะ:contentReference[oaicite:9]{index=9}

---

## 🧾 9. Risk Report
- ใช้สำหรับสื่อสารกับผู้บริหารระดับสูง  
- สรุปภาพรวม เช่น:
  - จำนวนความเสี่ยงทั้งหมด  
  - ระดับ Exposure  
  - การกระจายตามประเภทความเสี่ยง  
  - แนวโน้มและตัวชี้วัด (Trend & Metrics):contentReference[oaicite:10]{index=10}

---

## 🎛️ 10. การวิเคราะห์ความเสี่ยงเชิงคุณภาพ (Qualitative Risk Analysis)
- ประเมิน “ความน่าจะเป็น” และ “ผลกระทบ” เพื่อจัดลำดับความสำคัญ  
- เครื่องมือหลัก:
  - **Probability/Impact Matrix**
  - **Risk Factor Analysis**
  - **Top Ten Risk Tracking**:contentReference[oaicite:11]{index=11}

### 📊 Probability/Impact Matrix
- แบ่งระดับ **High / Medium / Low**  
- ใช้คำนวณ **Risk Index = Probability × Impact**

### 📈 Top Ten Risk Tracking
- จัดอันดับความเสี่ยง 10 อันดับแรก  
- ตรวจสอบความคืบหน้าและแนวโน้มในแต่ละเดือน  

---

## 🧮 11. การวิเคราะห์เชิงปริมาณ (Quantitative Risk Analysis)
ใช้ตัวเลขเพื่อประเมินความเสี่ยง  
เทคนิคหลัก:​:contentReference[oaicite:12]{index=12}
| เทคนิค | คำอธิบาย |
|----------|-----------|
| **Decision Tree + EMV** | คำนวณ *Expected Monetary Value* จากโอกาส × ผลกระทบทางการเงิน |
| **Simulation (Monte Carlo)** | จำลองผลลัพธ์ซ้ำหลายครั้งเพื่อดูการกระจายของความน่าจะเป็น |
| **Sensitivity Analysis** | วิเคราะห์ผลกระทบเมื่อเปลี่ยนค่าตัวแปรหนึ่งๆ |

---

## 🧱 12. การวางแผนตอบสนองความเสี่ยง (Planning Risk Responses)
### 🔹 สำหรับความเสี่ยงเชิงลบ (Threats)
| กลยุทธ์ | คำอธิบาย |
|-----------|------------|
| **Avoidance** | หลีกเลี่ยงต้นเหตุของความเสี่ยง |
| **Acceptance** | ยอมรับผลกระทบ |
| **Transference** | โอนความเสี่ยงให้บุคคลภายนอก เช่น ประกันภัย |
| **Mitigation** | ลดโอกาสหรือผลกระทบ |
| **Escalation** | แจ้งผู้บริหารระดับสูงเมื่ออยู่นอกขอบเขตอำนาจ:contentReference[oaicite:13]{index=13}

### 🔹 สำหรับความเสี่ยงเชิงบวก (Opportunities)
| กลยุทธ์ | คำอธิบาย |
|-----------|------------|
| **Exploitation** | ทำให้โอกาสเกิดขึ้นแน่นอน |
| **Sharing** | แบ่งปันผลประโยชน์ร่วมกับพันธมิตร |
| **Enhancement** | เพิ่มขนาดของโอกาส |
| **Acceptance** | ไม่ทำอะไรเพิ่มเติม |
| **Escalation** | แจ้งผู้บริหารเมื่อมีศักยภาพสูง:contentReference[oaicite:14]{index=14}

---

## ⚠️ 13. ประเภทของแผนสำรอง (Contingency Planning)
| ประเภท | คำอธิบาย |
|----------|-----------|
| **Contingency Plan** | แผนสำรองเมื่อความเสี่ยงเกิดขึ้น |
| **Fallback Plan** | ใช้เมื่อแผน Contingency ล้มเหลว |
| **Contingency Reserve** | งบประมาณสำรองสำหรับความเสี่ยงที่ระบุแล้ว |
| **Management Reserve** | งบสำรองสำหรับความเสี่ยงที่ไม่สามารถคาดการณ์ได้:contentReference[oaicite:15]{index=15}

---

## 🔄 14. การดำเนินการและติดตามความเสี่ยง
- ดำเนินการตาม Risk Response Plan  
- ตรวจสอบสถานะของแต่ละความเสี่ยง  
- ประเมินผลของแผนที่ใช้  
- ใช้ **Workaround** เมื่อไม่มีแผนสำรอง  
- อัปเดต Risk Register อย่างต่อเนื่อง:contentReference[oaicite:16]{index=16}

---

## 💻 15. ซอฟต์แวร์ที่ใช้ในการบริหารความเสี่ยง
- **Excel, Word:** ใช้สร้าง Risk Register  
- **Monte Carlo Tools:** จำลองสถานการณ์  
- **Project Management Software:** เช่น Primavera, MS Project, Jira:contentReference[oaicite:17]{index=17}

---

## 🌀 16. ความเสี่ยงในสภาพแวดล้อม Agile
- วิเคราะห์และจัดการความเสี่ยงในแต่ละ Iteration  
- ใช้ทีมข้ามสายงานและ Review บ่อยๆ เพื่อระบุความเสี่ยงใหม่  
- ปรับ Backlog ให้สอดคล้องกับระดับความเสี่ยง:contentReference[oaicite:18]{index=18}

---

## 📚 สรุปท้ายบท
- ความเสี่ยงคือ “ความไม่แน่นอนที่อาจส่งผลบวกหรือลบต่อโครงการ”  
- การบริหารความเสี่ยงเป็นการลงทุนที่ช่วยเพิ่มอัตราความสำเร็จ  
- ต้องดำเนินการต่อเนื่อง:  
  → **Plan → Identify → Analyze → Respond → Monitor**:contentReference[oaicite:19]{index=19}

---

## 🧾 แนวข้อสอบแบบกากบาท (Multiple Choice)

1. ขั้นตอนใดไม่อยู่ในกระบวนการบริหารความเสี่ยงของโครงการ  
   - A) Identifying Risks  
   - B) Performing Quantitative Risk Analysis  
   - ✅ C) Managing Quality  
   - D) Planning Risk Responses  

2. เอกสารใดใช้บันทึกรายละเอียดความเสี่ยงทั้งหมด  
   - A) Risk Report  
   - ✅ B) Risk Register  
   - C) Issue Log  
   - D) Risk Matrix  

3. ข้อใดเป็นความเสี่ยงเชิงบวก (Opportunity)  
   - A) งบประมาณเกิน  
   - B) ล่าช้า  
   - ✅ C) ทำงานเสร็จก่อนเวลา  
   - D) ระบบล่ม  

4. เครื่องมือใดใช้ในการระบุความเสี่ยงจากผู้เชี่ยวชาญหลายคน  
   - ✅ A) Delphi Technique  
   - B) Brainstorming  
   - C) SWOT  
   - D) Simulation  

5. “Risk Index” คำนวณจากสูตรใด  
   - ✅ A) Probability × Impact  
   - B) Probability + Impact  
   - C) Risk ÷ Exposure  
   - D) Cost × Time  

6. ข้อใดเป็นกลยุทธ์ตอบสนองความเสี่ยงเชิงลบ  
   - ✅ A) Mitigation  
   - B) Exploitation  
   - C) Enhancement  
   - D) Sharing  

7. “Contingency Plan” หมายถึง  
   - ✅ A) แผนสำรองเมื่อความเสี่ยงเกิดขึ้น  
   - B) แผนที่ใช้เมื่อโครงการจบ  
   - C) แผนสำหรับโอกาสทางธุรกิจ  
   - D) งบประมาณรายปี  

8. การวิเคราะห์แบบใดใช้จำลองสถานการณ์หลายครั้ง  
   - A) Decision Tree  
   - ✅ B) Monte Carlo Simulation  
   - C) Sensitivity Analysis  
   - D) Factor Analysis  

9. ใน Agile ความเสี่ยงถูกจัดการอย่างไร  
   - ✅ A) ตรวจสอบในแต่ละ Iteration  
   - B) วิเคราะห์เฉพาะต้นโครงการ  
   - C) ใช้เฉพาะ Scrum Master  
   - D) ไม่เน้นความเสี่ยง  

10. เอกสารใดสรุปภาพรวมของความเสี่ยงระดับองค์กร  
    - A) Risk Register  
    - ✅ B) Risk Report  
    - C) Workaround Log  
    - D) Change Request  

---

📖 **คำแนะนำก่อนสอบ**
- จำ 7 กระบวนการของ Risk Management ให้ครบ  
- เข้าใจความต่างระหว่าง Risk Register กับ Risk Report  
- ทบทวนสูตร **Risk Index = Probability × Impact**  
- รู้จักประเภทแผนสำรอง (Contingency, Fallback, Reserve)  
- จำเทคนิคหลัก: Brainstorming, Delphi, Monte Carlo, Sensitivity, Decision Tree  
