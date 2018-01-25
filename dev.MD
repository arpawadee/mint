# Command
► สร้าง local repo ในโฟลเดอร์
# git init
► แสดงข้อความ love ในไฟล์ jubjub.txt พร้อมสร้างไฟล์ jubjub.txt
# echo 'love' > jubjub.txt
► add ไฟล์ทัั้งหมด ทำให้ไฟล์นั้นถูก track
# git add .
► ตรวจสอบสถานะ repository  
# git status
► สร้าง snapshot ให้กับ repository ทำให้เราสามารถย้อนกลับมาดูว่าเราเปลี่ยนหรือแก้ไขโค๊ดอะไรไปบ้างได้
# commit -m "jubjub"
► เพิ่ม remote repository ในที่อยู่ github ของโฟลเตอร์นั้น
# git remote add origin https://github.com/arpawadee/mint.git
► เช็คว่า local repository นี้มี remote repository รึยัง
# git remote -v
► push ไฟล์ขึ้นไปใน github ที่ branch master
# git push -u origin master
► การ push และ fetch ที่ branch master
# git pull origin master
► ถ้าใน remote master กับ local master มีข้อมูลไม่ตรงกัน ให้ใช้คำสั่งนี้
# git merge origin/master --allow-unrelated-histories
► เช็คว่ามีอะไรเปลี่ยนแปลงบ้าง เช่น มีการแก้ไขไฟล์ อยากรู้ว่ามไฟล์มีอะไรเปลี่ยนแปลงไปจากเดิมบ้าง
# git diff HEAD
► การ undo ไฟล์ที่ยังไม่ได้ add
# git checkout -- test.txt 
► การ undo ไฟล์ที่ add ไปแล้ว
# git reset HEAD test.txt
► หากเรา commit ไปแล้ว คำสั่งนี้จะเป็นการย้อนกลับไปยัง commit ก่อนหน้านั้น
# git reset --soft HEAD~1
► เมื่อเอา commit ออกได้ เราก็ roll back กลับ โดยใช้คำสั่งนี้ได้
# git reset test.txt
► การลบไฟล์
# git rm test.txt
► สร้าง branch ใหม่ที่ชื่อว่า dev
# git branch dev
► ดู branch ทั้งหมดที่มีอยู่
# git branch -a
► ย้ายไป branch dev
# git checkout dev
► สร้าง branch ใหม่ที่ชื่อว่า dev พร้อมย้ายไป branch dev
# git checkout -b new
► เมื่อทดสอบ / แก้ไข เสร็จแล้ว ย้ายกลับมา branch master
# git checkout master
► สั่งดึงการเปลี่ยนแปลงใน branch dev เข้ามาใน branch master โดยการ merge ที่ branch master 
# git merge dev
► upload ไปยัง remote repository (github.com)
# git push
► upload ไฟล์ใน branch dev ไปยัง remote repository (github.com)
# git push -u origin dev
► update จาก master
# git pull --no-ff dev
► ซ่อนข้อความที่เพิ่งแก้ไขไป
# git stash
► เอาส่วนที่ซ่อนไว้คืนกลับมาแสดง
# git stash pop
► หากไปใช้เครื่องคอมคนละเครื่อง ต้องการดึงโฟลเดอร์ repository ใน github มาแสดงใช้คำสั่งนี้
# git clone https://github.com/arpawadee/mint.git