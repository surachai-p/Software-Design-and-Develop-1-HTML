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
```<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Table</title>
</head>
<style>
    table {
        width: 50%;
        border-collapse: collapse;
    }

    th, td {
        border: 1px solid black;
        padding: 8px;
        text-align: center;
    }

    th {
        background-color: #f2f2f2;
    }
</style>
<body>
    <h1>รายละเอียดข้อมูลส่วนตัว</h1>
    <table>
        <thead>
            <tr>
                <th>ข้อมูลส่วนตัว</th>
                <th>รายละเอียด</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>ชื่อนักศึกษา</td>
                <td>นายชยางกูร สองพิมพ์</td>
            </tr>
            <tr>
                <td>อายุ / ปี</td>
                <td>19</td>
            </tr>
            <tr>
                <td>ที่อยู่</td>
                <td>42/221 นิมิตใกม่40 แขวงสามวาตะวันออก เขตคลองสามวา กรุงเทพมหานคร</td>
            </tr>
            <tr>
                <td>มหาวิทยาลัย</td>
                <td>สถาบันเทคโนโลยีพระจอมเกล้าเจ้าคุณทหารลาดกระบัง</td>
            </tr>
            <tr>
                <td>คณะ</td>
                <td>คณะครุศาสตร์อุตสาหกรรมและเทคโนโลยี</td>
            </tr>
            <tr>
                <td>สาขาวิชา</td>
                <td>เทคโนโลยีคอมพิวเตอร์</td>
            </tr>
            <tr>
                <td>อีเมล</td>
                <td>chayanggoon.s13@gmail.com</td>
            </tr>
        </tbody>
    </table>
    <br>
    <hr>
    <h1>เมนูอาหาร</h1>
    <table>
        <thead>
            <tr>
                <th>ชื่ออาหาร</th>
                <th>NAME OF THE DISH</th>
                <th>ราคา (THB / USD)</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>ข้าวผัดหมู</td>
                <td>pork Fried Rice</td>
                <td>60 THB 
            </tr>
            <tr>
                <td>ผัดไทยกุ้งสด</td>
                <td>Pad Thai with Fresh Shrimp</td>
                <td>80 THB 
            </tr>
            <tr>
                <td>ต้มยำทะเล</td>
                <td>Tom Yum tale (Spicy Shrimp Soup)</td>
                <td>180 THB 
            </tr>
            <tr>
                <td>แกงเขียวหวานไก่</td>
                <td>Green Curry Chicken</td>
                <td>50 THB 
            </tr>
            <tr>
                <td>ผัดกระเพราหมูสับ</td>
                <td>Stir-fried Basil with Minced Pork</td>
                <td>50 THB 
            </tr>
            <tr>
                <td>ยำวุ้นเส้น</td>
                <td>Spicy Glass Noodle Salad</td>
                <td>70 THB /
            </tr>
            <tr>
                
        </tbody>
    </table>
</body>
</html>


```
- ภาพผลลัพธ์:
[วางภาพ screenshot ที่นี่]

![image](https://github.com/user-attachments/assets/16444f8e-b9da-4120-9e78-be692ce9aaf0)

