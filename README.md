# Physical-Computing-Project-2024---IT-KMITL 💻
☀️ArduinoChi🐡
# บทคัดย่อ (Abstact) 📁
โปรเจคนี้ได้จัดทำขึ้นมาเพื่อต้องการแสดงให้เห็นว่าทางเราสามารถสร้างเกมขึ้นได้ด้วยทรัพยากรที่จำกัด เน้นใช้ความคิดสร้างสรรค์เพื่อให้จำลองออกมาในรูปแบบของการเลี้ยงมอนสเตอร์ตัวน้อยในนามของ "ArduinoChi" ผ่านการใช้เซนเซอร์วัดอุณหภูมิเป็น Input และให้แสดงผลโดยใช้ LCD เป็น Output ออกมา

# ฟังก์ชัน Gameplay 📟
ArduinoChi จะมีชีวิตอยู่ได้ท่ามกลางสภาพแวดล้อมที่เหมาะสม กระตุ้นให้คนที่อยู่แต่ในบ้านรู้สึกอยากถ่ายเท หรือปรับอากาศเพื่อให้ร่างกายและ ArduinoChi ของตัวเองปรับตัวพร้อมรู้สึกได้รับการฟื้นฟูหลังจากทำงานหนักตลอดทั้งวัน โดยใช้ประโยชน์จากอุณหภูมิเป็นหลัก สำหรับรูปแบบการเล่นก็จะมีระบบคร่าวๆ ดังต่อไปนี้

<br>![Desc_1.png](/Picture/Desc_1.png)

<br>1) จากรูปข้างต้นบนจอ LCD ก็จะประกอบไปด้วย<br>
- Timer มีหน้าที่ใช้ในการจับเวลานับตั้งแต่ที่เริ่มเลี้ยงตัวของ ArduinoChi จนกระทั่งจบเกม<br>
- Stage ใช้ในการเพิ่มระดับความยากของเกม โดยในทุกๆ 30 วินาที จะเปลี่ยนระดับให้ยากขึ้นซึ่งจะส่งผลต่ออัตราการลดเลือดของ ArduinoChi ที่จะเยอะขึ้นตามจำนวนด่านละ 1 หน่วย<br>
- Temperature มีหน้าที่แสดงผลอุณหภูมิห้องในปัจจุบัน โดยรับค่ามาจากเซ็นเซอร์<br>
- Health ใช้บ่งบอกสถานะเลือดของ ArduinoChi ในปัจจุบัน<br>
- Food ใช้บอกจำนวนอาหารที่มีอยู่ โดยจะได้รับเสบียงเพิ่มขึ้น 2 หน่วย หากผู้เล่นสามารถผ่านเข้าสู่ด่านถัดไปได้<br>
- ArduinoChi แสดงตัวของมอนสเตอร์ที่เราเลี้ยง โดยที่มันจะขยับไปเรื่อยๆ และจะแสดงสีหน้าตามอารมณ์ของมัน<br>
2) โดยหลังจากที่เริ่มเกม ทางผู้เล่นจะต้องหาพื้นที่อุณหภูมิให้เหมาะสมกับที่ตัว ArduinoChi จะต้องการ ซึ่งจะอยู่ที่ 24-26 องศาเซลเซียส และจะมีกฏเพิ่มเติมคือ<br>
- ในอุณหภูมิ 24.5-25.5 องศาเซลเซียส Arduinochi จะได้รับการเพิ่มเลือด 5 หน่วยในทุกๆ 5 วินาที<br>
- หากอุณหภูมิปัจจุบันมีค่าต่ำกว่า 24 องศา หรือมากกว่า 26 องศาเซลเซียส Arduinochi จะถูกหักเลือดตามระดับความยากในทุกๆ 2 วินาที<br>
- นอกเหนือจากที่ได้กล่าวมาข้างต้น Arduinochi จะไม่ได้รับการเพิ่มเลือด หรือหักเลือดแต่อย่างใดจากสถานะอุณหภูมิ<br>
3) ในการผ่านด่านแต่ละครั้งเมื่อ ArduinoChi อายุมากขึ้น น้องก็มีความเสี่ยงที่จะเสียเลือดมากขึ้นเช่นกัน โดยจะเริ่มถูกหักเลือดเพิ่มขึ้น 1 หน่วย นับตั้งแต่เข้าสู๋ ST2 เป็นต้นไป

4) ผู้เลี้ยงน้องสามารถแก้ปัญหาสามารถให้อาหารได้โดยกดปุ่มที่ตัวบอร์ด จะดำเนินการให้อาหาร Arduinochi ซึ่งจะสามารถเพิ่มเลือดได้ 10 หน่วย และในช่วงรีฟิลอาหารแต่ละครั้งผู้เล่นสามารถสะสมเสบียงได้เรื่อยๆ

5) การสังเกตอาการของน้อง นอกจากการดูผ่าน Output แล้ว ในตัวบอร์ดจะมีไฟ LED ทั้งหมด 3 หลอด ซึ่งจะแบ่งเกณฑ์ได้ตามนี้
- หากไฟสีแดงสว่าง นั่นหมายความว่า มอนสเตอร์จะเหลือเลือดอยู่ราวๆ 1-10 หน่วย<br>
- หากไฟสีเหลืองสว่าง นั่นหมายความว่า มอนสเตอร์จะเหลือเลือดอยู่ราวๆ 11-20 หน่วย<br>
- และหากไฟสีเขียวสว่าง นั่นหมายความว่า มอนสเตอร์จะมีเลือดอยู่ประมาณ 21-30 หน่วย<br>
6) หากผู้เล่นไม่สามารถรักษาระดับชีพจรของ ArduinoChi เอาไว้ได้ เมื่อเลือดเหลือ 0 เท่าไหร่ เกมก็จะจบรอบทันทีโดยจะมีสถิติเวลาบอกไว้ในหน้า Game Over และหากผู้เล่นต้องการที่จะเล่นเกมต่อไปก็ให้กดที่ปุ่มซ้ำอีกรอบ

# สมาชิกกลุ่ม (Group Members) 👦👦👦👧
66070019 นายกุลกิติกรณ์ วรรณะ
<br>66070022 นายคณาธิป เข็มทอง
<br>66070054 นายฐีตพรรธ สังหิตกุล

โปรเจคนี้เป็นส่วนหนึ่งในรายวิชา PHYSICAL COMPUTING 06016409 ภาคเรียนที่ 1 ปีการศึกษา 2567 ของคณะเทคโนโลยีสารสนเทศ สาขาเทคโนโลยีสารสนเทศ สถาบันเทคโนโลยีพระจอมเกล้าเจ้าคุณทหารลาดกระบัง
