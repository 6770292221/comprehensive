# 📘 Chapter 12: Project Procurement Management

> แหล่งที่มา: *Information Technology Project Management (9th Edition)*  
> โดย Kathy Schwalbe / Twittie Senivongse (ed.)  
> “Procurement means acquiring goods or services from an outside source.”:contentReference[oaicite:1]{index=1}

---

## 🎯 Learning Objectives

1. เข้าใจความสำคัญของการจัดซื้อจัดจ้าง (Procurement) และการใช้ Outsourcing ในโครงการ IT  
2. อธิบายขั้นตอนการวางแผนการจัดซื้อ (Planning Procurement)  
3. รู้จักประเภทของสัญญา (Contract Types) และเกณฑ์การเลือกผู้ขาย  
4. เข้าใจการดำเนินการจัดซื้อ (Conduct Procurements) และการควบคุมสัญญา (Control Procurements)  
5. อธิบายเครื่องมือซอฟต์แวร์ที่ช่วยบริหารการจัดซื้อ  
6. อธิบายการพิจารณาการจัดซื้อใน Agile หรือ Adaptive Environments:contentReference[oaicite:2]{index=2}

---

## 🧩 ความสำคัญของ Project Procurement Management

- **Procurement = การได้มาซึ่งสินค้า/บริการจากภายนอก**
- ช่วยให้องค์กร **เข้าถึงทักษะหรือเทคโนโลยี** ที่ไม่มีภายใน  
- ช่วยลดต้นทุนประจำ (Fixed Cost) และเพิ่มความยืดหยุ่น  
- **Outsourcing** ช่วยให้โฟกัสที่ “Core Business”  
- ตัวอย่างเช่น Walmart พัฒนาเองทั้งหมด, แต่ Zulily ใช้ in-house software เพื่อความเร็วในการนวัตกรรม  
- แนวโน้มใหม่: **Urban Onshoring** – ดึงงาน IT กลับมาทำในประเทศ:contentReference[oaicite:3]{index=3}

---

## ⚙️ 3 กระบวนการหลักของ Project Procurement Management

| ลำดับ | Process | คำอธิบาย |
|--------|----------|-----------|
| 1️⃣ | **Plan Procurement Management** | วางแผนว่าจะจัดซื้ออะไร เมื่อไร และอย่างไร |
| 2️⃣ | **Conduct Procurements** | ดำเนินการขอเสนอราคา คัดเลือกผู้ขาย ทำสัญญา |
| 3️⃣ | **Control Procurements** | ตรวจสอบและบริหารความสัมพันธ์กับผู้ขาย ปิดสัญญาเมื่อเสร็จสิ้น:contentReference[oaicite:4]{index=4}

---

## 1️⃣ Plan Procurement Management

> ระบุว่า “สิ่งใดควรซื้อจากภายนอก” และ “สิ่งใดทำเองได้”:contentReference[oaicite:5]{index=5}

### 📋 ผลลัพธ์หลัก:
- **Make-or-Buy Decision**  
  ตัดสินใจ “ทำเอง (Make)” หรือ “ซื้อ (Buy)”

### 📘 ตัวอย่างการคำนวณ Make-or-Buy:
- ซื้อเครื่องจักร = 12,000 + 400/วัน  
- เช่าเครื่องจักร = 800/วัน  
- จุดคุ้มค่า:  
  \[
  800d = 12,000 + 400d \Rightarrow d = 30 \text{ วัน}
  \]
  ⇒ ถ้าใช้ < 30 วัน → เช่า / ถ้าใช้ > 30 วัน → ซื้อ:contentReference[oaicite:6]{index=6}

---

## 🔖 ประเภทของสัญญา (Types of Contracts)

| ประเภท | ลักษณะ | ตัวอย่าง / หมายเหตุ |
|----------|----------|----------------------|
| **Fixed-Price (FP)** | ราคาตายตัว เหมาะกับงานที่นิยามชัดเจน | FFP, FPIF, FP-EPA |
| **FPIF (Fixed Price Incentive Fee)** | มีรางวัลตามผลงาน | ใช้สูตร PTA คำนวณจุดที่ผู้ขายเริ่มรับภาระต้นทุนเอง |
| **Cost-Reimbursable (CR)** | ผู้ซื้อจ่ายต้นทุนจริง + ค่าธรรมเนียม | CPIF, CPFF, CPAF, CPPC |
| **Time & Material (T&M)** | จ่ายตามชั่วโมง + วัสดุจริง | $80/hr + $10,000 fixed |
| **Unit Price** | จ่ายตามหน่วยบริการ | เช่น ซื้อคอม 10 เครื่อง × $1,000 = $10,000:contentReference[oaicite:7]{index=7}

---

### 🔹 ตัวอย่างสูตร Point of Total Assumption (PTA)
\[
PTA = \frac{(Ceiling - Target Price)}{\text{Buyer’s Share Ratio}} + \text{Target Cost}
\]
- ใช้กับ **Fixed Price Incentive Fee Contract (FPIF)**  
- เมื่อผู้ขายรับภาระต้นทุนเกิน PTA → ขาดทุนเอง:contentReference[oaicite:8]{index=8}

---

## 🧠 เครื่องมือและเทคนิคสำหรับ Plan Procurement

| เครื่องมือ | รายละเอียด |
|-------------|-------------|
| **Make-or-Buy Analysis** | วิเคราะห์ต้นทุนการทำเอง vs จ้างภายนอก |
| **Expert Judgment** | ใช้ผู้เชี่ยวชาญช่วยตัดสินใจ |
| **Market Research** | ศึกษาผู้ขายในตลาด ประเมินแนวโน้มเทคโนโลยี:contentReference[oaicite:9]{index=9} |

---

## 📄 Procurement Management Plan

- ระบุขั้นตอนการจัดซื้อ, บทบาทผู้รับผิดชอบ, เอกสารมาตรฐาน  
- แนวทางเลือกผู้ขาย, Template สัญญา, ระยะเวลา lead time  
- การใช้ **Independent Estimate** เปรียบเทียบราคาผู้ขาย:contentReference[oaicite:10]{index=10}

---

### 🔹 Statement of Work (SOW)

> ขอบเขตงานที่ต้องการจัดซื้อ – แนบเป็นส่วนหนึ่งของสัญญา  
> ช่วยให้ผู้ขายเข้าใจความต้องการของผู้ซื้ออย่างชัดเจน:contentReference[oaicite:11]{index=11}

---

### 🔹 Procurement Documents

| เอกสาร | จุดประสงค์ |
|----------|--------------|
| **RFP (Request for Proposal)** | ขอข้อเสนอจากผู้ขาย (โครงการไม่ชัดเจน) |
| **RFQ (Request for Quotation)** | ขอราคา สำหรับสินค้ามาตรฐาน |
| **Bid / Tender** | เอกสารเสนอราคาอย่างเป็นทางการ:contentReference[oaicite:12]{index=12} |

---

### 🔹 Source Selection Criteria

| เกณฑ์ | น้ำหนัก (%) |
|---------|-------------|
| Technical Approach | 30 |
| Management Approach | 30 |
| Past Performance | 20 |
| Price | 20 |
> อาจมีการให้ผู้ขายเสนอ “Presentation” เพื่อประเมินเพิ่มเติม:contentReference[oaicite:13]{index=13}

---

## 2️⃣ Conduct Procurements

- ดำเนินการตามแผน  
- เชิญผู้ขาย → ส่งเอกสาร → รับข้อเสนอ → คัดเลือกผู้ขาย → เจรจาสัญญา:contentReference[oaicite:14]{index=14}

### 🔹 ขั้นตอนย่อย
1. ระบุผู้ขายที่ต้องการ  
2. จัด **Bidders’ Conference** เพื่อชี้แจงขอบเขตงาน  
3. ใช้ **Evaluation Sheet** เพื่อจัดอันดับข้อเสนอ  
4. ผู้ขายที่ผ่านเข้ารอบจะเสนอ **BAFO (Best and Final Offer)**  

---

## 3️⃣ Control Procurements

> ตรวจสอบให้มั่นใจว่า “ผู้ขายทำตามสัญญา”:contentReference[oaicite:15]{index=15}

### 🔹 เครื่องมือหลัก
- Contract Change Control System  
- Inspection & Audit  
- Performance Review  
- Backup Plans / Contingency  

### 🔹 Contract Closure
- ตรวจสอบว่างานครบถ้วน  
- ปิดสัญญาและเก็บบันทึก  
- หากมีข้อพิพาท → ใช้ **ADR (Alternative Dispute Resolution)** เช่น Mediation หรือ Arbitration:contentReference[oaicite:16]{index=16}

---

## 🧮 Software ที่ใช้ในการบริหารจัดซื้อ

| ประเภท | ตัวอย่างการใช้งาน |
|----------|--------------------|
| Word | เขียนสัญญาและข้อเสนอ |
| Excel | ทำตารางเปรียบเทียบผู้ขาย |
| Database | เก็บข้อมูล Supplier |
| PowerPoint | นำเสนอผลประเมิน |
| E-Procurement | ระบบจัดซื้อออนไลน์ เช่น SAP Ariba:contentReference[oaicite:17]{index=17} |

---

## ⚙️ Agile / Adaptive Environments

- เน้น “**Collaboration over Contract Negotiation**”  
- Buyer และ Seller ทำงานร่วมกันระหว่างการพัฒนา  
- วางแผนล่วงหน้าเพื่อไม่ให้การจัดซื้อกลายเป็นอุปสรรคต่อ Sprint:contentReference[oaicite:18]{index=18}

---

## 🧾 สรุปท้ายบท

- Procurement = การได้มาซึ่งสินค้า/บริการจากภายนอก  
- มีกระบวนการหลัก 3 ขั้นตอน: **Plan – Conduct – Control**  
- ใช้ประเภทสัญญาที่เหมาะสม เช่น FP, CR, T&M  
- ใช้เอกสารมาตรฐาน เช่น RFP / RFQ / SOW  
- มีการปิดสัญญา (Closure) และเรียนรู้บทเรียน (Procurement Audit):contentReference[oaicite:19]{index=19}

---

# 🧩 แบบทดสอบท้ายบท

1. ข้อใด **ไม่ใช่** กระบวนการของ Project Procurement Management  
   - [ ] Plan Procurements  
   - [ ] Conduct Procurements  
   - [ ] Control Procurements  
   - [X] Monitor Risks  

2. จุดมุ่งหมายของ Procurement คืออะไร  
   - [X] การได้มาซึ่งสินค้า/บริการจากภายนอก  
   - [ ] การบริหารทีมงานภายใน  
   - [ ] การตรวจสอบคุณภาพ  
   - [ ] การวิเคราะห์ต้นทุน  

3. Make-or-Buy Decision ใช้ในขั้นตอนใด  
   - [X] Plan Procurement  
   - [ ] Conduct Procurement  
   - [ ] Control Procurement  
   - [ ] Close Project  

4. Fixed-Price Contract เหมาะกับกรณีใด  
   - [X] งานที่มีขอบเขตชัดเจน  
   - [ ] งานที่เปลี่ยนบ่อย  
   - [ ] งานที่ไม่สามารถคาดต้นทุนได้  
   - [ ] งานทดลองเทคโนโลยีใหม่  

5. สัญญาแบบใดที่ผู้ขายได้รับ “ค่าตอบแทนตามต้นทุนจริง + โบนัส”  
   - [ ] FFP  
   - [X] CPIF  
   - [ ] T&M  
   - [ ] FP-EPA  

6. การประชุม Bidders’ Conference มีจุดประสงค์เพื่อ  
   - [X] ชี้แจงขอบเขตและความคาดหวังกับผู้ขาย  
   - [ ] ประกาศรายชื่อผู้ชนะ  
   - [ ] ปิดสัญญา  
   - [ ] ประเมินผลหลังส่งมอบ  

7. ข้อใดเป็น Output ของ Control Procurements  
   - [X] Closed Contract  
   - [ ] Risk Register  
   - [ ] SOW Document  
   - [ ] RFP Template  

8. ADR (Alternative Dispute Resolution) ใช้เพื่อ  
   - [X] แก้ไขข้อพิพาทระหว่างผู้ซื้อ-ผู้ขาย  
   - [ ] ลดต้นทุนการจัดซื้อ  
   - [ ] ปิดสัญญาเร็วขึ้น  
   - [ ] เพิ่มระยะเวลาสัญญา  

9. Agile Procurement เน้นสิ่งใดมากที่สุด  
   - [ ] เอกสารสัญญาละเอียด  
   - [X] ความร่วมมือระหว่าง Buyer และ Seller  
   - [ ] ราคาตายตัว  
   - [ ] การแข่งขันเสนอราคา  

10. เอกสารใดใช้สำหรับการขอ “ข้อเสนอแนวทาง” มากกว่าแค่ราคา  
    - [X] RFP  
    - [ ] RFQ  
    - [ ] Purchase Order  
    - [ ] Work Authorization  

---

## ✅ เฉลยท้ายบท

| ข้อ | คำตอบ | หมายเหตุ |
|-----|--------|-----------|
| 1 | ✅ Monitor Risks | ไม่อยู่ใน Procurement Mgmt |
| 2 | ✅ ได้มาซึ่งสินค้า/บริการ | Definition of Procurement |
| 3 | ✅ Plan Procurement | ใช้ตัดสินใจซื้อหรือทำเอง |
| 4 | ✅ Fixed Price | เหมาะกับขอบเขตชัดเจน |
| 5 | ✅ CPIF | Cost + Incentive Fee |
| 6 | ✅ Bidders’ Conf | ชี้แจงขอบเขตงาน |
| 7 | ✅ Closed Contract | ผลลัพธ์หลังควบคุมสัญญา |
| 8 | ✅ ADR | ใช้แก้ข้อพิพาท |
| 9 | ✅ Collaboration | Agile principle |
| 10 | ✅ RFP | ใช้ขอข้อเสนอเชิงเทคนิค |

---

> 💡 **Tips สำหรับสอบ**
> - จำ 3 ขั้นตอนหลัก: Plan → Conduct → Control  
> - สั
