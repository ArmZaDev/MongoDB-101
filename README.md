<h1 align="center"><strong>MongoDB</strong></h1>

### NoSQL

*MongoDB* เป็นฐานข้อมูลแบบ ฐานข้อมูลไม่ใช่เชิงสัมพันธ์ หรือเรียกอีกชื่อ คือ NoSQL (Not-Only SQL) ถูกคิดค้นขึ้นเพื่อจัดการข้อจำกัดการใช้งาน *Relational Database* ในอดีต เพื่อปรับเปลี่ยนโครงสร้างการจัดเก็บข้อมูลให้มีความยือหยุ่นมากขึ้นด้วย
	
NoSQL ถูกนำมาใช้งานสำหรับประมวลผลข้อมูลจากการใช้งาน Internet อย่างเเพร่หลายในยุดปัจจุบัน						ไม่ว่าจะมาจาก Social Media ต่างๆ ที่มีข้อมูลขนาดใหญ่ (Big Data) เพื่อแปลข้อมูลที่มีความหลากหลายมากขึ้น เช่น ข้อมูลรูปภาพ วิดีโอ เสียง ตัวอักษร เป็นต้น ซึ่งจะตอบโจทย์ในเรื่องความเร็วและความยืดหยุ่นในการจัดเก็บข้อมูล
***
<h3 align="left"><strong>ฐานข้อมูลไม่ใช่เชิงสัมพันธ์ (Non-Relational Database)</strong></h3>

 - ไม่มีการจัดเก็บข้อมูลในแบบตารางที่มีความสัมพันธ์กัน
 - ไม่มีโครงสร้างการจัดเก็ฐข้อมูลที่แน่นอน (UnStructure Data)
 - ง่ายต่อการปรับขนาดและโครงสร้าง
<h3 align="left"><strong>รูปแบบการจัดเก็บข้อมูล (NoSQL Store)</strong></h3>
	
NoSQL ไม่มีโครงสร้างการจัดเก็บข้อมูลที่แน่นอน เพื่อที่จะสามารถปรับเปลี่ยนโครงสรา้งได้ในอนาคต โดยจะเก็บข้อมูลอยู่ 4 รูปแบบ (ตามลักษณะการใช้งาน)
 - Key - Value Store
 - Document Store
 - Graph Store
 - Wide Column Store
 1. Key - Value Store เป็นระบบจัดการเก็ยข้อมูลในรูปแบบ *Associative Arrays* หรืออาร์เรย์ของชุดข้อมูลที่มีความสัมพันธ์กันในรูปแบบ (key : value) หรือ Dictionary
	 โดยคีย์ (key) จะทำหน้าที่เป็นตัวเชื่อมโยงไปยังค่า (value) ในโครงสร้างของฐานข้อมูลซึ่งจะมีได้คีย์เดียว และการดึงข้อมูลต้องระบุคีย์ที่เก็บข้อมูลนั้นๆไว้
![keyvalue](https://user-images.githubusercontent.com/106058972/227906377-97af6dd7-430c-4e6d-9818-53adc790e33f.png)
https://www.mongodb.com/databases/key-value-database

2. Document Store เป็ฯฐานข้อมูลเชิงเอกสารที่ออกแบบมาเพื่อจัดเก็บข้อมูล ดึงข้อมูล และจัดการข้อมูล ที่เรียกว่า *Document-Oriented* คือ ใช้โครงสร้างภายในของเอกสารเพื่อระบุการจัดเก็บข้อมูล ซึ่งมีลักษณะแบบกึ่งโครงสร้าง (Semi Structure Data) โดยเอกสาร (Document) จะถูกเข้ารหัสข้อมูลและจัดให้อยู่ในรูปแบบของ XML, JSON
![document](https://user-images.githubusercontent.com/106058972/227827753-33a9e30c-f020-4f3a-b524-3e591641368a.png)
https://www.mongodb.com/document-databases

3. Graph Store เป็นการจัดเก็บข้อมูลและความสัมพันธ์ของข้อมูลในรูปแบบกราฟ ข้อมูลด้านในจะเรียกว่าโหนด (Node) ซึ่งจะเก็บ Entity ของข้อมูลและกำหนดความสัมพันธ์ที่เชื่อมโยงความสัมพันธ์ดังกล่าวผ่าน Edge การใช้งานกราฟจะถูกนำเสนอผ่านความสัมพันธ์ของข้อมูล เช่น Social Network, AI และ Machine Learning เป็นต้น
![graph](https://user-images.githubusercontent.com/106058972/227905395-5b37b9be-4aff-4af2-b831-77c2618f02fa.png)
https://www.nebula-graph.io/posts/review-on-graph-databases

4. Wide Column Storage เป็นการจัดเก็บข้อมูลเป็นเรคคอร์ดหรือในรูปแบบตาราง แถว และคอลัมน์ ซึ่งจะแตกต่างจาก Relational Database คือจะมีความยืดหยุ่นมากกว่า ชื่อและรูปแบบของคอลัมน์เปลี่ยนจากแถวหนึ่งไปยังอีกแถวภายในตารางเดียวกันได้และขยายคอลัมน์ได้จำนวนมาก *(Extensible Record Store: ขยายการจัดเก็บข้อมูลในแต่ละเรคคอร์ด)* อาจจะมองเป็นรูปแบบ key : value ในรูปแบบสองมิติก็ได้
![wide](https://user-images.githubusercontent.com/106058972/227910748-d144361e-800c-4149-8334-93005c008e45.png)
https://i.imgur.com/8laydo6.png
***
###  What is MongoDB?
เป็นฐานข้อมูลเชิงเอกสาร (Document Store) สำหรับเก็บข้อมูลขนาดใหญ่ที่มีความยืดหยุ่นสูง ง่ายต่อการปรับขนาดและทำงานข้าม Platform ได้การจัดเก็บข้อมูลไม่ได้อยู่ในรูปแบบตาราง แต่จะอยู่ในรูปแบบเอกสาร JSON แล้วเซฟไว้ในเอกสารรูปแบบไบนารี BSON

### โครงสร้างการจัดเก็บข้อมูลของ MongoDB

 - Database (ฐานข้อมูล) เป็นส่วนที่ใช้เก็บ Collection หรือชุดข้อมูล
 - Collection หรือชุดข้อมูลเทียบได้กับตารางในฐานข้อมูลเชิงสัมพันธ์
 - Documents เอกสารที่จัดเก็บข้อมูลของคู่คีย์ (Key) และค่า (Value)
![mongodb](https://user-images.githubusercontent.com/106058972/227915124-2ecb6a12-7fbc-45fb-a7ac-7afca6b5ddc8.jpg)
https://dzone.com/articles/a-primer-on-open-source-nosql-databases
***
