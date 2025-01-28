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
    <title>ตารางข้อมูลส่วนตัวและเมนูอาหาร</title>
</head>
<body>
    <header>
        <h1>ข้อมูลส่วนตัวและเมนูอาหาร</h1>
    </header>

    <main>
        <!-- ตารางข้อมูลส่วนตัว -->
        <section>
            <h2>ตารางข้อมูลส่วนตัว</h2>
            <table border="1">
                <thead>
                    <tr>
                        <th>ชื่อ</th>
                        <th>นามสกุล</th>
                        <th>อายุ</th>
                        <th>อาชีพ</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>กฤตนัย</td>
                        <td>บุญน้อย</td>
                        <td>25</td>
                        <td>นักพัฒนา</td>
                    </tr>
                    <tr>
                        <td>บุญน้อย</td>
                        <td>กฤตนัย</td>
                        <td>30</td>
                        <td>นักออกแบบ</td>
                    </tr>
                </tbody>
            </table>
        </section>

        <!-- รายการเมนูอาหาร -->
        <section>
            <h2>รายการเมนูอาหาร</h2>
            <ul>
                <li>ข้าวผัด</li>
                <li>ก๋วยเตี๋ยว</li>
                <li>ส้มตำ</li>
                <li>ต้มยำกุ้ง</li>
            </ul>
        </section>
    </main>

    <footer>
        <hr>
        <p>จัดทำโดย: กฤตนัย บุญน้อย 67030011</p>
    </footer>
</body>
</html>
```
- ภาพผลลัพธ์:
![Lab5_tablelist.html](/html-workshop/screenshot/Lab5_tablelist.png)
