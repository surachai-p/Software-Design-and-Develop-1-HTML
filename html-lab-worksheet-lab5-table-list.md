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
<table border="1">
    <thead>
        <tr>
            <th>ชื่อเล่น</th>
            <th>ชื่อจริง</th>
            <th>อายุ</th>
            <th>ศึกษาอยู่ที่</th>
            <th>รหัสนักศึกษา</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ซิม</td>
            <td>นายภูมิชนะ เทียมแก้ว</td>
            <td>19 ปี</td>
            <td>สถาบันเทคโนโลยีพระจอมเกล้าเจ้าคุณทหารลาดกระบัง</td>
            <td>67030180</td>
        </tr>
    </tbody>
</table>
<br>
<hr>
<br>
<h1>รายการอาหาร</h1>
<ul>
<dl>
    <dt><strong>เมนูแนะนำ</strong></dt>
    <ul><dd><li>ผัดกระเพราหมูกรอบ</dd></ul></li>
    <ul><dd><li>ผัดกระเพราปลาหมึก</dd></ul></li>
    <ul><dd><li>ข้ามผัดทะเล</dd></ul></li>
    <ul><dd><li>ก๋วยเตี๋ยวต้มยำเนื้อวากิว</dd></ul></li>
    <dt><strong>อาหารจานเดียว</strong></dt>
    <ul><dd><li>ไข่เจียว</dd></ul></li>
    <ul><dd><li>ไข่ข้น</dd></ul></li>
    <ul><dd><li>ผัดมาม่า</dd></ul></li>
    <ul><dd><li>สุกี้หมู / ไก่ / เนื้อ</dd></ul></li>
    <ul><dd><li>ข้าวเปล่า</dd></ul></li>
<hr>
<dt><strong>เครื่องดื่ม</strong></dt>
<ul><dd><li>โค้ก</dd></ul></li>
<ul><dd><li>น้ำอัดลม</dd></ul></li>
</dl>
```
- ภาพผลลัพธ์:
[วางภาพ screenshot ที่นี่]
![image](https://github.com/user-attachments/assets/9304a9c0-9f6f-4e9a-95af-bda13f476089)

