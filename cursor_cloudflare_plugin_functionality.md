# Cloudflare plugin functionality
_Exported on 2/20/2026 at 22:12:13 GMT+7 from Cursor (2.5.17)_

---

**User**

Show me how the Cloudflare plugin works

---

**Cursor**

ยินดีต้อนรับสู่ **Cloudflare Plugin** ครับ! นี่คือภาพรวมของสิ่งที่คุณได้ติดตั้ง:

---

## Skills (ทักษะที่ใช้งานได้อัตโนมัติ)

Agent จะเรียกใช้ Skills เหล่านี้โดยอัตโนมัติเมื่อเกี่ยวข้อง หรือคุณสามารถเรียกใช้ด้วย `/` ได้:

| Skill | คำอธิบาย |
|---|---|
| **agents-sdk** | สร้าง AI agents บน Cloudflare Workers ด้วย Agents SDK (state management, WebSocket, scheduled tasks, MCP servers) |
| **building-ai-agent-on-cloudflare** | สร้าง AI agent พร้อม deploy บน Workers (real-time, tool calling, chat) |
| **building-mcp-server-on-cloudflare** | สร้าง remote MCP server บน Workers พร้อม OAuth authentication |
| **cloudflare** | Skill ครอบคลุมทั้งแพลตฟอร์ม: Workers, Pages, KV, D1, R2, Workers AI, Vectorize, Tunnel, WAF, Terraform, Pulumi |
| **durable-objects** | สร้าง Durable Objects สำหรับ stateful coordination (chat rooms, multiplayer, booking) |
| **sandbox-sdk** | Secure code execution สำหรับ AI code interpreters, CI/CD |
| **web-perf** | วิเคราะห์ Core Web Vitals และ performance ผ่าน Chrome DevTools |
| **workers-best-practices** | ตรวจสอบ Workers code ตาม production best practices |
| **wrangler** | ใช้ Wrangler CLI อย่างถูกต้องสำหรับ deploy และจัดการ Workers, KV, R2, D1 ฯลฯ |

## Commands (คำสั่งที่เรียกใช้ได้)

- `/build-agent` — สร้าง AI agent บน Cloudflare ด้วย Agents SDK
- `/build-mcp` — สร้าง remote MCP server บน Cloudflare พร้อม tools และ OAuth

## Rules (กฎที่ใช้อัตโนมัติ)

- **workers** — เมื่อสร้างแอปบน Cloudflare Workers จะดึงข้อมูลจาก documentation แทนที่จะใช้ training data เพื่อความถูกต้อง

## MCP Servers

- **cloudflare-docs** — ดึง documentation ของ Cloudflare
- **cloudflare-bindings** — จัดการ bindings (KV, D1, R2 ฯลฯ)
- **cloudflare-builds** — จัดการ builds
- **cloudflare-observability** — ดู logs และ metrics

---

ผมจะตรวจสอบสถานะ authentication ของ MCP servers ให้ครับ

ไม่พบไฟล์ STATUS.md สำหรับการตั้งค่า authentication ซึ่งหมายความว่า MCP servers น่าจะพร้อมใช้งานได้เลย หรืออาจต้องตั้งค่า Cloudflare API token แยกต่างหาก

---

## วิธีใช้งาน

1. **สร้าง AI Agent** — พิมพ์ `/build-agent` หรือบอกว่า "สร้าง AI agent บน Cloudflare"
2. **สร้าง MCP Server** — พิมพ์ `/build-mcp` หรือบอกว่า "สร้าง MCP server"
3. **ถามเรื่อง Cloudflare** — ถามอะไรก็ได้เกี่ยวกับ Workers, Pages, D1, R2, KV และ agent จะดึง docs ล่าสุดมาตอบ
4. **ตรวจสอบ Performance** — บอกว่า "วิเคราะห์ performance ของเว็บ" แล้ว agent จะใช้ web-perf skill
5. **Deploy** — ใช้ Wrangler commands ได้โดยตรง agent จะช่วยตรวจสอบความถูกต้อง

หากต้องการเริ่มใช้งานอะไร บอกได้เลยครับ!

