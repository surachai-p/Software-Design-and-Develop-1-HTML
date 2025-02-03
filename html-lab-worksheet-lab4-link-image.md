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
    <title>หน้าหลัก</title>
</head>
<body>
    <nav>
        <a href="index.html">หน้าหลัก</a>
        <a href="pages/contact.html">ติดต่อเรา</a>
    
    <section id="tops">
        <h1>IC Center </H1>
        <figure>
            <img src="images/logo.png" alt="logo website" width="300" height="300">
            
        </figure>
    </section>
<section id="products">
    <h2>สินค้าของเรา</h2>
    <h3>IC ที่ใช้ในรายวิชา FUNDAMENTAL OF DIGITAL DEVICES AND CIRCUITS</h3>
    <div>
        <figure>
            <a href="images/gallery/7400.png" >
                <img src="images/gallery/7400.png" alt="สินค้า 7400" width="200">
            </a>
            <figcaption>IC 7400 NAND Gate มี 4 วงจร แต่ละวงจรมีอินพุต 2 ขา</figcaption>
            <a href="files/7400.pdf" download>ดาวน์โหลด Datasheet</a>
        </figure>
        
    </div>
    <div>
        <figure>
            <a href="images/gallery/7402.png">
                <img src="images/gallery/7402.png" alt="คลิกเพื่อดูรูปขนาดใหญ่" width="200">
            </a>
            <figcaption>IC 7402 NOR Gate มี 4 วงจร แต่ละวงจรมีอินพุต 2 ขา</figcaption>
            <a href="files/7402.pdf" download>ดาวน์โหลด Datasheet</a>
        </figure>
        
    </div>
    <div>
        <figure>
            <a href="images/gallery/7404.png">
                <img src="images/gallery/7404.png" alt="คลิกเพื่อดูรูปขนาดใหญ่" width="200">
            </a>
            <figcaption>IC 7404 NOT Gate หรือ Inverter มี 6 วงจร</figcaption>
            <a href="files/7404.pdf" download>ดาวน์โหลด Datasheet</a>
        </figure>
        
    </div>
    <div>
        <figure>
            <a href="images/gallery/7408.png">
                <img src="images/gallery/7408.png" alt="คลิกเพื่อดูรูปขนาดใหญ่"" width="200">
            </a>
            <figcaption>IC 7408 AND Gate มี 4 วงจร แต่ละวงจรมีอินพุต 2 ขา</figcaption>
            <a href="files/7408.pdf" download>ดาวน์โหลด Datasheet</a>
        </figure>
        
    </div>
    <div>
        <figure>
            <a href="images/gallery/7432.png">
                <img src="images/gallery/7432.png" alt="คลิกเพื่อดูรูปขนาดใหญ่" width="200">
            </a>
            <figcaption>IC 7432 OR Gate มี 4 วงจร แต่ละวงจรมีอินพุต 2 ขา</figcaption>
            <a href="files/7432.pdf" download>ดาวน์โหลด Datasheet</a>
        </figure>
        
    </div>
    <div>
        <figure>
            <a href="images/gallery/7486.png">
                <img src="images/gallery/7486.png" alt="คลิกเพื่อดูรูปขนาดใหญ่" width="200">
            </a>
            <figcaption>IC 7486 NOR Gate มี 4 วงจร แต่ละวงจรมีอินพุต 2 ขา</figcaption>
            <a href="files/7486.pdf" download>ดาวน์โหลด Datasheet</a>
        </figure>
        
    </div>

    <a href="#top">กลับ
    </section>
</body>
</html>
```
- ภาพผลลัพธ์:
![สร้างแกลเลอรีสินค้า](Screenshot4.png)
