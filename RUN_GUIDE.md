# 1. اسم المشروع

لعبة تخمين الرقم (Number Guessing Game)

المجلد بعد فك الضغط: `Number-Guessing-Game---Python-main`

ملف البرنامج الرئيسي: `Number Guessing Game.py`

# 2. فكرة المشروع

اللعبة تختار رقمًا سريًا عشوائيًا بين 1 و 100. اللاعب يحاول تخمين هذا الرقم.

بعد كل تخمين تظهر إحدى الرسائل التالية:

- الرقم أكبر من المطلوب → Too high
- الرقم أصغر من المطلوب → Too low
- التخمين صحيح → Congratulations

بعد الفوز تعرض اللعبة عدد التخمينات العالية والمنخفضة والمجموع، ثم تسأل اللاعب إن كان يريد اللعب مرة أخرى.

# 3. متطلبات التشغيل

- نظام تشغيل Windows (تم التحقق على Windows 10)
- Python 3 مثبت على الجهاز
- لا توجد مكتبات خارجية مطلوبة

# 4. إصدار Python

تم التشغيل بنجاح باستخدام:

**Python 3.12.0**

أي إصدار حديث من Python 3 يكفي عادةً لأن المشروع يعتمد على المكتبة القياسية فقط.

# 5. طريقة فتح المشروع

1. افتح مجلد المشروع في مستكشف الملفات أو في Cursor / VS Code.
2. داخل مساحة العمل يوجد مجلد:
   `Number-Guessing-Game---Python-main`
3. ادخل إلى هذا المجلد قبل التشغيل، لأن ملف اللعبة موجود داخله وليس في المجلد الخارجي مباشرة.

من موجه الأوامر (PowerShell أو CMD):

```bat
cd D:\project_lv3\Number_Gussing_Game\Number-Guessing-Game---Python-main
```

إذا كان المشروع في مسار آخر، انتقل إلى المجلد الذي يحتوي ملف `Number Guessing Game.py`.

# 6. إنشاء البيئة الافتراضية

البيئة الافتراضية ليست إلزامية لأن المشروع لا يحتاج مكتبات خارجية، لكنها مفيدة للتدريب.

من داخل مجلد المشروع (`Number-Guessing-Game---Python-main`):

```bat
python -m venv .venv
```

# 7. تفعيل البيئة الافتراضية

في PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

إذا ظهر خطأ متعلق بتنفيذ السكربتات في PowerShell، يمكن التشغيل بدون تفعيل باستخدام مسار Python داخل البيئة، أو استخدام CMD:

```bat
.venv\Scripts\activate.bat
```

للتحقق بعد التفعيل:

```bat
python --version
```

# 8. تثبيت المكتبات

لا يحتاج هذا المشروع إلى تثبيت مكتبات خارجية.

لا يوجد ملف `requirements.txt`، والبرنامج يستورد فقط الوحدة المدمجة:

- `random`

# 9. تشغيل المشروع

الأمر الذي تم استخدامه بنجاح من داخل مجلد المشروع:

```bat
python "Number Guessing Game.py"
```

باستخدام البيئة الافتراضية بدون تفعيل:

```bat
.\.venv\Scripts\python.exe "Number Guessing Game.py"
```

مهم: اسم الملف يحتوي على مسافات، لذلك يجب وضع الاسم بين علامتي تنصيص `"..."`.

# 10. ماذا يحدث عند التشغيل؟

1. يبدأ البرنامج ويطلب تخمين رقم بين 1 و 100.
2. إذا أدخلت نصًا غير رقمي تظهر رسالة:
   `Invalid input. Please enter a number.`
3. إذا كان تخمينك أصغر من الرقم السري تظهر:
   `Too low, try again.`
4. إذا كان تخمينك أكبر من الرقم السري تظهر:
   `Too high, try again.`
5. إذا خمنت الرقم الصحيح تظهر رسالة التهنئة ثم إحصائيات التخمينات.
6. يسألك البرنامج: هل تريد اللعب مرة أخرى؟ `(y/n)`
7. إذا كتبت `y` تبدأ جولة جديدة برقم سري جديد.
8. أي إجابة أخرى غير `y` تنهي البرنامج برسالة شكر.

# 11. مثال على الاستخدام

مثال توضيحي (الرقم السري هنا 42 للشرح فقط؛ في التشغيل الحقيقي يكون الرقم عشوائيًا):

```text
Please guess a number between 1 and 100: 10

Too low, try again.
Please guess a number between 1 and 100: 90

Too high, try again.
Please guess a number between 1 and 100: 42

You got it correct! Congratulations!

Number of times too high: 1
Number of times too low: 1
Total number of guesses: 3

Do you want to play again? (y/n): n

Thanks for playing! 👋
```

# 12. المشاكل الشائعة وحلولها

## Python is not recognized

المعنى: النظام لا يجد أمر `python`.

الحل:

- ثبّت Python من الموقع الرسمي وفعّل خيار Add Python to PATH.
- أو جرّب:

```bat
py "Number Guessing Game.py"
```

## الخطأ: can't open file / No such file

السبب الشائع: التشغيل من المجلد الخطأ.

الحل: تأكد أنك داخل المجلد الذي يحتوي `Number Guessing Game.py`، واستخدم علامات التنصيص بسبب المسافات في الاسم.

## نسيان علامات التنصيص حول اسم الملف

أمر خاطئ:

```bat
python Number Guessing Game.py
```

أمر صحيح:

```bat
python "Number Guessing Game.py"
```

## البيئة الافتراضية غير مفعّلة

إذا أنشأت `.venv` وتريد استخدامها، فعّلها أولًا أو شغّل الملف عبر:

```bat
.\.venv\Scripts\python.exe "Number Guessing Game.py"
```

هذا المشروع يعمل أيضًا بـ Python النظام مباشرة دون بيئة افتراضية.

## إدخال غير رقمي

إذا كتبت حروفًا مثل `abc` لن يتوقف البرنامج، بل يعرض رسالة خطأ ويطلب تخمينًا جديدًا. هذا سلوك مقصود في الكود الحالي.
