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
                <td>สุธีมนต์ วงศ์พระราม</td>
            </tr>
            <tr>
                <td>อายุ</td>
                <td>20 ปี</td>
            </tr>
            <tr>
                <td>สาขา</td>
                <td>เทคโนโลยีคอมพิวเตอร์</td>
            </tr>
            <tr>
                <td>งานอดิเรก</td>
                <td>เล่นเกม ฟังเพลง</td>
            </tr>
        </tbody>
    </table>

    <h2>เมนูอาหาร</h2>

    <h3>เมนูแนะนำ (ไม่เรียงลำดับ)</h3>
    <ul>
        <li>ข้าวผัด</li>
        <li>ก๋วยเตี๋ยว</li>
        <li>ส้มตำ</li>
    </ul>

    <h3>เมนูยอดนิยม (เรียงลำดับ)</h3>
    <ol>
        <li>ต้มยำกุ้ง</li>
        <li>ผัดไทย</li>
        <li>หมูทอดกระเทียม</li>
    </ol>

    <h3>เครื่องดื่ม</h3>
    <dl>
        <dt>ชาเย็น</dt>
        <dd>ชาหวานเย็นใส่นม</dd>

        <dt>กาแฟ</dt>
        <dd>กาแฟร้อนหรือเย็นตามชอบ</dd>

```
- ภาพผลลัพธ์:
[วางภาพ screenshot ที่นี่]![alt text](../image/ผลการทดลองLab5.png)

