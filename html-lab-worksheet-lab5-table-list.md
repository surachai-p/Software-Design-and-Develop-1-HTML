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
    <title>Table and List Example</title>
</head>
<body>

    <h2>ตารางข้อมูลส่วนตัว</h2>
    <table border="1">
        <thead>
            <tr>
                <th>หัวข้อ</th>
                <th>ข้อมูล</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>ชื่อ</td>
                <td>พัชรพล กลิ่นอ่อน</td>
            </tr>
            <tr>
                <td>อายุ</td>
                <td>18 ปี</td>
            </tr>
            <tr>
                <td>อาชีพ</td>
                <td>นักศึกษา นักล่าปริญา</td>
            </tr>
            <tr>
                <td>ที่อยู่</td>
                <td>กรุงเทพมหานคร</td>
            </tr>
        </tbody>
    </table>

    <h2> เมนูอาหาร</h2>
    <ul>
        <li>กระเพราหมูสับไข่ดาว - 50 บาท</li>
        <li>กระเพราหมูกรอบไข่ดาว - 75 บาท</li>
        <li>กระเพราปลาหมึกไข่ดาว - 80 บาท</li>
        <li>กระเพราเครื่องในไก่ไข่ดาว - 65 บาท</li>
    </ul>

    <h2> รายการสั่งอาหาร</h2>
    <ul>
        <li><b>เด็กชาย1</b> - กระเพราปลาหมึกไข่ดาว</li>
        <li><b>เด็กชาย2</b> - กระเพราเครื่องในไก่ไข่ดาว </li>
    </ul>

</body>
</html>

```html

```
- ภาพผลลัพธ์:
- ![image](https://github.com/user-attachments/assets/603450b4-27f1-4128-b857-87d0fc01f7d8)

[วางภาพ screenshot ที่นี่]

