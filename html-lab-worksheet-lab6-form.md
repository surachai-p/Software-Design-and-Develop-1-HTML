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
```<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lab 6: การสร้างฟอร์ม - Weerapat Uamkasem</title>
    <style>
        body {
            font-family: 'Sarabun', sans-serif;
            margin: 20px;
            background-color: #f9f9f9;
        }
        h1, h2 {
            color: #333;
            border-bottom: 2px solid #ddd;
            padding-bottom: 10px;
        }
        form {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            max-width: 600px;
            margin: 0 auto 50px auto; /* จัดกึ่งกลาง */
        }
        fieldset {
            border: 1px solid #ccc;
            border-radius: 5px;
            margin-bottom: 20px;
            padding: 15px;
        }
        legend {
            font-weight: bold;
            color: #0056b3;
            padding: 0 5px;
        }
        .form-group {
            margin-bottom: 15px;
        }
        label {
            display: inline-block;
            width: 150px; /* จัดความกว้าง label ให้ตรงกัน */
            vertical-align: top;
            font-weight: 500;
        }
        /* ปรับ input ให้กว้างขึ้นและสวยงาม */
        input[type="text"], 
        input[type="email"], 
        input[type="tel"], 
        input[type="date"], 
        input[type="password"],
        input[type="number"],
        select, 
        textarea {
            padding: 5px;
            border: 1px solid #ccc;
            border-radius: 4px;
            width: 250px;
        }
        input[type="radio"], input[type="checkbox"] {
            width: auto;
            margin-right: 5px;
        }
        /* CSS สำหรับปุ่ม */
        button {
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            margin-right: 10px;
        }
        button[type="submit"] {
            background-color: #28a745;
            color: white;
        }
        button[type="submit"]:hover {
            background-color: #218838;
        }
        button[type="reset"] {
            background-color: #dc3545;
            color: white;
        }
        .required-mark {
            color: red;
            margin-left: 5px;
        }
        .hint {
            font-size: 0.8em;
            color: gray;
            margin-left: 155px; /* จัดให้ตรงกับ input */
            display: block;
            margin-top: 5px;
        }
    </style>
</head>
<body>

    <h1 style="text-align: center;">การทดลองที่ 6: การสร้างฟอร์ม</h1>
    <p style="text-align: center;"><strong>ผู้จัดทำ:</strong> นายวีระภัทร อ่วมเกษม (68030271)</p>

    <h2>1. ตัวอย่าง: ฟอร์มลงทะเบียนนักศึกษา</h2>
    
    <form action="#" method="post">
        <fieldset>
            <legend>ข้อมูลส่วนตัว</legend>
            
            <div class="form-group">
                <label for="studentId">รหัสนักศึกษา:</label>
                <input type="text" id="studentId" name="studentId" 
                       pattern="[0-9]{8}" placeholder="เช่น 68030271" required>
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
                <label for="male" style="width: auto;">ชาย</label>
                <input type="radio" id="female" name="gender" value="female">
                <label for="female" style="width: auto;">หญิง</label>
            </div>
        </fieldset>
    
        <fieldset>
            <legend>ข้อมูลการติดต่อ</legend>
    
            <div class="form-group">
                <label for="email">อีเมล:</label>
                <input type="email" id="email" name="email" placeholder="example@kmitl.ac.th" required>
            </div>
    
            <div class="form-group">
                <label for="phone">เบอร์โทรศัพท์:</label>
                <input type="tel" id="phone" name="phone" 
                       pattern="[0-9]{10}" placeholder="08xxxxxxxx" required>
            </div>
    
            <div class="form-group">
                <label for="address">ที่อยู่:</label>
                <textarea id="address" name="address" rows="3" required></textarea> 
                <span class="required-mark">*</span>
            </div>
        </fieldset>
    
        <fieldset>
            <legend>ข้อมูลการศึกษา</legend>
    
            <div class="form-group">
                <label for="faculty">คณะ:</label>
                <select id="faculty" name="faculty" required>
                    <option value="">เลือกคณะ</option>
                    <option value="siet">ครุศาสตร์อุตสาหกรรมฯ</option>
                    <option value="engineering">วิศวกรรมศาสตร์</option>
                    <option value="science">วิทยาศาสตร์</option>
                </select> <span class="required-mark">*</span>
            </div>
    
            <div class="form-group">
                <label for="major">สาขาวิชา:</label>
                <select id="major" name="major" required>
                    <option value="">เลือกสาขาวิชา</option>
                    <option value="ce">วิศวกรรมคอมพิวเตอร์</option>
                    <option value="it">เทคโนโลยีสารสนเทศ</option>
                    <option value="cs">วิทยาการคอมพิวเตอร์</option>
                </select> <span class="required-mark">*</span>
            </div>
    
            <div class="form-group">
                <label for="gpa">เกรดเฉลี่ยสะสม:</label>
                <input type="number" id="gpa" name="gpa" 
                       min="0" max="4" step="0.01" placeholder="0.00-4.00" required> <span class="required-mark">*</span>
            </div>
        </fieldset>
    
        <div class="form-group" style="text-align: center;">
            <button type="submit">ลงทะเบียน</button>
            <button type="reset">ล้างข้อมูล</button>
        </div>
    </form>

    <br><hr><br>

    <h2>2. แบบฝึกหัด: สมัครสมาชิกร้านค้าออนไลน์</h2>

    <form action="#" method="post" enctype="multipart/form-data">
        <fieldset>
            <legend>ข้อมูลบัญชีผู้ใช้ (Account)</legend>
            <div class="form-group">
                <label for="shop_email">อีเมล (Login ID):</label>
                <input type="email" id="shop_email" name="shop_email" required placeholder="name@example.com">
                <span class="required-mark">*</span>
            </div>
            <div class="form-group">
                <label for="shop_pwd">รหัสผ่าน:</label>
                <input type="password" id="shop_pwd" name="shop_pwd" minlength="8" required>
                <span class="required-mark">*</span>
                <span class="hint">ต้องมีความยาวอย่างน้อย 8 ตัวอักษร</span>
            </div>
            <div class="form-group">
                <label for="shop_pwd_confirm">ยืนยันรหัสผ่าน:</label>
                <input type="password" id="shop_pwd_confirm" name="shop_pwd_confirm" minlength="8" required>
                <span class="required-mark">*</span>
            </div>
        </fieldset>

        <fieldset>
            <legend>ข้อมูลส่วนตัว (Personal Info)</legend>
            <div class="form-group">
                <label for="shop_name">ชื่อ-นามสกุล:</label>
                <input type="text" id="shop_name" name="shop_name" required>
            </div>
            <div class="form-group">
                <label for="shop_dob">วันเกิด:</label>
                <input type="date" id="shop_dob" name="shop_dob">
            </div>
            <div class="form-group">
                <label>เพศ:</label>
                <input type="radio" id="shop_male" name="shop_gender" value="male"> <label for="shop_male" style="width:auto;">ชาย</label>
                <input type="radio" id="shop_female" name="shop_gender" value="female"> <label for="shop_female" style="width:auto;">หญิง</label>
                <input type="radio" id="shop_na" name="shop_gender" value="na" checked> <label for="shop_na" style="width:auto;">ไม่ระบุ</label>
            </div>
            <div class="form-group">
                <label for="shop_profile">รูปโปรไฟล์:</label>
                <input type="file" id="shop_profile" name="shop_profile" accept="image/png, image/jpeg, image/gif">
            </div>
        </fieldset>

        <fieldset>
            <legend>ที่อยู่จัดส่งสินค้า</legend>
            <div class="form-group">
                <label for="shop_phone">เบอร์โทรศัพท์:</label>
                <input type="tel" id="shop_phone" name="shop_phone" pattern="[0-9]{10}" placeholder="08XXXXXXXX" required>
                <span class="required-mark">*</span>
            </div>
            <div class="form-group">
                <label for="shop_address">ที่อยู่:</label>
                <textarea id="shop_address" name="shop_address" rows="3" required></textarea>
            </div>
        </fieldset>

        <fieldset>
            <legend>ความสนใจสินค้า</legend>
            <div class="form-group">
                <label style="width: 100%;">เลือกหมวดหมู่ที่สนใจ:</label><br>
                <div style="margin-left: 20px; margin-top: 10px;">
                    <input type="checkbox" id="cat_it" name="category" value="it"> <label for="cat_it" style="width:auto; margin-right:15px;">อุปกรณ์ไอที</label>
                    <input type="checkbox" id="cat_fashion" name="category" value="fashion"> <label for="cat_fashion" style="width:auto; margin-right:15px;">แฟชั่น</label>
                    <input type="checkbox" id="cat_home" name="category" value="home"> <label for="cat_home" style="width:auto; margin-right:15px;">ของใช้ในบ้าน</label>
                    <input type="checkbox" id="cat_gadget" name="category" value="gadget"> <label for="cat_gadget" style="width:auto; margin-right:15px;">Gadget</label>
                </div>
            </div>
        </fieldset>

        <div class="form-group">
            <input type="checkbox" id="shop_terms" name="shop_terms" required>
            <label for="shop_terms" style="width: auto; color: red;">
                ฉันยอมรับเงื่อนไขการใช้งานและนโยบายความเป็นส่วนตัว *
            </label>
        </div>

        <div class="form-group" style="text-align: center;">
            <button type="submit">สมัครสมาชิก</button>
        </div>
    </form>

</body>
</html>

```
- ภาพผลลัพธ์:
[วางภาพ screenshot ที่นี่]
![alt text](image.png)


