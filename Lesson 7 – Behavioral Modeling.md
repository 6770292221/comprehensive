# 🧩 Lesson 7 – Behavioral Modeling (Sequence, State Machine & CRUDE)
**Software Requirements Engineering – Chulalongkorn University**  
Instructor: นครทิพย์ พร้อมพูล  

---

## 🎯 Objectives
- เข้าใจกฎและแนวทางการสร้าง **Sequence Diagram** และ **Behavioral State Machine**  
- สามารถสร้าง **CRUDE Matrix** เพื่อแสดงการทำงานร่วมกันของ Objects  
- เชื่อมโยงความสัมพันธ์ระหว่าง **Behavioral – Structural – Functional Models**  
- ตรวจสอบความครบถ้วนและสอดคล้องของโมเดล (Verification & Validation)  

---

## 🧠 Concept Overview
> “Behavioral Models แสดงพฤติกรรมภายในของระบบ โดยอธิบายว่าคลาสและอ็อบเจ็กต์ทำงานร่วมกันอย่างไร เพื่อสนับสนุน Use Case แต่ละตัว” :contentReference[oaicite:1]{index=1}

- **Sequence Diagram** → โฟกัสที่ “การสื่อสาร (messages)” ระหว่าง objects  
- **Behavior State Machine** → โฟกัสที่ “สถานะ (states)” ของ object ในช่วงชีวิต  
- **CRUDE Matrix** → แสดงภาพรวมของความสัมพันธ์ระหว่าง objects ทั้งระบบ  

---

## 🧩 Interaction Diagrams

### 1. Sequence Diagram
- แสดงลำดับของ **messages** ที่ส่งระหว่าง **objects** เพื่อสนับสนุน Use Case  
- เป็น **Dynamic Model** ของระบบ  
- ใช้เพื่อวิเคราะห์ “การทำงานแบบเรียลไทม์” หรือ Use Case ที่ซับซ้อน:contentReference[oaicite:2]{index=2}

### Components:
| องค์ประกอบ | ความหมาย |
|-------------|-----------|
| **Object** | ตัวอย่างจริงของคลาส เช่น `patient : Patient` |
| **Lifeline** | เส้นแสดงอายุการทำงานของ object |
| **Message** | คำสั่งที่ส่งจาก object หนึ่งไปยังอีก object |
| **Execution Occurrence** | ช่วงเวลาที่ object กำลังทำงาน |
| **Guard Condition** | เงื่อนไขการทำงาน เช่น `[validUser]` |

---

### 2. Syntax Overview

```text
Actor → Object1 : request()
Object1 → Object2 : validateInfo()
Object2 → Object1 : result
Object1 → Actor : confirmation()
