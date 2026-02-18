# ใบงานการทดลอง HTML

## จุดประสงค์การเรียนรู้
1. อธิบายโครงสร้างของ HTML ได้
2. สามารถใช้งาน HTML tag พื้นฐานได้
3. สามารถสร้างหน้าเว็บเพจอย่างง่ายได้

## เครื่องมือที่ใช้
1. Visual Studio Code
2. Web Browser 
3. Extension Live Server


## การทดลองที่ 1: การติดตั้งและเตรียมเครื่องมือ

### ขั้นตอนที่ 1: การติดตั้ง Visual Studio Code
1. เปิดเว็บเบราว์เซอร์และเข้าไปที่ https://code.visualstudio.com
2. คลิกปุ่ม Download โดยเลือกตามระบบปฏิบัติการ
3. เมื่อดาวน์โหลดเสร็จ ให้เปิดไฟล์ที่ดาวน์โหลดมา
4. ทำตามขั้นตอนการติดตั้ง:
    - เลือกตัวเลือกเพิ่มเติม:
     * [✓] Add "Open with Code" action to Windows Explorer file context menu
     * [✓] Add "Open with Code" action to Windows Explorer directory context menu
     * [✓] Register Code as an editor for supported file types
     * [✓] Add to PATH

### ขั้นตอนที่ 2: การติดตั้ง Extension Live Server
1. เปิดโปรแกรม Visual Studio Code
2. คลิกไอคอน Extensions ที่แถบด้านซ้าย (รูปสี่เหลี่ยมจตุรัส 4 ชิ้น) หรือกด Ctrl+Shift+X
3. พิมพ์คำว่า "Live Server" ในช่องค้นหา
4. มองหา "Live Server" ของ Ritwick Dey (มักจะอยู่อันดับแรก)
5. คลิกปุ่ม "Install"
6. รอจนติดตั้งเสร็จ (ปุ่มจะเปลี่ยนเป็น "Uninstall")
7. คลิก "Reload" เพื่อเริ่มการทำงานของ Extension

### ขั้นตอนที่ 3: การสร้างโฟลเดอร์สำหรับเก็บไฟล์งาน
1. เปิด File Explorer (Windows) หรือ Finder (macOS)
2. ไปที่ตำแหน่งที่ต้องการสร้างโฟลเดอร์
3. คลิกขวา > New > Folder
4. ตั้งชื่อโฟลเดอร์เป็น "html-workshop"
5. เปิด VS Code
6. ไปที่ File > Open Folder หรือกด Ctrl+K Ctrl+O
7. เลือกโฟลเดอร์ "html-workshop" ที่สร้างไว้
8. คลิก "Select Folder"

### ขั้นตอนที่ 4: การทดสอบ Live Server
1. สร้างไฟล์ใหม่:
   - คลิกไอคอน New File ในแถบด้านซ้าย หรือกด Ctrl+N
   - ไปที่ File > Save หรือกด Ctrl+S
   - ตั้งชื่อไฟล์เป็น "test.html"
2. พิมพ์โค้ด HTML พื้นฐาน:
   ```html
   <!DOCTYPE html>
   <html>
   <head>
       <title>ทดสอบ Live Server</title>
   </head>
   <body>
       <h1>สวัสดี Live Server</h1>
   </body>
   </html>
   ```
3. บันทึกไฟล์ (Ctrl+S)
4. เริ่มใช้งาน Live Server โดยทำวิธีใดวิธีหนึ่ง:
   - คลิกขวาที่ไฟล์ test.html แล้วเลือก "Open with Live Server"
   - คลิก "Go Live" ที่แถบสถานะด้านล่าง
   - กด Alt+L Alt+O
5. เว็บเบราว์เซอร์จะเปิดขึ้นมาโดยอัตโนมัติที่ http://127.0.0.1:5500
6. ทดสอบการทำงาน:
   - แก้ไขข้อความใน <h1>
   - บันทึกไฟล์
   - สังเกตว่าเบราว์เซอร์รีเฟรชอัตโนมัติ
   - 
#### หมายเหตุ สามารถติดตั้ง Live Preview ของไมโครซอฟต์ แทนการใช้ Live Server เมื่อติดตั้งแล้ว สามารถคลิกเมาส์ด้านขวาที่ไฟล์ HTML เลือกเมนู Show Preview เพื่อดูผลลัพธ์ HTML ได้เช่นกัน
  
### บันทึกผลการทดลอง
<img width="412" height="197" alt="Screenshot 2026-02-18 000947" src="https://github.com/user-attachments/assets/48a95204-4c35-4695-bebc-6c715a6bfdaf" />


## การทดลองที่ 2: โครงสร้างพื้นฐาน HTML
### ขั้นตอนการทดลอง
1. สร้างไฟล์ index.html
2. เขียนโครงสร้างพื้นฐาน HTML:
```html
<!DOCTYPE html>
<html>
<head>
    <title>My First Web Page</title>
</head>
<body>
    <h1>Welcome to ...... (student name) web page</h1>
    <p>This is my first web page.</p>
    <div>This is a block element</div>
    <span>This is an inline element</span>
    <em>This text is emphasized</em>
    <strong>This text is strong</strong>    
</body>
</html>
```
3. บันทึกไฟล์และเปิดด้วย Live Server


### คำอธิบายเพิ่มเติม
- `<!DOCTYPE html>` คือการประกาศประเภทเอกสารเป็น HTML5
- `<html>` เป็น tag หลักที่ครอบคลุมทั้งเอกสาร
- `<head>` ใช้สำหรับข้อมูล metadata และการเชื่อมโยงไฟล์ภายนอก
- `<body>` คือส่วนที่แสดงผลบนหน้าเว็บ
- `<div>` เป็น block element ที่ขึ้นบรรทัดใหม่โดยอัตโนมัติ
- `<span>` เป็น inline element ที่ต่อเนื่องในบรรทัดเดียวกัน
- `<em>` ใช้เน้นข้อความ (แสดงเป็นตัวเอียง)
- `<strong>` ใช้เน้นข้อความ (แสดงเป็นตัวหนา)
  
  ### บันทึกผลการทดลอง
- รหัสเอกสาร HTML ที่เขียน:
```html
<!DOCTYPE html>
<html>
<head>
    <title>My First Web Page</title>
</head>
<body>
    <h1>Welcome to Pathittaya web page</h1>
    <p>This is my first web page.</p>
    <div>This is a block element</div>
    <span>This is an inline element</span>
    <em>This text is emphasized</em>
    <strong>This text is strong</strong>    
</body>
</html>
```
- ภาพผลลัพธ์:
<img width="592" height="208" alt="Screenshot 2026-02-18 001320" src="https://github.com/user-attachments/assets/8b968d24-4683-456f-8607-c28e721ff3ec" />

  
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
<html>
<head>
    <title>Pathittaya Web Page</title>
</head>
<body>
    <h1>แนะนำตัวเอง (About Me)</h1>
    <h2>ชื่อ-นามสกุล</h2>
    <hr><p>นางสาวปทิตญา ภูกิจคุณาเดชากร</p>

    <h2>ประวัติการศึกษา</h2>
    <hr><pre>
    มัธยมศึกษาตอนต้น <em> แผนการเรียนวิทยาศาสตร์ คณิตศาสตร์ และเทคโนโลยีสิ่งแวดล้อม (SMTE) </em><strong> โรงเรียนสมุทรสาครบูรณะ</strong><br>
    มัธยมศึกษาตอนปลาย <em> แผนการเรียนภาษาอังกฤษ-คอมพิวเตอร์ </em><strong> โรงเรียนสมุทรสาครบูรณะ</strong><br>
    ปริญญาตรี <em> สาขาวิชาเทคโนโลยีคอมพิวเตอร์ คณะครุศาสตร์อุตสาหกรรมและเทคโนโลยี </em><strong> สถาบันเทคโนโลยีพระจอมเกล้าเจ้าคุณทหารลาดกระบัง</strong></p>
</pre>

    <h2>งานอดิเรก</h2>
    <hr><p>ในเวลาว่างชอบ<strong> ฟังเพลง ร้องเพลง ดูคลิปวิดีโอเกี่ยวกับการออกแบบต่างๆและฝึกทำ </strong><br></p>

    <h2>เป้าหมายในอนาคต</h2>
    <hr><pre>
    1. เป็นครูที่ดี ที่น่ารัก และคอยซัพพอร์ตนักเรียนอย่างเต็มที่
    2. พัฒนาทักษะการสอนและความรู้ในสายงานเทคโนโลยีอย่างต่อเนื่อง
    3. มีบ้านที่อบอุ่น ให้คนในครอบครัวอยู่ด้วยกันพร้อมหน้าอย่างมีความสุข
    </pre>

</body>
</html>
```
- ภาพผลลัพธ์:
<img width="1906" height="777" alt="Screenshot 2026-02-18 011419" src="https://github.com/user-attachments/assets/b0d0ab20-d3a0-4abc-9b19-3ad76bfbd5da" />


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
[วางโค้ด HTML ที่นี่]
```
- ภาพผลลัพธ์:
[วางภาพ screenshot ที่นี่]


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
<img width="832" height="597" alt="Screenshot 2026-02-18 151701" src="https://github.com/user-attachments/assets/88141296-5005-43fd-b638-61e7184421c9" />





<img width="830" height="742" alt="Screenshot 2026-02-18 151726" src="https://github.com/user-attachments/assets/c28a0ebe-b464-45c1-ba1c-c1aaa8a6df29" />

## การทดลองที่ 6: การสร้างฟอร์ม
### วัตถุประสงค์
- สร้างฟอร์มรับข้อมูลได้ตามกำหนด
- เลือกใช้ประเภทของ input แบบต่างๆ ได้เหมาะสม
- สามารถใช้งาน form validation ได้

### ขั้นตอนการทดลอง
1. สร้างฟอร์มลงทะเบียนนักศึกษา:
```html
    <!-- กำหนดรูปแบบของฟอร์มบางส่วน -->
  <style>
        .form-group {
            margin-bottom: 15px;
        }
        
        .input-wrapper {
            display: flex;
            align-items: center;
        }
        
        .required-mark {
            color: red;
            margin-left: 5px;
        }
    </style>

    <body>
        <form action="/register" method="post">
            <!-- ส่วนข้อมูลส่วนตัว -->
            <fieldset>
                <legend>ข้อมูลส่วนตัว</legend>
                
                <div class="form-group">
                    <label for="studentId">รหัสนักศึกษา:</label>
                    <input type="text" id="studentId" name="studentId" 
                           pattern="[0-9]{8}" required>
                </div>
        
                <div class="form-group">
                    <label for="prefix">คำนำหน้า:</label>
                     <select id="prefix" name="prefix" required>
                        <option value="">เลือกคำนำหน้า</option>
                        <option value="mr">นาย</option>
                        <option value="ms">นางสาว</option>
                        <option value="mrs">นาง</option>
                    </select>
                </div>
        
                <div class="form-group">
                    <label for="firstName">ชื่อ:</label>
                    <input type="text" id="firstName" name="firstName" required>
                </div>
        
                <div class="form-group">
                    <label for="lastName">นามสกุล:</label>
                    <input type="text" id="lastName" name="lastName" required>
                </div>
        
                <div class="form-group">
                    <label for="birthdate">วันเกิด:</label>
                    <input type="date" id="birthdate" name="birthdate" required>
                </div>
        
                <div class="form-group">
                    <label>เพศ:</label>
                    <input type="radio" id="male" name="gender" value="male" required>
                    <label for="male">ชาย</label>
                    <input type="radio" id="female" name="gender" value="female">
                    <label for="female">หญิง</label>
                </div>
            </fieldset>
        
            <!-- ส่วนข้อมูลการติดต่อ -->
            <fieldset>
                <legend>ข้อมูลการติดต่อ</legend>
        
                <div class="form-group">
                    <label for="email">อีเมล:</label>
                    <input type="email" id="email" name="email" required>
                </div>
        
                <div class="form-group">
                    <label for="phone">เบอร์โทรศัพท์:</label>
                    <input type="tel" id="phone" name="phone" 
                           pattern="[0-9]{10}" required>
                </div>
        
                <div class="form-group">
                    <label for="address">ที่อยู่:</label>
                    <textarea id="address" name="address" 
                              rows="3" required></textarea> <span class="required-mark">*</span>
                </div>
            </fieldset>
        
            <!-- ส่วนข้อมูลการศึกษา -->
            <fieldset>
                <legend>ข้อมูลการศึกษา</legend>
        
                <div class="form-group">
                    <label for="faculty">คณะ:</label>
                    <select id="faculty" name="faculty" required>
                        <option value="">เลือกคณะ</option>
                        <option value="siet">ครุศาสตร์อุตสาหกรรมและเทคโนโลยี</option>
                        <option value="engineering">วิศวกรรมศาสตร์</option>
                        <option value="science">วิทยาศาสตร์</option>
                    </select> <span class="required-mark">*</span>
                </div>
        
                <div class="form-group">
                    <label for="major">สาขาวิชา:</label>
                    <select id="major" name="major" required>
                        <option value="">เลือกสาขาวิชา</option>
                        <!-- ตัวเลือกจะเปลี่ยนตามคณะที่เลือก ส่วนนี้ Code ยังไม่สมบูรณ์-->
                    </select> <span class="required-mark">*</span>
                </div>
        
                <div class="form-group">
                    <label for="gpa">เกรดเฉลี่ยสะสม:</label>
                    <input type="number" id="gpa" name="gpa" 
                           min="0" max="4" step="0.01" required> <span class="required-mark">*</span>
                </div>
            </fieldset>
        
            <!-- ส่วนความสนใจและกิจกรรม -->
            <fieldset>
                <legend>ความสนใจและกิจกรรม</legend>
        
                <div class="form-group">
                    <label>ความสนใจ:</label>
                    <input type="checkbox" id="sport" name="interests" value="sport">
                    <label for="sport">กีฬา</label>
                    <input type="checkbox" id="music" name="interests" value="music">
                    <label for="music">ดนตรี</label>
                    <input type="checkbox" id="art" name="interests" value="art">
                    <label for="art">ศิลปะ</label>
                    <input type="checkbox" id="tech" name="interests" value="tech">
                    <label for="tech">เทคโนโลยี</label>
                </div>
        
                <div class="form-group">
                    <label for="club">ชมรมที่สนใจ:</label>
                    <select id="club" name="club" multiple>
                        <option value="computer">ชมรมคอมพิวเตอร์</option>
                        <option value="robot">ชมรมหุ่นยนต์</option>
                        <option value="sport">ชมรมกีฬา</option>
                        <option value="music">ชมรมดนตรี</option>
                    </select>
                </div>
            </fieldset>
        
            <!-- ส่วนอัพโหลดเอกสาร -->
            <fieldset>
                <legend>เอกสารประกอบ</legend>
                <div class="form-group">
                    <label for="photo">รูปถ่าย:</label>
                    <input type="file" id="photo" name="photo" 
                           accept="image/*" required><span class="required-mark">*</span>
                </div>
        
                <div class="form-group">
                    <label for="transcript">ใบแสดงผลการเรียน:</label>
                    <input type="file" id="transcript" name="transcript" 
                           accept=".pdf,.doc,.docx" required>
                           <span class="required-mark">*</span>
                </div>
            </fieldset>
        
            <!-- ส่วนยืนยันข้อมูล -->
            <fieldset>
                <legend>การยืนยัน</legend>
        
                <div class="form-group">
                    <input type="checkbox" id="agree" name="agree" required>
                    <label for="agree">
                        ข้าพเจ้ายืนยันว่าข้อมูลทั้งหมดเป็นความจริง
                    </label>
                </div>
        
                <div class="form-group">
                    <button type="submit">ลงทะเบียน</button>
                    <button type="reset">ล้างข้อมูล</button>
                </div>
            </fieldset>
        </form>
```

### คำอธิบายเพิ่มเติม
1. Input Types ที่ใช้:
   - text: สำหรับข้อความทั่วไป
   - email: สำหรับอีเมล (มีการตรวจสอบรูปแบบอัตโนมัติ)
   - tel: สำหรับเบอร์โทรศัพท์
   - date: สำหรับวันที่
   - number: สำหรับตัวเลข
   - radio: สำหรับตัวเลือกเดียว
   - checkbox: สำหรับหลายตัวเลือก
   - file: สำหรับอัพโหลดไฟล์
   - select: สำหรับรายการแบบเลือก
   - textarea: สำหรับข้อความหลายบรรทัด

2. Attributes ที่สำคัญ:
   - required: จำเป็นต้องกรอก
   - pattern: กำหนดรูปแบบข้อมูล
   - min/max: กำหนดค่าต่ำสุด/สูงสุด
   - accept: กำหนดประเภทไฟล์ที่ยอมรับ
   - multiple: เลือกได้หลายตัวเลือก

### แบบฝึกหัด
1. สร้างฟอร์มสมัครสมาชิกร้านค้าออนไลน์ที่มี:
   - ข้อมูลส่วนตัว (ชื่อ-นามสกุล, วันเกิด, เพศ)
   - ข้อมูลการติดต่อ (อีเมล, เบอร์โทร, ที่อยู่จัดส่ง)
   - รูปโปรไฟล์
   - การยืนยันรหัสผ่าน
   - ความสนใจในหมวดหมู่สินค้า
   - การยอมรับเงื่อนไขการใช้งาน

2. เพิ่ม validation ที่เหมาะสม:
   - ตรวจสอบรูปแบบอีเมล
   - ตรวจสอบความยาวรหัสผ่าน
   - ตรวจสอบรูปแบบเบอร์โทร
   - ตรวจสอบขนาดไฟล์รูปภาพ

### บันทึกผลการทดลอง
```html
<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>แบบฝึกหัด: ฟอร์มสมัครสมาชิกร้านค้าออนไลน์</title>
    <style>
        body { 
            font-family: 'Sarabun', sans-serif; 
            line-height: 1.6; 
            padding: 40px 20px; 
            background-color: #f0f2f5; 
            display: flex;
            justify-content: center; /* จัดกึ่งกลางแนวนอน */
            align-items: flex-start;
            min-height: 100vh;
            margin: 0;
        }

        #regForm {
            width: 100%;
            max-width: 500px; /* ปรับความกว้างฟอร์มให้เล็กลง */
            background-color: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        h2 { text-align: center; color: #1a73e8; margin-bottom: 25px; }
        
        .form-group { margin-bottom: 15px; }
        .required-mark { color: red; margin-left: 5px; font-weight: bold; }
        
        fieldset { 
            border: 1px solid #e0e0e0; 
            padding: 15px; 
            border-radius: 8px; 
            margin-bottom: 20px; 
        }
        
        legend { font-weight: bold; padding: 0 10px; color: #555; font-size: 0.95em; }

        /* ส่วนความสนใจแบบเลื่อนได้ */
        .scroll-box {
            border: 1px solid #ddd;
            border-radius: 4px;
            height: 120px;
            overflow-y: scroll;
            padding: 10px;
            background: #fafafa;
            margin-top: 5px;
        }
        .interest-item { display: block; margin-bottom: 8px; font-size: 0.9em; }

        input[type="text"], input[type="email"], input[type="password"], input[type="tel"], textarea, select {
            width: 100%; 
            padding: 10px; 
            margin-top: 5px; 
            border: 1px solid #ddd; 
            border-radius: 6px; 
            box-sizing: border-box;
            transition: border-color 0.3s;
        }

        input:focus, select:focus, textarea:focus {
            border-color: #1a73e8;
            outline: none;
        }

        .error-text { color: red; font-size: 0.8em; display: none; margin-top: 5px; }

        .button-container { 
            display: flex; 
            gap: 10px; 
            justify-content: center; 
            margin-top: 20px;
        }

        button { 
            flex: 1;
            cursor: pointer; 
            padding: 12px; 
            border: none; 
            border-radius: 6px; 
            font-weight: bold;
            transition: opacity 0.3s, transform 0.1s;
        }

        .btn-submit { background-color: #28a745; color: white; }
        .btn-reset { background-color: #6c757d; color: white; }
        
        button:hover { opacity: 0.9; transform: translateY(-1px); }
        button:active { transform: translateY(0); }

        .terms-container { text-align: center; font-size: 0.9em; margin: 15px 0; }
    </style>
</head>
<body>

    <form action="/register" method="post" enctype="multipart/form-data" id="regForm">
        <h2>สมัครสมาชิก</h2>
        
        <fieldset>
            <legend>ข้อมูลส่วนตัว</legend>
            <div class="form-group">
                <label for="fullName">ชื่อ-นามสกุล:</label><span class="required-mark">*</span>
                <input type="text" id="fullName" name="fullName" placeholder="เช่น นายสมชาย ใจดี" required>
            </div>
            
            <div class="form-group">
                <label for="birthdate">วันเกิด (วว/ดด/ปปปป):</label><span class="required-mark">*</span>
                <input type="text" id="birthdate" name="birthdate" placeholder="DD/MM/YYYY" maxlength="10" required>
            </div>

            <div class="form-group">
                <label for="gender">เพศ:</label><span class="required-mark">*</span>
                <select id="gender" name="gender" required>
                    <option value="">-- เลือกเพศ --</option>
                    <option value="male">ชาย</option>
                    <option value="female">หญิง</option>
                    <option value="other">อื่นๆ / ไม่ระบุ</option>
                </select>
            </div>
        </fieldset>

        <fieldset>
            <legend>ข้อมูลการติดต่อ</legend>
            <div class="form-group">
                <label for="email">อีเมล:</label><span class="required-mark">*</span>
                <input type="email" id="email" name="email" placeholder="example@mail.com" required>
            </div>
            <div class="form-group">
                <label for="phone">เบอร์โทรศัพท์:</label><span class="required-mark">*</span>
                <input type="tel" id="phone" name="phone" pattern="[0-9]{10}" placeholder="081xxxxxxx" required>
            </div>
            <div class="form-group">
                <label for="address">ที่อยู่จัดส่ง:</label><span class="required-mark">*</span>
                <textarea id="address" name="address" rows="2" placeholder="ระบุที่อยู่..." required></textarea>
            </div>
        </fieldset>

        <fieldset>
            <legend>ความสนใจสินค้า <span class="required-mark">*</span></legend>
            <div class="scroll-box">
                <label class="interest-item"><input type="checkbox" name="interest" value="fashion"> แฟชั่น</label>
                <label class="interest-item"><input type="checkbox" name="interest" value="electronics"> เครื่องใช้ไฟฟ้า</label>
                <label class="interest-item"><input type="checkbox" name="interest" value="home"> บ้านและสวน</label>
                <label class="interest-item"><input type="checkbox" name="interest" value="beauty"> ความงาม</label>
                <label class="interest-item"><input type="checkbox" name="interest" value="sport"> อุปกรณ์กีฬา</label>
                <label class="interest-item"><input type="checkbox" name="interest" value="food"> อาหารและเครื่องดื่ม</label>
                <label class="interest-item"><input type="checkbox" name="interest" value="gadget"> ไอทีและเกมมิ่ง</label>
                <label class="interest-item">
                    <input type="checkbox" id="checkOther" name="interest" value="other"> อื่นๆ: 
                    <input type="text" id="otherText" name="otherInterest" placeholder="ระบุ..." style="width: 60%; padding: 4px; display:inline-block;">
                </label>
            </div>
            <p id="interestError" class="error-text">⚠️ โปรดเลือกอย่างน้อย 1 รายการ</p>
        </fieldset>

        <fieldset>
            <legend>โปรไฟล์และรหัสผ่าน</legend>
            <div class="form-group">
                <label for="photo">รูปโปรไฟล์:</label><span class="required-mark">*</span>
                <input type="file" id="photo" name="photo" accept="image/*" required>
                <p id="fileError" class="error-text">⚠️ ไฟล์ต้องไม่เกิน 2MB</p>
            </div>
            <div class="form-group">
                <label for="password">รหัสผ่าน:</label><span class="required-mark">*</span>
                <input type="password" id="password" name="password" minlength="8" placeholder="อย่างน้อย 8 ตัวอักษร" required>
            </div>
            <div class="form-group">
                <label for="confirmPassword">ยืนยันรหัสผ่าน:</label><span class="required-mark">*</span>
                <input type="password" id="confirmPassword" name="confirmPassword" placeholder="กรอกรหัสอีกครั้ง" required>
                <p id="passError" class="error-text">⚠️ รหัสผ่านไม่ตรงกัน</p>
            </div>
        </fieldset>

        <div class="terms-container">
            <input type="checkbox" id="terms" name="terms" required>
            <label for="terms">ยอมรับเงื่อนไขการใช้งาน</label><span class="required-mark">*</span>
        </div>

        <div class="button-container">
            <button type="submit" class="btn-submit">ยืนยันสมัครสมาชิก</button>
            <button type="reset" class="btn-reset">ล้างข้อมูล</button>
        </div>
    </form>

    <script>
        // เติม / ให้อัตโนมัติในช่องวันเกิด
        const birthInput = document.getElementById('birthdate');
        birthInput.addEventListener('input', (e) => {
            let v = e.target.value.replace(/\D/g,'');
            if (v.length > 2) v = v.slice(0,2) + '/' + v.slice(2);
            if (v.length > 5) v = v.slice(0,5) + '/' + v.slice(5,9);
            e.target.value = v;
        });

        // ตรวจสอบฟอร์มก่อนส่ง
        document.getElementById('regForm').onsubmit = function(e) {
            let valid = true;
            
            if(document.getElementById('password').value !== document.getElementById('confirmPassword').value) {
                document.getElementById('passError').style.display = 'block';
                valid = false;
            } else { document.getElementById('passError').style.display = 'none'; }

            const file = document.getElementById('photo').files[0];
            if(file && file.size > 2*1024*1024) {
                document.getElementById('fileError').style.display = 'block';
                valid = false;
            } else { document.getElementById('fileError').style.display = 'none'; }

            const checked = document.querySelectorAll('input[name="interest"]:checked');
            if(checked.length === 0) {
                document.getElementById('interestError').style.display = 'block';
                valid = false;
            } else { document.getElementById('interestError').style.display = 'none'; }

            if(!valid) { 
                e.preventDefault(); 
                alert('กรุณาตรวจสอบข้อมูลที่มีเครื่องหมาย * ให้ถูกต้อง'); 
            }
        };
    </script>
</body>
</html>
```
- ภาพผลลัพธ์:

<img width="698" height="905" alt="Screenshot 2026-02-18 144018" src="https://github.com/user-attachments/assets/884bcd19-1ede-4a9b-870d-b9a81c428332" />





<img width="694" height="818" alt="Screenshot 2026-02-18 144039" src="https://github.com/user-attachments/assets/52dec78e-7c6f-43c9-be40-69655100ffba" />


## การทดลองที่ 7: HTML Layout
### วัตถุประสงค์
- จัดวางองค์ประกอบในหน้าเว็บได้
- ใช้ semantic elements
- สร้าง responsive layout ได้

### ขั้นตอนการทดลอง
1. เรียนรู้ semantic elements:
semantic elements คือ elements ใน HTML5 ที่มีความหมายในตัวเอง ช่วยอธิบายโครงสร้างและความหมายของเนื้อหาในหน้าเว็บ
    ตัวอย่าง Semantic Elements หลักๆ:

```html
<header>      <!-- ส่วนหัวของหน้าเว็บหรือส่วน -->
<nav>         <!-- ส่วนเมนูนำทาง -->
<main>        <!-- เนื้อหาหลักของหน้าเว็บ -->
<article>     <!-- เนื้อหาที่เป็นบทความ สามารถแยกออกมาอ่านเดี่ยวๆ ได้ -->
<section>     <!-- ส่วนของเนื้อหาที่เกี่ยวข้องกัน -->
<aside>       <!-- เนื้อหาที่เกี่ยวข้องแต่ไม่ใช่เนื้อหาหลัก -->
<footer>      <!-- ส่วนท้ายของหน้าเว็บหรือส่วน -->
```

### ข้อดีของการใช้ Semantic Elements:


### SEO (Search Engine Optimization):

```html 
<!-- แบบไม่ใช้ Semantic -->
<div class="header">
    <div class="nav">...</div>
</div>

<!-- แบบใช้ Semantic - Search Engine เข้าใจโครงสร้างได้ดีกว่า -->
<header>
    <nav>...</nav>
</header>
```

### Accessibility:

```html
<!-- Screen reader จะอ่านและเข้าใจโครงสร้างได้ดีขึ้น -->
<main>
    <article>
        <h1>หัวข้อบทความ</h1>
        <p>เนื้อหา...</p>
    </article>
</main>
```
### ตัวอย่างการใช้งาน
```html
<body>
    <header>
        <h1>ชื่อเว็บไซต์</h1>
        <nav>
            <ul>
                <li><a href="/">หน้าแรก</a></li>
                <li><a href="/about">เกี่ยวกับเรา</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <article>
            <h2>บทความที่ 1</h2>
            <p>เนื้อหาบทความ...</p>
        </article>

        <aside>
            <h3>บทความที่เกี่ยวข้อง</h3>
            <ul>
                <li><a href="#">บทความอื่น 1</a></li>
                <li><a href="#">บทความอื่น 2</a></li>
            </ul>
        </aside>
    </main>

    <footer>
        <p>ลิขสิทธิ์ © 2024</p>
    </footer>
</body>
```


### บันทึกผลการทดลอง
<img width="413" height="523" alt="Screenshot 2026-02-18 014524" src="https://github.com/user-attachments/assets/33253981-b885-4457-a354-baced6bf1cc7" />

