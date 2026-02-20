# Create Plugin plugin functionality
_Exported on 2/20/2026 at 22:17:22 GMT+7 from Cursor (2.5.17)_

---

**User**

Show me how the Create Plugin plugin works

---

**Cursor**

## ภาพรวมของ Plugin "Create Plugin"

Plugin นี้ช่วยให้คุณสร้างและตรวจสอบ Cursor Plugin ใหม่ได้อย่างง่ายดาย โดยมีความสามารถหลักดังนี้:

---

### Skills (เรียกใช้โดยตรงหรือ Agent ใช้อัตโนมัติ)

1. **create-plugin-scaffold** - สร้างโครงสร้าง Plugin ใหม่ พร้อม manifest, directory และการเชื่อมต่อ marketplace ใช้เมื่อเริ่มสร้าง plugin ใหม่หรือเพิ่ม plugin ในโปรเจกต์ที่มีหลาย plugin

2. **review-plugin-submission** - ตรวจสอบ plugin ว่าพร้อมสำหรับการส่งขึ้น marketplace หรือยัง ตรวจ manifest, metadata, discovery paths และคุณภาพโดยรวม

---

### Subagents (เรียกใช้ด้วย `/` หรือ Agent เรียกอัตโนมัติ)

- **plugin-architect** - ผู้เชี่ยวชาญด้านสถาปัตยกรรม plugin ช่วยตัดสินใจเรื่องโครงสร้าง component, metadata และรูปแบบที่เหมาะสมสำหรับ plugin ใหม่

---

### Rules (ใช้งานอัตโนมัติ)

- **plugin-quality-gates** - ตรวจสอบความถูกต้องของ manifest, paths และ component metadata ระหว่างที่คุณเขียน plugin โดยอัตโนมัติ

---

### ตัวอย่างการใช้งาน

- อยากสร้าง plugin ใหม่? บอกได้เลยว่า "สร้าง Cursor plugin ใหม่" แล้ว skill `create-plugin-scaffold` จะช่วยสร้างโครงสร้างทั้งหมดให้
- อยากเช็คว่า plugin พร้อมส่ง marketplace ไหม? บอกว่า "ตรวจสอบ plugin ก่อนส่ง" แล้ว skill `review-plugin-submission` จะทำ audit ให้
- ไม่แน่ใจว่าควรใช้โครงสร้างแบบไหน? Agent จะเรียก `plugin-architect` มาช่วยวิเคราะห์ให้อัตโนมัติ

