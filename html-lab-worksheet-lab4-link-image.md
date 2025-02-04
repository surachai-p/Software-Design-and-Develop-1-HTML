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
    <title>หน้าหลัก</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            text-align: center;
        }
        
    
        nav a:hover {
            color: #333;
        }

        h2 {
            color: #333;
            margin-top: 20px;
        }

        /* ======= ส่วนของสินค้า ======= */
        section {
            background: white;
            padding: 30px;
            margin: 20px auto;
            border-radius: 10px;
            max-width: 1200px;
        }

        /* ======= แกลเลอรีสินค้า ======= */
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
            padding: 20px;
            max-width: 1000px;
            margin: auto;
        }
        figure {
            background: white;
            padding: 10px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        img {
            width: 100%;
            border-radius: 5px;
            transition: transform 0.3s ease-in-out;
        }
        img:hover {
            transform: scale(1.05);
        }
        figcaption {
            font-size: 14px;
            font-weight: bold;
            color: #333;
            margin-top: 8px;
        }

        /* ======= ปุ่มกลับด้านบน ======= */
        .back-to-top {
            display: inline-block;
            margin: 20px auto;
            padding: 10px 20px;
            background-color: #28a745;
            color: white;
            text-decoration: none;
            font-size: 16px;
            border-radius: 5px;
            transition: background 0.3s ease-in-out;
        }
        .back-to-top:hover {
            background-color: #218838;
        }
    </style>
</head>
<body>

    <!-- เมนูนำทาง -->
    <nav>
        <a href="index.html">หน้าหลัก</a>
        <a href="pages/about.html">เกี่ยวกับเรา</a>
        <a href="pages/contact.html">ติดต่อเรา</a>
        <a href="https://www.google.com" target="_blank">ไปยัง Google</a>
    </nav>

    <header>
        <h1 id="top">แกลเลอรีสินค้า</h1>
    </header>

        <!-- แกลเลอรีสินค้า -->
        <div class="gallery">
            <figure>
                <a href="images/products/product1.jpg" target="_blank">
                    <img src="images/products/product1.jpg" alt="สินค้าชิ้นที่ 1">
                </a>
                <figcaption>สินค้าชิ้นที่ 1 - รายละเอียดสินค้า </figcaption>
            </figcaption>ชื่อสินค้า: Bennett Vitamin C & E Soap
                    ประเภท: สบู่ทำความสะอาดผิว
                    กลิ่น: ส้ม (Orange)
                    ราคา: ประมาณ 50-80 บาท</figcaption>
            </figure>

            <figure>
                <a href="images/products/product2.jpg" target="_blank">
                    <img src="images/products/product2.jpg" alt="สินค้าชิ้นที่ 2">
                </a>
                <figcaption>สินค้าชิ้นที่ 2 - รายละเอียดสินค้า </figcaption>
            </figcaption>ชื่อสินค้า: ไลปอนเอฟ สูตรอนามัย
                    ประเภท: น้ำยาล้างจาน
                    กลิ่น: กลิ่นเลมอน (Lemon)
                    ราคา: ประมาณ 30-50 บาท</figcaption>
            </figure>

            <figure>
                <a href="images/products/product3.jpg" target="_blank">
                    <img src="images/products/product3.jpg" alt="สินค้าชิ้นที่ 3">
                </a>
                <figcaption>สินค้าชิ้นที่ 3 - รายละเอียดสินค้า </figcaption>
            </figcaption> ชื่อสินค้า: เอเชียนดีไลท์ เผือก
                    ประเภท: ไอศกรีมแท่ง
                    รสชาติ: เผือก (Taro)
                    ราคา: ประมาณ 15-25 บาท </figcaption>
            </figure>

            <figure>
                <a href="images/products/product4.jpg" target="_blank">
                    <img src="images/products/product4.jpg" alt="สินค้าชิ้นที่ 4">
                </a>
                <figcaption>สินค้าชิ้นที่ 4 - รายละเอียดสินค้า</figcaption>
            </figcaption> ชื่อสินค้า: Oishi Green Tea Honey Lemon (โออิชิ กรีนที น้ำผึ้งมะนาว)
                        ประเภท: เครื่องดื่มชาเขียวพร้อมดื่ม
                        รสชาติ: น้ำผึ้งมะนาว (Honey Lemon)
                        ปริมาณสุทธิ: 380 มล.
                        ราคา: 20 บาทต่อขวด </figcaption>
            </figure>

            <figure>
                <a href="images/products/product5.jpg" target="_blank">
                    <img src="images/products/product5.jpg" alt="สินค้าชิ้นที่ 5">
                </a>
                <figcaption>สินค้าชิ้นที่ 5 - รายละเอียดสินค้า</figcaption>
            </figcaption>ชื่อสินค้า: CeraVe Facial Moisturising Lotion AM SPF 50
                    ประเภท: มอยส์เจอไรเซอร์บำรุงผิวหน้าสำหรับผิวธรรมดาถึงผิวแห้ง พร้อมกันแดด SPF 50
                    กลิ่น: ปราศจากน้ำหอม (Fragrance-Free)
                    ราคา: 179 บาท</figcaption>
            </figure>

            <figure>
                <a href="images/products/product6.jpg" target="_blank">
                    <img src="images/products/product6.jpg" alt="สินค้าชิ้นที่ 6">
                </a>
                <figcaption>สินค้าชิ้นที่ 6 - รายละเอียดสินค้า </figcaption>
            </figcaption>ชื่อสินค้า: MizuMi เซรั่มลดรอยสิว 
                        ประเภท: เซรั่มบำรุงผิวหน้า
                        กลิ่น: ไม่ได้ระบุบนบรรจุภัณฑ์ แต่เน้นคุณสมบัติช่วยลดรอยแดงและรอยดำจากสิว 
                        ราคา: 49 บาท</figcaption>
            </figure>
        </div>
    </section>

    <!-- ปุ่มกลับด้านบน -->
    <a href="#top" class="back-to-top">กลับด้านบน</a>

</body>
</html>
[วางโค้ด HTML ที่นี่]
```
- ภาพผลลัพธ์:
[วางภาพ screenshot ที่นี่]
![image](https://github.com/user-attachments/assets/b09161f8-af35-404d-af64-6419d0534524)
![image](https://github.com/user-attachments/assets/74bdcd0f-93f7-4435-be05-de9467936399)





