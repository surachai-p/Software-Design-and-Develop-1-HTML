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

<table border="4">
    <h1>ตารางชีวิตในอังคาร</h1>
    <thead>
        <tr>
            <th>เวลาตื่น/นอน</th>
            <th>เวลาเรียน</th>
            <th>พักรับประทานข้าว</th>
            <th>เวลาเรียน</th>
            <th>กลับบ้านนอน</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>08:00-16:00</td>
            <td>08:00</td>
            <td>12:00</td>
            <td>16:00</td>
            <td>17:00เป็นต้นไป</td>
        </tr>
        <tr>
            <td></td>
            <td>LAB T.Piya</td>
            <td>Enjoy Eating</td>
            <td>Software Design</td>
            <td>Freetime/sleep</td>
        </tr>
    </tbody>
</table>
<h1>ตามสั่งลุงเอ</h1>
<ul>
    <li>กระเพราไก่ไข่ดาว 50 baht</li>
    <li>กระเพราหมูกรอบไข่ดาว 60 baht</li>
    <li>กระเพราทะเลไข่ดาว 60 baht</li>
    <li>กระเพราหมูสับไข่ดาว 50 baht</li>
</ul>

<ol>
    <li>กระเพราไก่ไข่ดาว 50 baht</li>
    <li>กระเพราหมูกรอบไข่ดาว 60 baht</li>
    <li>กระเพราทะเลไข่ดาว 60 baht</li>
    <li>กระเพราหมูสับไข่ดาว 50 baht</li>
</ol>

<dl>
    <dt>เจ๊แต๋ว</dt>
    <dd>สั่งกระเพราหมูสับไข่ดาว</dd>
    <dt>ลุงตู่</dt>
    <dd>สั่งกระเพราหมูกรอบไข่ดาว</dd>
</dl>

![{62676681-DF9D-4D30-A9F3-C1B63CECC801}](https://github.com/user-attachments/assets/d6121bcc-9213-4747-a8ac-a9d21c06a195)



