# 📘 Chapter 11: Project Risk Management

> แหล่งที่มา: *Information Technology Project Management (9th Edition)*  
> โดย Kathy Schwalbe / Twittie Senivongse (ed.)  
> “Risk is uncertainty that can have a negative **or positive** effect on project objectives.”:contentReference[oaicite:1]{index=1}

---

## 🎯 Learning Objectives

1. เข้าใจความหมายและความสำคัญของ Project Risk Management  
2. อธิบาย 7 กระบวนการบริหารความเสี่ยง  
3. รู้จักเครื่องมือสำคัญ เช่น Risk Register, Probability/Impact Matrix  
4. อธิบายการวิเคราะห์ความเสี่ยงเชิงคุณภาพและเชิงปริมาณ  
5. เข้าใจแนวทางการตอบสนองความเสี่ยง (Response Strategies)  
6. วิเคราะห์กรณี Contingency Plan, Fallback Plan และ Risk Reserves  
7. ระบุแนวทางบริหารความเสี่ยงใน Agile Project:contentReference[oaicite:2]{index=2}

---

## 🧩 ความหมายของ “Risk”

- **Risk = ความไม่แน่นอน (Uncertainty)** ที่อาจมีผล **บวกหรือผลลบ** ต่อวัตถุประสงค์ของโครงการ  
- **Negative Risk (Threat)** → เช่น งานล่าช้า, เกินงบ, ระบบล่ม  
- **Positive Risk (Opportunity)** → เช่น ทำงานเสร็จเร็ว, ลดต้นทุน, ได้ผลลัพธ์ดีกว่าคาด:contentReference[oaicite:3]{index=3}

### 🔹 Risk Utility

| ประเภท | ลักษณะ |
|----------|----------|
| **Risk-averse** | ไม่ชอบความเสี่ยง → พอใจในผลตอบแทนต่ำแต่แน่นอน |
| **Risk-neutral** | วิเคราะห์ตามเหตุผล → พิจารณาความคุ้มค่า |
| **Risk-seeking** | ยอมรับความเสี่ยงสูงเพื่อผลตอบแทนมากกว่า:contentReference[oaicite:4]{index=4} |

---

## ⚙️ 7 กระบวนการของ Project Risk Management

| ลำดับ | Process | คำอธิบาย |
|--------|----------|-----------|
| 1️⃣ | Plan Risk Management | วางแผนและกำหนดแนวทางจัดการความเสี่ยง |
| 2️⃣ | Identify Risks | ระบุความเสี่ยงที่อาจเกิดขึ้น |
| 3️⃣ | Perform Qualitative Risk Analysis | ประเมินความน่าจะเป็นและผลกระทบ |
| 4️⃣ | Perform Quantitative Risk Analysis | ประเมินผลเชิงตัวเลข เช่น EMV, Monte Carlo |
| 5️⃣ | Plan Risk Responses | วางแผนตอบสนองต่อความเสี่ยง |
| 6️⃣ | Implement Risk Responses | ดำเนินการตามแผนที่กำหนด |
| 7️⃣ | Monitor Risks | ตรวจสอบและติดตามผลการจัดการความเสี่ยง:contentReference[oaicite:5]{index=5}

---

## 1️⃣ Plan Risk Management

เอกสารผลลัพธ์หลักคือ **Risk Management Plan**  
ประกอบด้วย:  
- วิธีและเครื่องมือที่ใช้จัดการความเสี่ยง  
- บทบาทและความรับผิดชอบ  
- งบประมาณและตารางเวลาของกิจกรรมด้านความเสี่ยง  
- การประเมินโอกาสและผลกระทบ (Probability/Impact Criteria)  
- วิธีติดตามและรายงานผลความเสี่ยง:contentReference[oaicite:6]{index=6}

---

## 2️⃣ Identify Risks

> “You cannot manage what you do not identify.”  

### 🔹 Output
- **Risk Register**  
- **Risk Report**  

### 🔹 ตัวอย่างแหล่งความเสี่ยงในโครงการ IT:contentReference[oaicite:7]{index=7}

| ประเภท | ตัวอย่าง |
|----------|-----------|
| **Market Risk** | ผลิตภัณฑ์ไม่เป็นที่ต้องการของตลาด |
| **Financial Risk** | ROI ต่ำกว่าเป้าหมาย |
| **Technology Risk** | ใช้เทคโนโลยีใหม่ที่ไม่เสถียร |
| **People Risk** | ขาดบุคลากรที่มีทักษะ |
| **Process Risk** | ขาดการวางแผนหรือขั้นตอนที่ชัดเจน |

---

### 🧠 เครื่องมือในการระบุความเสี่ยง (Tools)

| เครื่องมือ | คำอธิบาย |
|-------------|-----------|
| **Brainstorming** | ระดมสมองโดยทีมงาน มี Facilitator ควบคุม |
| **Delphi Technique** | ใช้ผู้เชี่ยวชาญหลายฝ่ายให้ความเห็นแบบนิรนาม |
| **Interviewing** | สัมภาษณ์ผู้มีประสบการณ์ในโครงการคล้ายกัน |
| **SWOT Analysis** | วิเคราะห์จุดแข็ง จุดอ่อน โอกาส และภัยคุกคาม:contentReference[oaicite:8]{index=8} |

---

### 📋 ตัวอย่าง Risk Register

| ID | Risk Description | Category | Probability | Impact | Owner | Response |
|----|------------------|-----------|--------------|---------|--------|-----------|
| R01 | Hardware defect | Technical | Medium | High | IT Lead | Add warranty clause |
| R02 | Staff turnover | People | High | Medium | PM | Cross-train key staff |
| R03 | Market change | Market | Low | High | Sponsor | Revise business plan |

> ⚙️ **Risk Trigger:** สัญญาณเตือน เช่น “System error >5 ครั้ง/วัน”:contentReference[oaicite:9]{index=9}

---

## 3️⃣ Perform Qualitative Risk Analysis

- ประเมิน **โอกาส (Probability)** และ **ผลกระทบ (Impact)**  
- จัดลำดับความสำคัญของความเสี่ยง  
- ใช้ **Probability/Impact Matrix (P-I Matrix)**  
- อาจให้คะแนนเชิงตัวเลขเพื่อคำนวณ “Risk Index”  
  \[
  \text{Risk Index} = \text{Probability} \times \text{Impact}
  \]

| Impact \\ Probability | Low | Medium | High |
|-----------------------|------|---------|------|
| **High** | M | H | H |
| **Medium** | L | M | H |
| **Low** | L | L | M |

> โฟกัสที่ความเสี่ยงในช่อง **High–High** เป็นอันดับแรก:contentReference[oaicite:10]{index=10}

---

### 🔹 Top 10 Risk Tracking

ใช้เพื่อติดตาม 10 ความเสี่ยงหลักในแต่ละเดือน  
บันทึกการเปลี่ยนแปลงอันดับและความคืบหน้า:contentReference[oaicite:11]{index=11}

| Rank | Risk | Trend | Status |
|-------|------|--------|---------|
| 1 | Poor definition | ↑ | Ongoing |
| 2 | Leadership gap | ↓ | Assigned new PM |
| 3 | Cost estimate error | → | Reassessing |

---

## 4️⃣ Perform Quantitative Risk Analysis

> ใช้วิธีการทางตัวเลขเพื่อวัดผลกระทบของความเสี่ยง

| เทคนิค | รายละเอียด |
|----------|-------------|
| **Decision Tree & EMV** | คำนวณ Expected Monetary Value = Probability × Impact |
| **Monte Carlo Simulation** | สุ่มค่าหลายครั้งเพื่อดูการกระจายของเวลา/ต้นทุน |
| **Sensitivity Analysis** | วิเคราะห์ผลของการเปลี่ยนแปลงตัวแปรที่มีผลต่อผลลัพธ์มากที่สุด:contentReference[oaicite:12]{index=12} |

---

## 5️⃣ Plan Risk Responses

### 🔹 สำหรับ Negative Risks (Threats)
| กลยุทธ์ | คำอธิบาย | ตัวอย่าง |
|-----------|------------|-----------|
| **Avoid** | หลีกเลี่ยงต้นเหตุ | ใช้เทคโนโลยีที่คุ้นเคย |
| **Transfer** | โอนความเสี่ยงให้บุคคลที่สาม | ซื้อประกันหรือทำสัญญา |
| **Mitigate** | ลดโอกาสหรือผลกระทบ | จ้างผู้เชี่ยวชาญ |
| **Accept** | ยอมรับความเสี่ยง | เตรียมแผนสำรอง |
| **Escalate** | แจ้งผู้บริหารระดับสูง | กรณีเกินขอบเขตโครงการ |

### 🔹 สำหรับ Positive Risks (Opportunities)
| กลยุทธ์ | คำอธิบาย | ตัวอย่าง |
|-----------|------------|-----------|
| **Exploit** | ทำให้เกิดขึ้นแน่นอน | โปรโมทโครงการเพื่อสร้างชื่อเสียง |
| **Share** | ร่วมมือกับผู้อื่น | พันธมิตรทางธุรกิจ |
| **Enhance** | ขยายโอกาส | เพิ่มงบการตลาด |
| **Accept** | ไม่ทำอะไรเพิ่มเติม | ปล่อยให้เกิดเอง |
| **Escalate** | ส่งต่อผู้มีอำนาจมากกว่า | แจ้งฝ่ายบริหาร:contentReference[oaicite:13]{index=13}

---

### 🔹 แผนสำรองและงบสำรอง
| ประเภท | คำอธิบาย | ตัวอย่าง |
|----------|------------|-----------|
| **Contingency Plan** | แผนสำรองเมื่อความเสี่ยงเกิดขึ้น | ใช้ Backup Server |
| **Fallback Plan** | ใช้เมื่อ Contingency ล้มเหลว | ใช้ข้อมูลในเครื่อง |
| **Contingency Reserve** | งบเผื่อ “Known Unknowns” | คำนวณจาก EMV |
| **Management Reserve** | งบเผื่อ “Unknown Unknowns” | 5–10% ของงบทั้งหมด:contentReference[oaicite:14]{index=14} |

---

## 6️⃣ Implement Risk Responses

- ดำเนินการตามแผนที่วางไว้  
- อัปเดตเอกสาร / Risk Register  
- สร้าง Change Request หากจำเป็น:contentReference[oaicite:15]{index=15}

---

## 7️⃣ Monitor Risks

- ตรวจสอบความเสี่ยงที่ระบุไว้และความเสี่ยงใหม่  
- ประเมินประสิทธิผลของกลยุทธ์ที่ใช้  
- ใช้ **Workaround** สำหรับความเสี่ยงที่ไม่มีแผนสำรอง:contentReference[oaicite:16]{index=16}

---

## 💻 การใช้ Software ช่วยในการบริหารความเสี่ยง

- ใช้ Excel / PMIS / Specialized Tools เช่น @Risk, RiskyProject  
- ใช้สร้าง Risk Register, Matrix และ Monte Carlo Simulation:contentReference[oaicite:17]{index=17}

---

## ⚙️ Agile Risk Management

- ประเมินความเสี่ยงในแต่ละ Iteration  
- ใช้ Retrospective และ Daily Stand-up ตรวจสอบความเสี่ยง  
- Cross-functional Team → แชร์ความรู้และลด Blind Spot:contentReference[oaicite:18]{index=18}

---

# 🧩 แบบทดสอบท้ายบท

1. ข้อใด **ไม่ใช่** กระบวนการของ Project Risk Management  
   - [ ] Identify Risks  
   - [ ] Monitor Risks  
   - [ ] Plan Risk Responses  
   - [X] Control Resources  

2. ความหมายของ “Risk” คือ  
   - [X] ความไม่แน่นอนที่มีผลบวกหรือลบต่อวัตถุประสงค์  
   - [ ] ปัญหาที่เกิดขึ้นแน่นอน  
   - [ ] ผลกระทบเชิงลบเท่านั้น  
   - [ ] ความล้มเหลวในการบริหาร  

3. เครื่องมือใดใช้ในการระบุความเสี่ยง  
   - [ ] Pareto Chart  
   - [X] Delphi Technique  
   - [ ] Fishbone Diagram  
   - [ ] CPM  

4. Probability × Impact ใช้ในขั้นตอนใด  
   - [X] Qualitative Risk Analysis  
   - [ ] Quantitative Risk Analysis  
   - [ ] Risk Monitoring  
   - [ ] Risk Planning  

5. การซื้อประกันเพื่อโอนความเสี่ยง คือกลยุทธ์แบบใด  
   - [X] Transfer  
   - [ ] Mitigate  
   - [ ] Avoid  
   - [ ] Accept  

6. Monte Carlo Simulation ใช้เพื่อ  
   - [X] วิเคราะห์โอกาสทางสถิติของผลลัพธ์หลายรูปแบบ  
   - [ ] ประมาณค่าเฉลี่ยต้นทุน  
   - [ ] คำนวณ ROI  
   - [ ] แสดงกราฟ Gantt  

7. ข้อใดคือแผนสำรองเมื่อ Contingency Plan ล้มเหลว  
   - [ ] Risk Transfer  
   - [X] Fallback Plan  
   - [ ] Workaround  
   - [ ] Residual Risk  

8. Contingency Reserve ใช้สำหรับ  
   - [X] ความเสี่ยงที่รู้ล่วงหน้า (Known Unknowns)  
   - [ ] ความเสี่ยงใหม่ทั้งหมด  
   - [ ] Unknown Unknowns  
   - [ ] การล้มเหลวของ Contingency  

9. Positive Risk เรียกอีกชื่อว่า  
   - [ ] Threat  
   - [X] Opportunity  
   - [ ] Issue  
   - [ ] Residual  

10. ใน Agile Project การจัดการความเสี่ยงทำอย่างไร  
    - [X] ประเมินและปรับทุก Iteration  
    - [ ] ทำเฉพาะต้นโครงการ  
    - [ ] ไม่จำเป็นต้องมีการบริหารความเสี่ยง  
    - [ ] ทำเฉพาะเมื่อเกิดปัญหาใหญ่  

---

## ✅ เฉลยท้ายบท

| ข้อ | คำตอบ | หมายเหตุ |
|-----|--------|-----------|
| 1 | ✅ Control Resources | ไม่ใช่ใน Risk Mgmt |
| 2 | ✅ ความไม่แน่นอน | Definition of Risk |
| 3 | ✅ Delphi | วิธีระบุความเสี่ยง |
| 4 | ✅ Qualitative | ใช้คำนวณ Risk Index |
| 5 | ✅ Transfer | ซื้อประกัน/ทำสัญญา |
| 6 | ✅ Monte Carlo | Simulation เชิงสถิติ |
| 7 | ✅ Fallback Plan | ใช้เมื่อ Contingency ล้มเหลว |
| 8 | ✅ Known Unknowns | งบสำรองเฉพาะ |
| 9 | ✅ Opportunity | ผลบวกของความเสี่ยง |
| 10 | ✅ ทุก Iteration | Agile Risk Mgmt |

---

> 💡 **Tips สำหรับสอบ**
> - จำ 7 ขั้นตอน: Plan → Identify → Qualitative → Quantitative → Response → Implement → Monitor  
> - Threat → Avoid / Transfer / Mitigate / Accept  
> - Opportunity → Exploit / Share / Enhance / Accept  
> - Contingency vs Fallback vs Reserve ออกสอบบ่อย  
> - Monte Carlo = การสุ่มจำลอง / EMV = Probability × Impact  
> - Agile → ประเมินความเสี่ยงทุก Iteration  
> - Risk Register และ P-I Matrix คือหัวใจของการจัดการความเสี่ยง
