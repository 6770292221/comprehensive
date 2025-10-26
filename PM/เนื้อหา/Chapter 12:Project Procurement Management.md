# 📘 บทที่ 12: การจัดการการจัดซื้อจัดจ้างของโครงการ (Project Procurement Management)
จาก *Information Technology Project Management, Ninth Edition*:contentReference[oaicite:0]{index=0}

---

## 🎯 วัตถุประสงค์ของบทเรียน (Learning Objectives)
1. อธิบายความสำคัญของ **การจัดซื้อจัดจ้าง (Procurement Management)** และแนวโน้มการใช้ **Outsourcing** ในโครงการ IT  
2. อธิบายขั้นตอนการวางแผนจัดซื้อ รวมถึงการเลือกประเภทสัญญา การทำ Make-or-Buy Analysis และการจัดทำเอกสารที่เกี่ยวข้อง  
3. อธิบายการดำเนินการจัดซื้อ (Conduct Procurements) ตั้งแต่การขอเสนอราคาไปจนถึงการคัดเลือกผู้ขาย  
4. อธิบายการควบคุมการจัดซื้อ (Control Procurements) และการจัดการสัญญา  
5. ระบุประเภทของซอฟต์แวร์ที่ช่วยในการบริหารจัดซื้อ  
6. อธิบายแนวคิดการจัดซื้อในสภาพแวดล้อมแบบ **Agile/Adaptive**

---

## 💡 1. ความสำคัญของ Project Procurement Management
- **Procurement** หมายถึง การจัดหาสินค้าหรือบริการจากแหล่งภายนอก  
- ใช้คำเรียกอื่นว่า *Purchasing* หรือ *Outsourcing*  
- จุดประสงค์หลัก:
  - เข้าถึงทักษะและเทคโนโลยีที่องค์กรไม่มี  
  - ลดต้นทุนและเพิ่มความยืดหยุ่นของทรัพยากร  
  - มุ่งเน้นที่ธุรกิจหลัก (Core Business)  
  - เพิ่มความรับผิดชอบผ่าน “สัญญาทางกฎหมาย”  

> 🧠 *“Contract = ความรับผิดชอบที่ชัดเจนของทั้งสองฝ่าย”*:contentReference[oaicite:1]{index=1}

---

## ⚙️ 2. กระบวนการหลักของ Project Procurement Management
| ลำดับ | กระบวนการ | รายละเอียด |
|--------|-------------|-------------|
| 1️⃣ | **Planning Procurement Management** | วางแผนว่าจะจัดซื้ออะไร เมื่อใด และอย่างไร |
| 2️⃣ | **Conducting Procurements** | ขอเสนอราคา (RFP/RFQ), คัดเลือกผู้ขาย และเซ็นสัญญา |
| 3️⃣ | **Controlling Procurements** | ติดตามผลสัญญา การชำระเงิน และการปิดสัญญา:contentReference[oaicite:2]{index=2}

---

## 🧩 3. Planning Procurement Management
- ระบุว่าความต้องการใดของโครงการควรจัดซื้อจากภายนอก  
- ประเมินว่าจะ “ทำเอง” หรือ “ซื้อมา” (Make-or-Buy)  
- หากไม่มีความจำเป็นต้องจัดซื้อ → ไม่ต้องทำขั้นตอนอื่น  

### 📘 Output สำคัญ:  
- Make-or-Buy Decision  
- Procurement Management Plan  
- Procurement Documents (RFP, RFQ)  
- Source Selection Criteria:contentReference[oaicite:3]{index=3}

---

## 🧾 4. ประเภทของสัญญา (Types of Contracts)
| ประเภท | ลักษณะ | ตัวอย่าง |
|----------|----------|------------|
| **1. Fixed Price (FP)** | ราคาคงที่ตายตัว | เหมาะกับงานที่ขอบเขตชัดเจน |
| – FFP | ราคาคงที่แน่นอน | จ่ายเท่าที่ตกลง |
| – FP-EPA | ปรับราคาได้เมื่อสภาวะตลาดเปลี่ยน | ใช้กับโครงการระยะยาว |
| – FPIF | มีค่าจูงใจตามผลงาน | ใช้สูตรคำนวณ PTA: จุดที่ผู้ขายรับผิดชอบต้นทุนเกิน:contentReference[oaicite:4]{index=4} |
| **2. Cost-Reimbursable (CP)** | จ่ายตามต้นทุนจริง + ค่าธรรมเนียม | เหมาะกับงานไม่แน่นอน |
| – CPIF | ต้นทุน + ค่าจูงใจ |
| – CPFF | ต้นทุน + ค่าคงที่ |
| – CPAF | ต้นทุน + ค่ารางวัลตามความพอใจผู้ซื้อ |
| – CPPC | ต้นทุน + เปอร์เซ็นต์ (ไม่แนะนำ):contentReference[oaicite:5]{index=5} |
| **3. Time & Material (T&M)** | คิดตามชั่วโมง + ค่าวัสดุ | เหมาะกับที่ระยะเวลาไม่แน่นอน |
| **4. Unit Price** | จ่ายตามจำนวนหน่วย | เช่น คอมพิวเตอร์เครื่องละ $1,000 จำนวน 10 เครื่อง:contentReference[oaicite:6]{index=6} |

> 💬 **Tip:** สัญญาควรมี “Termination Clause” เผื่อยกเลิกได้ตามเงื่อนไข

---

## 🧮 5. เครื่องมือช่วยวางแผนจัดซื้อ
| เครื่องมือ | รายละเอียด | ตัวอย่าง |
|--------------|-------------|-----------|
| **Make-or-Buy Analysis** | วิเคราะห์ว่าควรทำเองหรือซื้อ | ซื้ออุปกรณ์ราคา $12,000 หรือเช่า $800/วัน → หากใช้น้อยกว่า 30 วันควรเช่า |
| **Expert Judgment** | ใช้ผู้เชี่ยวชาญภายใน/ภายนอก |
| **Market Research** | ศึกษาตลาดและผู้ขายที่เป็นไปได้:contentReference[oaicite:7]{index=7} |

---

## 📋 6. Procurement Management Plan
กำหนดแนวทางในการจัดซื้อ ตั้งแต่เอกสารจนถึงการปิดสัญญา  
ประกอบด้วย:
- ประเภทของสัญญาที่ใช้  
- เอกสารมาตรฐาน / Template  
- ขอบเขตงาน (SOW) และ WBS ที่เกี่ยวข้อง  
- บทบาทของทีมงานและฝ่ายกฎหมาย  
- ระยะเวลาในการจัดซื้อ  
- รายชื่อผู้ขายที่ผ่านการรับรอง:contentReference[oaicite:8]{index=8}

---

## 🧾 7. Statement of Work (SOW)
- เอกสารขอบเขตงานที่แนบกับสัญญา  
- แสดงรายละเอียดงานที่ผู้ขายต้องทำให้ครบตามความคาดหวังของผู้ซื้อ  
- ถือเป็นส่วนหนึ่งของสัญญาอย่างเป็นทางการ:contentReference[oaicite:9]{index=9}

---

## 📑 8. เอกสารการจัดซื้อ (Procurement Documents)
| ประเภท | ลักษณะ |
|----------|----------|
| **RFP (Request for Proposal)** | ใช้เมื่อผู้ขายสามารถเสนอแนวทางแตกต่างกันได้ |
| **RFQ (Request for Quotation)** | ใช้เมื่อสินค้าเป็นมาตรฐาน เช่น ราคาคงที่หรือจำนวนแน่นอน:contentReference[oaicite:10]{index=10} |

---

## 🎯 9. เกณฑ์การคัดเลือกผู้ขาย (Source Selection Criteria)
| เกณฑ์ | น้ำหนัก (%) |
|---------|--------------|
| Technical Approach | 30 |
| Management Approach | 30 |
| Past Performance | 20 |
| Price | 20 |
> ✅ ผู้จัดการโครงการของผู้ขายควรเป็นผู้นำเสนอเองในการ Pitch:contentReference[oaicite:11]{index=11}

---

## 🔎 10. Conducting Procurements
กระบวนการหลังจากวางแผนเสร็จ:
1. ระบุผู้ขายที่มีศักยภาพ  
2. ส่งเอกสาร RFP/RFQ  
3. จัดประชุมผู้เสนอราคา (Bidder’s Conference) เพื่อชี้แจง  
4. ประเมินข้อเสนอโดยทีมเทคนิค การจัดการ และต้นทุน  
5. จัดทำ Shortlist และต่อรองราคา  
6. ออก **Contract** อย่างเป็นทางการ:contentReference[oaicite:12]{index=12}

---

## 🧱 11. Controlling Procurements
ดูแลให้ผู้ขายปฏิบัติตามสัญญา  
- ควรมีฝ่ายกฎหมายร่วมร่างสัญญา  
- หลีกเลี่ยง “Constructive Change Orders” (การเปลี่ยนแปลงโดยไม่เป็นทางการ)  
- ใช้เครื่องมือ:
  - **Change Control System**
  - **Performance Review**
  - **Procurement Audits**
  - **Records Management System**  
- การปิดสัญญาควรผ่านการตรวจสอบงานและเอกสารครบถ้วน:contentReference[oaicite:13]{index=13}

---

## 💻 12. ซอฟต์แวร์ที่ช่วยจัดการจัดซื้อ
| ประเภท | การใช้งาน |
|----------|------------|
| Word / Docs | เขียนสัญญาและข้อเสนอ |
| Excel / Sheets | วิเคราะห์ราคาและเกณฑ์คะแนน |
| Database | จัดเก็บข้อมูลผู้ขาย |
| Presentation | สรุปผลการจัดซื้อ |
| E-Procurement | จัดซื้อแบบอิเล็กทรอนิกส์:contentReference[oaicite:14]{index=14} |

---

## 🌀 13. Procurement ในสภาพแวดล้อม Agile
- ยึดหลัก “**Customer Collaboration over Contract Negotiation**”  
- ผู้ซื้อและผู้ขายร่วมมือกันตลอดวงจรชีวิตการพัฒนา  
- เน้นความเร็วและการปรับตัว  
- ต้องวางแผนล่วงหน้าเพื่อให้สอดคล้องกับรอบ Sprint:contentReference[oaicite:15]{index=15}

---

## 📚 สรุปท้ายบท
- **Procurement = การจัดหาสินค้าหรือบริการจากภายนอก**  
- มีกระบวนการหลัก 3 ขั้นตอน: **Plan → Conduct → Control**  
- ต้องเลือกประเภทสัญญาให้เหมาะสม และกำหนดขอบเขตงานชัดเจน  
- การใช้ซอฟต์แวร์ช่วยบริหารจัดซื้อช่วยเพิ่มประสิทธิภาพ  
- ใน Agile ต้องสร้างความร่วมมือมากกว่าการต่อรอง:contentReference[oaicite:16]{index=16}

---

## 🧾 แนวข้อสอบแบบกากบาท (Multiple Choice)

1. กระบวนการใดไม่ใช่ส่วนหนึ่งของ Project Procurement Management  
   - A) Planning  
   - B) Conducting  
   - ✅ C) Monitoring Communications  
   - D) Controlling  

2. “Make-or-Buy Analysis” ใช้เพื่ออะไร  
   - A) เลือกผู้ขาย  
   - ✅ B) ตัดสินใจว่าจะทำเองหรือซื้อจากภายนอก  
   - C) ประเมินราคาเสนอ  
   - D) วิเคราะห์ต้นทุนจริง  

3. สัญญาแบบใดที่ราคาคงที่และผู้ขายรับความเสี่ยงสูงสุด  
   - ✅ A) Fixed Price  
   - B) Cost Reimbursable  
   - C) Time & Material  
   - D) Unit Price  

4. “FP-EPA” หมายถึงอะไร  
   - A) Fixed Price + Evaluation Plan Agreement  
   - ✅ B) Fixed Price with Economic Price Adjustment  
   - C) Flexible Price Estimation Agreement  
   - D) Fixed Procurement Evaluation Agreement  

5. เอกสารใดใช้เมื่อผู้ขายสามารถเสนอแนวทางต่างกันได้  
   - ✅ A) RFP  
   - B) RFQ  
   - C) Contract SOW  
   - D) Procurement Plan  

6. ในเกณฑ์คัดเลือกผู้ขาย ข้อใดมีน้ำหนักมากที่สุดโดยทั่วไป  
   - ✅ A) Technical Approach  
   - B) Price  
   - C) Past Performance  
   - D) Management Approach  

7. สถานการณ์ใดถือว่าเป็น “Constructive Change Order”  
   - ✅ A) ผู้ขายทำงานเกินขอบเขตโดยไม่ได้รับคำสั่งเป็นทางการ  
   - B) ผู้ซื้อจ่ายเงินช้ากว่ากำหนด  
   - C) เปลี่ยนผู้ขายระหว่างโครงการ  
   - D) ปิดสัญญาก่อนเวลา  

8. ซอฟต์แวร์ประเภทใดช่วยในการจัดซื้ออัตโนมัติ  
   - A) Power BI  
   - ✅ B) E-Procurement  
   - C) Excel  
   - D) Jira  

9. ใน Agile ควรเน้นสิ่งใดมากที่สุด  
   - ✅ A) ความร่วมมือกับลูกค้า  
   - B) การต่อรองสัญญา  
   - C) การทำเอกสารอย่างละเอียด  
   - D) การใช้ Fixed Price Contract  

10. “Statement of Work (SOW)” มีวัตถุประสงค์เพื่อ  
    - ✅ A) อธิบายขอบเขตงานที่ผู้ขายต้องทำตามสัญญา  
    - B) สรุปผลการดำเนินงาน  
    - C) แสดงต้นทุนรวมของโครงการ  
    - D) เป็นเอกสารภายในทีมเท่านั้น  

---

📖 **คำแนะนำก่อนสอบ**
- จำกระบวนการ 3 ขั้นตอน: **Plan – Conduct – Control**  
- ท่องประเภทสัญญา FP, CP, T&M และตัวอย่าง  
- จำความหมายของ RFP vs RFQ  
- รู้สูตร PTA (Point of Total Assumption)  
- เข้าใจแนวคิด Agile: “Collaboration > Negotiation”  
