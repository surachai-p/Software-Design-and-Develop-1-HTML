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
```<table border="1">
    <thead>
        <tr>
            <th>หัวข้อ</th>
            <th>รายละเอียด</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ชื่อ</td>
            <td>วรัทยา</td>
        </tr>
        <tr>
            <td>นามสกุล</td>
            <td>รอดเมล์</td>
        </tr>
        <tr>
            <td>ชื่อเล่น</td>
            <td>นิว</td>
        </tr>
        <tr>
            <td>อายุ</td>
            <td>19 ปี</td>
        </tr>
        <tr>
            <td>สถานศึกษา</td>
            <td>สถาบันเทคโนโลยีพระจอมเกล้าเจ้าคุณทหารลาดกระบัง</td>
        </tr>
        <tr>
            <td>คณะ</td>
            <td>ครุศาสตร์อุตสาหกรรม</td>
        <tr>
            <td>สาขา</td>
            <td>เทคโนโลยีคอมพิวเตอร์</td>
        </tr>
        <tr>
            <td>ชั้นปี</td>
            <td>ปี 1</td>
        </tr>
    </tbody>
</table>

<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <title>รายการอาหารและเครื่องดื่ม</title>
</head>
<body>

    <h1>รายการอาหารและเครื่องดื่ม</h1>
    <hr>

    <h2>1. รายการอาหารคาว</h2>
    <ol>
        <li>ก๋วยเตี๋ยวต้มยำ</li>
        <li>ราดหน้า</li>
        <li>ผัดซีอิ๊ว</li>
    </ol>

    <hr>

    <h2>2. รายการอาหารหวาน</h2>
    <ol>
        <li>ข้าวเหนียวมะม่วง</li>
        <li>ขนมถ้วย</li>
        <li>ลูกชุบ</li>
    </ol>

    <hr>

    <h2>3. รายการเครื่องดื่ม</h2>
    <ol>
        <li>โกโก้เข้มๆ</li>
        <li>ชาไทย</li>
        <li>นมชมพู</li>
    </ol>

    <hr>
    <p><a href="#">กลับไปด้านบน</a></p>

</body>
</html>

```
- ภาพผลลัพธ์:
[![alt text](image-3.png)]

