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
```html
<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <title>Table and List</title>
</head>
<body>
    <h2>ตารางข้อมูลส่วนตัว</h2>

    <table border="1" cellpadding="8">
        <tr>
            <th>หัวข้อ</th>
            <th>ข้อมูล</th>
        </tr>
        <tr>
            <td>ชื่อ-นามสกุล</td>
            <td>ณภัทร สิงห์ตุ้ย</td>
        </tr>
        <tr>
            <td>อายุ</td>
            <td>19 ปี</td>
        </tr>
        <tr>
            <td>สาขา</td>
            <td>เทคโนโลยีคอมพิวเตอร์</td>
        </tr>
        <tr>
            <td>อีเมล</td>
            <td>68030080@kmitl.ac.th</td>
        </tr>
    </table>

    <hr>

    <h2>ตารางเมนูอาหาร</h2>

<table border="1" cellpadding="8">
    <tr>
        <th>ลำดับ</th>
        <th>ชื่อเมนู</th>
        <th>ประเภท</th>
        <th>ราคา (บาท)</th>
    </tr>

    <tr>
        <td>1</td>
        <td>ข้าวผัด</td>
        <td>อาหารจานเดียว</td>
        <td>50</td>
    </tr>

    <tr>
        <td>2</td>
        <td>ผัดกะเพรา</td>
        <td>อาหารจานเดียว</td>
        <td>55</td>
    </tr>

    <tr>
        <td>3</td>
        <td>ต้มยำกุ้ง</td>
        <td>อาหารประเภทต้ม</td>
        <td>120</td>
    </tr>

    <tr>
        <td>4</td>
        <td>ส้มตำ</td>
        <td>อาหารอีสาน</td>
        <td>40</td>
    </tr>

    <tr>
        <td>5</td>
        <td>ชาเย็น</td>
        <td>เครื่องดื่ม</td>
        <td>30</td>
    </tr>
</table>

```
- ภาพผลลัพธ์:
[![alt text](image-5.png)]

