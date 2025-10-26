# 🎓 Online Learning Platform
## การวิเคราะห์ Trade-off ของสถาปัตยกรรมซอฟต์แวร์

---

### 🔹 บทนำ
ระบบเรียนออนไลน์ต้องรองรับผู้ใช้จำนวนมากในเวลาเดียวกัน  
เน้นการเข้าถึงได้ทุกที่ทุกเวลา (availability) และการสตรีมวิดีโอได้ต่อเนื่อง (performance)

---

## 🧭 การเลือกสถาปัตยกรรม

| สไตล์ | บทบาท | เหตุผล |
|--------|---------|---------|
| **Microservices Architecture** | แยกบริการ เช่น วิดีโอ, แบบทดสอบ, คะแนน | รองรับผู้ใช้จำนวนมากได้ |
| **Event-Driven Architecture** | ใช้สำหรับแจ้งผลคะแนน / การส่งงาน / การแจ้งเตือน | ทำงานเร็วและไม่รอผลลัพธ์ |
| **Layered Architecture** | ใช้ในส่วนเว็บไซต์และแดชบอร์ดผู้สอน | จัดการโค้ดง่าย ดูแลสะดวก |

---

## ⚖️ การวิเคราะห์ Trade-off

### ⚙️ 1. Microservices Architecture  
**เน้น:** 🟢 *Scalability / Availability*  
**แลก:** ⚙️ *Complexity / Cost*

- แยกบริการ เช่น Video / Quiz / Report  
  หากส่วนใดล่ม ส่วนอื่นยังทำงานได้  
- แต่ใช้เซิร์ฟเวอร์หลายเครื่อง ทำให้ต้นทุนสูง  

**แนวทางลดผลกระทบ:**  
- ใช้ container และระบบจัดการอัตโนมัติ (เช่น Kubernetes)  
- รวมบริการที่มีโหลดต่ำเข้าด้วยกันเพื่อลดค่าใช้จ่าย  

---

### ⚙️ 2. Event-Driven Architecture  
**เน้น:** ⚡ *Performance / Real-time Response*  
**แลก:** ⚙️ *Debugging / Reliability*

- ใช้ส่งการแจ้งเตือน เช่น “ส่งงานสำเร็จ”, “ได้คะแนนใหม่”  
- ทำงานรวดเร็วแบบ asynchronous  

**แนวทางลดผลกระทบ:**  
- เก็บ log ทุก event  
- ตั้งระบบตรวจสอบ event ที่ค้าง  
- มีคิวสำรองเมื่อ broker ล่ม  

---

### ⚙️ 3. Layered Architecture  
**เน้น:** 🔧 *Maintainability*  
**แลก:** ⏱️ *Performance*

- ช่วยให้โค้ดส่วนหน้าและส่วนหลังแยกจากกันชัดเจน  
- แต่เพิ่มเวลาในการสื่อสารระหว่าง layer  

**แนวทางลดผลกระทบ:**  
- ใช้ cache สำหรับข้อมูลที่ถูกเรียกบ่อย  
- ลดจำนวนชั้นในส่วนสำคัญ  

---

## 📊 สรุปภาพรวม

| สไตล์ | เน้น | แลก | วิธีลดผลกระทบ |
|--------|------|------|----------------|
| Microservices | Scalability / Availability | Complexity / Cost | container, รวมบริการย่อย |
| Event-Driven | Performance / Real-time | Debugging / Reliability | log, queue สำรอง |
| Layered | Maintainability | Performance | cache, ลด layer |

---

> 💬 สรุป: ระบบเรียนออนไลน์เน้น “เข้าถึงได้ทุกที่” และ “ตอบสนองเร็ว”  
> จึงเลือกใช้ Microservices + Event-Driven เพื่อเน้น Performance และ Availability
