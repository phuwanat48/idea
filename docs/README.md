# AI Team Starter (OpenCode)

ชุดตั้งต้นทีม AI agent 10 บทบาทตาม workflow diagram

## วิธีใช้ (Windows 11)
1. คัดลอกทุกอย่างในโฟลเดอร์นี้ (`.opencode`, `docs`, `tests`, `AGENTS.md`, `opencode.json`) ไปไว้ในโฟลเดอร์โปรเจกต์ของคุณ
2. เปิดเทอร์มินัลในโฟลเดอร์โปรเจกต์ แล้วรัน `opencode`
3. ตรวจว่า agent ครบ: `opencode agent list` หรือพิมพ์ `@` ในช่องแชต
4. ตรวจว่าอยู่ใน agent `orchestrator` (กด Tab เพื่อสลับ) แล้วสั่งงาน เช่น
   > ทำเว็บ todo list ที่เพิ่ม/ลบ/ติ๊กเสร็จได้ เก็บข้อมูลใน localStorage

## ถ้า orchestrator เรียก subagent เองไม่ได้
(บางเวอร์ชันมีบั๊ก custom primary agent ไม่มี task tool)
- ลองอัปเดต OpenCode เป็นเวอร์ชันล่าสุด
- หรือสั่งมือทีละขั้น: `@pm ...` → `@ux ...` → `@architect ...` → `@sa ...` → `@dev ...` → `@security ...` → `@qa ...` → `@devops ...` → `@writer ...`
- หรือสลับไปใช้ agent `build` แล้วบอกให้ทำตามลำดับใน AGENTS.md

## ปรับแต่ง
- ระบุ `model:` ในไฟล์ agent เพื่อกำหนดโมเดลแต่ละตัว (เช่น ใช้โมเดลถูกให้ writer)
- ปรับสิทธิ์ที่ `permission:` ในแต่ละไฟล์
