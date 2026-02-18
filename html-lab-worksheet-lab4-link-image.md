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
```<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <title>ร้านเก้าอี้มหัศจรรย์ - Amazing chair Gallery</title>
</head>
<body>

    <div id="top"></div>
    <h1>Amazing Chair Gallery ร้านเก้าอี้มหัศจรรย์</h1>
    <p>ยินดีต้อนรับสู่ร้านขายเก้าอี้ของเรา เชิญชมสินค้าสุดแปลก และแหวกแนวได้ที่นี่เลยค่าาา</p>
    <hr>

    <figure>
        <a href="http://www.infinitydesign.in.th/wp-content/uploads/2014/10/A-11-445x450.jpg">
            <img src="http://www.infinitydesign.in.th/wp-content/uploads/2014/10/A-11-445x450.jpg" alt="เก้าอี้แลบลิ้น" width="500">
        </a>
        <figcaption>เก้าอี้แลบลิ้น แพร่บ แพร่บ - <strong>ราคา 175,000 บาท</strong></figcaption>
    </figure>

    <figure>
        <a href="http://www.infinitydesign.in.th/wp-content/uploads/2014/10/A-1.jpg">
            <img src="http://www.infinitydesign.in.th/wp-content/uploads/2014/10/A-1.jpg" alt="เก้าอี้อ้าปาก" width="500">
        </a>
        <figcaption>เก้าอี้อ้าปากเห็นฟัน - <strong>ราคา 109,000 บาท</strong></figcaption>
    </figure>

    <figure>
        <a href="http://www.infinitydesign.in.th/wp-content/uploads/2014/10/A-26-450x421.jpg">
            <img src="http://www.infinitydesign.in.th/wp-content/uploads/2014/10/A-26-450x421.jpg" alt="เก้าอี้หัวกุ๊กกู๋" width="500">
        </a>
        <figcaption>เก้าอี้หัวกุ๊กกู๋ ระวังผีหลอก - <strong>ราคา 65,000 บาท</strong></figcaption>
    </figure>

    <figure>
        <a href="http://www.infinitydesign.in.th/wp-content/uploads/2014/10/A-9-450x450.jpg">
            <img src="http://www.infinitydesign.in.th/wp-content/uploads/2014/10/A-9-450x450.jpg" alt="เก้าอี้ขากิ้งกือ" width="500">
        </a>
        <figcaption>เก้าอี้ขากิ้งกือ - <strong>ราคา 72,000 บาท</strong></figcaption>
    </figure>

    <figure>
        <a href="https://i0.wp.com/marketeeronline.co/wp-content/uploads/2016/06/659555-650-1455021498-rocking-chair.jpg?w=650&ssl=1">
            <img src="https://i0.wp.com/marketeeronline.co/wp-content/uploads/2016/06/659555-650-1455021498-rocking-chair.jpg?w=650&ssl=1" alt="เก้าอี้ไม้วิเศษ" width="500">
        </a>
        <figcaption>เก้าอี้มีไฟ วิบ วิบ - <strong>ราคา 119,000 บาท</strong></figcaption>
    </figure>

    <hr>

    <p><a href="#top">กลับไปด้านบนสุด</a></p>

</body>
</html>
```
- ภาพผลลัพธ์:
[![alt text](image-2.png)]



