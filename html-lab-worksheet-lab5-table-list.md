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
    <title>ตารางชีวิตประจำวัน</title>
</head>
<body>
    <table border="5">
        <h1>ตารางชีวิตประจำวัน</h1>
        <thead>
            <tr>
                <th>เวลาตื่นนอน</th>
                <th>เวลาเรียนไป</th>
                <th>พักเที่ยง/กินข้าว</th>
                <th>เวลาเลิกเรียน</th>
                <th>กลับบ้าน</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>07:00</td>
                <td>08:00</td>
                <td>12:00</td>
                <td>16:00</td>
                <td>16:30</td>
            </tr>
        </tbody>
        <thead>
            <tr>
                <th>พัฒนาทักษะ</th>
                <th>ออกกำลังกาย</th>
                <th>กินข้าวเย็น</th>
                <th>ดูหนัง-นอนเล่น</th>
                <th>เข้านอน</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>17:00-18:00</td>
                <td>18:30-19:00</td>
                <td>20:00</td>
                <td>21:00-23:00</td>
                <td>00:00</td>
            </tr>
        </tbody>
    </table>
    <h1>สุกี้พี่แว่น</h1>
    <ul>
        <li>สุกี้แห้งหมู 50 บาท</li>
        <li>สุกี้แห้งไก่ 50 บาท</li>
        <li>สุกี้แห้งเนื้อ 60 บาท</li>
        <li>สุกี้แห้งพิเศษ 70 บาท</li>
    </ul>
    
    <ol>
        <li>สุกี้แห้งหมู 50 บาท</li>
        <li>สุกี้แห้งไก่ 50 บาท</li>
        <li>สุกี้แห้งเนื้อ 60 บาท</li>
        <li>สุกี้แห้งพิเศษ 70 บาท</li>
    </ol>
</body>
</html>
```
- ภาพผลลัพธ์:
![image](https://github.com/user-attachments/assets/5f237574-8e49-448b-9e4a-a08b131ef66b)

[วางภาพ screenshot ที่นี่]

