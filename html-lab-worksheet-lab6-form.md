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
</body>
</html>
<style>
    body {
        font-family: Arial, sans-serif;
        background-color: #f4f4f9;
        padding: 20px;
    }
    .form-container {
        max-width: 700px;
        margin: 0 auto;
        padding: 20px;
        background-color: white;
        border-radius: 8px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }
    .form-container h2 {
        text-align: center;
        margin-bottom: 20px;
    }
    .form-group {
        margin-bottom: 15px;
    }
    label {
        display: block;
        font-weight: bold;
        margin-bottom: 5px;
    }
    input, textarea, select, button {
        width: 100%;
        padding: 10px;
        border: 1px solid #ccc;
        border-radius: 4px;
        font-size: 16px;
    }
    button {
        background-color: #007BFF;
        color: white;
        cursor: pointer;
        font-weight: bold;
        border: none;
    }
    button:hover {
        background-color: #0056b3;
    }
    .error {
        color: red;
        font-size: 14px;
    }
</style>
    <title>สมัครสมาชิกร้านค้าออนไลน์</title>
    <style></style>
    <div class="form-container">
        <h2>สมัครสมาชิกร้านค้าออนไลน์</h2>
        <form id="signupForm" enctype="multipart/form-data" action="/submit-form" method="POST">
            <!-- ข้อมูลส่วนตัว -->
            <div class="form-group">
                <label for="fullName">ชื่อ-นามสกุล:</label>
                <input type="text" id="fullName" name="fullName" required>
            </div>

<!--วันเกิด-->
        <div class="form-group">
            <label for="dob">วันเกิด:</label>
            <input type="date" id="dob" name="dob" required>
        </div>
<!--เพศ-->
<div class="form-group">
    <label>เพศ:</label>
    <label for="male">ชาย</label>
    <input type="radio" id="male" name="gender" value="ชาย" required>
    <label for="female">หญิง</label>
    <input type="radio" id="female" name="gender" value="หญิง" required>
        </div>
    <!--email-->
        <div class="form-group">
            <label for="email">อีเมล์:</label>
            <input type="email" id="email" name="email" required>
            <div id="emailError" class="error"></div>
        </div>
        <div class="form-group">
            <label for="password">รหัสผ่าน:</label>
            <input type="password" id="password" name="password" required>
            <div id="passwordError" class="error"></div>
        </div>
        <div class="form-group">
            <label for="confirmPassword">ยืนยันรหัสผ่าน:</label>
            <input type="password" id="confirmPassword" name="confirmPassword" required>
            <div id="confirmPasswordError" class="error"></div>
        </div>
        

<!--เบอร์-->
        <div class="form-group">
            <label for="phone">เบอร์โทร:</label>
            <input type="tel" id="phone" name="phone" pattern="[0-9]{10}" required>
            <div id="phoneError" class="error"></div>
        </div>
<!--ที่อยู่-->
        <div class="form-group">
            <label for="address">ที่อยู่จัดส่ง:</label>
            <textarea id="address" name="address" rows="4" required></textarea>
        </div>

        <!-- รูปโปรไฟล์ -->
        <div class="form-group">
            <label for="profileImage">รูปโปรไฟล์:</label>
            <input type="file" id="profileImage" name="profileImage" accept="image/*" required>
            <div id="imageError" class="error"></div>
        </div>
        <!-- ความสนใจในหมวดหมู่สินค้า -->
        <div class="form-group">
            <label for="category">ความสนใจในหมวดหมู่สินค้า:</label>
            <select id="category" name="category" required>
                <option value="electronics">อิเล็กทรอนิกส์</option>
                <option value="fashion">แฟชั่น</option>
                <option value="homeGoods">ของใช้ในบ้าน</option>
                <option value="books">หนังสือ</option>
                <option value="other">อื่นๆ</option>
            </select>
        </div>

        <!-- การยอมรับเงื่อนไขการใช้งาน -->
        <div class="form-group">
            <label for="terms">
                <input type="checkbox" id="terms" name="terms" required>
                ยอมรับข้อตกลงและเงื่อนไขการใช้งาน
            </label>
        </div>

        <button type="submit">สมัครสมาชิก</button>
    </form>
</div>

<script>
    // ฟังก์ชันตรวจสอบอีเมล
    function validateEmail() {
        const email = document.getElementById("email").value;
        const emailError = document.getElementById("emailError");
        const emailRegex = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;
        if (!emailRegex.test(email)) {
            emailError.textContent = "กรุณากรอกอีเมลที่ถูกต้อง";
            return false;
        } else {
            emailError.textContent = "";
            return true;
        }
    }

    // ฟังก์ชันตรวจสอบเบอร์โทร
    function validatePhone() {
        const phone = document.getElementById("phone").value;
        const phoneError = document.getElementById("phoneError");
        const phoneRegex = /^[0-9]{10}$/;
        if (!phoneRegex.test(phone)) {
            phoneError.textContent = "กรุณากรอกเบอร์โทรที่ถูกต้อง";
            return false;
        } else {
            phoneError.textContent = "";
            return true;
        }
    }

    // ฟังก์ชันตรวจสอบขนาดไฟล์รูปภาพ
    function validateImage() {
        const fileInput = document.getElementById("profileImage");
        const imageError = document.getElementById("imageError");
        const file = fileInput.files[0];
        if (file && file.size > 2 * 1024 * 1024) { // 2MB
            imageError.textContent = "ขนาดไฟล์รูปภาพต้องไม่เกิน 2MB";
            return false;
        } else {
            imageError.textContent = "";
            return true;
        }
    }

    // ฟังก์ชันตรวจสอบรหัสผ่าน
    function validatePassword() {
        const password = document.getElementById("password").value;
        const confirmPassword = document.getElementById("confirmPassword").value;
        const passwordError = document.getElementById("passwordError");
        const confirmPasswordError = document.getElementById("confirmPasswordError");

        if (password.length < 6) {
            passwordError.textContent = "รหัสผ่านต้องมีอย่างน้อย 6 ตัวอักษร";
            return false;
        } else {
            passwordError.textContent = "";
        }

        if (password !== confirmPassword) {
            confirmPasswordError.textContent = "รหัสผ่านไม่ตรงกัน";
            return false;
        } else {
            confirmPasswordError.textContent = "";
            return true;
        }
    }

    // ฟังก์ชันสำหรับการส่งฟอร์ม
    document.getElementById("signupForm").onsubmit = function(event) {
        event.preventDefault();
        if (validateEmail() && validatePhone() && validateImage() && validatePassword()) {
            this.submit(); // ส่งฟอร์มเมื่อข้อมูลถูกต้อง
        }
    };
</script>



```
- ภาพผลลัพธ์:
[วางภาพ screenshot ที่นี่]

![lab6 2](https://github.com/user-attachments/assets/9a1edcb0-5ba5-4c74-8d62-281ab921bafe)
![lab6 1](https://github.com/user-attachments/assets/ebb3db50-02b4-4a67-a245-025944dac5e2)


