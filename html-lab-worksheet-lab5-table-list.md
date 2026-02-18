# ใบงานการทดลอง HTML

## การทดลองที่ 5: การสร้างตารางและรายการ
### วัตถุประสงค์
- เรียนรู้การสร้างตารางข้อมูล
- เรียนรู้การสร้างรายการแบบต่างๆ

### ขั้นตอนการทดลอง
1. สร้างไฟล์ tablelist.html ดังตัวอย่าง:
```html
<table border="1">
    <thead>
        <tr>
            <th>Header 1</th>
            <th>Header 2</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Row 1, Cell 1</td>
            <td>Row 1, Cell 2</td>
        </tr>
        <tr>
            <td>Row 2, Cell 1</td>
            <td>Row 2, Cell 2</td>
        </tr>
    </tbody>
</table>
```

### คำอธิบายเพิ่มเติม
- `<table>` กำหนดขอบเขตของตาราง
- `<thead>` สำหรับส่วนหัวตาราง
- `<tbody>` สำหรับเนื้อหาตาราง
- `<tr>` แทนแถว
- `<th>` แทนเซลล์หัวตาราง
- `<td>` แทนเซลล์ข้อมูล

2. การสร้างรายการ โดยเพิ่มเติม Code ในไฟล์ tablelist.html :
```html
<ul>
    <li>Unordered item 1</li>
    <li>Unordered item 2</li>
</ul>

<ol>
    <li>Ordered item 1</li>
    <li>Ordered item 2</li>
</ol>

<dl>
    <dt>Term 1</dt>
    <dd>Definition 1</dd>
    <dt>Term 2</dt>
    <dd>Definition 2</dd>
</dl>
```

### คำอธิบายเพิ่มเติม
- `<ul>` สำหรับรายการแบบไม่เรียงลำดับ
- `<ol>` สำหรับรายการแบบเรียงลำดับ
- `<dl>` สำหรับรายการแบบคำจำกัดความ
- `<li>` แทนรายการแต่ละรายการ

### แบบฝึกหัด
1. สร้างตารางแสดงข้อมูลส่วนตัว
2. สร้างรายการเมนูอาหาร

[<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <title>การทดลองที่ 5: การสร้างตารางและรายการ</title>
    <style>
        table {
            width: 50%;
            border-collapse: collapse;
            margin-bottom: 20px;
        }
        th, td {
            padding: 8px;
            text-align: left;
        }
    </style>
</head>
<body>

    <h1>การสร้างตารางและรายการ</h1>

    <h2>1. ตารางแสดงข้อมูลส่วนตัว</h2>
    <table border="1">
        <thead>
            <tr>
                <th>หัวข้อ</th>
                <th>รายละเอียด</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>ชื่อ-นามสกุล</td>
                <td>นางสาวณัฏฐวรรณ ช่างเก็บ</td>
            </tr>
            <tr>
                <td>สถาบันการศึกษา</td>
                <td>สถาบันเทคโนโลยีพระจอมเกล้าเจ้าคุณทหารลาดกระบัง</td>
            </tr>
            <tr>
                <td>สาขาวิชา</td>
                <td>เทคโนโลยีคอมพิวเตอร์</td>
            </tr>
            <tr>
                <td>ความเชี่ยวชาญ</td>
                <td>figma , UX/UI</td>
            </tr>
        </tbody>
    </table>

    <hr>

    <h2>2. รายการเมนูอาหาร (Food Menu)</h2>
    
    <h3>รายการอาหารแนะนำ (Unordered List)</h3>
    <ul>
        <li>ผัดไทยกุ้งสด</li>
        <li>ก๋วยเตี๋ยวเส้นเล็กต้มยำ</li>
        <li>ส้มไทยข้าวโพด</li>
    </ul>

    <h3>ขั้นตอนการสั่งอาหาร (Ordered List)</h3>
    <ol>
        <li>เลือกเมนูอาหารที่ต้องการ</li>
        <li>ระบุจำนวนและรายละเอียดเพิ่มเติม</li>
        <li>ยืนยันการสั่งซื้อและชำระเงิน</li>
    </ol>

    <h3>คำจำกัดความของประเภทอาหาร (Definition List)</h3>
    <dl>
        <dt>อาหารตามสั่ง</dt>
        <dd>อาหารที่ปรุงขึ้นใหม่ตามคำสั่งของผู้ซื้อ</dd>
        <dt>Fast Food</dt>
        <dd>อาหารที่เน้นความรวดเร็วในการบริการและเตรียมการ</dd>
    </dl>

</body>
</html>]
```html

```
- ภาพผลลัพธ์:
[Lab05\05.png]

