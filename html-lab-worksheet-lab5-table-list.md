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
<table border="1" style="width: 50%; text-align: left; border-collapse: collapse;">
    <thead>
        <tr>
            <th>เมนูอาหาร</th>
            <th>ออเดอร์</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ผัดกะเพรา</td>
            <td>1</td>
        </tr>
        <tr>
            <td>ต้มยำกุ้ง</td>
            <td>2</td>
        </tr>
        <tr>
            <td>แกงเขียวหวาน</td>
            <td>1</td>
        </tr>
        <tr>
            <td>ข้าวมันไก่</td>
            <td>3</td>
        </tr>
        <tr>
            <td>ส้มตำ</td>
            <td>2</td>
        </tr>
    </tbody>
</table>

<h3>เมนูอาหารไทยเพิ่มเติม</h3>
<ul>
    <li>ข้าวซอย</li>
    <li>หมูทอดกระเทียม</li>
    <li>ขนมจีนน้ำยา</li>
    <li>ไก่ย่าง</li>
    <li>ก๋วยเตี๋ยวเรือ</li>
</ul>

<ol>
    <li>ต้มข่าไก่</li>
    <li>มัสมั่นไก่</li>
</ol>

<dl>
    <dt>ต้มข่าไก่</dt>
    <dd>ซุปไก่รสชาติกลมกล่อม ผสมกะทิและข่า</dd>
    <dt>มัสมั่นไก่</dt>
    <dd>แกงเข้มข้นรสชาติหวานเค็ม เผ็ดอ่อน ๆ</dd>
</dl>

```
- ภาพผลลัพธ์:
[วางภาพ screenshot ที่นี่]

![alt text](image-6.png)

