# 📘 Chapter 6: Project Schedule Management

> แหล่งที่มา: *Information Technology Project Management (9th Edition)*  
> เรียบเรียงโดย Twittie Senivongse (ed.)  
> “เวลาเป็นทรัพยากรที่ไม่สามารถเพิ่มได้ — Schedule คือหัวใจของความสำเร็จของโครงการ”

---

## 🎯 Learning Objectives

1. อธิบายความสำคัญของการจัดการตารางเวลา (Schedule Management)  
2. ระบุ 6 กระบวนการใน Project Schedule Management  
3. ใช้เครื่องมือในการกำหนดลำดับกิจกรรม (Network Diagram)  
4. คำนวณค่า Duration, Float, Critical Path และ PERT  
5. อธิบายแนวคิด Critical Chain Scheduling และ Schedule Control  
6. อธิบายบทบาทของซอฟต์แวร์และ Agile ต่อการจัดการเวลา

---

## 🧩 6 กระบวนการหลักของ Schedule Management

| # | Process | Output สำคัญ |
|---|----------|----------------|
| 1️⃣ | **Plan Schedule Management** | Schedule Management Plan |
| 2️⃣ | **Define Activities** | Activity List / Attributes / Milestone List |
| 3️⃣ | **Sequence Activities** | Network Diagram |
| 4️⃣ | **Estimate Activity Durations** | Duration Estimate |
| 5️⃣ | **Develop Schedule** | Gantt Chart / CPM / Baseline |
| 6️⃣ | **Control Schedule** | Work Performance Data / Change Requests |

---

## 🕓 1️⃣ Plan Schedule Management
วางแผนการสร้างและควบคุมตารางเวลา โดยกำหนด:
- ระดับความละเอียดและหน่วยเวลา (เช่น ชั่วโมง, วัน)
- Variance Threshold (เช่น ±10%)
- วิธีรายงานสถานะ
- Format ของรายงาน (เช่น Weekly Gantt)
- วิธีประเมิน % ความคืบหน้า:contentReference[oaicite:1]{index=1}

---

## 🧱 2️⃣ Define Activities

- ระบุ “กิจกรรม (Activities)” ที่ต้องทำเพื่อให้เกิด Deliverables ตาม WBS  
- สร้าง **Activity List** และ **Activity Attributes** (Predecessor, Successor, Lead/Lag, Resource, Constraint)
- **Milestone** = เหตุการณ์สำคัญ ไม่มี Duration  
  เช่น “Sign-off document” หรือ “Go-live”:contentReference[oaicite:2]{index=2}

---

## 🔗 3️⃣ Sequence Activities

จัดลำดับก่อน-หลังของกิจกรรมด้วย **Network Diagram**
- **ประเภทของ Dependency**
  - **Mandatory (Hard Logic)** เช่น “Testing หลัง Coding”
  - **Discretionary (Soft Logic)** เช่น “Design หลัง User Sign-off”
  - **External** เช่น “Install หลังส่งมอบ Hardware”
  - **Internal** เช่น “System Test หลัง Unit Test”

### 📘 รูปแบบ Diagram
| แบบ | ชื่อเต็ม | ลักษณะ |
|------|-----------|----------|
| ADM | Activity-on-Arrow (AOA) | ใช้ลูกศรแทนกิจกรรม |
| PDM | Activity-on-Node (AON) | ใช้กล่องแทนกิจกรรม (นิยมที่สุด):contentReference[oaicite:3]{index=3} |

---

## ⏳ 4️⃣ Estimate Activity Durations

- **Duration** = เวลาทั้งหมดที่ใช้รวมเวลารอ  
- **Effort** = จำนวนชั่วโมง/วันทำงานจริง (ไม่เท่ากับ Duration)  
- ใช้ **Three-point Estimate** → Optimistic (O), Most Likely (M), Pessimistic (P)
  
📘 **สูตร PERT Weighted Average:**
> \( TE = (O + 4M + P) / 6 \)  
> ใช้คำนวณเวลาเฉลี่ยเมื่อมีความไม่แน่นอนสูง:contentReference[oaicite:4]{index=4}:contentReference[oaicite:5]{index=5}

---

## 📅 5️⃣ Develop Schedule

นำข้อมูลจากขั้นตอนก่อนหน้ามาสร้างตารางเวลาที่สมจริง  
**เครื่องมือหลัก:**
1. **Gantt Chart** – แสดงกิจกรรม + วันที่เริ่ม/สิ้นสุด  
   - 🔹 Diamond = Milestone  
   - 🔹 Thick Bar = Summary Task  
   - 🔹 Arrow = Dependency  
2. **Tracking Gantt** – เปรียบเทียบ Planned vs Actual  
3. **Critical Path Method (CPM)** – หาลำดับกิจกรรมที่ยาวที่สุด (เวลารวมมากสุด)  
4. **PERT** – ใช้ความน่าจะเป็นของเวลา (Optimistic, Likely, Pessimistic)  
5. **Critical Chain** – พิจารณาทรัพยากรจำกัดและใช้ Buffer ป้องกันความล่าช้า:contentReference[oaicite:6]{index=6}

---

### 🧮 CPM Concepts
| Term | Meaning | Formula |
|------|----------|----------|
| **ES** | Early Start | เริ่มเร็วสุด |
| **EF** | Early Finish | ES + Duration |
| **LS** | Late Start | LF - Duration |
| **LF** | Late Finish | จบช้าที่สุดโดยไม่ล่าช้า |
| **TS (Total Slack)** | เวลาที่กิจกรรมจะเลื่อนได้โดยไม่กระทบโครงการ | TS = LS - ES |
| **FS (Free Slack)** | เลื่อนโดยไม่กระทบงานถัดไป | FS = min(ES next) - (ES + Duration) |

🧠 **Critical Path = เส้นทางที่ TS = 0**

---

### ⚡ Schedule Compression Techniques
- **Crashing:** เพิ่มทรัพยากรเพื่อย่นเวลา (เพิ่มค่าใช้จ่าย)
- **Fast Tracking:** ทำกิจกรรมบางส่วนพร้อมกัน
- **Resource Leveling:** กระจายทรัพยากรเพื่อหลีกเลี่ยง Overload:contentReference[oaicite:7]{index=7}:contentReference[oaicite:8]{index=8}

---

## 🧱 6️⃣ Control Schedule

เป้าหมายคือ “รู้สถานะเวลา” และ “จัดการการเปลี่ยนแปลงได้”  
เครื่องมือที่ใช้:
- Earned Value Analysis (ดู Ch.7)
- Iteration Burndown Chart (Agile)
- Critical Path / Schedule Compression
- PMIS Software (Microsoft Project, Jira)
- Resource Optimization:contentReference[oaicite:9]{index=9}

---

## 🔗 Critical Chain Scheduling

- ใช้แนวคิด **Theory of Constraints (TOC)**  
- ลดการ Multitasking และเพิ่ม Focus
- ใช้ **Buffers** เพื่อป้องกันความล่าช้า:
  - **Project Buffer** → ท้าย Critical Chain  
  - **Feeding Buffer** → เชื่อม Non-critical → Critical Chain  
  - **Resource Buffer** → สำรองทรัพยากรสำคัญ
- ป้องกัน **Parkinson’s Law** (“งานขยายเต็มเวลา”) และ **Student Syndrome** (“เริ่มงานช้า”):contentReference[oaicite:10]{index=10}

---

## ⚙️ Agile & Adaptive Environment

- ไม่เน้นการคาดการณ์เวลารวมของโครงการ  
- ใช้ “Iteration” หรือ “Sprint” แทน Gantt Chart  
- ประมาณงานด้วย **Story Points**  
- ทีมเลือกงานให้เหมาะกับเวลาในแต่ละรอบ (Time-boxed):contentReference[oaicite:11]{index=11}

---

## 🧾 Chapter Summary

- กระบวนการสำคัญ: Plan – Define – Sequence – Estimate – Develop – Control  
- เครื่องมือหลัก: Gantt, Network Diagram, CPM, PERT, Critical Chain  
- คำสำคัญ: Slack, Duration, Dependency, Buffer  
- การอัปเดต Critical Path อย่างสม่ำเสมอคือสิ่งจำเป็นที่สุด

---

# 🧩 แบบทดสอบท้ายบท

1. ข้อใดคือกระบวนการแรกของ Project Schedule Management  
   - [X] Plan Schedule Management  
   - [ ] Define Activities  
   - [ ] Sequence Activities  
   - [ ] Control Schedule  

2. เอกสารใดระบุรายละเอียดของกิจกรรม เช่น Lead/Lag และ Resource  
   - [ ] Activity List  
   - [X] Activity Attributes  
   - [ ] WBS Dictionary  
   - [ ] Milestone List  

3. ข้อใดไม่ใช่ประเภทของ Dependency  
   - [ ] Mandatory  
   - [ ] Discretionary  
   - [X] Sequential  
   - [ ] External  

4. กิจกรรมที่ไม่มี Duration เรียกว่าอะไร  
   - [X] Milestone  
   - [ ] Work Package  
   - [ ] Activity  
   - [ ] Buffer  

5. ถ้า TS = 0 หมายถึงอะไร  
   - [X] เป็น Critical Activity  
   - [ ] มีเวลาเหลือ  
   - [ ] ล่าช้าได้บางส่วน  
   - [ ] ไม่อยู่ใน Critical Path  

6. สูตรคำนวณค่าเวลาเฉลี่ยของ PERT คือ  
   - [ ] (O + M + P)/3  
   - [X] (O + 4M + P)/6  
   - [ ] (O + 2M + P)/4  
   - [ ] (O + P)/2  

7. วิธีใดย่นระยะเวลาโดยการทำงานคู่ขนาน  
   - [ ] Crashing  
   - [X] Fast Tracking  
   - [ ] Leveling  
   - [ ] Buffering  

8. Critical Chain ต่างจาก Critical Path อย่างไร  
   - [X] พิจารณาทรัพยากรและเพิ่ม Buffer  
   - [ ] ใช้เวลาเฉลี่ยจาก PERT  
   - [ ] ไม่คำนวณ Float  
   - [ ] ใช้เฉพาะใน Agile  

9. ใน Agile Project การจัดตารางเวลาเน้นอะไร  
   - [ ] Gantt Chart รายปี  
   - [ ] Network Diagram  
   - [X] Time-boxed Iteration และ Story Points  
   - [ ] CPM  

10. เครื่องมือใดใช้ควบคุมความคืบหน้าของแผนเวลา  
    - [ ] Gantt Chart  
    - [ ] Activity List  
    - [X] Tracking Gantt / Burndown Chart  
    - [ ] Scope Baseline  

---

## ✅ เฉลยท้ายบท

| ข้อ | คำตอบ | คำอธิบาย |
|-----|--------|-----------|
| 1 | ✅ Plan | ขั้นแรกคือการวางแผนการบริหารเวลา |
| 2 | ✅ Activity Attributes | เก็บข้อมูล Lead, Lag, Resource |
| 3 | ✅ Sequential | ไม่ใช่ประเภท Dependency |
| 4 | ✅ Milestone | ไม่มี Duration ใช้กำหนดจุดสำคัญ |
| 5 | ✅ Critical | TS=0 หมายถึงอยู่ใน Critical Path |
| 6 | ✅ (O+4M+P)/6 | สูตร PERT |
| 7 | ✅ Fast Tracking | ทำงานคู่ขนาน |
| 8 | ✅ Critical Chain | เพิ่ม Buffer และพิจารณาทรัพยากร |
| 9 | ✅ Time-boxed | Agile เน้น Iteration |
| 10 | ✅ Tracking Gantt | ใช้ควบคุมและตรวจสอบความคืบหน้า |

---

> 💡 **Tips สำหรับสอบ**
> - จำ 6 ขั้นตอน: Plan → Define → Sequence → Estimate → Develop → Control  
> - CPM → เส้นทางยาวที่สุด (TS=0)  
> - PERT → (O+4M+P)/6  
> - Fast Track = ทำขนาน, Crash = เพิ่มทรัพยากร  
> - Agile → ใช้ Story Points, Time-boxed Iteration
``
