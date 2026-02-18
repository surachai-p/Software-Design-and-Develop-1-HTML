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
    <title>ตารางข้อมูล</title>
</head>

<body>
    <h2>ตารางแสดงข้อมูลส่วนตัว</h2>
<table border="1">

    <thead>
        <tr>
            <th>รหัสนักศึกษา</th>
            <th>ชื่อ</th>
            <th>นามสกุล</th>
        </tr>
    </thead>

    <tbody>
        <tr>
            <td>68030250</td>
            <td>วชิระพล</td>
            <td>สิริอิสสระนันท์</td>
        </tr>
    </tbody>
</table>

<h2>รายการเมนูร้านอาหาร</h2>
    <ul>
        <li>ปีกไก่ทอดเกลือ</li>
        <li>เฟรนช์ฟรายส์ชีส</li>
    </ul>

    <ol>
        <li>ข้าวผัดกะเพราเนื้อไข่ดาว</li>
        <li>เส้นใหญ่ผัดซีอิ๊วหมู</li>
    </ol>

    <dl>
        <dt>อาหารประเภทต้ม</dt>
        <dd>ต้มจืดเต้าหู้หมูสับ</dd>
        <dt>อาหารประเภทผัด</dt>
        <dd>ไก่ผัดเม็ดมะม่วงหิมพานต์</dd>
        <dt>อาหารประเภทแกง</dt>
        <dd>แกงมัสมั่นเนื้อ</dd>
    </dl>

</body>
</html>
```
- ภาพผลลัพธ์:
![screenshot-lab5](../images/screenshots/lab5.png)

