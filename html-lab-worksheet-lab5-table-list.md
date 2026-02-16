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

### บันทึกผลการทดลอง
- รหัสเอกสาร HTML ที่เขียน:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <table border="1">
    <thead>
        <tr>
            <th>ชื่อ</th>
            <th>นามสกุล</th>
            <th>อายุ</th>
            <th>ตำแหน่ง</th>
            <th>ศึกษาที่</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ชิษณุพัศก์</td>
            <td>วายุสุวรรณวิทย์</td>
            <td>20</td>
            <td>Devops</td>
            <td>KMITL</td>
            
            
        </tr>
        <tr>
            <td>Doe</td>
            <td>Joe</td>
            <td>40</td>
            <td>Backend</td>
            <td>CU</td>
        </tr>
        
    </tbody>
    
</table>

<h2>เมนูอาหาร</h2>
<h3>ประเภทของอาหาร</h3>
<ul>
    <li>กับข้าว</li>
    <li>เมนูเส้น</li>
    <li>ผัด</li>
</ul>

<h3></h3>
<ol>
    <li>ต้มยำกุ้ง</li>
    <li>หมี่ได่ฉีด</li>
    <li>ผัดไทย</li>
</ol>

<h3>เครื่องดื่ม</h3>
<dl>
    <dt>น้ำหวาน</dt>
    <dd>ชาเขียวหวาน, กาแฟหวาน, </dd>
    <dt>น้ำเปล่า</dt>
    <dd>น้ำเปล่า, น้ำเปล่าใส่น้ำแข็ง</dd>
</dl>
</body>
</html>
```

- ภาพผลลัพธ์:
![alt text](image-3.png)

