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
[<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <title>หน้าหลัก</title>
</head>

<body>

<!-- จุดบนสุดของหน้า -->
<section id="top"></section>

<!-- โลโก้บริษัท (บนสุด) -->
<header>
    <img src="images/logo.jpg" 
         alt="โลโก้บริษัท"
         width="200">
</header>

<hr>

<!-- เมนูนำทาง -->
<nav>
    <a href="index.html">หน้าหลัก</a> |
    <a href="pages/about.html">เกี่ยวกับเรา</a> |
    <a href="pages/contact.html">ติดต่อเรา</a> |
    <a href="https://www.google.com" target="_blank">
        ไปยัง Google
    </a>
</nav>

<hr>

<!-- เนื้อหาส่วนบน -->
<section>
    <h1>เนื้อหาส่วนบน</h1>
    <p>ยินดีต้อนรับสู่เว็บไซต์ของเรา</p>
</section>

<hr>

<!-- ส่วนสินค้า -->
<section>
    <h2>แกลเลอรีรูปภาพ</h2>

    <figure>
        <a href="images/product/product1.jpg" target="_blank">
            <img src="images\product\product1.jpg" 
                 alt="ภาพที่ 1"
                 width="250">
        </a>
        <figcaption>ภาพที่ 1</figcaption>
        <figcaption>ขวดน้ำหอมทรงกลมสีชมพูอ่อน ดีไซน์เรียบหรู ดูอ่อนหวาน ให้ความรู้สึกสดใสและโรแมนติก</figcaption>
    </figure>

    <figure>
        <a href="images/product/product2.jpg" target="_blank">
            <img src="images\product\product2.jpg" 
                 alt="ภาพที่ 2"
                 width="250">
        </a>
        <figcaption>ภาพที่ 2</figcaption>
        <figcaption>ขวดน้ำหอมทรงสี่เหลี่ยมสีชมพู ตกแต่งด้วยโบว์สีดำ ดูหรูหรา น่ารัก และมีความเป็นแฟชั่น</figcaption>
    </figure>

    <figure>
        <a href="images/product/product3.jpg" target="_blank">
            <img src="images\product\product3.jpg" 
                 alt="ภาพที่ 3"
                 width="250">
        </a>
        <figcaption>ภาพที่ 3</figcaption>
        <figcaption>ขวดน้ำหอมสีฟ้าใส ถูกถืออยู่กลางท้องฟ้า ให้ความรู้สึกสดชื่น สะอาด และทันสมัย</figcaption>
    </figure>

    <figure>
        <a href="images/product/product4.jpg" target="_blank">
            <img src="images\product\product4.jpg" 
                 alt="ภาพที่ 4"
                 width="250">
        </a>
        <figcaption>ภาพที่ 4</figcaption>
        <figcaption>ขวดน้ำหอมสีเขียวอ่อน ดีไซน์เรียบหรู ดูสบายตา ให้ความรู้สึกสดชื่นและเป็นธรรมชาติ</figcaption>
    </figure>

<hr>

<!-- ลิงก์ภายในหน้า -->
<p>
    <a href="#top">กลับด้านบน</a> |
    <a href="#products">ไปยังสินค้า</a>
</p>

<hr>

<!-- ดาวน์โหลดเอกสาร -->
<section>
    <h2>เอกสาร</h2>
    <a href="files/document.pdf" download>
        ดาวน์โหลดเอกสาร
    </a>
</section>

<hr>

<hr>

<!-- ข้อมูลติดต่อ (ล่างสุด) -->
<footer>
    <h2>ติดต่อเรา</h2>
    <p>
        <a href="mailto:contact@example.com">ส่งอีเมลหาเรา</a><br>
        <a href="tel:+66812345678">โทร 081-234-5678</a>
    </p>
</footer>

</body>
</html>
]
```
- ภาพผลลัพธ์:
[![alt text](image-5.png)]
![alt text](image-4.png)


