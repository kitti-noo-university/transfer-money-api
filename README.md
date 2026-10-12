# Transfer Money API (Robot Framework)

ชุดทดสอบ API สำหรับกรณีการโอนเงิน พัฒนาด้วย Robot Framework โดยแยกโครงสร้าง test case, keyword และ resources ออกจากกัน เพื่อให้ดูแลและขยายต่อได้ง่าย

## Project Overview
โปรเจกต์นี้เน้นการทดสอบ API ในโดเมนการโอนเงิน (Transfer Money) โดยรองรับการจัดการ test data และ reusable keywords เพื่อใช้ซ้ำในหลายสถานการณ์ทดสอบ

## Repository Structure
- `testcases/` — เก็บไฟล์ test suites ของ Robot Framework
- `keywords/` — เก็บ custom keywords
- `resources/` — เก็บ resource files ที่ใช้ร่วมกัน
- `import.resource` — ไฟล์รวม imports ที่ใช้ในหลาย test suites
- `requirements.txt` — dependencies สำหรับรันเทสต์

## Prerequisites
- Python 3.9+ (แนะนำ)
- pip
- Robot Framework libraries ตามที่ระบุใน `requirements.txt`

## Recommended Tools
- Visual Studio Code
  - Extension: **Robot Framework Language Server**
  - Extension: **Python Extension Pack**

## Installation
1. Clone repository
2. Create virtual environment
   - macOS / Linux
     ```bash
     python3 -m venv venv
     ```
   - Windows
     ```powershell
     python -m venv venv
     ```
3. Activate virtual environment
   - macOS / Linux
     ```bash
     source venv/bin/activate
     ```
   - Windows (PowerShell)
     ```powershell
     .\venv\Scripts\Activate.ps1
     ```
4. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```

## Run Tests
รันเทสต์หลักและเก็บผลลัพธ์ไว้ในโฟลเดอร์ `result`:

```bash
robot -d result testcases/transfer_money_api.robot
```

## Test Output
หลังรันเสร็จ Robot Framework จะสร้างไฟล์สำคัญ เช่น:
- `result/log.html`
- `result/report.html`
- `result/output.xml`

## Notes
- หากมีหลาย environment (เช่น dev / staging / prod) แนะนำให้แยกตัวแปร config เป็น resource file ตาม environment
- ควรตั้งชื่อ test cases ให้สื่อ business scenario เพื่อให้อ่าน report ได้ง่าย

## License
ยังไม่ได้ระบุ License ใน repository นี้
