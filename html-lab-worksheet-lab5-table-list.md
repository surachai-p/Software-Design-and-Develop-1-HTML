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
<h3>ตารางข้อมูลส่วนตัว</h3>
<table border="1" cellpadding="10" cellspacing="0" style="width: 100%; border-collapse: collapse;">
    <thead style="background-color: #f2f2f2;">
        <tr>
            <th>หัวข้อ</th>
            <th>รายละเอียด</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>ชื่อ-นามสกุล</strong></td>
            <td>นางสาวนภัสสร คำปัน</td>
        </tr>
        <tr>
            <td><strong>อาชีพ</strong></td>
            <td>นักศึกษา</td>
        </tr>
        <tr>
            <td><strong>งานอดิเรก</strong></td>
            <td>เขียนนิยาย , อ่านหนังสือ , วาดรูป , ฟังเพลง</td>
        </tr>
        <tr>
            <td><strong>คติประจำใจ</strong></td>
            <td>"Error คือครูที่ดีที่สุด"</td>
        </tr>
    </tbody>
</table>

<h3>เมนูอาหารแนะนำประจำวันนี้</h3>

<ul>
    <li>
        <strong>อาหารคาว (Main Course)</strong>
        <ol>
            <li>ข้าวผัดกะเพราไข่ดาว</li>
            <li>ขนมจีนแกงเขียวหวานไก่</li>
            <li>ส้มตำปูปลาร้า</li>
        </ol>
    </li>
    
    <br>
    
    <li>
        <strong>เครื่องดื่ม (Beverages)</strong>
        <ol>
            <li>ชาใต้</li>
            <li>ชาเขียว</li>
            <li>น้ำมะนาวโซดา</li>
        </ol>
    </li>
</ul>

<dl>
    <dt><em>* โปรโมชั่นพิเศษ Valentine's Day</em></dt>
    <dd>คนโสดลด 20%</dd>
</dl>

```
- ภาพผลลัพธ์:
[![alt text](<ภาพถ่ายหน้าจอ 2569-02-17 เวลา 19.22.01.jpeg>)]

