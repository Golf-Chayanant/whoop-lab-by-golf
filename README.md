# 🛏️ Sleep Expert Starter — สร้างคลังความรู้ "การนอน" ด้วย Claude Code + Obsidian

เทมเพลตสำหรับให้ **Claude Code** เป็น "ผู้เชี่ยวชาญเรื่องการนอน" ส่วนตัวของคุณ
โดยกลั่นความรู้จากคลิป YouTube คุณภาพสูง (Huberman, Matthew Walker ฯลฯ) มาเก็บเป็น
**Obsidian wiki** (เทคนิค LLM Wiki สไตล์ Karpathy) แล้วให้ Claude ใช้เป็นแหล่งอ้างอิงเวลาให้คำแนะนำ

> 📘 **เพิ่งเริ่ม? อ่าน [SETUP.md](SETUP.md)** — ทำตามได้เลย **ไม่ต้องรู้จัก git ไม่ต้องแตะ Terminal**
> (แค่กด **Code → Download ZIP** แล้วเปิดโฟลเดอร์ใน Claude Code)

## Workflow แบบย่อ
```
1. หาความรู้   → เอา link YouTube ใส่ NotebookLM → copy transcript
2. วาง         → paste transcript ให้ Claude (หรือวางไฟล์ใน inbox/)
3. /ingest     → Claude clean + สรุป + สร้างโน้ตใน vault/
4. /wiki-link  → เชื่อมโน้ต + อัปเดตภาพรวม (MOC)
5. /advise ... → ถามขอคำแนะนำ Claude ตอบพร้อมอ้างอิงโน้ต
```

## มีอะไรในเทมเพลตนี้
| ส่วน | หน้าที่ |
|------|---------|
| `CLAUDE.md` | กติกา + บทบาท "ผู้เชี่ยวชาญการนอน" (Claude Code โหลดอัตโนมัติ) |
| `.claude/commands/` | slash commands: `/ingest` `/wiki-link` `/advise` |
| `vault/` | Obsidian vault — คลังความรู้ (เริ่มต้นว่าง) |
| `vault/templates/` | แม่แบบโน้ต (source / concept / protocol) |
| `data/` | (Phase 2) พื้นที่ข้อมูลการนอนจริง เช่น Whoop |

## อยากเปลี่ยนหัวข้อจาก "การนอน" เป็นเรื่องอื่น?
เทมเพลตนี้ใช้ได้กับความรู้ทุกแขนง (การเทรด, โภชนาการ, ฯลฯ) — แค่แก้ `CLAUDE.md`
(บทบาท + ศัพท์เทคนิค) กับชื่อโฟลเดอร์/MOC ให้ตรงหัวข้อใหม่ ส่วน workflow เหมือนเดิม

## เครดิต
สร้างด้วย [Claude Code](https://claude.com/claude-code) · แนวคิด LLM Wiki จาก Andrej Karpathy
