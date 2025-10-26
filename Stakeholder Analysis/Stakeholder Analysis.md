# 🧭 Stakeholder Analysis (แบ่งเชิงบวก–ลบ)

> Stakeholders คือบุคคลหรือหน่วยงานที่ **ได้รับผลกระทบจากระบบ**  
> ทั้งใน **เชิงบวก (Positive Stakeholders)** และ **เชิงลบ (Negative Stakeholders)**  
> การวิเคราะห์ทั้งสองฝั่งช่วยให้เข้าใจความต้องการ–ข้อกังวล และวางแผนการสื่อสารหรือแก้ปัญหาได้ตรงจุด

---

## 🧩 โครงสร้างการตอบมาตรฐาน

| หมวด | รายละเอียด |
|------|-------------|
| **Stakeholder Name / Class** | ชื่อหรือประเภทผู้มีส่วนได้ส่วนเสีย |
| **Role / Responsibility** | บทบาทและหน้าที่ต่อระบบ |
| **Impact Type** | Positive / Negative |
| **Positive Aspects (ความคาดหวัง / ประโยชน์)** | สิ่งที่ผู้มีส่วนได้ส่วนเสียจะได้รับหรือคาดหวัง |
| **Negative Aspects (ข้อกังวล / ผลกระทบ)** | ความเสี่ยง ความกลัว หรือสิ่งที่อาจเสียไป |
| **Possible Mitigation** | แนวทางลดผลกระทบหรือสร้างสมดุล |

---

## 🧠 ตัวอย่างโจทย์ที่ 1: Smart Bus Tracking System

| Stakeholder | Role | Impact | Positive Aspects | Negative Aspects | Mitigation |
|--------------|------|---------|------------------|------------------|-------------|
| **Passenger** | ใช้บริการ | Positive | เดินทางตรงเวลา, เห็นตำแหน่งรถแบบ Real-time | อาจต้องใช้สมาร์ตโฟนและอินเทอร์เน็ต | ออกแบบ UI ใช้ง่าย, รองรับ Offline Map |
| **Driver** | ขับรถ | Positive / Negative | ได้ข้อมูลเส้นทางที่ดีที่สุด | ถูกติดตามเวลาและพฤติกรรม | ตั้งนโยบายความเป็นส่วนตัวชัดเจน |
| **Transport Authority** | ผู้ควบคุมระบบ | Positive | ลดความล่าช้า, มีข้อมูลประสิทธิภาพ | ต้องรับแรงกดดันจากประชาชนเมื่อระบบล่ม | วางแผนระบบสำรองและประกาศ SLA |
| **Maintenance Team** | บำรุงรักษาอุปกรณ์ | Positive | ตรวจสอบอุปกรณ์รวดเร็ว | ภาระงานเพิ่มขึ้น | จัดตารางบำรุงอัตโนมัติ |
| **Citizen (Indirect)** | ได้ผลประโยชน์จากระบบขนส่งดีขึ้น | Positive / Negative | จราจรดีขึ้น, ลดมลพิษ | เสียงรบกวนจากเซนเซอร์, กล้อง | จำกัดพื้นที่ใช้งานอย่างเหมาะสม |

---

## 🧠 ตัวอย่างโจทย์ที่ 2: Smart Waste Separation (SmartCondo)

| Stakeholder | Role | Impact | Positive Aspects | Negative Aspects | Mitigation |
|--------------|------|---------|------------------|------------------|-------------|
| **Resident** | ผู้ใช้งานหลัก | Positive | ได้แต้มสะสม, ช่วยลดขยะ | ต้องเรียนรู้วิธีแยกขยะใหม่ | จัดทำ Learning Mode ในแอป |
| **Condo Staff** | ผู้ดูแลถัง | Positive / Negative | มีระบบดูแลสะดวก | ภาระตรวจสอบเพิ่ม | ระบบแจ้งเตือนอัตโนมัติ |
| **Condo Manager** | บริหารระบบ | Positive | ใช้รายงานเพื่อบริหาร | ต้องรับผิดชอบเมื่อระบบมีปัญหา | มี Dashboard ตรวจสอบสถานะเรียลไทม์ |
| **Recycling Company** | รับขยะรีไซเคิล | Positive | ได้ข้อมูลเรียลไทม์ | ต้องปรับระบบให้รองรับ API | ใช้มาตรฐานข้อมูลกลาง (Open API) |
| **Resident (บางกลุ่ม)** | ผู้ใช้ไม่สนใจรีไซเคิล | Negative | - | รู้สึกยุ่งยาก ไม่อยากเปลี่ยนนิสัย | ใช้แรงจูงใจจากแต้ม/รางวัล |

---

## 🧠 ตัวอย่างโจทย์ที่ 3: Smart Hospital Appointment System

| Stakeholder | Role | Impact | Positive Aspects | Negative Aspects | Mitigation |
|--------------|------|---------|------------------|------------------|-------------|
| **Patient** | ผู้รับบริการ | Positive | จองคิวง่าย, ลดเวลารอ | ใช้เทคโนโลยีไม่คล่อง | มีเจ้าหน้าที่ช่วยในจุดบริการ |
| **Doctor** | ผู้ให้บริการ | Positive / Negative | ตารางตรวจเป็นระบบ | เวลานัดแน่น, ต้องอัปเดตข้อมูลตลอด | ระบบซิงค์อัตโนมัติ |
| **Nurse / Staff** | ผู้จัดการคิว | Negative | - | ต้องเปลี่ยนวิธีทำงาน | อบรมการใช้ระบบก่อนใช้งานจริง |
| **Hospital IT** | ฝ่ายดูแลระบบ | Positive | ระบบเสถียร, เก็บ log ง่าย | ภาระงานบำรุงรักษาเพิ่ม | ตั้ง alert และ automation |
| **Ministry of Health** | หน่วยงานกำกับ | Positive | ใช้ข้อมูลเพื่อวิเคราะห์นโยบายสุขภาพ | ต้องมั่นใจความปลอดภัยข้อมูล | ใช้มาตรฐาน HL7/FHIR และ PDPA Compliance |

---

## 🧠 ตัวอย่างโจทย์ที่ 4: Smart Airport Baggage Tracking

| Stakeholder | Role | Impact | Positive Aspects | Negative Aspects | Mitigation |
|--------------|------|---------|------------------|------------------|-------------|
| **Passenger** | ผู้ใช้บริการ | Positive | มั่นใจว่ากระเป๋าไม่หาย | กังวลข้อมูลส่วนตัวจาก Tag | แจ้งนโยบายข้อมูลส่วนตัวชัดเจน |
| **Airline Staff** | ผู้โหลดกระเป๋า | Negative | - | ถูกตรวจสอบผลงานอย่างละเอียด | มีระบบ feedback สองทาง |
| **Airport Authority** | ควบคุมระบบ | Positive | ลดการร้องเรียน | ต้นทุนติดตั้งสูง | ใช้ระบบ pilot ก่อนเต็มรูปแบบ |
| **Security Team** | ผู้ตรวจสอบความปลอดภัย | Positive | ตรวจสอบง่ายขึ้น | ต้องเชื่อมระบบใหม่ | ฝึกอบรมใช้งานระบบ |

---

## 🧭 วิธีการวิเคราะห์เพิ่มเติม

### 1️⃣ Stakeholder Mapping (Positive vs Negative)

| กลุ่ม | ลักษณะ | ตัวอย่าง |
|--------|----------|-----------|
| **Positive Stakeholders** | สนับสนุนระบบ / ได้รับประโยชน์ | End-user, Manager, Regulator |
| **Negative Stakeholders** | รู้สึกเสียผลประโยชน์ / ต่อต้านการเปลี่ยนแปลง | พนักงานเดิม, ผู้รับจ้างภายนอก, ผู้ที่สูญเสียอำนาจ |
| **Neutral Stakeholders** | ไม่กระทบโดยตรงแต่มีส่วนสังเกต | สาธารณชน, กลุ่มวิชาการ |

---

### 2️⃣ Stakeholder Conflict Analysis

| Conflict Type | ตัวอย่าง | แนวทางแก้ไข |
|----------------|------------|--------------|
| Goal Conflict | ผู้บริหารต้องการลดงบ แต่ผู้ใช้ต้องการฟังก์ชันเพิ่ม | ประชุมเจรจาและใช้ MoSCoW Prioritization |
| Process Conflict | ฝ่ายปฏิบัติกลัวระบบใหม่ยุ่งยาก | Prototype และฝึกใช้งาน |
| Value Conflict | ผู้ใช้ต้องการความสะดวก แต่ฝ่ายความปลอดภัยต้องการเข้มงวด | ใช้ Balance Policy: UX + Security |

---

### 3️⃣ Power–Interest Grid (เชิงบวก–ลบผสม)
| กลุ่ม | ตัวอย่าง | การจัดการ |
|--------|-----------|-------------|
| **High Power / Positive** | ผู้บริหาร, รัฐบาล | รักษาความสัมพันธ์ |
| **High Power / Negative** | ฝ่ายต่อต้านการเปลี่ยนระบบ | สื่อสารโปร่งใส, ให้มีส่วนร่วม |
| **Low Power / Positive** | ผู้ใช้ทั่วไป | ให้ Feedback สม่ำเสมอ |
| **Low Power / Negative** | ผู้ใช้ไม่สนใจ | ใช้ Incentive เช่น คะแนนสะสม |

---

## 🧩 แนวข้อสอบที่มักออก

### 🔹 ข้อเขียน
- ยกตัวอย่าง Stakeholder ทั้งเชิงบวกและลบของระบบ Smart City  
- อธิบายผลกระทบเชิงบวกและลบของ Stakeholder ต่อระบบ  
- วิเคราะห์ความขัดแย้งระหว่าง Stakeholder สองฝ่ายและแนวทางแก้ไข  

### 🔹 ข้อวิเคราะห์
- เขียนตาราง Stakeholder Analysis สำหรับระบบที่กำหนด  
- จัดกลุ่ม Stakeholder ด้วย Power–Interest Grid และวิเคราะห์ผลกระทบ  
- เสนอแนวทางลดผลกระทบเชิงลบจาก Stakeholder ที่มีอิทธิพลสูง  

---

📚 **อ้างอิง**
- Nakornthip Phromphoo, *Lesson 3 – Requirements Elicitation (2024)*:contentReference[oaicite:2]{index=2}  
- Dennis, Wixom, & Tegarden, *Systems Analysis and Design with UML, 4th Ed.*:contentReference[oaicite:3]{index=3}  
- ISO/IEC/IEEE 29148:2011 – *Systems and Software Engineering — Requirements Engineering*  

✍️ *Prepared by Aphirak P. — Stakeholder Analysis for Exam & Project Use*
