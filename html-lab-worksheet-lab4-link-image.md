# ใบงานการทดลอง HTML

## การทดลองที่ 4: การสร้างลิงก์และการแทรกรูปภาพ

### การเตรียมโครงสร้างโฟลเดอร์และไฟล์
1. สร้างโครงสร้างโฟลเดอร์:
   ```
   html-workshop/
   ├── index.html
   ├── pages/
   │   ├── about.html
   │   └── contact.html
   ├── images/
   │   ├── logo.jpg
   │   └── products/
   │       ├── product1.jpg
   │       └── product2.jpg
   └── files/
       └── document.pdf
   ```

2. ขั้นตอนการสร้างโครงสร้าง:
   - คลิกขวาในโฟลเดอร์ html-workshop > New Folder > สร้าง "pages"
   - คลิกขวาในโฟลเดอร์ html-workshop > New Folder > สร้าง "images"
   - ในโฟลเดอร์ images > New Folder > สร้าง "products"
   - คลิกขวาในโฟลเดอร์ html-workshop > New Folder > สร้าง "files"

3. สร้างไฟล์ HTML:
   - ในโฟลเดอร์หลัก: สร้าง index.html (ใช้ไฟล์เดิมที่มีได้)
   - ในโฟลเดอร์ pages: สร้าง about.html และ contact.html

4. จัดเตรียมไฟล์:
   - นำรูปภาพที่ต้องการใช้ไปไว้ในโฟลเดอร์ images
   - นำรูปภาพสินค้าไปไว้ในโฟลเดอร์ products
   - นำไฟล์เอกสารไปไว้ในโฟลเดอร์ files

### ขั้นตอนการทดลอง

#### ส่วนที่ 1: การสร้างลิงก์
1. เปิดไฟล์ index.html และใส่โครงสร้างพื้นฐาน:
```html
<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <title>หน้าหลัก</title>
</head>
<body>
    <!-- ส่วนของเนื้อหา -->
</body>
</html>
```

2. สร้างเมนูนำทางพื้นฐาน:
```html
<nav>
    <!-- ลิงก์ภายใน - ไปยังหน้าในเว็บไซต์เดียวกัน -->
    <a href="index.html">หน้าหลัก</a>
    <a href="pages/about.html">เกี่ยวกับเรา</a>
    <a href="pages/contact.html">ติดต่อเรา</a>
    
    <!-- ลิงก์ภายนอก - เปิดในแท็บใหม่ -->
    <a href="https://www.google.com" target="_blank">
        ไปยัง Google
    </a>
</nav>
```
คำอธิบาย:
- `href="..."` - กำหนดเส้นทางของลิงก์
- `target="_blank"` - เปิดลิงก์ในแท็บใหม่

3. สร้างลิงก์ภายในหน้าเดียวกัน:
```html
<!-- สร้างจุดเชื่อมโยง -->
<section id="top">
    <h1>เนื้อหาส่วนบน</h1>
</section>

<section id="products">
    <h2>สินค้าของเรา</h2>
</section>

<!-- ลิงก์ไปยังจุดเชื่อมโยง -->
<a href="#top">กลับด้านบน</a>
<a href="#products">ไปยังสินค้า</a>
```
คำอธิบาย:
- `id="..."` - กำหนดจุดเชื่อมโยง
- `href="#..."` - ลิงก์ไปยัง id ที่กำหนด

4. สร้างลิงก์พิเศษ:
```html
<!-- ลิงก์อีเมล -->
<a href="mailto:contact@example.com">ส่งอีเมลหาเรา</a>

<!-- ลิงก์โทรศัพท์ -->
<a href="tel:+66812345678">โทร 081-234-5678</a>

<!-- ลิงก์ดาวน์โหลด -->
<a href="files/document.pdf" download>
    ดาวน์โหลดเอกสาร
</a>
```
คำอธิบาย:
- `mailto:` - เปิดโปรแกรมอีเมล
- `tel:` - เปิดโปรแกรมโทรศัพท์
- `download` - ดาวน์โหลดไฟล์แทนการเปิด

#### ส่วนที่ 2: การแทรกรูปภาพ
1. แทรกรูปภาพพื้นฐาน:
```html
<!-- รูปภาพในโฟลเดอร์ images -->
<img src="images/logo.jpg" 
     alt="โลโก้บริษัท"
     width="200">

<!-- รูปภาพในโฟลเดอร์ย่อย products -->
<img src="images/products/product1.jpg" 
     alt="สินค้าชิ้นที่ 1"
     width="300"
     height="200">
```
คำอธิบาย:
- `src="..."` - ระบุตำแหน่งของรูปภาพ
- `alt="..."` - ข้อความทดแทนเมื่อไม่สามารถแสดงรูปได้
- `width="..."` - กำหนดความกว้าง
- `height="..."` - กำหนดความสูง

2. ใช้ figure และ figcaption:
```html
<figure>
    <img src="images/products/product2.jpg" 
         alt="สินค้าชิ้นที่ 2">
    <figcaption>
        รายละเอียดสินค้าชิ้นที่ 2
    </figcaption>
</figure>
```
คำอธิบาย:
- `<figure>` - จัดกลุ่มรูปภาพและคำอธิบาย
- `<figcaption>` - คำอธิบายประกอบรูปภาพ

3. สร้างรูปภาพที่คลิกได้:
```html
<a href="images/products/product1.jpg">
    <img src="images/products/product1.jpg" 
         alt="คลิกเพื่อดูรูปขนาดใหญ่"
         width="200">
</a>
```

### หมายเหตุ
- ตรวจสอบการสะกดชื่อไฟล์และโฟลเดอร์ให้ถูกต้อง
- path ของรูปภาพต้องถูกต้องตามโครงสร้างโฟลเดอร์
- ทดสอบการทำงานของลิงก์ทุกจุด

### แบบฝึกหัด
1. สร้างแกลเลอรีสินค้า:
   - สร้างโฟลเดอร์ images/gallery
   - ใส่รูปภาพอย่างน้อย 4 รูป
   - แต่ละรูปต้องคลิกดูขนาดใหญ่ได้
   - มีคำอธิบายใต้รูป
   - มีปุ่มกลับด้านบน

### บันทึกผลการทดลอง
- รหัสเอกสาร HTML ที่เขียน:
```html
<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>แบบฝึกหัด : การสร้างลิงก์และการแทรกรูปภาพ</title>
    <style>
        /* จัดการ Font และ Layout พื้นฐาน */
        body { 
            font-family: 'Tahoma', sans-serif; 
            text-align: center; 
            background-color: #f4f4f4; 
            margin: 0;
            padding: 0;
        }

        /* ส่วนหัวของหน้า */
        header {
            background-color: #333;
            color: white;
            padding: 20px 0;
            margin-bottom: 30px;
        }

        /* แกลเลอรีสินค้า */
        .gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* การ์ดสินค้าแต่ละชิ้น */
        .item { 
            width: 250px; 
            background: white; 
            padding: 15px; 
            border-radius: 12px; 
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .item:hover { 
            transform: translateY(-10px); 
        }

        /* จัดการขนาดรูปภาพ */
        .item img {
            width: 100%;
            height: 200px;
            object-fit: cover; /* ให้รูปพอดีกรอบโดยไม่เสียสัดส่วน */
            border-radius: 8px;
            cursor: pointer;
        }

        /* คำอธิบายใต้รูป */
        .caption { 
            margin-top: 15px; 
            font-size: 16px;
            font-weight: bold;
            color: #2c3e50; 
        }

        /* ปุ่มกลับด้านบน */
        .back-to-top {
            display: inline-block;
            margin: 50px 0;
            padding: 12px 25px;
            background-color: #e67e22;
            color: white;
            text-decoration: none;
            border-radius: 25px;
            font-weight: bold;
            transition: background 0.3s;
        }

        .back-to-top:hover {
            background-color: #d35400;
        }
    </style>
</head>
<body>

    <header id="top-anchor">
        <h1>แกลเลอรีสินค้า</h1>
        <p>เมนูน้ำจิ้ม Freeze-Dried</p>
    </header>

    <div class="gallery">
        <div class="item">
            <a href="gallery/sukiyaki.png" target="_blank">
                <img src="gallery/sukiyaki.png" alt="น้ำจิ้มสุกี้">
            </a>
            <p class="caption">น้ำจิ้มสุกี้ (Sukiyaki)</p>
        </div>

        <div class="item">
            <a href="gallery/chicken.png" target="_blank">
                <img src="gallery/chicken.png" alt="น้ำจิ้มไก่">
            </a>
            <p class="caption">น้ำจิ้มไก่ (Chicken Sauce)</p>
        </div>

        <div class="item">
            <a href="gallery/jeaw.png" target="_blank">
                <img src="gallery/jeaw.png" alt="น้ำจิ้มแจ่ว">
            </a>
            <p class="caption">น้ำจิ้มแจ่ว (Jaew Sauce)</p>
        </div>

        <div class="item">
            <a href="gallery/seafood.png" target="_blank">
                <img src="gallery/seafood.png" alt="น้ำจิ้มซีฟู้ด">
            </a>
            <p class="caption">น้ำจิ้มซีฟู้ด (Seafood)</p>
        </div>
    </div>

    <a href="#top-anchor" class="back-to-top">กลับสู่ด้านบน</a>

    <footer style="padding: 20px; color: #888;">
        <p>&copy; 2026 freeze-dried sauces</p>
    </footer>

</body>
</html>
```
- ภาพผลลัพธ์:

<img width="1905" height="901" alt="Screenshot 2026-02-18 155410" src="https://github.com/user-attachments/assets/1084f6bb-b1ff-4c7b-ade2-904e6d07a491" />




