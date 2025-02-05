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
[Lab 4

<!DOCTYPE html>
<html lang="en">
<head>
    <title>My First Web Page</title>
</head>
<body>
    
    <nav>
        <!-- ลิงก์ภายใน - ไปยังหน้าในเว็บไซต์เดียวกัน -->
       
        <!-- รูปภาพในโฟลเดอร์ images -->
            <img src="images/1.jpg" 
            alt="โลโก้บริษัท"
            height="80"
            width="80">
            <a href="index.html">หน้าหลัก</a>
        <a href="test.html">กลับ</a>
        
        <!-- ลิงก์ภายนอก - เปิดในแท็บใหม่ -->
        <a href="https://www.google.com" target="_blank">
            ไปยัง Google
        </a>
    </nav>
    <!-- สร้างจุดเชื่อมโยง -->
<section id="top">
    <h1>Supercar รถที่ใครก็ใครก็คู่ควร</h1>
</section>

<section id="products">
    <h2>สินค้าของเรา</h2>
</section>

<!-- กล่องใส่สินค้า -->
<figure>
    <!-- รูปภาพที่กดเพื่อดูขนาดใหญ่ -->
    <a href="images/product/2.jpg">
        <img src="images/product/2.jpg" 
             alt="สินค้าชิ้นที่ 1"
             width="300"
             height="200">
    </a>
    <figcaption>รายละเอียดสินค้า</figcaption>
    <figcaption><strong>Lamborghini Aventador SVJ</strong>
        เครื่องยนต์: V12 6.5 ลิตร 770 แรงม้าอัตราเร่ง: 0-100 กม./ชม. ใน 2.8 วินาทีความเร็วสูงสุด: 350 กม./ชม
        จุดเด่น:
        ดีไซน์สุดโฉบเฉี่ยวพร้อม Aero Dynamic ที่ล้ำสมัย
        ระบบขับเคลื่อน 4 ล้อสุดเสถียร
        ตัวถังคาร์บอนไฟเบอร์ น้ำหนักเบาแต่แข็งแกร่ง
        เสียงเครื่องยนต์ดุดันสไตล์ Lamborghini</figcaption>
</figure>
<hr>

<figure>
    <a href="images/product/4.jpg">
        <img src="images/product/4.jpg" 
             alt="สินค้าชิ้นที่ 1"
             width="300"
             height="200">
    </a>
    <figcaption>รายละเอียดสินค้า</figcaption>
    <figcaption><strong>Lamborghini Huracán EVO</strong>
        เครื่องยนต์: V10 5.2 ลิตร 640 แรงม้าอัตราเร่ง: 0-100 กม./ชม. ใน 2.9 วินาทีความเร็วสูงสุด: 325 กม./ชม.
        จุดเด่น:
        ดีไซน์คมชัด โฉบเฉี่ยว พร้อมระบบ Aerodynamics ที่ยอดเยี่ยม
        ระบบขับเคลื่อน 4 ล้อและเทคโนโลยี LDVI ควบคุมการขับขี่แบบ AI
        เสียงเครื่องยนต์ V10 ดุดันสะใจ</figcaption>
</figure>

<figure>
<hr>
    <a href="images/product/3.jpg">
    <img src="images/product/3.jpg" 
         alt="สินค้าชิ้นที่ 1"
         width="300"
         height="200">
    </a>
    <figcaption>รายละเอียดสินค้า</figcaption>
    <figcaption><strong>Lamborghini Aventador LP780-4 Ultimae (สี Bianco Canopus)</strong>
        เครื่องยนต์: V12 6.5 ลิตร 780 แรงม้าอัตราเร่ง: 0-100 กม./ชม. ใน 2.8 วินาทีความเร็วสูงสุด: 355 กม./ชม.
        จุดเด่น:
        เป็นรุ่นสุดท้ายของ Aventador ก่อนเปลี่ยนโฉม
        ดีไซน์ล้ำสมัย พร้อมระบบ Aerodynamics ที่พัฒนาขึ้น
        ขับเคลื่อน 4 ล้อ ให้ความมั่นใจทุกสภาพถนน
        สีขาวด้าน (Bianco Canopus) เพิ่มความพิเศษและดุดัน</figcaption>
</figure>

<hr>
<figure>
    <!-- รูปภาพที่กดเพื่อดูขนาดใหญ่ -->
    <a href="images/product/1.jpg">
        <img src="images/product/1.jpg" 
             alt="สินค้าชิ้นที่ 1"
             width="300"
             height="200">
    </a>
    <figcaption>รายละเอียดสินค้า</figcaption>
    <figcaption><strong>Lamborghini Aventador SVJ</strong>
        เครื่องยนต์: V12 6.5 ลิตร 770 แรงม้าอัตราเร่ง: 0-100 กม./ชม. ใน 2.8 วินาทีความเร็วสูงสุด: 350 กม./ชม
        จุดเด่น:
        ดีไซน์สุดโฉบเฉี่ยวพร้อม Aero Dynamic ที่ล้ำสมัย
        ระบบขับเคลื่อน 4 ล้อสุดเสถียร
        ตัวถังคาร์บอนไฟเบอร์ น้ำหนักเบาแต่แข็งแกร่ง
        เสียงเครื่องยนต์ดุดันสไตล์ Lamborghini</figcaption>
</figure>
<hr>

</body>
</html>]
```
- ภาพผลลัพธ์:
[![alt text](image-5.png)]

![alt text](image-6.png)



