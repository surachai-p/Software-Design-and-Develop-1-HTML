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
    <title>Document</title>
</head>
<body>
    <table border="1">
        <thead>
            <tr>
                <th>ข้อมูลส่วนตัว</th>
                <th>Header 2</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>หัวข้อราย</td>
                <td>รายละเอียด</td>
            </tr>
            <tr>
                <td>ชื่อ</td>
                <td>นางสาวปภัสสร เอี่ยมสอาด</td>
            <tr>
                <td>รหัสประจำตัวนักศึกษา</td>
                <td>67030311</td>
            </tr>
            <tr>
                <td>คณะครุศาสตร์อุตสาหกรรมและเทคโนโลยี</td>
                <td>สาขาเทคโนโลยีคอมพิวเตอร์</td>
            </tr>
                <td>อายุ 20 ปี</td>
            </tr>
            <tr>
                <td>วัน/เดือน/ปีเกิด</td>
                <td>25 พฤศจิกายน ปี พ.ศ 2547</td>
            </tr>
            </tr>
        </tbody>
    </table>
            <h1>เมนูอาหารที่ชอบ</h1>
            <ul>
                <li>กะเพรา</li>
                <li>ข้าวผัด</li>
            </ul>
            
            <ol>
                <li>ยำวุ้นเส้น</li>
                <li>ข้าวไข่เจียว</li>
            </ol>
</body>
</html>
```
- ภาพผลลัพธ์:
[วางภาพ screenshot ที่นี่]
![lab05](https://github.com/user-attachments/assets/24b2459d-ca91-4dfa-9447-4567eae41c32)
