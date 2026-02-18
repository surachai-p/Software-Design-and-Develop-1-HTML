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
<h2>ตารางแสดงข้อมูลส่วนตัว</h2>
<table border="1">
    <thead>
        <tr>
            <th>ชื่อ-นามสกุล</th>
            <th>รหัสนักศึกษา</th>
            <th>สาขาวิชา</th>
            <th>ชั้นปี</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>นางสาววณิชชา จับปรั่ง</td>
            <td>68030251</td>
            <td>เทคโนโลยีคอมพิวเตอร์</td>
            <td>ปีที่ 1</td>
        </tr>
    </tbody>
</table>
<h2>รายการอาหาร</h2>
<ul>
    <li>ข้าวผัดกุ้ง</li>
        <li>ผัดกะเพราไก่</li>
        <li>ต้มยำกุ้ง</li>
        <li>ไอศกรีม</li>
        <li>เค้กช็อกโกแลต</li>
        <li>บัวลอย</li>
</ul>
```
- ภาพผลลัพธ์:
![lab5](images/lab5.png)

