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

[<table border="4.5">
    <thead>
        <tr>
            <th>ข้อมูล</th>
            <th>รายละเอียด</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ชื่อ-นามสกุล</td>
            <td>นายธนวัฒน์ พุทธา</td>
        </tr>
        <tr>
            <td>อายุ</td>
            <td>19ปี</td>
        </tr>
        <tr>
            <td>ที่อยู่</td>
            <td>91หมู่5 อ.ลำดวน จ.สุรินทร์</td>
        </tr>
        <tr>
            <td>ช่องทางติดต่อ</td>
            <td>IG: popcorn"j1 / Tel: 0809396912</td>

        </tr>
    </tbody>
</table>

<p><strong>เมนูอาหาร</strong></p>
<ul>
    <li>ราเม็ง</li>
    <li>ซูชิ</li>
    <li>ต้มยำกุ้ง</li>
    <li>แกงมัสมั่น</li>
    <li>ปาเอยา</li>
</ul>


]
```html

```
- ภาพผลลัพธ์:
[วางภาพ screenshot ที่นี่]
![alt text](image-7.png)
