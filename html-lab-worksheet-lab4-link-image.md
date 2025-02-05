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
<!DOCTYPE html>
<html lang="th">

<head>
    <meta charset="UTF-8">
    <title>หน้าหลัก</title>
</head>

<body>

    <div style="text-align: center;">
        <img src="images/BMW-Logo-1997-1600x900.jpg" alt="โลโก้บริษัท" width="150">
        <h1>Applezzz THAILAND</h1>
    </div>

    <nav>
        <p>
            <a href="index.html">หน้าหลัก</a> |
            <a href="pages/about.html">เกี่ยวกับเรา</a> |
            <a href="pages/contact.html">ติดต่อเรา</a> |
            <a href="https://www.apple.com/" target="_blank">สเปค</a>
        </p>
    </nav>

    <hr>

    <section id="top">
        <h1>ประวัติบริษัท</h1>
        <p>
            Apple Inc. ก่อตั้งขึ้นเมื่อวันที่ 1 เมษายน 1976 โดย สตีฟ จอบส์, สตีฟ วอซเนียก และ รอน เวย์น เพื่อพัฒนาและจำหน่ายคอมพิวเตอร์ส่วนบุคคล
            เครื่องแรกของบริษัทคือ Apple I และตามมาด้วย Apple II ซึ่งประสบความสำเร็จอย่างมาก ปี 1984 Apple เปิดตัว Macintosh คอมพิวเตอร์ที่ใช้กราฟิกอินเทอร์เฟซ (GUI)
            ตัวแรก แต่ในช่วงปี 1990s บริษัทเผชิญปัญหาทางธุรกิจจนกระทั่งปี 1997 สตีฟ จอบส์กลับมาเป็น CEO และนำ Apple สู่ความสำเร็จอีกครั้ง
        </p>
    </section>

    <hr>

    <section id="products">
        <h2>สินค้าของเรา</h2>

        <figure>
            <a href="images/iphone-16.png" target="_blank">
                <img src="images/iphone-16.png" alt="iPhone 16" width="400">
            </a>
            <figcaption>
                <strong>iPhone 16</strong> มาพร้อมดีไซน์ใหม่ที่มีหน้าจอขนาด 6.1 นิ้วสำหรับรุ่นปกติ และ 6.9 นิ้วสำหรับรุ่น Plus
                กล้องหลัก 48MP และชิป A18 ประสิทธิภาพสูง รองรับ iOS 18
                <br>
                <a href="https://www.apple.com/th/iphone-16/" target="_blank">ดูสเปค</a>
            </figcaption>
        </figure>

        <figure>
            <a href="images/ipadpro.jpg" target="_blank">
                <img src="images/ipadpro.jpg" alt="iPad Pro" width="400">
            </a>
            <figcaption>
                <strong>iPad Pro</strong> มาพร้อมจอ Ultra Retina XDR และชิป M4 รองรับ Apple Pencil Pro และ Magic Keyboard
                <br>
                <a href="https://support.apple.com/th-th/119892" target="_blank">ดูสเปค</a>
            </figcaption>
        </figure>

        <figure>
            <a href="images/Macbookpro.jpg" target="_blank">
                <img src="images/Macbookpro.jpg" alt="MacBook Pro" width="400">
            </a>
            <figcaption>
                <strong>MacBook Pro</strong> ใช้ชิป M4 หน้าจอคุณภาพสูง รองรับการใช้งานระดับมืออาชีพ
                <br>
                <a href="https://www.apple.com/th/macbook-pro/" target="_blank">ดูสเปค</a>
            </figcaption>
        </figure>

    </section>

    <hr>

    <footer>
        <p>© APPLEZZZ THAILAND 2025</p>
        <p>
            <a href="index.html">กลับสู่หน้าหลัก</a> |
            <a href="https://www.apple.com/th/shop/browse/home_th_en">ไปยังสินค้า</a>
        </p>
        <p>
            <a href="mailto:67030142@kmitl.ac.th">ส่งอีเมลหาเรา</a> |
            <a href="tel:+66623495577">โทร 062-349-5577</a>
        </p>
        <p>
            <a href="files/Doc6652.pdf" download>ดาวน์โหลดเอกสาร</a>
        </p>
    </footer>

</body>
</html>
- ภาพผลลัพธ์:
![alt text](image-4.png)
![alt text](image-5.png)
![alt text](image-6.png)