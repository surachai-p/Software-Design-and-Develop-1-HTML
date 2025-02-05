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
<html>
<head>
    <title>หนาหลัก</title>
</head>
<body>
    
<div>
    <img src="images/logo.jpg" 
     alt="โลโก้บริษัท"
     width="200">
</div>

<nav>
    <a href="index.html">หน้าหลัก</a>
    <a href="pages/about.html">เกี่ยวกับเรา</a>
    <a href="pages/contact.html">ติดต่อเรา</a>
        
    <a href="https://www.naiin.com/" target="_blank">
     สินค่าเพื่มเติม
    </a>
</nav>

<section id="top">
    <h1>ร้านหนังสือ หนังเสือ</h1>
</section>

<section id="products">
    <h2>หนังสือแนะนำร้านเรา</h2>
</section>

<figure>
    <a href="images/products/product1.jpg">
        <img src="images/products/product1.jpg" 
        alt="คลิกเพื่อดูรูปขนาดใหญ่"
        width="200">
    </a>
    <figcaption>
        ข้อสอบ A-Level ภาษาไทย ฉบับอัปเดต<br>
        ผู้เขียน: อ.ปิง เจริญศิริวัฒน์<br>
        สำนักพิมพ์: ร.ร.กวดวิชา อ.ปิง<br>
        หมวดหมู่: หนังสือเตรียมสอบ แนวข้อสอบ , เตรียมสอบเข้ามหาวิทยาลัย<br>
    </figcaption>
</figure>

<figure>
    <a href="images/products/product2.jpg">
        <img src="images/products/product2.jpg" 
        alt="คลิกเพื่อดูรูปขนาดใหญ่"
        width="200">
    </a>
    <figcaption>
        ใช้คลื่นพลังบวกดึงดูดพลังสุข<br>
        ผู้เขียน: Vex King (เว็กซ์ คิงส์)<br>
        สำนักพิมพ์: อมรินทร์ How to<br>
        หมวดหมู่: จิตวิทยา การพัฒนาตัวเอง , การพัฒนาตัวเอง how to<br>

    </figcaption>
</figure>

<figure>
    <a href="images/products/product3.jpg">
        <img src="images/products/product3.jpg" 
        alt="คลิกเพื่อดูรูปขนาดใหญ่"
        width="200">
    </a>
    <figcaption>
        ข้อสอบ A-Level สังคม ฉบับอัปเดต<br>
        ผู้เขียน: อ.ปิง เจริญศิริวัฒน์<br>
        สำนักพิมพ์: ร.ร.กวดวิชา อ.ปิง<br>
        หมวดหมู่: หนังสือเตรียมสอบ แนวข้อสอบ , เตรียมสอบเข้ามหาวิทยาลัย<br>

    </figcaption>
</figure>

<figure>
    <a href="images/products/product4.jpg">
        <img src="images/products/product4.jpg" 
        alt="คลิกเพื่อดูรูปขนาดใหญ่"
        width="200">
    </a>
    <figcaption>
        จิตวิทยาสายดาร์ก<br>
        ผู้เขียน: Dr.Hiro<br>
        สำนักพิมพ์: วีเลิร์น (WeLearn)<br>
        หมวดหมู่: จิตวิทยา การพัฒนาตัวเอง , การพัฒนาตัวเอง how to<br>

    </figcaption>
</figure>

<figure>
    <a href="images/products/product5.jpg">
        <img src="images/products/product5.jpg" 
        alt="คลิกเพื่อดูรูปขนาดใหญ่"
        width="200">
    </a>
    <figcaption>
        แนวข้อสอบ A-LEVEL ภาษาอังกฤษ<br>
        ผู้เขียน: รศ.ดร.ศุภวัฒน์ พุกเจริญ<br>
        สำนักพิมพ์: ศุภวัฒน์ พุกเจริญ/Suphawat Pukcharoen<br>
        หมวดหมู่: หนังสือเตรียมสอบ แนวข้อสอบ , เตรียมสอบเข้ามหาวิทยาลัย<br>

    </figcaption>
</figure>

<a href="#top">กลับด้านบน</a>
<a href="#products">ไปยังสินค้า<br></a>
<hr>
<a href="mailto:contact@example.com">ส่งอีเมลหาเรา</a>

<a href="tel:+66812345678">โทร 081-234-3245</a>

<a href="files/document.pdf" download>
    ดาวน์โหลดเอกสาร
</a>

</body>
</html>
[วางโค้ด HTML ที่นี่]
```
- ภาพผลลัพธ์:
![image](https://github.com/user-attachments/assets/a63fcdb3-6d04-4c02-8c1d-57ce0acf9302)
![image](https://github.com/user-attachments/assets/7facee73-36f6-4d88-8097-31dc6e1dbd06)
![image](https://github.com/user-attachments/assets/fce91063-f513-425a-b9d2-f35bde8d6cab)
[วางภาพ screenshot ที่นี่]



