# bitkub-tsl
Cryptocurrency Trailing stop for BitKub exchange.
โปรแกรมช่วยขายเหรียญคริปโตอัตโนมัติบน BitKub Exchange โปรแกรมพัฒนาด้วย python และเรียกใช้งาน BitKub Official API (https://github.com/bitkub/bitkub-official-api-docs)

***Note BitKub API มีบัคกับจำนวนเหรียญที่จะสามารถส่งคำสั่งขายได้จำนวนต้องไม่น้อยกว่า 0.01 เหรียญ (ไม่ว่าจะเป็นเหรียญอะไรก็ตาม) โปรแกรมจะทำการตรวจสอบเหรียญในกระเป๋าให้ว่ามีเพียงพอหรือไม่

## How to use
โปรแกรมประกอบด้วย 3 ไฟล์
- cPandaBitKubTSL.exe  <-- Program TSL
- API.txt <-- ไฟล์สำหรับเก็บค่า KEY ส่วนตัวสำหรับการเข้าถึง Account ของเราใน BitKub
- THB_XXX.txt <-- ไฟล์สำหรับตั้งค่าเหรียญต่างๆ ที่เราต้องการใช้งาน

## สร้าง API & KEY บน BitKub

![image](https://user-images.githubusercontent.com/56244402/147461471-7f83da7a-84f6-42fb-bcb2-205f6e59edb2.png)

กดสร้าง API KEY & SECRET แล้วนำไปใส่ในไฟล์ API.txt

![image](https://user-images.githubusercontent.com/56244402/147462137-06d94cdb-046d-4312-bdbf-11fe4b3215e6.png)

![image](https://user-images.githubusercontent.com/56244402/147461646-150a486e-ad72-4a27-8945-9a5fb97bc2da.png)

** ห้ามส่ง API KEY & SECRET ให้ใครรู้เป็นอันขาด !!! 

## การตั้งค่าในไฟล์ THB_XXX.txt (แทนที่ XXX ด้วยชื่อเหรียญที่เราต้องการ)

![image](https://user-images.githubusercontent.com/56244402/147461883-e7a932f1-98c1-47a5-8a04-7a5e7ac75801.png)

`Symbol` - ชื่อคู่เหรียญกับเงินบาทกับชื่อเหรียญ ตัวอย่าง THB_KUB

`cost`   - ต้นทุนของเหรียญที่เราซื้อมา ถ้ารู้ก็ใส่คร่าวๆ ได้ โปรแกรมจะนำไปใช้คำนวนเป็นเปอร์เซ็นต์กำไรให้ ถ้านึกไม่ออกจริงๆ ก็ใส่ 0  

`gridsize` - ระยะห่างจากราคาปัจจุบันของเหรียญนั้นๆ เช่น ราคา KUB ปัจจุบันอยู่ที่ 450 บ. แล้วเราอยากจะวาง Stoploss เริ่มต้นที่ 400 บ. ก็ให้ใส่ค่า gridsize=50 

`sellsize` - ปริมาณที่ต้องการขายเมื่อราคาลงมาชนกับ TSL ที่ตั้งไว้  1 = 100% (ขายหมดพอร์ต) ,  0.2 = ขาย 20% ของเหรียญที่มีอยู่

## วิธีการใช้งาน

เข้า Command Prompt ไปที่ folder ที่เราเก็บโปรแกรมไว้ แล้วพิมพ์คำสั่ง

`cPandaBitKubTSL.exe -f THB_KUB.txt`

(สามารถสร้างไฟล์ config คู่เงินหลายๆ ไฟล์ แล้วสั่งทำงานหลายจอได้)

![image](https://user-images.githubusercontent.com/56244402/147463383-edf70ab1-23ac-4bb6-9f64-6f047b32e866.png)

## Support
หากพบปัญหาหรือต้องการฟีเจอร์เพิ่มเติม สามารถโพสไว้ในหัวข้อ issue ได้เลยครับ 

ถ้าเห็นว่าโปรแกรมมีประโยชน์ สามารถช่วยกดติดตามเป็นกำลังใจช่องเกมของผมได้ที่ 

[![Youtube_Badge](https://img.shields.io/badge/Youtube-CrazypandaGaming-red)](https://www.youtube.com/channel/UC9PgjH7Bc0_P4tbc8c6K25Q)
[![Facebook Badge](https://img.shields.io/badge/Facebook-CrazypandaGaming-blue)](https://fb.com/crazypandagaming)

หรือช่วยสนับสนุนค่ากาแฟก็ยินดีนะครับ 

BTC : bc1qtczemkkmqdle9n838la3sk407jgzqx2ap03dtg

ETH : 0x08cb7F954aAC9710cc5D5cCd3DBaE86ab972A391

BNB (Smart Chain) : 0x5a60f4f993837F637a868Fb0A4789d6F861E5eCA
