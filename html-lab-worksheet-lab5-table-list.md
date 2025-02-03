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
[วางโค้ด HTML ที่นี่]
```<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>ข้อมูลส่วนตัว</h1>
    <table border="1">
        <thead>
            <tr>
                <th>หัวข้อ</th>
                <th>รายละเอียด</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>ชื่อ</td>
                <td>นายศิวาถัทร อุยสุย</td>
            </tr>
            <tr>
                <td>รหัสประจำตัวนักศึกษา</td>
                <td>67030351</td>
            </tr>
            <tr>
                <td>คณะ</td>
                <td>ครุศาสตร์อุตสาหกรรมและเทคโนโลยี</td>
            </tr>
            <tr>
                <td>สาขา</td>
                <td>เทคโนโลยีคอมพิวเตอร์</td>
            </tr>
            <tr>
                <td>อายุ</td>
                <td>19 ปี</td>
            </tr>
            <tr>
                <td>อีเมล</td>
                <td>67030351@kmitl.ac.th</td>
            </tr>
            <tr>
                <td>วัน/เดือน/ปี เกิด</td>
                <td>16 กันยายน ปี พ.ศ.2548</td>
            </tr>
            <tr>
                <td>เบอร์โทร</td>
                <td>095-427-6527</td>
            </tr>
            <tr>
                <td>ที่อยู่</td>
                <td>บ้านเลขที่:215 ถนน:วิเศษกุล ตำบล:ทับเทียง อำเภอ:เมือง จังหวัด:ตรัง</td>
            </tr>
        </tbody>
    </table>
</body>
</html>l
```
- ภาพผลลัพธ์:
![ตารางข้อมูลส่วนตัว](Screenshot4.png)
2. สร้างรายการเมนูอาหาร
[วางโค้ด HTML ที่นี่]
```html
<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>เมนูอาหาร</title>
</head>
<body>

    <h1>เมนูอาหาร</h1>
    <h2>เมนูแนะนำ</h2>
    <ol>
        <li>
            <dt>ข้าวผัด</dt>
            <dd>หมู / ไก่ / กุ้ง / ปลาหมึก / ทะเล</dd>
        </li>

        <li>            <dt>กะเพรา</dt>
            <dd>หมูสับ-ชิ้น/ไก่สับ-ชิ้น/ทะเล/หมูกรอบ</dd>
        </li>
        <li>ผัดผักรวม</li>
    </ol>
    <h2>เมนูข้าว</h2>
    <ul>
        <li>
            <dt>ข้าวผัด</dt>
            <dd>หมู/ไก่/กุ้ง/ปลาหมึก/ทะเล</dd>
        </li>
        <li>
            <dt>กะเพรา</dt>
            <dd>หมูสับ-ชิ้น/ไก่สับ-ชิ้น/ทะเล/หมูกรอบ</dd>
        </li>
        <li>
            <dt>ผัดพริกแกง</dt>
            <dd>หมูสับ-ชิ้น/ไก่สับ-ชิ้น/ทะเล/หมูกรอบ</dd>
        </li>
        <li>
            <dt>ทอดกระทียม</dt>
            <dd>หมู/ไก่/ปลาหมึก/กุ้ง</dd>
        </li>
        <li>
            <dt>ผัดพริกหยวก</dt>
            <dd>หมู/ไก่/ปลาหมึก/กุ้ง/ทะเล</dd>
        </li>
        <li>
            <dt>ไข่เจียว</dt>
            <dd>หมูสับ/ไก่สับ</dd>
        </li>
        <li>ผัดคะน้าหมูกรอบ </li>
        <li>ผัดผักบุ้ง</li>
        <li>ผัดผักรวม</li>
        <li>ผัดผงกะหรี่</li>
    </ul>
        

```
- ภาพผลลัพธ์:
[วางภาพ screenshot ที่นี่]
![เนนูอาหาร](Screenshot5.png)
