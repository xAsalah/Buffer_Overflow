<div dir="rtl">
	<h1>Buffer Overflow الـ</h1>

بالبدية لازم نفهم ماهو الـBuffer وكيف يصير له الـBuffer Overflow :
الـBuffer هو عبارة عن مساحة تخزينية محددة داخل الـMemory
في حال كانت مدخلات المستخدم أكبر من حجم السعة المحدده هنا بصير مفهوم الـBuffer Overflow

* * *

ملاحظة :
اذا كان البرنامج يستخدم أحد هذه االدوال قد يسبب حدوث الثغرة strcpy - strcat بسبب أنها
<br>
لا تعمل validate input قبل التشغيل
<br>
أيضا لا تعمل check input boundaries

* * *
من أهم الـregister  اللي نركز عليها في الـBuffer Overflow 
<ul>
<li>ESP : points to the top of the stack</li>
<li>EIP :points to the next instruction</li>
<li>EBP : points to the end of the stack </li>

قبل ما نحاول نستغل ثغرة الـ Buffer Overflow لازم نعرف كيف نوصلها ؟
<br>
اذا كان لدينا الـ source code نستخدم splint or cppcheek
<br>
اذا كان لدينا الـ exe نستخدم Fuzzer وهي عبارة عن ادخال مدخلات عشوائيه بهدف معرفة سلوك البرنامج.


