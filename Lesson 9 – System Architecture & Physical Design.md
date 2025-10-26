# 🧩 Lesson 9: System Architecture & Non-Functional Requirements
> Subject: Software Requirements Engineering (2110623)  
> Lecturer: N. Prompoon, Chulalongkorn University, 2024  

---

## 🎯 บทสรุปเนื้อหา
ระบบซอฟต์แวร์สมัยใหม่ทำงานบนหลายเครื่องและหลายเครือข่าย  
**System Architecture** คือการกำหนดว่า  
> ซอฟต์แวร์ใดรันบนเครื่องใด ใช้สถาปัตยกรรมใด และเชื่อมต่อกันอย่างไร  

บทนี้เน้นการออกแบบ **Physical Architecture Layer**,  
การวิเคราะห์ผลของ **Non-Functional Requirements (NFRs)**  
และการสร้าง **Deployment Diagram / Network Model / Package Diagram**

---

## 🧱 แนวข้อสอบพร้อมคำตอบ

### 🧩 หมวดที่ 1: พื้นฐานของสถาปัตยกรรม

**Q1.** อธิบายความหมายของ “Physical Architecture Layer”  
> การออกแบบระดับกายภาพของระบบ ว่าซอฟต์แวร์ส่วนใดรันบนเครื่องไหน ใช้เครือข่ายอะไร และสื่อสารกันอย่างไร เพื่อรองรับ requirement ของระบบ

---

**Q2.** องค์ประกอบของ Physical Architecture มีอะไรบ้าง  
| หมวด | รายละเอียด |
|------|-------------|
| **Software Components** | Data Storage, Data Access Logic, Application Logic, Presentation Logic |
| **Hardware Components** | Client, Server, Network Devices |

---

**Q3.** ปัจจัยที่ใช้เลือกสถาปัตยกรรม (Architecture Selection Criteria)  
> Cost, Ease of Development, Interface Capabilities, Control & Security, Scalability

---

**Q4.** ความแตกต่างระหว่าง Server-Based, Client-Based และ Client-Server Architecture  
| ประเภท | ลักษณะ | จุดเด่น | จุดด้อย |
|----------|----------|----------|----------|
| **Server-Based** | ทุกอย่างอยู่บน Server | ปลอดภัย ควบคุมง่าย | ต้นทุนสูง, ขยายยาก |
| **Client-Based** | Client โหลดข้อมูลมาประมวลผล | พัฒนาเร็ว | Network ช้า, ภาระ client สูง |
| **Client-Server** | แบ่งงานระหว่าง Client/Server | ขยายระบบง่าย, ยืดหยุ่น | พัฒนาและดูแลซับซ้อน |

---

**Q5.** อธิบายความแตกต่างของ 2-Tier, 3-Tier, n-Tier Architecture  
- **2-Tier:** Client ทำ logic ส่วนใหญ่, Server เก็บข้อมูล  
- **3-Tier:** แยก Application Server ออกมาต่างหาก  
- **n-Tier:** แยกหลายชั้น (API, DB, Services) → ใช้ในระบบ Enterprise  

---

### ☁️ หมวดที่ 2: Cloud Computing

**Q6.** แนวคิดของ Cloud Computing คืออะไร  
> การให้บริการทรัพยากร IT แบบ “pay-as-you-go” ผ่านอินเทอร์เน็ต โดยผู้ใช้ไม่ต้องดูแลฮาร์ดแวร์เอง

---

**Q7.** จำแนก Cloud ตาม *Deployment Model*  
| ประเภท | คำอธิบาย | ตัวอย่าง |
|----------|------------|-----------|
| **Private Cloud** | ใช้ภายในองค์กร | Internal Data Center |
| **Public Cloud** | ใช้ได้ทั่วไป | AWS, Azure, GCP |
| **Hybrid Cloud** | ผสมสองแบบ | Private Cloud + Public Storage |

---

**Q8.** จำแนก Cloud ตาม *Service Model*  
| Service | รายละเอียด | ตัวอย่าง |
|----------|-------------|-----------|
| **IaaS** | ให้บริการ Infrastructure (Server/Storage) | AWS EC2 |
| **PaaS** | ให้บริการ Platform พร้อม Tools | Google App Engine |
| **SaaS** | ให้บริการซอฟต์แวร์สำเร็จรูป | Salesforce, Gmail |

---

### ⚙️ หมวดที่ 3: Non-Functional Requirements (NFRs)

**Q9.** ประเภทหลักของ NFRs มีอะไรบ้าง  
1. Operational  
2. Performance  
3. Security  
4. Cultural & Political  

---

**Q10.** ยกตัวอย่าง Operational Requirements  
> Portability, System Integration, Maintainability

**Q11.** Performance Requirements ที่พบบ่อย  
> Speed, Capacity, Availability, Reliability

**Q12.** Security Requirements มีอะไรบ้าง  
> Access Control, Encryption, Authentication, Virus Control

**Q13.** Cultural & Political Requirements หมายถึงอะไร  
> ความต้องการที่เกี่ยวกับภาษา, กฎหมาย, นโยบายองค์กร หรือความแตกต่างทางวัฒนธรรม

---

### 🧩 หมวดที่ 4: ความสัมพันธ์ NFRs ↔ Architecture

| NFR | สถาปัตยกรรมที่เหมาะสม | เหตุผล |
|------|--------------------------|----------|
| **Operational – Portability** | Thin Client | ใช้มาตรฐานเว็บ เช่น HTML/XML |
| **Maintainability** | Server-Based / Thin Client | ไม่ต้องติดตั้งซ้ำในทุกเครื่อง |
| **Performance – Speed** | Client-Server | ปรับเซิร์ฟเวอร์และ balance load ได้ |
| **Security – Access Control** | Server-Based | ควบคุมศูนย์กลาง |
| **Cultural – Multilingual** | Thin Client | แยก UI ตามภาษาได้ง่าย |

---

### 📡 หมวดที่ 5: Deployment & Network Model

**Q14.** Deployment Diagram คืออะไร  
> แผนภาพที่แสดงการเชื่อมต่อระหว่างอุปกรณ์ (nodes) และซอฟต์แวร์ (artifacts) ที่ถูกติดตั้งในระบบ

**องค์ประกอบหลัก:** Node, Artifact, Communication Path

---

**Q15.** ความแตกต่างระหว่าง *Specification Level* กับ *Instance Level* Deployment Diagram  
| ระดับ | รายละเอียด |
|--------|--------------|
| **Specification Level** | แสดงชนิดของ node (ไม่ระบุชื่อเครื่องจริง) |
| **Instance Level** | แสดงชื่อเครื่องจริง เช่น `app-srv01`, `db-srv02` |

---

**Q16.** Network Model ใช้ทำอะไร  
> ใช้แสดงโครงสร้างเครือข่ายจริงขององค์กร แสดงการเชื่อมต่อระหว่างสาขา และเป็นพื้นฐานในการเขียน Hardware/Software Specification  

**ขั้นตอนสร้าง:**  
1. วาด Top-Level Network Model (ภาพรวม)  
2. เพิ่ม Low-Level Model สำหรับแต่ละ node  

---

### 💾 หมวดที่ 6: Hardware / Software Specification

**Q17.** เนื้อหาที่ต้องมีใน Hardware & Software Specification  
| ประเภท | รายการ |
|----------|---------|
| **Hardware** | Server, Storage, Network Device, Backup |
| **Software** | OS, DBMS, Application Server, License |
| **Others** | Training, Maintenance, Warranty |

---

**Q18.** การตรวจสอบ (Verification & Validation) ของ Physical Architecture Layer  
1. ตรวจสอบความสอดคล้องระหว่าง Deployment Diagram ↔ Network Model ↔ Spec  
2. ตรวจสอบ NFR ผ่าน Load / Performance / Security Testing  
3. ตรวจสอบว่า topology รองรับ scalability ที่กำหนดไว้ใน requirement

---

### 📦 หมวดที่ 7: Package Diagram

**Q19.** Package Diagram ใช้เพื่ออะไร  
> ใช้จัดกลุ่ม Class / Use Case เพื่อให้โมเดลไม่ซับซ้อน และแสดง Dependency ระหว่างกลุ่ม (Package)

**แนวทางสร้าง:**  
- รวมคลาสที่สัมพันธ์กัน  
- วาด dependency  
- ตั้งชื่อสั้นและสื่อความหมาย  

---

**Q20.** ระบุ 5 ชั้น (Layers) ของ Package Diagram  
| Layer | รายละเอียด |
|--------|--------------|
| 1. Foundation | Data Type และ Utility Class |
| 2. Problem Domain | คลาสที่เกี่ยวข้องกับ business logic |
| 3. Data Management | การจัดเก็บและเข้าถึงข้อมูล |
| 4. HCI Layer | ส่วนโต้ตอบกับผู้ใช้ |
| 5. Physical Architecture | Network, Server, OS, Cloud, Security |

---

## 🧾 สรุปสั้นท้ายบท

| หัวข้อ | เนื้อหา |
|---------|----------|
| **Architecture Types** | Server-Based / Client-Based / Client-Server / Cloud |
| **NFRs Categories** | Operational, Performance, Security, Cultural |
| **Diagram สำคัญ** | Deployment Diagram / Network Model / Package Diagram |
| **Specification Document** | Hardware & Software Specification |
| **จุดเน้นสอบ** | Mapping ระหว่าง NFR ↔ Architecture, Tier, Cloud Model |

---

## 💡 Tips สำหรับสอบ
- จำตาราง “NFR ↔ Architecture” ให้ได้  
- เข้าใจความแตกต่างระหว่าง 2-tier / 3-tier / n-tier  
- Deployment Diagram = Node + Artifact + Communication Path  
- Package Diagram = กลุ่มของ class / use case ที่มี dependency  
- Cloud = Private / Public / Hybrid + (IaaS, PaaS, SaaS)  
- NFR มี 4 กลุ่มใหญ่ → Operational / Performance / Security / Cultural  

---
