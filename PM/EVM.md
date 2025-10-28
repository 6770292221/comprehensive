# 📘 Earned Value Analysis (EVA) — Project Cost Management Summary

> แหล่งอ้างอิง: Chapter 7 Project Cost Management (IT Project Management, 9th Edition)  
> ใช้ในรายวิชา Project Management หรือ Software Project Management

---

## 🎯 บทนำ: ความสำคัญของ Earned Value Management (EVM)

**EVM** เป็นเทคนิคการวัดสมรรถนะโครงการ โดยรวม **ขอบเขต (Scope)**, **เวลา (Time)**, และ **ต้นทุน (Cost)** เข้าด้วยกัน  
เพื่อดูว่าโครงการ “ทำไปถึงไหนแล้ว” และ “ใช้ทรัพยากรคุ้มค่าหรือไม่”  

> ✅ จุดเด่น: สามารถตรวจจับปัญหาเกินงบ / ล่าช้า ได้ก่อนจะสายเกินไป

---

## 🧩 ค่าหลักใน EVA

| สัญลักษณ์ | ชื่อเต็ม (อังกฤษ) | ความหมาย |
|-------------|---------------------|------------|
| **BAC** | Budget at Completion | งบประมาณรวมของโครงการ |
| **PV** | Planned Value | มูลค่าของงานที่ควรทำเสร็จตามแผน ณ เวลานั้น |
| **EV** | Earned Value | มูลค่าของงานที่ทำเสร็จจริง ณ เวลานั้น |
| **AC** | Actual Cost | ต้นทุนจริงที่ใช้ไป ณ เวลานั้น |

---

## 📊 สูตรหลักและการตีความ

| สูตร | ความหมาย | ตีความค่า |
|-------|-------------|-------------|
| **CV = EV – AC** | Cost Variance (ส่วนต่างต้นทุน) | CV < 0 → เกินงบ, CV > 0 → ประหยัด |
| **SV = EV – PV** | Schedule Variance (ส่วนต่างเวลา) | SV < 0 → ล่าช้า, SV > 0 → เร็วกว่าแผน |
| **CPI = EV / AC** | Cost Performance Index | < 1 = Over Budget, > 1 = Under Budget |
| **SPI = EV / PV** | Schedule Performance Index | < 1 = Behind Schedule, > 1 = Ahead Schedule |
| **EAC = BAC / CPI** | Estimate at Completion | คาดการณ์งบรวมใหม่ |
| **ETC = EAC – AC** | Estimate to Complete | เงินที่ต้องใช้เพิ่ม |
| **Time to Complete = เวลาเดิม / SPI** | คาดการณ์เวลาใหม่ | SPI < 1 → ใช้เวลานานขึ้น |
| **TCPI = (BAC – EV) / (BAC – AC)** | To-Complete Performance Index | <1 = สบาย, >1 = ต้องเร่งมาก |

---

## 📘 ตัวอย่างโจทย์คำนวณ

**โจทย์:**  
โครงการติดตั้ง Web Server  
- BAC = 10,000  
- เสร็จจริง 40% (EV = 4,000)  
- ควรเสร็จ 50% (PV = 5,000)  
- ใช้เงินจริง 6,000 (AC = 6,000)

**คำนวณ:**
| สูตร | ค่า | วิเคราะห์ |
|------|-----|------------|
| CV = 4000 - 6000 = **-2000** | เกินงบ 2,000 |
| SV = 4000 - 5000 = **-1000** | ล่าช้า 1,000 |
| CPI = 4000 / 6000 = **0.67** | ใช้งบเกิน 33% |
| SPI = 4000 / 5000 = **0.8** | ล่าช้า 20% |
| EAC = 10,000 / 0.67 = **14,925** | คาดว่างบจะบานเป็น 14,925 |
| ETC = 14,925 - 6,000 = **8,925** | ต้องใช้เพิ่มอีก 8,925 |
| TCPI = (10,000-4,000)/(10,000-6,000)=**1.5** | ต้องเพิ่มประสิทธิภาพ 50% |

---

## 💡 การวิเคราะห์ค่า CPI/SPI

| ดัชนี | ค่า | ความหมาย |
|--------|------|------------|
| **CPI < 1** | เกินงบประมาณ | ใช้เงินเกินแผน |
| **CPI > 1** | ประหยัด | ใช้งบมีประสิทธิภาพ |
| **SPI < 1** | ล่าช้า | งานไม่ทันตามแผน |
| **SPI > 1** | เร็วกว่าแผน | ทำงานได้เร็ว |

---

## 🧠 แนวทางตอบข้อสอบ

### ❓ ตัวอย่างคำถามที่ออกบ่อย

| คำถาม | คำตอบ |
|--------|--------|
| ถ้า CPI < 1 หมายถึงอะไร | ใช้งบเกินงบประมาณ (Over Budget) |
| ถ้า SPI > 1 หมายถึงอะไร | ทำงานเร็วกว่าแผน |
| สูตรหาค่า Estimate at Completion คืออะไร | EAC = BAC / CPI |
| ถ้า EV < PV หมายถึงอะไร | งานล่าช้า (Behind Schedule) |
| ถ้า EV > AC หมายถึงอะไร | ใช้งบคุ้มกว่าที่วางไว้ |

---

## 📈 เทคนิคจำง่าย

> **“EV กลาง – PV แผน – AC เงิน”**  
> ซ้าย (EV–PV) = ความเร็ว  
> ขวา (EV–AC) = ความคุ้มงบ  

- CPI ต่ำ = “เงินหมดเร็ว”  
- SPI ต่ำ = “ทำงานช้า”

---

## 🧾 สรุปภาพรวม EVM

| หมวด | เป้าหมาย | เครื่องมือที่ใช้ |
|-------|------------|----------------|
| **Plan Cost Management** | วางแผนต้นทุน | Expert Judgment, Templates |
| **Estimate Costs** | ประมาณค่าใช้จ่าย | Analogous, Bottom-up, Parametric |
| **Determine Budget** | กำหนดงบประมาณรวม | Cost Baseline |
| **Control Costs** | ควบคุมการใช้จ่าย | Earned Value Management (EVM) |

---

## 📚 แหล่งอ้างอิงเพิ่มเติม

- Kathy Schwalbe, *Information Technology Project Management*, 9th Edition, Chapter 7  
- Twittie Senivongse (Ed.), Slide “Project Cost Management”  
- https://acqnotes.com/acqnote/tasks/to-complete-performance-indexev  
- https://www.methodsandtools.com/archive/archive.php?id=61  

---

> ✏️ **Tip สำหรับสอบ:**  
> ถ้าเห็นโจทย์มีตัวเลข “EV, PV, AC” → ให้เริ่มด้วยการหาค่า CPI/SPI ก่อนเสมอ  
> แล้วค่อยตอบว่า “Over Budget / Behind Schedule”  
> จำว่า **CPI = เงิน / SPI = เวลา**

---
