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
    <title>การสร้างตารางและรายการ</title>

    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 40px;
        }

        table {
            border-collapse: collapse;
            width: 60%;
            margin-bottom: 30px;
        }

        th, td {
            border: 1px solid black;
            padding: 10px;
            text-align: left;
        }

        th {
            background-color: #f2f2f2;
        }

        h2 {
            margin-top: 40px;
        }
    </style>
</head>
<body>

    <h1>1. ตารางข้อมูลส่วนตัว</h1>

    <table>
        <thead>
            <tr>
                <th>หัวข้อ</th>
                <th>ข้อมูล</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>ชื่อ-นามสกุล</td>
                <td>นางสาว ฐิติกานต์ ประสิทธิ์</td>
            </tr>
            <tr>
                <td>รหัสนักศึกษา</td>
                <td>68030072</td>
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
                <td>อีเมล</td>
                <td>68030072@kmitl.ac.th</td>
            </tr>
        </tbody>
    </table>

    <h2>2. รายการเมนูอาหาร</h2>

    <h3>เมนูอาหารจานหลัก (Unordered List)</h3>
    <ul>
        <li>ข้าวผัด</li>
        <li>ผัดกะเพรา</li>
        <li>ต้มยำกุ้ง</li>
    </ul>

    <h3>เมนูเครื่องดื่ม (Ordered List)</h3>
    <ol>
        <li>ชาไทย</li>
        <li>กาแฟเย็น</li>
        <li>น้ำมะนาว</li>
    </ol>

    <h3>เมนูของหวาน (Description List)</h3>
    <dl>
        <dt>ไอศกรีม</dt>
        <dd>ของหวานเย็น รสหวาน หลากหลายรสชาติ</dd>

        <dt>บัวลอย</dt>
        <dd>ขนมไทย ทำจากแป้งในน้ำกะทิหวาน</dd>
    </dl>

</body>
</html>


```
- ภาพผลลัพธ์:
[วางภาพ screenshot ที่นี่]

![alt text](5.PNG)


