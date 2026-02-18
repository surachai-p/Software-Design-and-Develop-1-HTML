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
[<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lab 6: Advanced Form & Validation</title>
    <style>
        :root { --primary: #4a90e2; --error: #e74c3c; }
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background: #f0f2f5; padding: 20px; }
        .container { max-width: 700px; margin: auto; background: white; padding: 30px; border-radius: 12px; box-shadow: 0 4px 15px rgba(0,0,0,0.1); }
        h2 { color: var(--primary); border-bottom: 2px solid var(--primary); padding-bottom: 10px; }
        fieldset { border: 1px solid #ddd; border-radius: 8px; padding: 20px; margin-bottom: 25px; }
        legend { font-weight: bold; padding: 0 10px; color: #555; }
        .form-group { margin-bottom: 15px; }
        label { display: block; margin-bottom: 5px; font-weight: 600; }
        
        /* Input Styles */
        input[type="text"], input[type="email"], input[type="password"], 
        input[type="tel"], input[type="number"], input[type="date"], 
        select, textarea {
            width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 5px; box-sizing: border-box;
        }
        input:focus { border-color: var(--primary); outline: none; box-shadow: 0 0 5px rgba(74,144,226,0.3); }
        
        /* Validation Colors */
        input:invalid:not(:placeholder-shown) { border-color: var(--error); }
        .required { color: var(--error); }
        
        .btn-row { display: flex; gap: 10px; margin-top: 20px; }
        button { flex: 1; padding: 12px; border: none; border-radius: 5px; cursor: pointer; font-size: 16px; font-weight: bold; }
        button[type="submit"] { background: var(--primary); color: white; }
        button[type="reset"] { background: #95a5a6; color: white; }
    </style>
</head>
<body>

<div class="container">
    <h2>สมัครสมาชิกและลงทะเบียนระบบ (Lab 6)</h2>
    <form action="#" method="post" enctype="multipart/form-data">
        
        <fieldset>
            <legend>🔒 ข้อมูลความปลอดภัย</legend>
            <div class="form-group">
                <label for="email">อีเมลสมัครใช้งาน <span class="required">*</span></label>
                <input type="email" id="email" name="email" placeholder="example@kmitl.ac.th" required>
            </div>
            <div class="form-group">
                <label for="pwd">รหัสผ่าน (อย่างน้อย 8 ตัวอักษร) <span class="required">*</span></label>
                <input type="password" id="pwd" name="pwd" minlength="8" required>
            </div>
            <div class="form-group">
                <label for="confirm_pwd">ยืนยันรหัสผ่าน <span class="required">*</span></label>
                <input type="password" id="confirm_pwd" name="confirm_pwd" required>
            </div>
        </fieldset>

        <fieldset>
            <legend>👤 ข้อมูลส่วนตัว</legend>
            <div class="form-group">
                <label for="fullname">ชื่อ-นามสกุล <span class="required">*</span></label>
                <input type="text" id="fullname" name="fullname" placeholder="นางสาวณัฏฐวรรณ ช่างเก็บ" required>
            </div>
            <div style="display: flex; gap: 15px;">
                <div class="form-group" style="flex: 1;">
                    <label for="birthdate">วันเกิด</label>
                    <input type="date" id="birthdate" name="birthdate" required>
                </div>
                <div class="form-group" style="flex: 1;">
                    <label>เพศ</label>
                    <div style="padding-top: 10px;">
                        <input type="radio" name="gender" value="male" id="m"> <label for="m" style="display:inline;">ชาย</label>
                        <input type="radio" name="gender" value="female" id="f"> <label for="f" style="display:inline;">หญิง</label>
                    </div>
                </div>
            </div>
            <div class="form-group">
                <label for="phone">เบอร์โทรศัพท์ (10 หลัก)</label>
                <input type="tel" id="phone" name="phone" pattern="[0-9]{10}" placeholder="08XXXXXXXX" required>
            </div>
        </fieldset>

        <fieldset>
            <legend>🏷️ ความสนใจและเอกสาร</legend>
            <div class="form-group">
                <label>หมวดหมู่ที่สนใจ:</label>
                <input type="checkbox" name="fav" value="iot"> ผัดไทยกุ้งสด / IoT 
                <input type="checkbox" name="fav" value="photo"> ก๋วยเตี๋ยวเส้นเล็กต้มยำ 
                <input type="checkbox" name="fav" value="web"> ส้มตำไทยข้าวโพด
            </div>
            <div class="form-group">
                <label for="photo">อัปโหลดรูปโปรไฟล์ (จำกัดไฟล์รูปภาพ) <span class="required">*</span></label>
                <input type="file" id="photo" name="photo" accept="image/*" required>
            </div>
            <div class="form-group">
                <label for="address">ที่อยู่จัดส่งสินค้า / ที่อยู่ติดต่อ</label>
                <textarea id="address" name="address" rows="3" placeholder="ระบุบ้านเลขที่ ซอย ถนน แขวง..."></textarea>
            </div>
        </fieldset>

        <div class="form-group">
            <input type="checkbox" id="terms" name="terms" required>
            <label for="terms" style="display:inline;">ฉันยอมรับ <a href="#">เงื่อนไขการใช้งาน</a> และนโยบายความเป็นส่วนตัว</label>
        </div>

        <div class="btn-row">
            <button type="submit">ยืนยันการสมัคร</button>
            <button type="reset">ล้างข้อมูล</button>
        </div>
    </form>
</div>

</body>
</html>]
```html

```
- ภาพผลลัพธ์:
[Lab06\06.png]



