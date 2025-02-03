# ใบงานการทดลอง HTML
 
## การทดลองที่ 3: การจัดการข้อความและการจัดรูปแบบ
### ขั้นตอนการทดลอง
1. ทดลองใช้ tag ต่างๆ:
```html
<h1>หัวข้อระดับ 1</h1>
<h2>หัวข้อระดับ 2</h2>
<p>ย่อหน้าปกติ</p>
<p>ข้อความ <strong>ตัวหนา</strong> และ <em>ตัวเอียง</em></p>
<p>ขึ้นบรรทัดใหม่<br>ด้วย br</p>
<hr>
<pre>
    ข้อความที่ต้องการ
    รักษารูปแบบ
    การเว้นวรรค
</pre>
```

### แบบฝึกหัด
1. สร้างหน้าเว็บแนะนำตัวเองที่ประกอบด้วย:
   - ชื่อ-นามสกุล
   - ประวัติการศึกษา
   - งานอดิเรก
   - เป้าหมายในอนาคต
 ข้อกำหนดที่ต้องมี:
   - หัวข้อหลักและหัวข้อย่อย
   - ย่อหน้าที่มีการจัดรูปแบบ
   - การขึ้นบรรทัดใหม่
   - เส้นคั่นระหว่างเนื้อหา
### บันทึกผลการทดลอง
- รหัสเอกสาร HTML ที่เขียน:
```html
<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>แนะนำตัวเอง - Kanruethai Kaewsawang</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            background-color: white; /* ปรับพื้นหลังเป็นสีขาว */
        }
        header {
            text-align: center;
        }
        main {
            padding: 20px;
            background-color: white;
            margin: 20px auto;
            max-width: 800px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1, h2 {
            color: black; /* ปรับสีตัวอักษรเป็นสีดำ */
        }
        hr {
            border: 1px solid #ddd;
        }
        p {
            font-size: 16px;
            color: black; /* ปรับสีตัวอักษรเป็นสีดำ */
        }
        ul {
            list-style-type: square;
        }
        footer {
            text-align: center;
            padding: 10px;
        }
    </style>
</head>
<body>

<header>
    <h1>แนะนำตัวเอง</h1>
</header>

<main>
    <h2>ข้อมูลส่วนตัว</h2>
    <p><strong>ชื่อ-นามสกุล:</strong> Kanruethai Kaewsawang</p>

    <h2>ประวัติการศึกษา</h2>
    <p>จบจาก <strong>โรงเรียนสุรวิทยาคาร</strong> ปัจจุบันกำลังศึกษาอยู่ในสาขา <strong>เทคโนโลยีคอมพิวเตอร์</strong> คณะ <strong>ครุศาสตร์อุตสาหกรรมและเทคโนโลยี</strong> สถาบัน <strong>เทคโนโลยีพระจอมเกล้าเจ้าคุณทหารลาดกระบัง</strong></p>

    <h2>งานอดิเรก</h2>
    <ul>
        <li>ดูหนัง</li>
        <li>อ่านนิยาย</li>
        <li>ฟังเพลง</li>
    </ul>

    <h2>เป้าหมายในอนาคต</h2>
    <p>อยากเป็น <strong>ครูคอมพิวเตอร์</strong> เพื่อที่จะมีโอกาสในการช่วยเหลือนักเรียนในการเรียนรู้และเข้าใจเทคโนโลยีคอมพิวเตอร์อย่างลึกซึ้ง</p>

    <hr>
</main>

<footer>
    <p>&copy; 2025 Kanruethai Kaewsawang</p>
</footer>

</body>
</html>
```
- ภาพผลลัพธ์:
  ![คำอธิบายรูป](https://drive.google.com/uc?export=view&id=1CzPZZdD3Mr56qFHU7h6nijO7bMzo8M)





