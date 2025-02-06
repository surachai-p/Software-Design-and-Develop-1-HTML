# ใบงานการทดลอง HTML

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

[วางโค้ด HTML ที่นี่]
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Menu</title>
</head>
<body>

  <!-- Navigation -->
  <nav>
    <a href="index.html">Home</a>
    <a href="pages/about.html">About</a>
    <a href="pages/contact.html">Contact</a>
    <a href="files/document.pdf" download>Download Document</a>
  </nav>

  <button onclick="history.back()">⬅ Back</button>

  <h2>Personal Information</h2>
  <table border="1">
    <thead>
      <tr>
        <th>Field</th>
        <th>Details</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Name</td>
        <td>Suvijak Lawang</td>
      </tr>
      <tr>
        <td>Age</td>
        <td>20</td>
      </tr>
      <tr>
        <td>Email</td>
        <td>67030248@kmitl.ac.th</td>
      </tr>
    </tbody>
  </table>

  <h2>Food Menu</h2>
  <ul>
    <li>พิซซ่า</li>
    <li>ไก่ทอด</li>
    <li>เค้ก</li>
    <li>เบอร์เกอร์</li>
  </ul>

  <div>
    <div onclick="showDialog('images/products/pizza.jpg', 'พิซซ่า')">
      <img src="images/products/pizza.jpg" alt="พิซซ่า" style="width:100%; max-width:250px; height:auto;">
      <p>พิซซ่า</p>
    </div>
    <div onclick="showDialog('images/products/ไก่ทอด.jpg', 'ไก่ทอด')">
      <img src="images/products/ไก่ทอด.jpg" alt="ไก่ทอด" style="width:100%; max-width:250px; height:auto;">
      <p>ไก่ทอด</p>
    </div>
    <div onclick="showDialog('images/products/เค้ก.jpg', 'เค้ก')">
      <img src="images/products/เค้ก.jpg" alt="เค้ก" style="width:100%; max-width:250px; height:auto;">
      <p>เค้ก</p>
    </div>
    <div onclick="showDialog('images/products/เบอร์เกอร์.jpg', 'เบอร์เกอร์')">
      <img src="images/products/เบอร์เกอร์.jpg" alt="เบอร์เกอร์" style="width:100%; max-width:250px; height:auto;">
      <p>เบอร์เกอร์</p>
    </div>
  </div>

  <div id="dialog" style="display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0, 0, 0, 0.8); display: flex; align-items: center; justify-content: center;">
    <div style="background: white; padding: 16px; border-radius: 12px; max-width: 600px; text-align: center;">
      <img id="dialog-image" src="" alt="" style="width: 100%; border-radius: 12px;">
      <p id="dialog-description"></p>
      <button onclick="closeDialog()">Close</button>
    </div>
  </div>

  <script>
    function showDialog(imageSrc, description) {
      document.getElementById('dialog-image').src = imageSrc;
      document.getElementById('dialog-description').textContent = description;
      document.getElementById('dialog').style.display = 'flex';
    }

    function closeDialog() {
      document.getElementById('dialog').style.display = 'none';
    }
  </script>

</body>
</html>
```
- ภาพผลลัพธ์:
![labhtml5](https://github.com/user-attachments/assets/2dfbef9c-de2d-4e55-937f-d24b0fb03096)


