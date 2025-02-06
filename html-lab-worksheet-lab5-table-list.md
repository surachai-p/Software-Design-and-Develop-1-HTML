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
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ข้อมูลส่วนตัวและเมนูอาหาร</title>
</head>
<body>

    <h2>ข้อมูลส่วนตัว</h2>
    <table border="1">
        <thead>
            <tr>
                <th>หัวข้อ</th>
                <th>ข้อมูล</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>ชื่อ</td>
                <td>ภวินท์</td>
            </tr>
            <tr>
                <td>อายุ</td>
                <td>20 ปี</td>
            </tr>
            <tr>
                <td>อาชีพ</td>
                <td>นักศึกษา</td>
            </tr>
            <tr>
                <td>ที่อยู่</td>
                <td>กรุงเทพฯ</td>
            </tr>
        </tbody>
    </table>

    <h2>เมนูอาหาร</h2>

    <h3>รายการเมนูอาหาร</h3>
    <ul>
        <li>ข้าวผัด</li>
        <li>ผัดไทย</li>
        <li>ต้มยำกุ้ง</li>
        <li>แกงเนื้อ</li>
    </ul>

    <h3>รายการเมนูอาหารที่ชอบ</h3>
    <ol>
        <li>ข้าวผัด</li>
        <li>แกงส้ม</li>
        <li>ต้มยำกุ้ง</li>
        <li>แกงเนื้อ</li>
    </ol>

    <h3>รายการเมนูอาหารพร้อมส่วนผสมแบบคร่าวๆ</h3>
    <dl>
        <dt>ข้าวผัด</dt>
        <dd>ข้าวผัดกับไข่และเนื้อสัตว์ต่างๆ</dd>

        <dt>ผัดไทย</dt>
        <dd>ก๋วยเตี๋ยวผัดใส่ไข่, ถั่วงอก, และน้ำซอสพริก</dd>

        <dt>ต้มยำกุ้ง</dt>
        <dd>น้ำซุปเผ็ดและเปรี้ยวใส่กุ้ง</dd>

        <dt>แกงเนื้อ</dt>
        <dd>แกงกะทิรสเผ็ดจัด ใส่เนื้อสัตว์และมะเขือ</dd>
    </dl>

</body>
</html>

```
- ภาพผลลัพธ์:
[วางภาพ screenshot ที่นี่]
![image](https://github.com/user-attachments/assets/9cef7504-1810-4a43-846e-ae6f219ad32d)

