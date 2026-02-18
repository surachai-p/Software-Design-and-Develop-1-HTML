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

<img width="698" height="905" alt="Screenshot 2026-02-18 144018" src="https://github.com/user-attachments/assets/67e7e8d3-939a-4307-b7b6-7905ebadf82c" />




<img width="694" height="818" alt="Screenshot 2026-02-18 144039" src="https://github.com/user-attachments/assets/60deb836-0c5f-49b1-8a2b-fc1a2cdfebf5" />


