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

<title>Table and List</title>

</head>

<body>

<h1>ตารางข้อมูลส่วนตัวเเละรายการอาหาร</h1>

<hr>

<h1>ข้อมูลส่วนตัว</h1>


<table border="2">

<tr>

<th>ชื่อ</th>

<td>นางสาวศศิธร  รอบคอบพรมาช</td>

</tr>

<tr>

<th>ชื่อเล่น</th>

<td>ปันปัน</td>

</tr>

<tr>

<th>อายุ</th>

<td>19 ปี</td>

</tr>

<tr>

<th>สาขา</th>

<td>เทคโนโลยีคอมพิวเตอร์</td>

</tr>

<tr>

<th>สถาบัน</th>

<td>สถาบันเทคโนโลยีพรจอมเกล้าเจ้าคุณทหารลาดกระบัง</td>

</tr>

</table>

<hr>

<h1>รายการอาหาร(FOOD LIST)</h1>

<ul>

<li>กะเพราปลาหมึก</li>

<li>ผัดพริกแกงกุ้ง</li>

<li>ยำหอยนางรม</li>

<li>ข้าวผัดทะเลเดือด</li>

</ul>

<hr>

<h1>รายการเครื่องดื่ม (BEVERAGE LIST)</h1>

<ol>

<li>มัทฉะลาเต้</li>

<li>ชานม</li>

<li>กาแฟเย็น</li>

<li>ชาเขียวร้อน</li>

</ol>

<hr>

</body>

</html>

```
- ภาพผลลัพธ์:
[วางภาพ screenshot ที่นี่]
<img width="950" height="978" alt="image" src="https://github.com/user-attachments/assets/8a35992d-2f41-4c36-b013-fefacdadb29a" />

