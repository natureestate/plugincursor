# Parallel plugin functionality
_Exported on 2/20/2026 at 22:15:25 GMT+7 from Cursor (2.5.17)_

---

**User**

Show me how the Parallel plugin works

---

**Cursor**

# Parallel Plugin - ภาพรวม

คุณเพิ่งติดตั้ง **Parallel Plugin** สำเร็จแล้ว! นี่คือปลั๊กอินสำหรับ **ค้นหาเว็บ, ดึงเนื้อหาจาก URL, วิจัยเชิงลึก, และเพิ่มข้อมูลแบบ Bulk** โดยใช้ parallel-cli

---

## Commands (ใช้งานด้วย `/`)

| Command | การใช้งาน | คำอธิบาย |
|---|---|---|
| `/parallel-search` | `/parallel-search <query>` | ค้นหาเว็บทั่วไป - เหมาะกับคำถามส่วนใหญ่ |
| `/parallel-extract` | `/parallel-extract <url> [url2] [url3]` | ดึงเนื้อหาจาก URL (เว็บเพจ, บทความ, PDF) |
| `/parallel-research` | `/parallel-research <topic>` | วิจัยเชิงลึกแบบหลายแหล่ง (ช้ากว่า ใช้เมื่อต้องการจริงๆ) |
| `/parallel-enrich` | `/parallel-enrich <file or entities> with <fields>` | เพิ่มข้อมูลจากเว็บให้กับรายชื่อบริษัท/บุคคล แบบ Bulk |
| `/parallel-status` | `/parallel-status <run_id>` | เช็คสถานะงานวิจัยที่กำลังรัน |
| `/parallel-result` | `/parallel-result <run_id>` | ดึงผลลัพธ์ของงานวิจัยที่เสร็จแล้ว |
| `/parallel-setup` | `/parallel-setup` | ตั้งค่า Parallel plugin (ติดตั้ง CLI และ authenticate) |

---

## Skills (ถูกเรียกใช้อัตโนมัติตามบริบท)

- **parallel-web-search** - ค่าเริ่มต้นสำหรับทุกการค้นหาและคำถามที่ต้องการข้อมูลปัจจุบัน เร็วและประหยัด
- **parallel-web-extract** - ดึงเนื้อหาจาก URL ทุกประเภท รองรับเว็บเพจ, บทความ, PDF, และเว็บที่ใช้ JavaScript หนัก
- **parallel-deep-research** - วิจัยเชิงลึกแบบครอบคลุม ใช้เฉพาะเมื่อคุณขอ "deep research" หรือ "exhaustive" โดยเฉพาะ
- **parallel-data-enrichment** - เพิ่มข้อมูลจากเว็บ (เช่น ชื่อ CEO, ข้อมูล funding, ข้อมูลติดต่อ) ให้กับรายชื่อบริษัท/บุคคล/สินค้า

---

## Rules (ใช้อัตโนมัติ)

- **citation-standards** - มาตรฐานการอ้างอิงสำหรับผลการค้นหาเว็บ จะถูกนำมาใช้อัตโนมัติเมื่อแสดงผลลัพธ์จากการค้นหา

---

## ตัวอย่างการใช้งาน

- อยากรู้อะไร? พิมพ์ `/parallel-search React 19 new features`
- อยากอ่านเนื้อหาจากลิงก์? พิมพ์ `/parallel-extract https://example.com/article`
- อยากวิจัยเรื่องใหญ่แบบละเอียด? พิมพ์ `/parallel-research AI trends 2026`
- มีรายชื่อบริษัท อยากเพิ่มข้อมูล? พิมพ์ `/parallel-enrich companies.csv with CEO, funding, website`

หากยังไม่ได้ตั้งค่า ให้รัน `/parallel-setup` ก่อนเริ่มใช้งานครับ!

