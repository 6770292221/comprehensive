# 📘 Lesson 5: Business Process and Functional Modeling  
**รายวิชา:** 2110623 – วิศวกรรมความต้องการซอฟต์แวร์ (Software Requirements Engineering)  
**ผู้สอน:** ผศ. ดร. นครทิพย์ พร้อมพูล  
**ภาควิชา:** วิศวกรรมคอมพิวเตอร์ คณะวิศวกรรมศาสตร์ จุฬาลงกรณ์มหาวิทยาลัย  

---

## 🎯 วัตถุประสงค์ของบทเรียน
- เข้าใจขั้นตอนการระบุ **กระบวนการทางธุรกิจ (Business Processes)** และ **Use Cases**  
- เข้าใจวิธีสร้าง **Use-Case Diagram** และ **Use-Case Description**  
- เข้าใจหลักการสร้าง **Activity Diagram** เพื่อจำลองกระบวนการทางธุรกิจ  
- สามารถสร้าง **Functional Model** ที่ประกอบด้วย Use Case Diagram, Use Case Description และ Activity Diagram  
- เข้าใจหลัก **Verification & Validation** ของโมเดลเชิงฟังก์ชัน  

---

## 🧩 ความหมายของ Functional Model
- เป็น **แบบจำลองเชิงตรรกะ (Logical Model)** ที่อธิบาย “สิ่งที่ระบบต้องทำ” โดยไม่ขึ้นกับวิธีการพัฒนา  
- ใช้แปลง “Requirements” ให้อยู่ในรูปแบบที่ชัดเจนและเป็นระบบ  
- ประกอบด้วย 3 องค์ประกอบหลัก  
  1. **Use-Case Diagram**  
  2. **Use-Case Description**  
  3. **Activity Diagram**  

---

## 🧱 Use Case (กรณีการใช้งาน)
- เป็น **ตัวขับเคลื่อนหลักของ UML**  
- แสดง “สิ่งที่ผู้ใช้ทำได้” และ “ระบบตอบสนองอย่างไร”  
- แต่ละ Use Case = 1 ฟังก์ชันหลักของระบบ  
- ใช้ทั้งในขั้นตอนออกแบบ การสื่อสารกับผู้ใช้ และการทดสอบ  

---

## 🧭 ขั้นตอนการสร้าง Use-Case Diagram
1. ทบทวนเอกสารความต้องการ (Requirement Definition)  
2. ระบุขอบเขตของระบบ (System Boundary)  
3. ระบุ **Actors หลัก** และเป้าหมายของแต่ละคน  
4. ระบุ **Business Processes / Major Use Cases**  
5. ตรวจสอบและปรับโครงสร้างให้เหมาะสม (แยกหรือรวม)  
6. วาด Actors และ Use Cases  
7. เชื่อมความสัมพันธ์ระหว่าง Actors ↔ Use Cases  

---

## 🧍‍♂️ ประเภทของ Actor (4 ประเภท)
| ประเภท | คำอธิบาย | ตัวอย่าง |
|----------|-------------|-----------|
| **Primary Business Actor** | ผู้ได้รับประโยชน์หลักจาก Use Case | พนักงานได้รับเงินเดือน |
| **Primary System Actor** | ผู้ใช้งานที่โต้ตอบกับระบบโดยตรง | Teller กรอกข้อมูลฝากเงิน |
| **External Server Actor** | ระบบภายนอกที่ตอบสนองต่อคำขอ | ระบบตรวจสอบเครดิตบูโร |
| **External Receiver Actor** | ผู้รับข้อมูลหรือผลลัพธ์จากระบบ | คลังสินค้ารับใบส่งของ |

---

## 🧮 การจำแนก Use Case ตามระดับ (Cockburn’s Model)

| ระดับ | ชื่อเรียก | ลักษณะ | ตัวอย่าง |
|--------|------------|----------|-----------|
| Level 1 | **Summary / Cloud / Kite** | ระดับองค์กรหรือหน่วยธุรกิจ | “ขายสินค้าให้ลูกค้า” |
| Level 2 | **User Goal / Sea Level** | กิจกรรมของผู้ใช้ 2–20 นาที | “เพิ่มลูกค้าใหม่”, “ชำระเงิน” |
| Level 3 | **Subfunction / Fish / Clam** | รายละเอียดระดับฟังก์ชันย่อย | “เข้าสู่ระบบ”, “ตรวจสอบรหัสผ่าน” |

---

## 🔗 ความสัมพันธ์ระหว่าง Use Cases
| ความสัมพันธ์ | ความหมาย | ตัวอย่าง |
|----------------|-----------|-----------|
| **Include** | Base Case ต้องเรียก Use Case อื่นทุกครั้ง | “Update Grade” → *Include* “Verify Student ID” |
| **Extend** | เป็นฟังก์ชันเสริม (Optional) | “Make Appointment” → *Extend* “Payment Arrangement” |
| **Generalization** | ใช้แนวคิด inheritance | “Place Order” → “Place Internet Order” / “Phone Order” |

---

## 🧠 โครงสร้างของ Use-Case Description

**1. Overview Section**  
- Name (ชื่อ)  
- ID Number  
- Type (Overview / Detail, Essential / Real)  
- Primary Actor  
- Brief Description  
- Importance Level  
- Stakeholders  
- Trigger (External / Temporal)

**2. Relationship Section**  
- Association, Include, Extend, Generalization  

**3. Flow of Events**  
- Normal Flow  
- Sub-flows  
- Alternate / Exception Flows  

**4. Optional Characteristics**  
- Complexity, Time, Preconditions, Postconditions, Constraints

---

## 🧾 วิธีเขียน Use Case Description ที่ดี
- ใช้รูปประโยค **Subject–Verb–Object (SVO)**  
- เขียนจากมุมมองผู้สังเกตกลาง ไม่ใช่ระบบหรือผู้ใช้  
- ใช้ **KISS Principle** (Keep It Simple & Short)  
- หากขั้นตอนยาวเกินไป → แยกเป็น Sub-flow หรือ Use Case ย่อย  
- ตรวจสอบกับผู้ใช้และทีม dev เพื่อยืนยันความถูกต้อง  
- ใช้ include/extend/generalization อย่างเหมาะสม  

---

## ⚙️ Business Process Modeling (BPM)
- คือการจำลอง **ลำดับกิจกรรมทางธุรกิจ (Workflows)** ที่เกิดขึ้นจริงในองค์กร  
- ใช้ **Activity Diagram (UML)** เพื่ออธิบายขั้นตอนการทำงาน  
- ใช้ได้ทั้งระดับสูง (ข้ามหลาย Use Case) และระดับย่อย (Use Case เดียว)

---

## 🧩 สัญลักษณ์ใน Activity Diagram

| สัญลักษณ์ | ความหมาย |
|-------------|------------|
| ● จุดเริ่มต้น (Start Node) |
| ⬛ จุดสิ้นสุด (Final Node / Final Flow Node) |
| ➡️ ลูกศร | แสดงลำดับการไหล (Control Flow) |
| ◆ Decision / Merge | จุดตัดสินใจ / รวมเส้นทาง |
| ╱╲ Fork / Join | การแยกหรือรวมเส้นทางขนาน |
| ⬜ Activity / Action | กิจกรรมในกระบวนการ |
| 🧍 Swimlane | แบ่งตามบทบาทหรือหน่วยงาน |

> **หลักการวาด:**  
> - ใช้ชื่อกิจกรรมเป็น “Verb + Noun” เช่น *Approve Request*  
> - เส้นทางต้องไม่ไขว้กันมาก  
> - ทุก decision ต้องมี merge node คู่กัน  

---

## ✅ ขั้นตอนการสร้าง Activity Diagram
1. เลือก Business Process ที่ระบุไว้ใน Use Case  
2. ศึกษาเอกสาร Requirements / Use Case Description  
3. ระบุชุดกิจกรรมหลัก  
4. กำหนด **Control Flow / Object Flow**  
5. ระบุจุดตัดสินใจ (Decision Node)  
6. ระบุความเป็นขนาน (Parallel Activities)  
7. วาด Diagram ให้เส้นทางชัดเจนและเข้าใจง่าย  

---

## 🧪 Verification & Validation (V&V)
| ประเภท | คำอธิบาย |
|----------|-----------|
| **Verification** | ตรวจสอบว่าระบบ “สร้างได้ตรงตามสเปก” — *Are we building the system right?* |
| **Validation** | ตรวจสอบว่าระบบ “ตรงตามความต้องการจริง” — *Are we building the right system?* |

**รูปแบบการตรวจสอบ:**  
- ใช้ Walkthrough (การทบทวนร่วม) ระหว่างทีมพัฒนาและผู้ใช้  
- มี **Facilitator**, **Presenter**, **Recorder** ในการประชุม  

---

## 🧩 กฎสำหรับการตรวจสอบโมเดล (V&V Rules)

1. แต่ละ Use Case ต้องมี Use Case Description เพียง 1 ชุด  
2. Actors ใน Description ต้องปรากฏใน Diagram  
3. Stakeholders อาจอยู่ใน Diagram (ขึ้นอยู่กับนโยบาย)  
4. เหตุการณ์ใน Description ต้องสอดคล้องกับ Activity Diagram  
5. วัตถุที่ใช้ใน Activity ต้องปรากฏใน Use Case Description  
6. ลำดับเหตุการณ์ใน Use Case = ลำดับกิจกรรมใน Activity  
7. ความสัมพันธ์ (Include/Extend/Generalization) ต้องสอดคล้องกัน  
8. Diagram ทั้งหมดต้องเป็นไปตาม Syntax & Semantics ของ UML  

---

## 🧾 ตัวอย่าง Requirements

### 🟩 Functional Requirements
1. **Schedule Appointment**  
   - ระบบรับคำขอนัดหมายจากลูกค้า  
   - แสดงรายการบริการ  
   - อนุญาตให้ลูกค้าเลือกเวลา  
   - อัปเดตตารางและส่งการยืนยัน  

2. **Communicate Real-time**  
   - ลูกค้าร้องขอการพูดคุยแบบเรียลไทม์  
   - ผู้ดูแลตอบกลับด้วยช่วงเวลาและความพร้อม  

3. **Tele-health Assessment**  
   - ระบบให้ลูกค้าตอบแบบสอบถาม  
   - วิเคราะห์เบื้องต้นและนัดหมาย video conference หากจำเป็น  

### 🟦 Non-Functional Requirements
| ประเภท | ตัวอย่าง |
|----------|------------|
| **Operational** | ทำงานได้บน web/mobile, เชื่อมระบบเดิม |
| **Performance** | ตอบสนอง < 3 วินาที, เก็บข้อมูลทุก 2 วินาที |
| **Security** | จำกัดสิทธิ์เข้าถึงเฉพาะบุคลากรทางการแพทย์ |
| **Cultural/Political** | ปฏิบัติตามกฎหมาย HIPAA / กฎระเบียบสาธารณสุข |

---

## 🧠 แนวคำถาม–คำตอบ (พร้อมเฉลย)

| # | คำถาม | เฉลย |
|---|--------|-------|
| 1 | Functional Model ประกอบด้วยอะไรบ้าง | Use Case Diagram, Use Case Description, Activity Diagram |
| 2 | Use Case คืออะไร | การอธิบายฟังก์ชันที่ผู้ใช้โต้ตอบกับระบบ |
| 3 | ประเภทของ Actor มีกี่แบบ | 4 แบบ: Business, System, Server, Receiver |
| 4 | ระดับของ Use Case มีอะไรบ้าง | Summary (Cloud/Kite), User Goal (Sea), Subfunction (Fish/Clam) |
| 5 | ความสัมพันธ์ Include กับ Extend ต่างกันอย่างไร | Include = ส่วนบังคับ, Extend = ส่วนเสริม |
| 6 | Trigger ของ Use Case หมายถึงอะไร | เหตุการณ์ที่ทำให้ Use Case เริ่มต้น เช่น ผู้ใช้โทรจองเวลา |
| 7 | Activity Diagram ใช้เพื่ออะไร | แสดงลำดับกิจกรรมของกระบวนการทางธุรกิจ |
| 8 | Swimlane ใช้เพื่ออะไร | แสดงการแบ่งบทบาท/หน่วยงานในกิจกรรม |
| 9 | Verification ต่างจาก Validation อย่างไร | Verification = ถูกต้องตามสเปก, Validation = ตรงความต้องการผู้ใช้ |
| 10 | ขั้นตอนการตรวจสอบโมเดลมีอะไรบ้าง | ตรวจสอบลำดับ, ความสัมพันธ์, ความสอดคล้องของ Actor–Activity |
| 11 | Functional Requirement คืออะไร | สิ่งที่ระบบ “ต้องทำ” เพื่อให้ตอบโจทย์การใช้งาน |
| 12 | Non-Functional Requirement คืออะไร | คุณภาพของระบบ เช่น ความเร็ว ความปลอดภัย ความเสถียร |
| 13 | กฎสำคัญของ Use Case คืออะไร | 1 Use Case มี Description เดียว |
| 14 | การ Walkthrough คืออะไร | การประชุมตรวจสอบโมเดลร่วมระหว่าง dev และลูกค้า |
| 15 | ทำไมต้องทำ BPM ก่อนออกแบบระบบ | เพื่อเข้าใจกระบวนการจริงและกำหนด Use Case ที่ตรงจุด |

---

## 💡 เคล็ดจำก่อนสอบ
| หัวข้อ | เทคนิคจำ |
|---------|------------|
| ส่วนประกอบของ Functional Model | **U–U–A** → Use Case Diagram, Use Case Description, Activity Diagram |
| ความสัมพันธ์ Use Case | **I–E–G** → Include, Extend, Generalization |
| ตรวจสอบโมเดล | **8 กฎ V&V** จำคู่ Actor–Activity–Flow |
| โมเดล BPM | ใช้ Activity Diagram + Swimlane |
| ระดับ Use Case | **Cloud–Sea–Fish** (จากกว้างไปแคบ) |

---

## 📚 แหล่งอ้างอิง
- Dennis, Wixom, & Tegarden (2012), *System Analysis and Design with UML (4th Ed.)*  
- Sommerville (2015), *Software Engineering*  
- ISO/IEC/IEEE 29148: Systems and Software Requirements  
- Chulalongkorn University – 2110623 Software Requirements Engineering Lecture Notes  

---

> 🧭 **สรุปสั้นจำง่าย:**  
> Functional Model = Use Case + Activity Diagram + Verification & Validation  
> แก่นสำคัญของบทนี้คือ “เข้าใจระบบผ่านมุมมองของผู้ใช้” ก่อนจะออกแบบหรือเขียนโค้ด ✅
