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
<html>
<head>
    <title>Table and List Example</title>
</head>
<body>
    <table border="1">
        <thead>
            <tr>
                <th>Field</th>
                <th>Value</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>ชื่อ-นามสกุล</td>
                <td>ทีฆทัศน์ พินิจทรัพย์</td>
            </tr>
            <tr>
                <td>วันเกิด</td>
                <td>20 กุมภาพันธ์ พ.ศ. 2550</td>
            </tr>
            <tr>
                <td>งานอดิเรก</td>
                <td>เล่นกีต้า, เล่นเกม, สร้างเว็บไซต์, ออกแบบ</td>
            </tr>
            <tr>
                <td>เป้าหมาย</td>
                <td>สร้างจรวดเพื่อไปดาวอังคาร</td>
            </tr>
        </tbody>
    </table>

    <ul>
        <li>เมนูอาหาร 1</li>
        <li>เมนูอาหาร 2</li>
    </ul>

    <ol>
        <li>Ordered item 1</li>
        <li>Ordered item 2</li>
    </ol>

    <dl>
        <dt>Term 1</dt>
        <dd>Definition 1</dd>
    </dl>
</body>
</html>

```
- ภาพผลลัพธ์:
[วางภาพ screenshot ที่นี่]
![alt text](image-4.png)
