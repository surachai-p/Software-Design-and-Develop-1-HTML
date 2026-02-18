# ใบงานการทดลอง HTML

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
[วางโค้ด HTML ที่นี่]
```html
    <!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>แบบฟอร์มสมัครสมาชิก</title>
</head>
<body>
    <h1>แบบฟอร์มสมัครสมาชิกร้านค้าออนไลน์</h1>
    
    <form action="/register" method="post" enctype="multipart/form-data" onsubmit="validateForm(event)">
    
        <h2>ข้อมูลส่วนตัว</h2>
        <table border="1" cellpadding="10" cellspacing="0">
            <tr>
                <td><label for="firstName">ชื่อ *</label></td>
                <td><input type="text" id="firstName" name="firstName" placeholder="กรุณากรอกชื่อ" required></td>
            </tr>
            <tr>
                <td><label for="lastName">นามสกุล *</label></td>
                <td><input type="text" id="lastName" name="lastName" placeholder="กรุณากรอกนามสกุล" required></td>
            </tr>
            <tr>
                <td><label for="birthdate">วันเกิด *</label></td>
                <td><input type="date" id="birthdate" name="birthdate" required></td>
            </tr>
            <tr>
                <td><label>เพศ *</label></td>
                <td>
                    <input type="radio" id="male" name="gender" value="male" required> <label for="male">ชาย</label>
                    <input type="radio" id="female" name="gender" value="female"> <label for="female">หญิง</label>
                    <input type="radio" id="other" name="gender" value="other"> <label for="other">อื่น ๆ</label>
                </td>
            </tr>
        </table>
    
        <h2>ข้อมูลการติดต่อ</h2>
        <table border="1" cellpadding="10" cellspacing="0">
            <tr>
                <td><label for="email">อีเมล *</label></td>
                <td><input type="email" id="email" name="email" placeholder="example@email.com" pattern="[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}" required></td>
            </tr>
            <tr>
                <td><label for="phone">เบอร์โทรศัพท์ *</label></td>
                <td><input type="tel" id="phone" name="phone" placeholder="0812345678" pattern="0[0-9]{9}" required></td>
            </tr>
            <tr>
                <td><label for="address">ที่อยู่จัดส่ง *</label></td>
                <td><textarea id="address" name="address" rows="4" cols="30" placeholder="กรุณากรอกที่อยู่เต็มที่" required></textarea></td>
            </tr>
        </table>
    
        <h2>รูปโปรไฟล์</h2>
        <table border="1" cellpadding="10" cellspacing="0">
            <tr>
                <td><label for="profile_pic">อัพโหลดรูปโปรไฟล์ *</label></td>
                <td>
                    <input type="file" id="profile_pic" name="profile_pic" accept="image/*" required onchange="validateImageFile(this)">
                    <br><small>รองรับไฟล์: JPG, PNG, GIF (ขนาดสูงสุด 5 MB)</small>
                    <div id="profile_pic_error" style="color: red; display: none;"></div>
                </td>
            </tr>
        </table>
    
        <h2>รหัสผ่าน</h2>
        <table border="1" cellpadding="10" cellspacing="0">
            <tr>
                <td><label for="password">รหัสผ่าน *</label></td>
                <td>
                    <input type="password" id="password" name="password" placeholder="กรุณากรอกรหัสผ่าน" minlength="8" pattern="^(?=.*[a-z])(?=.*[A-Z])(?=.*\d).*$" required onkeyup="validatePassword(this)">
                    <br><small>ต้องมีอย่างน้อย 8 ตัวอักษร, ตัวพิมพ์เล็ก, ตัวพิมพ์ใหญ่, และตัวเลข</small>
                </td>
            </tr>
            <tr>
                <td><label for="confirm_password">ยืนยันรหัสผ่าน *</label></td>
                <td>
                    <input type="password" id="confirm_password" name="confirm_password" placeholder="กรุณากรอกรหัสผ่านอีกครั้ง" required onkeyup="comparePasswords()">
                    <div id="password_match_error" style="color: red; display: none;"></div>
                </td>
            </tr>
        </table>
    
        <h2>ความสนใจในหมวดหมู่สินค้า</h2>
        <table border="1" cellpadding="10" cellspacing="0">
            <tr>
                <td><label>เลือกหมวดหมู่ที่คุณสนใจ *</label></td>
                <td>
                    <input type="checkbox" name="categories" value="electronics"> อุปกรณ์อิเล็กทรอนิกส์
                    <br><input type="checkbox" name="categories" value="fashion"> แฟชั่นและเสื้อผ้า
                    <br><input type="checkbox" name="categories" value="home"> สินค้าเพื่อบ้านและครอบครัว
                    <br><input type="checkbox" name="categories" value="sports"> กีฬาและสุขภาพ
                    <br><input type="checkbox" name="categories" value="books"> หนังสือและการศึกษา
                    <br><input type="checkbox" name="categories" value="food"> อาหารและเครื่องดื่ม
                    <div id="categories_error" style="color: red; display: none;"></div>
                </td>
            </tr>
        </table>
    
        <h2>เงื่อนไขการใช้งาน</h2>
        <table border="1" cellpadding="10" cellspacing="0">
            <tr>
                <td><label>การยอมรับ *</label></td>
                <td>
                    <input type="checkbox" id="terms" name="terms" required>
                    <label for="terms">ฉันยอมรับ<a href="#" target="_blank"> เงื่อนไขการใช้งาน</a>และ<a href="#" target="_blank"> นโยบายความเป็นส่วนตัว</a></label>
                </td>
            </tr>
            <tr>
                <td><label>ข้อมูลข่าวสาร</label></td>
                <td>
                    <input type="checkbox" id="newsletter" name="newsletter">
                    <label for="newsletter">ฉันต้องการรับข้อมูลข่าวสารและสิ่งโปรโมชั่นจากบริษัท</label>
                </td>
            </tr>
        </table>
    
        <h2>ส่งแบบฟอร์ม</h2>
        <table border="1" cellpadding="10" cellspacing="0">
            <tr>
                <td colspan="2">
                    <button type="submit">สมัครสมาชิก</button>
                    <button type="reset">ล้างข้อมูล</button>
                </td>
            </tr>
        </table>
    
    </form>
    
   
        
        
</body>
</html>
```
- ภาพผลลัพธ์:
![alt text](image-5.png)



