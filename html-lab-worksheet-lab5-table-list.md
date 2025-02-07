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

<body>
    <h2 style="text-align: center;">ข้อมูลส่วนตัว</h2>
    <table border="1">
        <tr>
            <th>หัวข้อ</th>
            <th>รายละเอียด</th>
        </tr>
        <tr>
            <td>ชื่อ</td>
            <td>ธีธัช</td>
        </tr>
        <tr>
            <td>อายุ</td>
            <td>21 ปี</td>
        </tr>
        <tr>
            <td>ที่อยู่</td>
            <td>กรุงเทพมหานคร, ประเทศไทย</td>
        </tr>
        <tr>
            <td>อีเมล</td>
            <td>67030302@kmil.ac.th</td>
        </tr>
        <tr>
            <td>เบอร์โทร</td>
            <td>098-895-8597</td>
        </tr>
    </table>

    <h2 style="text-align: center;">เมนูอาหาร</h2>
    <table border="1">
        <tr>
            <th>รูปภาพ</th>
            <th>ชื่อเมนู</th>
            <th>ประเภท</th>
            <th>ราคา (บาท)</th>
        </tr>
        <tr>
            <td><img src="image/tomyum.jpg" alt="ต้มยำกุ้ง"width="200"></td>
            <td>ต้มยำกุ้ง</td>
            <td>อาหารไทย</td>
            <td>150</td>
            
        </tr>
        <tr>
            <td><img src="image/padthai.jpg" alt="ผัดไทย"width="200"></td>
            <td>ผัดไทย</td>
            <td>อาหารไทย</td>
            <td>120</td>
        </tr>
        <tr>
            <td><img src="image/spaghetti.jpg" alt="สปาเก็ตตี้คาโบนาร่า"width="200"></td>
            <td>สปาเก็ตตี้คาโบนาร่า</td>
            <td>อาหารอิตาเลียน</td>
            <td>200</td>
        </tr>
        <tr>
            <td><img src="image/sushi.jpg" alt="ซูชิแซลมอน"width="200"></td>
            <td>ซูชิแซลมอน</td>
            <td>อาหารญี่ปุ่น</td>
            <td>250</td>
        </tr>
        <tr>
            <td><img src="image/steak.jpg" alt="สเต็กเนื้อ"width="200"></td>
            <td>สเต็กเนื้อ</td>
            <td>อาหารตะวันตก</td>
            <td>350</td>
        </tr>
    </table>
</body>
</html>

```
- ภาพผลลัพธ์:
![image](https://github.com/user-attachments/assets/83cf0f08-5dbd-459d-a621-ea166609697e)


