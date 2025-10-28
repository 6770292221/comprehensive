# 📘 Function Point Analysis (FPA) — Software Cost Estimation Summary

> อ้างอิง: Chapter 7 Project Cost Management, Information Technology Project Management (9th Edition)  
> ผู้เรียบเรียง: Twittie Senivongse (ed.)

---

## 🎯 จุดประสงค์ของ Function Point Analysis (FPA)

**Function Point Analysis (FPA)** คือวิธีการวัด *ขนาดเชิงตรรกะ (Logical Size)* ของซอฟต์แวร์  
เพื่อใช้ในการ **ประมาณต้นทุน (Effort & Cost Estimation)** โดยไม่ขึ้นกับภาษา Programming ที่ใช้

> ✅ เหมาะสำหรับคำนวณ “จำนวนงาน” ที่ระบบต้องทำ — ก่อนจะมีโค้ดจริง

---

## 💡 แนวคิดสำคัญ

- FPA วัดจาก **ฟังก์ชันที่ผู้ใช้เห็นและใช้งานได้** (User-Visible Functions)  
- ไม่วัดจาก Line of Code (LOC) โดยตรง แต่ใช้ค่า LOC ต่อ Function Point ภายหลังเพื่อแปลงเป็น KLOC (Backfiring)
- ใช้ในการเปรียบเทียบ / วิเคราะห์ความซับซ้อนของระบบหลายระบบได้

---

## 🧩 องค์ประกอบ 5 ประเภทของ FPA

| หมวด | ชื่อเต็ม | ประเภทข้อมูล | ตัวอย่าง |
|-------|-----------|---------------|-----------|
| **EI** | External Input | ข้อมูลที่ผู้ใช้ป้อนเข้าระบบ | แบบฟอร์ม, ปุ่ม Add/Delete |
| **EO** | External Output | ข้อมูลที่ระบบประมวลผลและส่งออก | รายงาน, ข้อความแจ้งเตือน |
| **EQ** | External Inquiry | การสืบค้น / รายงานผลโดยไม่เปลี่ยนข้อมูล | ค้นหาลูกค้า, Dropdown list |
| **ILF** | Internal Logical File | ข้อมูลที่จัดเก็บภายในระบบ | ตาราง Customer, Order |
| **EIF** | External Interface File | ข้อมูลจากระบบภายนอก | ไฟล์ Tax Service, API Exchange |

> 🔸 3 ตัวแรก (EI, EO, EQ) คือ “Transaction Functions”   
> 🔹 2 ตัวหลัง (ILF, EIF) คือ “Data Functions”

---

## 🧮 วิธีให้คะแนน Function Point

1. **นับจำนวน DET (Data Element Type)**  
   → จำนวน field, ข้อความ, ปุ่ม, error message ฯลฯ  
2. **นับ FTR (File Type Referenced)** หรือ **RET (Record Element Type)**  
   → จำนวนไฟล์หรือ table ที่เกี่ยวข้อง  
3. **กำหนดระดับ Low / Average / High**  
   ตามตารางมาตรฐาน (IFPUG) และแปลงเป็นคะแนน FP เชิงตัวเลข  
   เช่น Low = 3, Average = 4, High = 6 (ขึ้นอยู่กับประเภท function)

---

## 📊 ตัวอย่าง การคำนวณ เบื้องต้น

| ประเภท | DET | FTR / RET | ระดับ | ค่า FP |
|----------|------|------------|---------|---------|
| EI (แบบฟอร์มลูกค้า) | 12 | 1 | Low | 3 |
| EO (รายงานยอดขาย) | 7 | 2 | Average | 5 |
| EQ (ค้นหาประชากร รัฐ) | 4 | 1 | Low | 3 |
| ILF (Customer DB) | 18 DET / 3 RET | – | Low | 7 |
| EIF (Tax data) | 20 DET / 1 RET | – | Low | 5 |

> 🔹 รวมคะแนน FP ทั้งสิ้น = **3 + 5 + 3 + 7 + 5 = 23 Unadjusted Function Points**

---

## ⚙️ การปรับคะแนน (Function Point Adjustment)

ใช้ **Value Adjustment Factor (VAF)** คำนวณจาก **14 General System Characteristics (GSCs)** เช่น Data Communication, Performance, Reusability ฯลฯ  
ให้คะแนน 0 – 5 แล้วรวมผลรวม ΣFi เพื่อนำมาปรับ FP

\[
VAF = 0.65 + 0.01 \times \Sigma Fi \quad (ค่าปกติอยู่ในช่วง 0.65 – 1.35)
\]
\[
\text{Adjusted FP} = \text{Unadjusted FP} \times VAF
\]

ตัวอย่าง:  
ΣFi = 30 → VAF = 0.65 + 0.3 = 0.95  
→ Adjusted FP = 23 × 0.95 = **21.85 FP**

---

## 🔢 การแปลง Function Point เป็น KLOC (Backfiring)

ใช้ค่า **Gearing Factor** ของภาษา โปรแกรม (จาก QSM table)

| ภาษา | LOC / FP โดยเฉลี่ย |
|--------|-------------------|
| Java | 53 |
| C++ | 55 |
| Python | 42 |
| SQL | 13 |

\[
KLOC = (FP \times \text{Gearing Factor}) / 1000
\]

เช่น 21.85 FP สำหรับ Java  
→ KLOC = (21.85 × 53) / 1000 = **1.16 KLOC**

---

## 📈 การใช้ FPA ใน Cost Estimation

1. หาค่า Function Point ของระบบ  
2. แปลงเป็น KLOC หรือ Person-Month ตามประสิทธิภาพเฉลี่ย  
3. ใช้โมเดลเช่น COCOMO คำนวณ Effort / Cost  
4. นำไปใช้ในการวางแผน Resource และ Schedule

---

## 🧠 แนวข้อสอบ / คำถามที่พบบ่อย

| คำถาม | คำตอบ |
|--------|--------|
| จุดประสงค์ของ Function Point Analysis ค
