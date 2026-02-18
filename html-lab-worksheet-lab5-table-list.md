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

[วางโค้ด HTML ที่นี่]
```<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <title>ข้อมูลส่วนตัวและเมนูอาหาร</title>
</head>
<body>

    <h2>1. ข้อมูลส่วนตัว</h2>
    <table border="1" cellpadding="8" cellspacing="0">
        <thead>
            <tr>
                <th>หัวข้อ</th>
                <th>รายละเอียด</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>ชื่อ</td>
                <td>วัฒนพงศ์</td>
            </tr>
            <tr>
                <td>นามสกุล</td>
                <td>พรหมภิราม</td>
            </tr>
            <tr>
                <td>อายุ</td>
                <td>19 ปี</td>
            </tr>
            <tr>
                <td>วัน/เดือน/ปีเกิด</td>
                <td>18 ตุลาคม 2549</td>
            </tr>
        </tbody>
    </table>

    <hr>

    <h2>2. รายการเมนูอาหาร</h2>
    
    <ul>
        <li><strong>เมนูข้าว</strong>
            <ul>
                <li>ข้าวหมูแดง</li>
                <li>ข้าวหมูกรอบ</li>
                <li>ข้าวขาหมู</li>
            </ul>
        </li>
        <br>
        <li><strong>เมนูเส้น</strong>
            <ul>
                <li>ผัดซีอิ้ว</li>
                <li>ผัดหมี่โคราช</li>
                <li>ผัดไท</li>
            </ul>
        </li>
    </ul>

</body>
</html>
```
- ภาพผลลัพธ์:
[![alt text](image-4.png)]

