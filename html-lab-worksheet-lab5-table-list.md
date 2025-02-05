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
    <title>Table</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            padding: 0;
            background-color: #f9f9f9;
        }
        table {
            width: 50%;
            border-collapse: collapse;
            margin-bottom: 20px;
        }
        th, td {
            border: 1px solid black;
            padding: 8px;
            text-align: center;
        }
        .menu-item {
            margin: 10px 0;
            padding: 10px;
            border: 1px solid #ddd;
            background-color: #fff;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        .menu-item h3 {
            margin: 0 0 5px;
            font-size: 1.2rem;
        }
        .menu-item p {
            margin: 0;
            color: #666;
        }
    </style>
</head>
<body>

    <h1>ข้อมูลส่วนตัว</h1>
    <table>
        <thead>
            <tr>
                <th>หัวข้อ</th>
                <th>ข้อมูล</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>ชื่อ</td>
                <td>วิชญาพร เนียมเที่ยง</td>
            </tr>
            <tr>
                <td>ชื่อเล่น</td>
                <td>หญิง , หงิง</td>
            </tr>
            <tr>
                <td>อายุ</td>
                <td>19 ปี</td>
            </tr>
            <tr>
                <td>อาชีพที่อยากเป็นในอนาคต</td>
                <td>คุณครู</td>
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
        </tbody>
    </table>

    <h1>เมนูอาหาร</h1>
    <div class="menu-item">
        <h3>ข้าวไข่ข้นกุ้ง</h3>
        <p>ราคา: 80 บาท</p>
    </div>
    <div class="menu-item">
        <h3>มาม่าต้มยำทะเลหม้อไฟ</h3>
        <p>ราคา: 200 บาท</p>
    </div>
    <div class="menu-item">
        <h3>ปีกไก่ทอดน้ำปลา </h3>
        <p>ราคา (ชิ้นละ): 10 บาท</p>
    </div>
    <div class="menu-item">
        <h3>สเต็กหมูพริกไทยดำ</h3>
        <p>ราคา: 150 บาท</p>
    </div>
    <div class="menu-item">
        <h3>ต้มแซ่บกระดูกอ่อน</h3>
        <p>ราคา: 70 บาท</p>
    </div>
    <div class="menu-item">
        <h3>มะนาวโซดาน้ำผึ้ง</h3>
        <p>ราคา: 50 บาท</p>
    </div>
    <div class="menu-item">
        <h3>สตรอว์เบอร์รีสมูทตี้</h3>
        <p>ราคา: 70 บาท</p>
    </div>
    <div class="menu-item">
        <h3>ชาเขียวมัทฉะลาเต้เย็น</h3>
        <p>ราคา: 65 บาท</p>
    </div>
    <div class="menu-item">
        <h3>แตงโมปั่น</h3>
        <p>ราคา: 45 บาท</p>
    </div>

</body>
</html>
```
- ภาพผลลัพธ์:
[วางภาพ screenshot ที่นี่]
<img width="1440" alt="ภาพถ่ายหน้าจอ 2568-02-05 เวลา 23 30 01" src="https://github.com/user-attachments/assets/d67f6e01-e3a4-4559-b7ff-9791b8604bb4" />
<img width="1439" alt="ภาพถ่ายหน้าจอ 2568-02-05 เวลา 23 30 15" src="https://github.com/user-attachments/assets/a0b9b48b-7e9a-4c8e-b881-cbddfd2ee3cf" />



