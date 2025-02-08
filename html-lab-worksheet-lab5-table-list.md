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
<html lang="th">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>kinmai</title>
</head>
<body>

  <!-- Navigation -->
  <nav>
    <a href="index.html">หน้าหลัก</a>
    <a href="pages/about.html">เกี่ยวกับ</a>
    <a href="pages/contact.html">ติดต่อเรา</a>
    <a href="files/document.pdf" download>Download Document</a>
  </nav>

  <button onclick="history.back()">⬅ กลับหน้าหลัก</button>

  <h2>ข้อมูลส่วนตัว</h2>
  <table border="1">
    <thead>
      <tr>
        <th>หัวข้อ</th>
        <th>รายละเอียด</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>ชื่อ</td>
        <td>สุมารี</td>
      </tr>
      <tr>
        <td>อายุ</td>
        <td>18</td>
      </tr>
    </tbody>
  </table>

  <h2>เมนูอาหาร</h2>
  <ul>
    <li>ส้มตำไทย</li>
    <li>ต้มยำกุ้ง</li>
    <li>ผัดไทย</li>
    <li>แกงเขียวหวาน</li>
  </ul>

  <div>
    <div onclick="showDialog('images/products/food1.jpg', 'ส้มตำไทย')">
      <img src="images/products/food1.jpg" alt="food1" style="width:100%; max-width:250px; height:auto;">
      <p>ส้มตำไทย</p>
    </div>
    <div onclick="showDialog('images/products/food2.jpg', 'ต้มยำกุ้ง')">
      <img src="images/products/food2.jpg" alt="food2" style="width:100%; max-width:250px; height:auto;">
      <p>ต้มยำกุ้ง</p>
    </div>
    <div onclick="showDialog('images/products/food3.jpg', 'ผัดไทย')">
      <img src="images/products/food3.jpg" alt="food3" style="width:100%; max-width:250px; height:auto;">
      <p>ผัดไทย</p>
    </div>
    <div onclick="showDialog('images/products/food4.jpg', 'แกงเขียวหวาน')">
      <img src="images/products/food4.jpg" alt="food4" style="width:100%; max-width:250px; height:auto;">
      <p>แกงเขียวหวาน</p>
    </div>
  </div>

  <div id="dialog" style="display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: hsl(0, 0%, 100%); display: flex; align-items: center; justify-content: center;">
    <div style="background: #ffffff; padding: 20px; border-radius: 20px; max-width: 1200px; text-align: center;">
      <img id="dialog-image" src="" alt="" style="width: 100%; border-radius: 12px;">
      <p id="dialog-description"></p>
      <button onclick="closeDialog()">ปิดหน้านี้</button>
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
![lab5](https://github.com/user-attachments/assets/634b4606-1379-4323-848d-ca0f58725216)


