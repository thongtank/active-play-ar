# ACTIVE PLAY AR – Prototype

สื่อการเรียนรู้แบบ Interactive สำหรับทดสอบแนวคิด Active Play ด้วยกล้องและ AI Hand/Pose Tracking

## ไฟล์
- `index.html` — หน้าเกมหลัก

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
