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
    <title> Table and list</title>
</head>
<body>

<body>

    <h1>ตารางข้อมูลส่วนตัว</h1>
    <table border="1">
        <thead>
            <tr>
                <th>ข้อมูลส่วนตัวของฉัน</th>
                <th>นาย รัฐภูมิ สอนเขียว</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>ชื่อ</td>
                <td>รัฐภูมิ สอนเขียว</td>
            </tr>
            <tr>
                <td>อายุ</td>
                <td>19</td>
            </tr>
            <tr>
                <td>ที่อยู่</td>
                <td>15 ซอย สามัคคีพัฒนา 13 หัวหมาก บางกะปิ กรุงเทพ 10240</td>
            </tr>
            <tr>
                <td>อีเมล</td>
                <td>67030338@kmitl.ac.th</td>
            </tr>
        </tbody>
    </table>

    <hr>

    <h1>รายการเมนูอาหาร</h1>

    <h2>รายการอาหารที่แนะนำ</h2>
    <ul>
        <li>ข้าวผัดกุ้ง</li>
        <li>ต้มยำกุ้ง</li>
        <li>ผัดไทย</li>
        <li>แกงเขียวหวาน</li>
        <li>ส้มตำ</li>
        <li>ไก่ทอด</li>
    </ul>

   


</body>
</html>

```
- ภาพผลลัพธ์:
[วางภาพ screenshot ที่นี่]

![tl](https://github.com/user-attachments/assets/73aa1529-9ab6-45fa-b8c4-37602bb5a594)
