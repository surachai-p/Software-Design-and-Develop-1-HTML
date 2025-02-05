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
<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ข้อมูลส่วนตัว</title>
</head>
<body>
    <h2>ข้อมูลส่วนตัว</h2>
    <table border="1">
        <tr>
            <th>หัวข้อ</th>
            <th>ข้อมูล</th>
        </tr>
        <tr>
            <td>ชื่อ</td>
            <td>ปิยะวิทย์ พลศรี</td>
        </tr>
        <tr>
            <td>อายุ</td>
            <td>21 ปี</td>
        </tr>
        <tr>
            <td>อีเมล</td>
            <td>PpeePiyawit9@gmail.com</td>
        </tr>
        <tr>
            <td>ที่อยู่</td>
            <td>1212312121 KMITL กรุงเทพมหานคร</td>
        </tr>
    </table>

    <h2>เมนูอาหาร</h2>
    <ul>
        <li>สเต็กหนอนด้วง</li>
        <li>ข้าวผัดแมลงทอด</li>
        <li>ซุปปูทะเลเสือดาว</li>
        <li>ผัดหมึกยักษ์กับมะพร้าวเผา</li>
        <li>ส้มตำทุเรียน</li>
        <li>ไข่หวานผสมปลาหมึกดำ</li>
        <li>ขนมจีบไส้หนอนผีเสื้อ</li>
        <li>เส้นหมี่ผัดหอยทากกับใบสะระแหน่</li>
        <li>ข้าวเหนียวปลาหมึกย่างสอดไส้ถั่วแดง</li>
        <li>ไก่ย่างกรอบผสมถั่วแระญี่ปุ่น</li>
    </ul>
</body>
</html>
- ภาพผลลัพธ์:
![alt text](image-7.png)