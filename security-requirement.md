# 📣 [OWASP ASVS](https://owasp.org/www-project-application-security-verification-standard/)
## 13.2.1 RESTful Web Service 🕸️
> Verify that enabled RESTful HTTP methods are a valid choice for the user or action, such as preventing normal users using DELETE or PUT on protected API or resources.

### 1. ChatGPT:

  - เน้นเรื่อง **การควบคุมการใช้ HTTP Methods ใน RESTful API** เพื่อป้องกัน **การใช้งานที่ไม่เหมาะสมและอาจก่อให้เกิดความเสียหายต่อระบบ** โดยควรทำสิ่งต่อไปนี้:

    🔏 จำกัดการใช้ HTTP Methods ตามสิทธิ์ของผู้ใช้
  
    ✅ ใช้ Role-Based Access Control (RBAC) หรือ ACLs เพื่อตรวจสอบสิทธิ์
  
    📲 กำหนดให้ต้องมีการยืนยันตัวตน (Authentication) และการอนุญาต (Authorization) ก่อนเข้าถึง API
  
    🛡️ ป้องกัน Cross-Site Request Forgery (CSRF) สำหรับคำสั่งที่เปลี่ยนแปลงข้อมูล

### 2. Gemini:
  
  - เน้นเรื่อง **การยืนยันว่า HTTP method ที่เปิดใช้งานสำหรับ RESTful API นั้นเหมาะสมกับผู้ใช้หรือการกระทำนั้นๆ** โดยมีจุดประสงค์หลักคือ **ป้องกันไม่ให้ผู้ใช้ทั่วไปใช้ HTTP method ที่มีความเสี่ยง เช่น DELETE หรือ PUT บน API หรือ resources ที่ได้รับการป้องกัน**

    **ความหมายและหลักการทำงาน**

      🫱🏻‍🫲🏻 HTTP Methods: RESTful API ใช้ HTTP methods (เช่น GET, POST, PUT, DELETE) เพื่อกำหนดการกระทำที่ต้องการทำกับ resource บน server

      🔑 การตรวจสอบสิทธิ์: API ควรมีการตรวจสอบสิทธิ์ เพื่อให้แน่ใจว่าผู้ใช้ที่ส่งคำขอมานั้นมีสิทธิ์ในการเข้าถึงและใช้งาน resource นั้นๆ

      🔐 การป้องกันการเข้าถึงโดยไม่ได้รับอนุญาต: ผู้ใช้ทั่วไปไม่ควรมีสิทธิ์ในการแก้ไขหรือลบข้อมูลสำคัญ ดังนั้น API จึงต้องป้องกันไม่ให้ผู้ใช้เหล่านี้ใช้ HTTP methods ที่มีความเสี่ยง เช่น DELETE (ลบข้อมูล) หรือ PUT (แก้ไขข้อมูล) บน resources ที่สำคัญ

### 3. Myself:

  - V13.2.1 จะ **จำกัดสิทธิ์การใช้ HTTP Methods ใน RESTful API** เพื่อป้องกันไม่ให้ผู้ใช้ที่ไม่มีสิทธิ์สามารถทำสิ่งที่เป็นอันตราย

    > เช่น **ห้ามให้ผู้ใช้ทั่วไปใช้ PUT หรือ DELETE** ในข้อมูลที่สำคัญ ⚙️

## 👥 Member
  - [Chonnikarn Sangwang](security-requirement.md)
  - [Natnicha Nontraudon]
