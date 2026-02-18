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

```html
<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>แบบฝึกหัด HTML: ตารางข้อมูลส่วนตัวและรายการเมนูอาหาร</title>
    <style>
        body { 
            font-family: 'Sarabun', sans-serif; 
            line-height: 1.6; 
            padding: 40px; 
            background-color: #f8f9fa; 
            display: flex;
            justify-content: center;
        }

        .content-card {
            width: 100%;
            max-width: 600px;
            background: white;
            padding: 35px;
            border-radius: 12px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }

        h2 { text-align: center; color: #333; margin-bottom: 25px; }
        
        .section-title {
            font-weight: bold;
            font-size: 1.2em;
            margin-top: 30px;
            color: #1a73e8;
            border-left: 5px solid #1a73e8;
            padding-left: 10px;
            margin-bottom: 15px;
        }

        /* สไตล์ตาราง */
        table { 
            width: 100%; 
            border-collapse: collapse; 
            margin-bottom: 20px; 
        }
        th, td { 
            border: 1px solid #ddd; 
            padding: 12px; 
            text-align: left; 
        }
        th { background-color: #f2f2f2; width: 35%; }

        /* สไตล์รายการเมนูอาหาร */
        .menu-container {
            background-color: #fafafa;
            padding: 15px;
            border-radius: 8px;
            border: 1px dashed #ccc;
        }
        ul, ol { margin-left: 20px; }
        li { margin-bottom: 8px; }
        .price { color: #d32f2f; font-weight: bold; margin-left: 10px; }
    </style>
</head>
<body>

    <div class="content-card">
        <h2>ตารางข้อมูลส่วนตัวและรายการเมนูอาหาร</h2>

        <div class="section-title">1. ตารางแสดงข้อมูลส่วนตัว</div>
        <table>
            <tbody>
                <tr>
                    <th>ชื่อ-นามสกุล</th>
                    <td>ปทิตญา ภูกิจคุณาเดชากร</td>
                </tr>
                <tr>
                    <th>ชื่อเล่น</th>
                    <td>เนม</td>
                </tr>
                <tr>
                    <th>วันเกิด</th>
                    <td>25 สิงหาคม 2549</td>
                </tr>
                <tr>
                    <th>สาขา</th>
                    <td>เทคโนโลยีคอมพิวเตอร์</td>
                </tr>
                <tr>
                    <th>คณะ</th>
                    <td>ครุศาสตร์อุตสาหกรรมและเทคโนโลยี</td>
                </tr>
                <tr>
                    <th>สถาบัน</th>
                    <td>สถาบันเทคโนโลยีพระจอมเกล้าเจ้าคุณทหารลาดกระบัง</td>
                </tr>
            </tbody>
        </table>

        <div class="section-title">2. รายการเมนูอาหาร</div>
        <div class="menu-container">
            <p><strong>เมนูอาหารคาว (แบบมีลำดับเลข):</strong></p>
            <ol>
                <li>ข้าวผัดกะเพราเนื้อไข่ดาว <span class="price">65 บาท</span></li>
                <li>เส้นเล็กน้ำตกหมู <span class="price">50 บาท</span></li>
                <li>ข้าวมันไก่ผสม <span class="price">55 บาท</span></li>
            </ol>

            <p><strong>เมนูเครื่องดื่ม (แบบสัญลักษณ์):</strong></p>
            <ul>
                <li>ชาไทยเย็น <span class="price">35 บาท</span></li>
                <li>อเมริกาโน่น้ำส้ม <span class="price">55 บาท</span></li>
                <li>น้ำเปล่าแช่เย็น <span class="price">10 บาท</span></li>
            </ul>

            <p><strong>รายละเอียดการสั่งซื้อ (Definition List):</strong></p>
            <dl>
                <dt><strong>Take away</strong></dt>
                <dd>- บริการห่อกลับบ้าน</dd>
                <dt><strong>Delivery</strong></dt>
                <dd>- บริการจัดส่งถึงบ้าน (ค่าส่งตามระยะทาง)</dd>
            </dl>
        </div>
    </div>

</body>
</html>
```
- ภาพผลลัพธ์:
<img width="832" height="597" alt="Screenshot 2026-02-18 151701" src="https://github.com/user-attachments/assets/60299e7e-eb2e-45da-bf29-950f5e61c352" />





<img width="830" height="742" alt="Screenshot 2026-02-18 151726" src="https://github.com/user-attachments/assets/a9f14256-627c-4842-84ae-ff4b8fdcab06" />


