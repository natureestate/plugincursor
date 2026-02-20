# Superpowers plugin functionality
_Exported on 2/20/2026 at 22:08:16 GMT+7 from Cursor (2.5.17)_

---

**User**

Show me how the Superpowers plugin works

---

**Cursor**

ยินดีต้อนรับสู่ plugin **Superpowers**! นี่คือภาพรวมของความสามารถทั้งหมดที่คุณได้รับ:

---

## Skills (ทักษะอัตโนมัติ)

Skills จะถูกใช้โดย agent อัตโนมัติเมื่อเหมาะสม หรือคุณสามารถเรียกใช้ด้วย `/` ได้:

| Skill | ใช้เมื่อไหร่ |
|---|---|
| **brainstorming** | ก่อนงานสร้างสรรค์ทุกชนิด - สร้าง feature, component หรือแก้ไข behavior |
| **writing-plans** | เมื่อมี spec หรือ requirements สำหรับงานหลายขั้นตอน ก่อนเขียน code |
| **executing-plans** | เมื่อมีแผนการ implement พร้อมแล้ว ต้องการ execute พร้อม review checkpoints |
| **test-driven-development** | เมื่อ implement feature หรือ bugfix - เขียน test ก่อน implementation |
| **systematic-debugging** | เมื่อเจอ bug, test failure หรือ behavior ที่ไม่คาดคิด |
| **dispatching-parallel-agents** | เมื่อมี 2+ tasks อิสระที่ทำพร้อมกันได้ |
| **subagent-driven-development** | เมื่อ execute แผนที่มี tasks อิสระใน session ปัจจุบัน |
| **verification-before-completion** | ก่อนจะบอกว่างานเสร็จ - ต้อง run verification ก่อนเสมอ |
| **requesting-code-review** | เมื่อทำงานเสร็จ ก่อน merge เพื่อตรวจสอบคุณภาพ |
| **receiving-code-review** | เมื่อได้รับ feedback จาก code review |
| **finishing-a-development-branch** | เมื่อ implementation เสร็จ ต้องการ merge, PR หรือ cleanup |
| **using-git-worktrees** | เมื่อต้องการ isolation สำหรับ feature work |
| **writing-skills** | เมื่อสร้างหรือแก้ไข skills ใหม่ |

---

## Commands (คำสั่งที่เรียกใช้ด้วย `/`)

- **`/brainstorm`** - สำรวจ requirements และ design ก่อนลงมือ implement
- **`/write-plan`** - สร้างแผนการ implement แบบละเอียดเป็น task ย่อยๆ
- **`/execute-plan`** - Execute แผนเป็นชุดๆ พร้อม review checkpoints

---

## Subagents (agent ย่อย)

- **code-reviewer** - ใช้เมื่อทำ feature สำคัญเสร็จ จะตรวจสอบ code เทียบกับแผนและ coding standards อัตโนมัติ

---

## Hooks (ทำงานอัตโนมัติ)

- **SessionStart** - ทำงานอัตโนมัติเมื่อเริ่ม session ใหม่

---

## แนวทางการใช้งาน

1. เริ่มจาก `/brainstorm` เพื่อคิดก่อนลงมือ
2. ใช้ `/write-plan` เพื่อวางแผน
3. ใช้ `/execute-plan` เพื่อ implement ตามแผน
4. Agent จะเรียก **verification** และ **code-reviewer** ให้อัตโนมัติเมื่อถึงจุดที่เหมาะสม

Plugin นี้ออกแบบมาเพื่อให้ workflow มีโครงสร้าง มีคุณภาพ และตรวจสอบได้ทุกขั้นตอนครับ!

