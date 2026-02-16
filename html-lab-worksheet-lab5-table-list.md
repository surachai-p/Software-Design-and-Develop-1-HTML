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
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <table border="1">
    <thead>
        <tr>
            <th>ชื่อ</th>
            <th>นามสกุล</th>
            <th>ชื่อเล่น</th>
            <th>อายุ</th>
            <th>รหัสนักศึกษา</th>
            <th>คณะ</th>
            <th>สาขา</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>นัทธพงศ์</td>
            <td>เหมือนประสาน</td>
            <td>นัทธ</td>
            <td>19</td>
            <td>68030135</td>
            <td>ครุศาสตร์อุสาหกรรและเทคโนโลยี</td>
            <td>เทคโนโลยีคอมพิวเตอร์</td>
        </tr>
    </tbody>
</table>

<ul>
    <li>อาหาร</li>
</ul>

<ol>
    <li>ข้าวผัดหมู</li>
    <li>กะเพราไก่</li>
    <li>ผัดไทย</li>
    <li>กะเพราไข่เยี่ยวม้า</li>
    <li>หมูกรอบผัดพริกแกง</li>
    <li>สุกี้ทะเล</li>
    <li>ราดหน้าหมู</li>
</ol>

<ul>
    <li>เครื่องดื่ม</li>
</ul>

<ol>
    <li>น้ำเปล่า</li>
    <li>น้ำอัดลม</li>
    <li>น้ำผลไม้</li>
    <li>กาแฟ</li>
    <li>ชา</li>
</ol>

<dl>
    <dt>สโลแกน</dt>
    <dd>อร่อยถูกใจอนามัยถูกลืม</dd>
    <dt>รสชาติ</dt>
    <dd>อร่อยไม่ซ้ำจำสูตรไม่ได้</dd>
</dl>
</body>
</html>
```
- ภาพผลลัพธ์:
![alt text](image-6.png)

