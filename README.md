# ACTIVE PLAY AR – Phase 1

สื่อการเรียนรู้แบบ Interactive สำหรับ ป.5 ตามนวัตกรรม Active Play ใช้กล้องและ AI Hand/Pose Tracking เพื่อให้ผู้เรียนเคลื่อนไหวจริง และเก็บผลการเล่นสำหรับใช้วิเคราะห์ PA

## ไฟล์
- `index.html` — หน้าเริ่มสำหรับนักเรียน, การตรวจความพร้อม, เกม และผลลัพธ์

## สถานะ: Phase 1

- เก็บชั้น ห้อง เลขที่ ชื่อ และรหัสนักเรียน (หากมี)
- ตรวจกล้อง การพบร่างกาย และการพบมือก่อนเริ่ม
- บันทึกผล Session, Mission และ Movement ในรูปแบบที่พร้อมส่งต่อ
- ไม่เก็บภาพ วิดีโอ หรือข้อมูล pose รายเฟรม
- หากยังไม่กำหนด Google Apps Script URL จะเก็บข้อมูลชั่วคราวใน `localStorage`

## เชื่อม Google Sheets

หลัง Deploy Google Apps Script Web App ให้ใส่ URL ในตัวแปร `APPS_SCRIPT_URL` ภายใน `index.html` เพื่อส่งข้อมูลผ่าน Apps Script แทนการเขียน Google Sheet โดยตรง

ไฟล์ [google-apps-script/Code.gs](google-apps-script/Code.gs) สร้างชีตฐานข้อมูลทั้ง 6 ชีตตาม Project Brief และรับข้อมูล Session, Mission และ Movement จากเกม

## วิธีนำขึ้น GitHub Pages
1. สร้าง Repository แบบ Public เช่น `active-play-ar`
2. อัปโหลด `index.html` เข้า Repository
3. ไปที่ Settings → Pages
4. เลือก Deploy from a branch → `main` → `/ (root)` → Save
5. เปิด URL ที่ GitHub Pages สร้างให้

## สำคัญ
เกมต้องทำงานผ่าน HTTPS หรือ localhost เพื่อขอสิทธิ์กล้อง
เกมรุ่นนี้โหลด MediaPipe และโมเดลจาก CDN/Google Storage จึงต้องมีอินเทอร์เน็ต
ควรทดสอบบน Chrome/Edge และ Safari รุ่นปัจจุบันก่อนนำไปใช้จริง

## ขั้นต่อไปที่แนะนำ
- ระบบรายชื่อนักเรียน/รหัสนักเรียน
- บันทึกคะแนน เวลา และจำนวนครั้งของแต่ละภารกิจ
- Dashboard สำหรับครู
- QR Code เข้าเกม
- โหมดเล่นเป็นทีม
- ปรับเกณฑ์การตรวจจับท่าทางให้เหมาะกับนักเรียน ป.5
