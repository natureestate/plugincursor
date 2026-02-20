# Context7 plugin functionality
_Exported on 2/20/2026 at 22:07:59 GMT+7 from Cursor (2.5.17)_

---

**User**

Show me how the Context7 plugin works

---

**Cursor**

# Context7 Plugin - ภาพรวม

คุณเพิ่งติดตั้ง **Context7** plugin (Upstash Context7 MCP server) สำเร็จแล้ว นี่คือสิ่งที่มันทำได้:

## ความสามารถหลัก

**Context7** ช่วยดึงเอกสาร (documentation) และตัวอย่างโค้ดที่อัปเดตล่าสุดจาก library และ framework ต่างๆ เข้ามาในบริบทของคุณโดยตรง ทำให้ได้ข้อมูลที่ตรงกับเวอร์ชันที่ใช้งานจริง

## สิ่งที่ใช้ได้

| ประเภท | ชื่อ | วิธีใช้ |
|--------|------|---------|
| **Skill** | `documentation-lookup` | ทำงานอัตโนมัติเมื่อคุณถามเกี่ยวกับ library/framework หรือเรียกใช้ด้วย `/` |
| **Subagent** | `docs-researcher` | Agent เบาๆ สำหรับดึง docs โดยไม่รกบทสนทนาหลัก เรียกใช้ด้วย `/` |
| **Command** | `/docs` | ค้นหา documentation ของ library ใดก็ได้ |
| **MCP Server** | `context7` | เซิร์ฟเวอร์ที่เชื่อมต่อกับแหล่ง documentation |

## ตัวอย่างการใช้งาน

- พิมพ์ `/docs` แล้วตามด้วยชื่อ library เช่น `/docs react` เพื่อดึง docs ของ React
- ถามคำถามเกี่ยวกับ library เช่น "Next.js app router ใช้ยังไง?" แล้ว skill จะทำงานอัตโนมัติ
- ใช้ `/docs-researcher` เมื่อต้องการค้นหา docs แบบไม่รบกวนบทสนทนาหลัก

---

ให้ผมตรวจสอบสถานะการตั้งค่า MCP server ก่อนนะครับ

Context7 MCP server ใช้การเชื่อมต่อแบบ HTTP ไปที่ `https://mcp.context7.com/mcp` โดย **ไม่ต้องตั้งค่า authentication ใดๆ เพิ่มเติม** -- พร้อมใช้งานได้เลยครับ!

## สรุป

Plugin พร้อมใช้งานแล้ว คุณสามารถ:
1. ใช้คำสั่ง `/docs` เพื่อค้นหา documentation ของ library ต่างๆ
2. ถามคำถามเกี่ยวกับ framework แล้ว skill จะทำงานอัตโนมัติ
3. ใช้ subagent `/docs-researcher` สำหรับค้นหา docs แบบแยกบริบท

