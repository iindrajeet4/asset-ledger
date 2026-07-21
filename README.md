# Asset Ledger

[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE) [![Live Demo](https://img.shields.io/badge/demo-live-blue.svg)](https://iindrajeet4.github.io/asset-ledger/) [![Dependencies](https://img.shields.io/badge/dependencies-none-brightgreen.svg)](#)

A lightweight, 100% client-side IT asset tracker for small multi-branch businesses.
One HTML file, no server, no build step, no dependencies — open `index.html` in any modern browser.

**[🔗 Live Demo / ลองใช้เลย](https://iindrajeet4.github.io/asset-ledger/)**

## Getting started

1. Try it instantly at **https://iindrajeet4.github.io/asset-ledger/**, or download / clone this repository.
2. Open `index.html` in any modern browser (Chrome, Edge, Firefox, Safari).
3. Click **Demo data** to explore, or **+ Add asset** to start your own ledger.

No installation, no account, no internet connection required.

## Features

- **Asset CRUD** — name, category (Laptop / Desktop / Phone / Tablet / Printer / Scale / POS / Other), serial number, assigned person, branch/location, purchase date, warranty expiry, price, status (In use / In stock / Repair / Retired), notes.
- **Table view** — full-text search plus branch, category, and status filters; click any column header to sort.
- **Summary cards** — total assets, assets in repair, warranties expiring within 60 days (including already expired), and total asset value.
- **Warranty highlighting** — expired warranties shown in red, warranties expiring within 60 days in amber.
- **Printable asset labels** — each asset has a label modal (name, branch, serial) with a **Code 128-B barcode** rendered as SVG, ready to print. *Design note: a Code 128 barcode was chosen instead of a QR code because it can be implemented compactly and verifiably in vanilla JS (standard 106-entry module-width table + checksum). Serials must be ASCII (letters, digits, dashes, etc., up to 40 chars); non-ASCII serials fall back to a clean framed text label.*
- **Import / Export** — JSON backup and restore (replace or merge; imported records are validated and sanitized), and CSV export with UTF-8 BOM so Thai text opens correctly in Excel.
- **Robust storage** — corrupt localStorage data is ignored safely instead of breaking the app, and you are warned if the browser cannot save (e.g. storage full).
- **Form validation** — required name, non-negative prices, and a check that warranty expiry is not before the purchase date.
- **Bilingual** — English / Thai toggle (persisted), full UI translation.
- **Dark / light theme** — persisted, clean admin-panel design.
- **Demo data** — one click loads 8 sample assets across 3 branches.

## Privacy

All data is stored in your browser's `localStorage` and **never leaves your computer**. There are no accounts, no network requests, and no tracking.

## Backup advice

Because data lives only in the browser:

- Click **Backup JSON** regularly and keep the file somewhere safe (shared drive, cloud folder).
- Clearing browser data / site data will erase the ledger — restore from your latest JSON backup via **Import JSON**.
- Each browser profile and each computer has its own separate ledger; use JSON export/import to move data between machines.

## License

MIT — see [LICENSE](LICENSE).

---

# Asset Ledger (ภาษาไทย)

ระบบสมุดทะเบียนทรัพย์สินไอทีแบบเบา ๆ สำหรับธุรกิจขนาดเล็กที่มีหลายสาขา
ทำงานฝั่งเบราว์เซอร์ 100% ไฟล์ HTML ไฟล์เดียว ไม่ต้องมีเซิร์ฟเวอร์ ไม่ต้องติดตั้งอะไร — เปิด `index.html` ในเบราว์เซอร์รุ่นใหม่ได้เลย

## เริ่มต้นใช้งาน

1. ลองใช้ได้ทันทีที่ **https://iindrajeet4.github.io/asset-ledger/** หรือดาวน์โหลด/clone โปรเจกต์นี้
2. เปิดไฟล์ `index.html` ในเบราว์เซอร์รุ่นใหม่ (Chrome, Edge, Firefox, Safari)
3. กด **ข้อมูลตัวอย่าง** เพื่อทดลองใช้ หรือกด **+ เพิ่มทรัพย์สิน** เพื่อเริ่มบันทึกของคุณเอง

ไม่ต้องติดตั้ง ไม่ต้องสมัครบัญชี และไม่ต้องต่ออินเทอร์เน็ต

## ฟีเจอร์

- **เพิ่ม/แก้ไข/ลบทรัพย์สิน** — ชื่อ, หมวดหมู่ (โน้ตบุ๊ก / เดสก์ท็อป / โทรศัพท์ / แท็บเล็ต / ปริ้นเตอร์ / เครื่องชั่ง / POS / อื่น ๆ), หมายเลขซีเรียล, ผู้ใช้งาน, สาขา/สถานที่, วันที่ซื้อ, วันหมดประกัน, ราคา, สถานะ, หมายเหตุ
- **ตารางข้อมูล** — ค้นหาได้ทุกช่อง พร้อมตัวกรองสาขา หมวดหมู่ สถานะ และคลิกหัวตารางเพื่อเรียงลำดับ
- **การ์ดสรุป** — ทรัพย์สินทั้งหมด, กำลังซ่อม, ประกันที่จะหมดภายใน 60 วัน (รวมที่หมดแล้ว), มูลค่ารวม
- **ไฮไลต์ประกัน** — ประกันหมดอายุแสดงสีแดง ใกล้หมด (ภายใน 60 วัน) แสดงสีเหลืองอำพัน
- **ป้ายทรัพย์สินพร้อมพิมพ์** — แต่ละรายการมีป้าย (ชื่อ, สาขา, ซีเรียล) พร้อม **บาร์โค้ด Code 128-B** แบบ SVG *หมายเหตุการออกแบบ: เลือกใช้บาร์โค้ด Code 128 แทน QR code เพราะสามารถเขียนด้วย JavaScript ล้วนได้อย่างกะทัดรัดและตรวจสอบความถูกต้องได้ ซีเรียลต้องเป็นอักขระ ASCII (ตัวอักษรอังกฤษ ตัวเลข ขีด ฯลฯ ไม่เกิน 40 ตัว) หากไม่ใช่ ระบบจะแสดงป้ายข้อความในกรอบแทน*
- **นำเข้า / ส่งออก** — สำรองและกู้คืนข้อมูลเป็น JSON (เลือกแทนที่หรือรวมได้ พร้อมตรวจสอบและกรองข้อมูลที่นำเข้า) และส่งออก CSV พร้อม UTF-8 BOM เพื่อให้เปิดภาษาไทยใน Excel ได้ถูกต้อง
- **จัดเก็บข้อมูลอย่างปลอดภัย** — ข้อมูลที่เสียหายใน localStorage จะถูกข้ามโดยไม่ทำให้แอปพัง และมีการแจ้งเตือนหากเบราว์เซอร์บันทึกไม่สำเร็จ (เช่น พื้นที่เต็ม)
- **ตรวจสอบฟอร์ม** — ต้องกรอกชื่อ ราคาต้องไม่ติดลบ และวันหมดประกันต้องไม่อยู่ก่อนวันที่ซื้อ
- **สองภาษา** — สลับอังกฤษ / ไทยได้ และระบบจำค่าที่เลือกไว้
- **ธีมมืด / สว่าง** — จำค่าที่เลือกไว้ ดีไซน์แบบแผงผู้ดูแลระบบที่สะอาดตา
- **ข้อมูลตัวอย่าง** — คลิกเดียวโหลดทรัพย์สินตัวอย่าง 8 รายการจาก 3 สาขา

## ความเป็นส่วนตัว

ข้อมูลทั้งหมดถูกเก็บใน `localStorage` ของเบราว์เซอร์ และ**ไม่ถูกส่งออกไปที่ไหนเลย** ไม่มีบัญชีผู้ใช้ ไม่มีการเชื่อมต่ออินเทอร์เน็ต ไม่มีการติดตามใด ๆ

## คำแนะนำการสำรองข้อมูล

เนื่องจากข้อมูลอยู่ในเบราว์เซอร์เท่านั้น:

- กด **สำรอง JSON** เป็นประจำ และเก็บไฟล์ไว้ในที่ปลอดภัย (ไดรฟ์ส่วนกลางหรือคลาวด์)
- การล้างข้อมูลเบราว์เซอร์จะทำให้ข้อมูลหายทั้งหมด — กู้คืนได้จากไฟล์สำรองล่าสุดผ่านปุ่ม **นำเข้า JSON**
- แต่ละเบราว์เซอร์และแต่ละเครื่องมีข้อมูลแยกกัน ใช้การส่งออก/นำเข้า JSON เพื่อย้ายข้อมูลระหว่างเครื่อง

## สัญญาอนุญาต

MIT — ดูไฟล์ [LICENSE](LICENSE)
