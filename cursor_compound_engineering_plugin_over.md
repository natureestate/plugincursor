# Compound Engineering plugin overview
_Exported on 2/20/2026 at 22:08:23 GMT+7 from Cursor (2.5.17)_

---

**User**

Show me how the Compound Engineering plugin works

---

**Cursor**

# Compound Engineering Plugin - ภาพรวม

คุณเพิ่งติดตั้ง **Compound Engineering** plugin สำเร็จแล้ว! นี่คือ plugin สำหรับพัฒนาซอฟต์แวร์ที่ขับเคลื่อนด้วย AI ประกอบด้วยเครื่องมือจำนวนมาก แบ่งออกเป็นหมวดหลัก ๆ ดังนี้:

---

## Skills (19 ทักษะ) - ใช้อัตโนมัติหรือเรียกด้วย `/`

ทักษะเหล่านี้จะถูกใช้อัตโนมัติเมื่อเกี่ยวข้อง หรือเรียกใช้ตรง ๆ ได้:

- **brainstorming** - ช่วยคิดวิเคราะห์ก่อนลงมือ code
- **frontend-design** - สร้าง UI ระดับ production-grade ที่สวยงาม
- **agent-browser** - ควบคุม browser อัตโนมัติ (กรอกฟอร์ม, คลิก, screenshot)
- **gemini-imagegen** - สร้าง/แก้ไขรูปภาพด้วย Gemini API
- **git-worktree** - จัดการ Git worktree สำหรับทำงานหลาย branch พร้อมกัน
- **rclone** - อัปโหลดไฟล์ไปยัง cloud storage (S3, R2, Google Drive ฯลฯ)
- **create-agent-skills** / **skill-creator** - สร้าง skills ใหม่
- **document-review** - ตรวจสอบเอกสาร brainstorm/plan
- และอื่น ๆ อีกหลายตัว (Ruby/Rails, DSPy, style guides)

## Subagents (29 ตัว) - Agent เฉพาะทาง เรียกด้วย `/`

### Code Review Agents
- **architecture-strategist** - วิเคราะห์สถาปัตยกรรม
- **security-sentinel** - ตรวจสอบช่องโหว่ด้านความปลอดภัย
- **performance-oracle** - วิเคราะห์ปัญหา performance
- **code-simplicity-reviewer** - ตรวจความเรียบง่ายของ code
- **pattern-recognition-specialist** - ตรวจ design patterns
- **data-integrity-guardian** - ตรวจ migrations และ data models

### Research Agents
- **repo-research-analyst** - วิจัยโครงสร้าง codebase
- **best-practices-researcher** - ค้นหา best practices
- **git-history-analyzer** - วิเคราะห์ประวัติ git

### Design Agents
- **design-implementation-reviewer** - เทียบ UI กับ Figma
- **design-iterator** - ปรับปรุง UI ซ้ำ ๆ จนสวย
- **figma-design-sync** - sync ระหว่าง code กับ Figma

### Language-specific Reviewers
- **kieran-typescript-reviewer**, **kieran-python-reviewer**, **kieran-rails-reviewer**, **dhh-rails-reviewer** ฯลฯ

## Commands (22 คำสั่ง) - เรียกด้วย `/`

คำสั่งหลัก ๆ ที่น่าสนใจ:

| คำสั่ง | คำอธิบาย |
|--------|----------|
| `/lfg` | Workflow วิศวกรรมอัตโนมัติเต็มรูปแบบ |
| `/slfg` | เหมือน `/lfg` แต่ใช้ swarm mode ทำงานขนานกัน |
| `/workflowsreview` | Code review แบบ multi-agent |
| `/workflowsplan` | แปลง feature description เป็น project plan |
| `/workflowsbrainstorm` | Brainstorm ก่อนวางแผน |
| `/workflowswork` | ทำงานตาม plan อย่างมีประสิทธิภาพ |
| `/changelog` | สร้าง changelog จาก merge ล่าสุด |
| `/reproduce-bug` | สืบสวนและ reproduce bug |
| `/test-browser` | รัน browser test |
| `/deepen-plan` | เพิ่มความลึกให้ plan ด้วย research agents |

## MCP Server - Context7

ให้เข้าถึงเอกสาร documentation ล่าสุดของ libraries ต่าง ๆ ได้

---

ให้ผมตรวจสอบสถานะของ MCP server ว่าต้องตั้งค่าอะไรเพิ่มหรือไม่

ไม่พบไฟล์ STATUS.md สำหรับ MCP server ซึ่งหมายความว่า **Context7 MCP server น่าจะพร้อมใช้งานแล้ว** โดยไม่ต้องตั้งค่าเพิ่มเติม

---

## วิธีเริ่มต้นใช้งาน

1. **อยากให้ AI ทำงานให้ทั้งหมด?** → พิมพ์ `/lfg` แล้วบอกสิ่งที่ต้องการ
2. **อยาก review code?** → พิมพ์ `/workflowsreview`
3. **อยากวางแผนก่อนทำ?** → พิมพ์ `/workflowsbrainstorm` แล้วตามด้วย `/workflowsplan`
4. **อยากให้ตรวจ PR?** → subagents ต่าง ๆ จะถูกเรียกใช้อัตโนมัติเมื่อเกี่ยวข้อง

Plugin นี้ทรงพลังมากครับ มีอะไรอยากลองใช้เป็นอย่างแรกบ้างไหม?

