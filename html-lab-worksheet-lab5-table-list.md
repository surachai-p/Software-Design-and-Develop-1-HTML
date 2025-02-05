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
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>ข้อมูลส่วนตัว</h1>
    <table border="1">
        <thead>
            <tr>
                <th>หัวข้อ</th>
                <th>รายละเอียด</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>ชื่อ</td>
                <td>นายวัทธิกร อินทองคำ</td>
            </tr>
            <tr>
                <td>รหัสประจำตัวนักศึกษา</td>
                <td>67030207</td>
            </tr>
            <tr>
                <td>คณะ</td>
                <td>ครุศาสตร์อุตสาหกรรมและเทคโนโลยี</td>
            </tr>
            <tr>
                <td>สาขา</td>
                <td>เทคโนโลยีคอมพิวเตอร์</td>
            </tr>
            <tr>
                <td>อายุ</td>
                <td>18 ปี</td>
            </tr>
            <tr>
                <td>อีเมล</td>
                <td>67030207@kmitl.ac.th</td>
            </tr>
            <tr>
                <td>วัน/เดือน/ปี เกิด</td>
                <td>20 พฤษภาคม ปี พ.ศ.2549</td>
            </tr>
            <tr>
                <td>เบอร์โทร</td>
                <td>086-306-6053</td>
            </tr>
            <tr>
                <td>ที่อยู่</td>
                <td>บ้านเลขที่:91/578 ตำบล:บางบัวทอง อำเภอ:บางบัวทอง จังหวัด:นนทบุรี</td>
            </tr>
        </tbody>
    </table>
</body>
</html>
```
- ภาพผลลัพธ์:
![image](https://github.com/user-attachments/assets/fcb7c0b8-16d4-4b6d-95ef-b67e72aabec7)


