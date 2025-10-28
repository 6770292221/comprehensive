# 📘 Chapter 5: Project Scope Management

> แหล่งที่มา: *Information Technology Project Management (9th Edition)* — Kathy Schwalbe / Twittie Senivongse (ed.)  
> Scope คือ “งานทั้งหมดที่ต้องทำเพื่อให้ได้ผลลัพธ์ตามวัตถุประสงค์ของโครงการ”

---

## 🎯 Learning Objectives

1. เข้าใจความสำคัญของการบริหารขอบเขตโครงการ (Scope Management)  
2. อธิบายกระบวนการวางแผน กำหนด และควบคุมขอบเขต  
3. อธิบายวิธีรวบรวมความต้องการ (Collect Requirements)  
4. เข้าใจการสร้าง WBS และ WBS Dictionary  
5. อธิบายการตรวจสอบและควบคุมขอบเขตโครงการ (Validate & Control Scope)  
6. อธิบายบทบาทของซอฟต์แวร์และแนวทาง Agile ต่อ Scope Management:contentReference[oaicite:1]{index=1}

---

## 🧩 ความหมายของ Project Scope Management

**Project Scope Management** คือกระบวนการที่ช่วยกำหนดและควบคุม “งานที่อยู่ในขอบเขต” และ “งานที่ไม่อยู่ในขอบเขต”  
เพื่อให้ทุกฝ่ายเข้าใจตรงกันเกี่ยวกับสิ่งที่โครงการจะส่งมอบ (Deliverables)

- **Scope** = งานทั้งหมดที่เกี่ยวข้องกับการสร้างผลิตภัณฑ์หรือบริการของโครงการ  
- **Deliverable** = ผลผลิตของโครงการ เช่น รายงาน เอกสาร ระบบ หรือบริการ:contentReference[oaicite:2]{index=2}

---

## 🧠 กระบวนการหลักของ Scope Management (6 ขั้นตอน)

| ลำดับ | กระบวนการ | คำอธิบายสั้น ๆ |
|--------|-------------|----------------|
| 1️⃣ | **Plan Scope Management** | วางแผนว่าขอบเขตจะถูกกำหนด ควบคุม และตรวจสอบอย่างไร |
| 2️⃣ | **Collect Requirements** | รวบรวมและบันทึกความต้องการจากผู้มีส่วนเกี่ยวข้อง |
| 3️⃣ | **Define Scope** | จัดทำเอกสาร Project Scope Statement |
| 4️⃣ | **Create WBS** | แตกโครงสร้างงานเป็นชิ้นย่อย ๆ |
| 5️⃣ | **Validate Scope** | ตรวจสอบและยืนยันผลลัพธ์กับลูกค้า |
| 6️⃣ | **Control Scope** | ควบคุมการเปลี่ยนแปลงไม่ให้เกิด “Scope Creep” |

---

## 1️⃣ Plan Scope Management

- ใช้ **Expert Judgment**, **Data Analysis**, และ **Meetings** เพื่อสร้าง  
  - **Scope Management Plan** → ระบุวิธีสร้างและควบคุมขอบเขต  
  - **Requirements Management Plan** → ระบุวิธีรวบรวม วิเคราะห์ และติดตามความต้องการ  
- เนื้อหาของแผนรวมถึง  
  - วิธีสร้าง **Scope Statement**  
  - แนวทางสร้างและอนุมัติ **WBS**  
  - วิธีควบคุมการเปลี่ยนแปลงขอบเขต:contentReference[oaicite:3]{index=3}

---

## 2️⃣ Collect Requirements

> “หากไม่กำหนดความต้องการอย่างชัดเจน → โครงการจะต้องเสียเวลาแก้ไขภายหลัง”

### เทคนิคในการเก็บ Requirements
- การสัมภาษณ์ (Interviews)  
- Focus Groups / Workshops  
- แบบสอบถาม (Surveys)  
- การสังเกต (Observation)  
- การวิเคราะห์เอกสาร (Document Analysis)  
- การสร้างต้นแบบ (Prototyping)  
- การเปรียบเทียบ Benchmarking:contentReference[oaicite:4]{index=4}

### เครื่องมือสำคัญ: **Requirements Traceability Matrix (RTM)**
| Requirement ID | ชื่อ | ประเภท | แหล่งที่มา | สถานะ |
|----------------|------|----------|-------------|--------|
| R32 | Laptop Memory | Hardware | Charter / Spec | ✅ Completed |

RTM ใช้ติดตามความต้องการแต่ละข้อจากต้นทางจนถึงการทดสอบ:contentReference[oaicite:5]{index=5}

---

## 3️⃣ Define Scope

**Project Scope Statement** ต้องมีองค์ประกอบดังนี้:
- Product Description  
- Acceptance Criteria  
- Deliverables ทั้งหมด  
- Boundaries, Constraints, Assumptions  
- References เอกสารแนบ

> เมื่อเวลาผ่านไป ขอบเขตควรชัดเจนและละเอียดมากขึ้นเรื่อย ๆ:contentReference[oaicite:6]{index=6}

---

## 4️⃣ Create Work Breakdown Structure (WBS)

**WBS** = การแบ่งงาน (Deliverable-Oriented Decomposition)  
เพื่อกำหนด Scope ทั้งหมดของโครงการ

- งานที่เล็กที่สุดใน WBS เรียกว่า **Work Package**  
- **Scope Baseline** = Scope Statement + WBS + WBS Dictionary  
- วิธีสร้าง WBS:
  1. **Using Guidelines**  
  2. **Analogy Approach** (อ้างอิงจากโครงการเก่า)  
  3. **Top-Down Approach**  
  4. **Bottom-Up Approach**  
  5. **Mind Mapping**:contentReference[oaicite:7]{index=7}

> ⚙️ WBS Dictionary คือเอกสารอธิบายรายละเอียดของแต่ละ WBS Item  
> เพื่อให้เข้าใจตรงกันในขอบเขตและลำดับความรับผิดชอบ:contentReference[oaicite:8]{index=8}

---

## 5️⃣ Validate Scope

- การตรวจสอบความถูกต้องของ Deliverables  
- ผู้ใช้หรือลูกค้าจะตรวจและ “เซ็นรับงาน” อย่างเป็นทางการ  
- Output = Accepted Deliverables หรือ Change Requests  
- ปัญหาที่มักพบ: **Scope Creep** → ขอบเขตขยายโดยไม่ผ่านอนุมัติ:contentReference[oaicite:9]{index=9}

---

## 6️⃣ Control Scope

- ควบคุมการเปลี่ยนแปลงในขอบเขตโครงการ  
- ใช้ **Variance Analysis** เพื่อเปรียบเทียบ Planned vs Actual  
- ข้อเสนอแนะ:
  - มีผู้ใช้ในทีมตั้งแต่ต้น  
  - สื่อสารอย่างสม่ำเสมอ  
  - บันทึก Requirements ไว้เป็นลายลักษณ์อักษร  
  - จัดการ Change Requests ด้วยระบบที่ชัดเจน:contentReference[oaicite:10]{index=10}

---

## 💻 Software & Agile Environment

| หัวข้อ | ตัวอย่าง |
|--------|-----------|
| **Software Tools** | Word, Excel, PowerPoint, MindMap, Jira |
| **Agile Scope** | ขอบเขตละเอียดถูกกำหนดในแต่ละ Iteration |
| **ผลลัพธ์ Agile** | ส่งมอบ Product ใช้งานได้จริงทุกรอบ Iteration:contentReference[oaicite:11]{index=11} |

---

## 🧾 Chapter Summary

- Scope Management ครอบคลุมการกำหนดและควบคุมงานทั้งหมดของโครงการ  
- ขั้นตอนหลัก 6 ขั้น (Plan → Collect → Define → Create → Validate → Control)  
- WBS คือหัวใจสำคัญในการวางแผนและติดตาม Scope  
- ควรมีระบบควบคุม Scope Creep ด้วยการสื่อสารและอนุมัติที่ชัดเจน:contentReference[oaicite:12]{index=12}

---

# 🧩 แบบทดสอบท้ายบท (เลือกคำตอบที่ถูกต้องเพียงข้อเดียว)

1. ข้อใดอธิบาย “Project Scope” ได้ถูกต้องที่สุด  
   - [ ] งบประมาณของโครงการทั้งหมด  
   - [X] งานทั้งหมดที่ต้องทำเพื่อสร้างผลลัพธ์ตามวัตถุประสงค์ของโครงการ  
   - [ ] ระยะเวลาโครงการ  
   - [ ] ความเสี่ยงที่เกี่ยวข้องกับการส่งมอบ  

2. เอกสารใดใช้ระบุวิธีควบคุมและตรวจสอบขอบเขตโครงการ  
   - [X] Scope Management Plan  
   - [ ] Work Breakdown Structure  
   - [ ] Risk Management Plan  
   - [ ] Communication Plan  

3. เครื่องมือที่ใช้ติดตามความต้องการของผู้ใช้แต่ละข้อคืออะไร  
   - [ ] Gantt Chart  
   - [X] Requirements Traceability Matrix (RTM)  
   - [ ] WBS Dictionary  
   - [ ] Risk Register  

4. “Deliverable” หมายถึงอะไร  
   - [X] ผลลัพธ์ที่โครงการต้องส่งมอบ เช่น เอกสารหรือระบบ  
   - [ ] งบประมาณที่ใช้ไป  
   - [ ] รายงานสถานะ  
   - [ ] KPI ของทีมงาน  

5. ขั้นตอนใดเป็นการตรวจสอบและยืนยันการรับมอบงานจากลูกค้า  
   - [ ] Control Scope  
   - [ ] Define Scope  
   - [X] Validate Scope  
   - [ ] Collect Requirements  

6. ปัญหา “Scope Creep” หมายถึงอะไร  
   - [ ] การยกเลิกโครงการก่อนเวลา  
   - [X] การขยายขอบเขตโดยไม่ได้รับอนุมัติ  
   - [ ] การควบคุมงบประมาณผิดพลาด  
   - [ ] การวางแผนไม่ครบถ้วน  

7. วิธีสร้าง WBS แบบ Top-down คือ  
   - [X] เริ่มจากงานใหญ่แล้วแตกย่อยลงเป็นงานเล็ก  
   - [ ] รวมงานเล็กเข้าด้วยกันเป็นงานใหญ่  
   - [ ] เริ่มจาก Work Package ก่อน  
   - [ ] ใช้การ Brainstorm โดยไม่จัดลำดับ  

8. เอกสารใดประกอบอยู่ใน Scope Baseline  
   - [X] Project Scope Statement, WBS, WBS Dictionary  
   - [ ] RTM, Risk Register, Gantt Chart  
   - [ ] Stakeholder Register, Budget Plan  
   - [ ] Lessons Learned Report  

9. ใน Agile Environment การกำหนดขอบเขตทำเมื่อใด  
   - [X] ก่อนเริ่มแต่ละ Iteration  
   - [ ] หลังจบทุก Sprint  
   - [ ] เมื่อโครงการเสร็จสมบูรณ์  
   - [ ] ตอนวางแผนระยะยาวเท่านั้น  

10. ข้อใดไม่ใช่เทคนิคในการเก็บ Requirements  
    - [ ] Interviews  
    - [ ] Surveys  
    - [ ] Prototyping  
    - [X] Earned Value Analysis  

---

## ✅ เฉลยท้ายบท

| ข้อ | คำตอบ | คำอธิบาย |
|-----|--------|------------|
| 1 | ✅ งานทั้งหมด | ความหมายตาม PMBOK |
| 2 | ✅ Scope Mgmt Plan | ระบุวิธีบริหารและควบคุมขอบเขต |
| 3 | ✅ RTM | ใช้ติดตาม Requirement แต่ละข้อ |
| 4 | ✅ Deliverable | ผลลัพธ์ของโครงการ |
| 5 | ✅ Validate Scope | การตรวจรับงานจากลูกค้า |
| 6 | ✅ Scope Creep | การเพิ่มขอบเขตโดยไม่ได้อนุมัติ |
| 7 | ✅ Top-down | เริ่มจากงานใหญ่ไปเล็ก |
| 8 | ✅ Scope Baseline | ชุดเอกสารหลักของ Scope |
| 9 | ✅ ก่อนเริ่ม Iteration | Agile = ปรับ Scope รายรอบ |
| 10 | ✅ Earned Value | ใช้ใน Cost Management ไม่ใช่ Scope |

---

> 💡 **Tip สำหรับสอบ:**  
> - จำลำดับ 6 ขั้นตอน “Plan – Collect – Define – Create – Validate – Control”  
> - “WBS” = แตกงาน / “RTM” = ติดตามความต้องการ / “Scope Creep” = ระวังเพิ่มงาน  
> - Agile → Scope จะละเอียดในแต่ละรอบ (Iteration)
