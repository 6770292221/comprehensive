# 📡 Deployment Diagrams - ตัวอย่าง

ตัวอย่าง Deployment Diagrams สำหรับ Lesson 9: System Architecture & Physical Design

---

## 📂 ไฟล์ในโฟลเดอร์

| ไฟล์ | รายละเอียด |
|------|------------|
| `01-3-tier-architecture.puml` | 3-Tier Architecture (Specification Level) |
| `02-3-tier-instance.puml` | 3-Tier Architecture (Instance Level) |
| `03-cloud-hybrid.puml` | Hybrid Cloud Architecture |
| `04-microservices.puml` | Microservices E-Commerce |
| `05-automate-parking-system.puml` | Automate Parking System |

---

## 🔧 วิธีใช้งาน

### ออนไลน์
1. เปิด [PlantUML Online](http://www.plantuml.com/plantuml/uml/)
2. Copy โค้ดจากไฟล์ .puml
3. Paste และ Submit

### VS Code
1. ติดตั้ง extension: **PlantUML**
2. เปิดไฟล์ .puml
3. กด `Alt+D` เพื่อ preview

### Command Line
```bash
# ติดตั้ง
brew install plantuml

# Generate PNG
plantuml *.puml

# Generate SVG
plantuml -tsvg *.puml
```

---

## 📊 องค์ประกอบของ Deployment Diagram

| องค์ประกอบ | Syntax | ตัวอย่าง |
|------------|--------|----------|
| Node | `node "name" { }` | Server, Client |
| Artifact | `artifact "file"` | .jar, .war |
| Database | `database "name"` | MySQL, PostgreSQL |
| Connection | `-->` | A --> B |
| Stereotype | `<<type>>` | <<device>>, <<server>> |

---

## 💡 PlantUML Tips

### สี
```plantuml
skinparam nodeBackgroundColor lightyellow
```

### ทิศทาง
```plantuml
A -down-> B
A -right-> C
A -up-> D
A -left-> E
```

### Grouping
```plantuml
cloud "AWS Cloud" {
  node "EC2"
}

rectangle "Internal Network" {
  node "App Server"
}
```

### Notes
```plantuml
note right of server
  This is a note
end note
```

---

## ✅ Checklist

- [ ] ระบุ nodes ครบ (Client, Server, DB)
- [ ] แสดง artifacts ที่ติดตั้ง
- [ ] มี communication paths
- [ ] ระบุ protocols (HTTP, JDBC)
- [ ] สอดคล้องกับ NFRs
- [ ] มี Firewall/DMZ ถ้าต้องการความปลอดภัย
- [ ] มี Load Balancer ถ้าต้องการ HA

---

## 📚 แหล่งข้อมูล

- [PlantUML Official](https://plantuml.com/)
- [Deployment Diagram Guide](https://plantuml.com/deployment-diagram)
- [PlantUML Cheat Sheet](https://ogom.github.io/draw_uml/plantuml/)

---

สร้างโดย: Claude Code
วันที่: 2025-10-23
อ้างอิงจาก: Lesson 9 - System Architecture & Physical Design
