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
```html
<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <title>สมัครสมาชิก - Praphaphorn Online Shop</title>
    <style>
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; line-height: 1.6; padding: 20px; background-color: #f4f4f4; }
        form { max-width: 600px; margin: auto; background: white; padding: 20px; border-radius: 8px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
        h1 { text-align: center; color: #333; }
        fieldset { border: 1px solid #ddd; padding: 15px; margin-bottom: 20px; border-radius: 5px; }
        legend { font-weight: bold; color: #0056b3; padding: 0 10px; }
        .form-group { margin-bottom: 15px; }
        label { display: block; margin-bottom: 5px; font-weight: bold; }
        input[type="text"], input[type="email"], input[type="tel"], input[type="password"], input[type="date"], select, textarea {
            width: 100%; padding: 8px; border: 1px solid #ccc; border-radius: 4px; box-sizing: border-box;
        }
        .required { color: red; }
        .btn-submit { background-color: #28a745; color: white; border: none; padding: 10px 20px; border-radius: 4px; cursor: pointer; font-size: 16px; }
        .btn-reset { background-color: #6c757d; color: white; border: none; padding: 10px 20px; border-radius: 4px; cursor: pointer; font-size: 16px; }
    </style>
</head>
<body>

    <h1>สมัครสมาชิกใหม่</h1>
    <p style="text-align:center">รหัสนักศึกษา: 68030085 | ประภาภรณ์ ภูผาลี</p>

    <form action="/submit-registration" method="post" enctype="multipart/form-data">
        
        <fieldset>
            <legend>ข้อมูลส่วนตัว</legend>
            <div class="form-group">
                <label for="fullname">ชื่อ-นามสกุล <span class="required">*</span></label>
                <input type="text" id="fullname" name="fullname" placeholder="กรุณากรอกชื่อจริง-นามสกุล" required>
            </div>
            <div class="form-group">
                <label for="birthdate">วันเกิด <span class="required">*</span></label>
                <input type="date" id="birthdate" name="birthdate" required>
            </div>
            <div class="form-group">
                <label>เพศ</label>
                <input type="radio" id="m" name="gender" value="male"> <label for="m" style="display:inline">ชาย</label>
                <input type="radio" id="f" name="gender" value="female"> <label for="f" style="display:inline">หญิง</label>
                <input type="radio" id="o" name="gender" value="other"> <label for="o" style="display:inline">อื่นๆ</label>
            </div>
        </fieldset>

        <fieldset>
            <legend>ข้อมูลการติดต่อ</legend>
            <div class="form-group">
                <label for="email">อีเมล <span class="required">*</span></label>
                <input type="email" id="email" name="email" placeholder="example@email.com" required>
            </div>
            <div class="form-group">
                <label for="phone">เบอร์โทรศัพท์ <span class="required">*</span></label>
                <input type="tel" id="phone" name="phone" pattern="[0-9]{10}" title="กรุณากรอกเบอร์โทรศัพท์เป็นตัวเลข 10 หลัก" placeholder="08XXXXXXXX" required>
            </div>
            <div class="form-group">
                <label for="address">ที่อยู่จัดส่ง <span class="required">*</span></label>
                <textarea id="address" name="address" rows="3" required></textarea>
            </div>
        </fieldset>

        <fieldset>
            <legend>การตั้งค่ารหัสผ่าน</legend>
            <div class="form-group">
                <label for="pwd">รหัสผ่าน <span class="required">*</span></label>
                <input type="password" id="pwd" name="password" minlength="8" placeholder="อย่างน้อย 8 ตัวอักษร" required>
            </div>
            <div class="form-group">
                <label for="confirm_pwd">ยืนยันรหัสผ่าน <span class="required">*</span></label>
                <input type="password" id="confirm_pwd" name="confirm_password" minlength="8" required>
            </div>
        </fieldset>

        <fieldset>
            <legend>ข้อมูลเพิ่มเติม</legend>
            <div class="form-group">
                <label for="profile_img">รูปโปรไฟล์ (เฉพาะไฟล์ภาพ)</label>
                <input type="file" id="profile_img" name="profile_img" accept="image/*">
            </div>
            <div class="form-group">
                <label>หมวดหมู่สินค้าที่สนใจ</label>
                <input type="checkbox" name="interest" value="fashion"> แฟชั่น
                <input type="checkbox" name="interest" value="electronics"> อิเล็กทรอนิกส์
                <input type="checkbox" name="interest" value="home"> บ้านและสวน
            </div>
        </fieldset>

        <div class="form-group">
            <input type="checkbox" id="terms" name="terms" required>
            <label for="terms" style="display:inline">ฉันยอมรับ <a href="#">เงื่อนไขการใช้งาน</a> และนโยบายความเป็นส่วนตัว</label>
        </div>

        <div style="text-align: center;">
            <button type="submit" class="btn-submit">ลงทะเบียนสมาชิก</button>
            <button type="reset" class="btn-reset">ล้างข้อมูล</button>
        </div>

    </form>
</body>
</html>
```
- ภาพผลลัพธ์:
<img width="875" height="904" alt="6" src="https://github.com/user-attachments/assets/57f01c22-b6ec-443f-810e-28eb157b6c78" />




