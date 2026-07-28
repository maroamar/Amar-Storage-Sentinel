
```markdown
# 🛡️ Amar Storage Sentinel (v1.8)

> **Zero-Freeze Async Engine | Games, Programs & System Storage Optimizer**  
> *أداة هندسية خفيفة لمسح وتنظيف الأقراص الصلبة والألعاب دون تجميد النظام أو إجهاد الأقراص.*

---

## 🌐 Language Options / خيارات اللغة
* 🇬🇧 [English Readme](#-english)
* 🇸🇩 [النسخة العربية](#--العربية)

---

## 🇬🇧 English

### 💡 What is Amar Storage Sentinel?
**Amar Storage Sentinel** is a high-performance, lightweight graphical utility built natively in PowerShell (WPF) to reclaim valuable disk space without compromising system responsiveness. Unlike traditional disk scanners that lock up or stress your hardware, this tool features an independent **Asynchronous Background Engine** combined with **Micro-sleep Throttling** to protect your mechanical hard drives (HDD) and SSDs from thermal and I/O fatigue.

### 🚀 Key Features & Architectural Advantages

* **Zero-Freeze UI:** Powered by background runspaces and dispatcher timers; the interface remains 100% fluid and responsive during deep scans.
* **Ultra-Low Disk Stress:** Designed with intelligent micro-pauses between directory queries to prevent 100% disk usage spikes or mechanical drive wear.
* **Targeted Deep Traversal:** Intentionally focuses on high-capacity clutter zones (Downloads, Program Files, User folders, Steam libraries, and custom game paths like *FIFA14 mods*), bypassing redundant system folders like `WinSxS`.
* **Smart Size Filtering:** Instantly filters and extracts large files exceeding **100MB**, sorting them by weight to help you spot heavy bottlenecks immediately.
* **Interactive Actions:** 
  * 📂 **Open Location:** Inspect the file's directory instantly.
  * 📦 **Smart Move:** Safely relocate bulky files to another drive with automatic list refreshing.
  * 🗑️ **Force Delete:** Purge unwanted clutter with explicit confirmation prompts.
* **Branding & Portable Ready:** Features native logo integration, standalone execution, and a real-time audit logger (`Storage_Sentinel_Log.txt`).

---

### 🖥️ User Interface Preview

```text
+--------------------------------------------------------------+
| [🛡️ Logo] Amar Storage Sentinel v1.8             [Branded]   |
|           Zero-Freeze Async Engine                           |
+--------------------------------------------------------------+
| Select Drive: [ C: [120 GB free / 465 GB] ]  [ Scan >100MB ] |
+--------------------------------------------------------------+
| Size (GB) | File Name           | Full Path                  |
|-----------|---------------------|----------------------------|
| 14.50     | data_block.big      | C:\Games\FIFA14 mods\...   |
| 4.20      | setup_archive.zip   | C:\Users\Admin\Downloads\..|
+--------------------------------------------------------------+
| [ Open Location ]       [ Smart Move ]       [ Force Delete ]|
+--------------------------------------------------------------+
| Storage Sentinel v1.8 Initialized. Logo Active.              |
+--------------------------------------------------------------+

```

---

### ⚙️ Requirements & Execution

* **OS:** Windows 10 / 11 (Requires PowerShell 5.1+).
* **Privileges:** Runs with automatic Administrator elevation to ensure full access permissions across protected directories.
* **Logo Integration:** Place your custom `logo.png` (Recommended: `128x128px` Transparent PNG) in the same directory as the script or compiled executable.

---

### 📥 Download & Usage

#### 🚀 Option 1: Quick Download (Pre-compiled Executable)

1. Go to the **[Releases](https://www.google.com/search?q=../../releases)** section on the right side of this repository.
2. Download `Amar_Storage_Sentinel_v1.8.zip`.
3. Extract the ZIP file (ensure `Amar_Storage_Sentinel.exe` and `logo.png` remain in the same folder).
4. Run `Amar_Storage_Sentinel.exe` directly as Administrator.

#### 🛠️ Option 2: Build from Source (.PS1)

If you prefer running or compiling the source script yourself:

1. Clone or download `Amar_Storage_Sentinel.ps1`.
2. Compile it using `ps2exe` with no console window and your custom icon:

```powershell
Invoke-PS2EXE -InputFile "Amar_Storage_Sentinel.ps1" `
              -OutputFile "Amar_Storage_Sentinel.exe" `
              -iconFile "app_icon.ico" `
              -noConsole `
              -requireAdmin `
              -title "Amar Storage Sentinel" `
              -version "1.8.0.0"

```

---

## 🇸🇩 العربية

### 💡 ما هي أداة Amar Storage Sentinel؟

**Amar Storage Sentinel** هي أداة خفيفة وعالية الأداء مزودة بواجهة رسومية (WPF) مبنية بلغة PowerShell، صُممت لاستعادة المساحات المفقودة في وحدات التخزين دون التأثير على استجابة النظام. بخلاف أدوات الفحص التقليدية التي تتسبب في تجميد الجهاز أو إجهاده، تعتمد هذه الأداة على **محرك خلفي غير متزامن (Async Engine)** مدعوم بـ **تقنية التهدئة الميكروية (Micro-sleep Throttling)** لحماية الأقراص الصلبة (HDD) وأقراص (SSD) من الإجهاد الحراري وارتفاع ضغط القراءة والكتابة (I/O).

### 🚀 المميزات الرئيسية والمعمارية

* **واجهة سلسة تماماً (Zero-Freeze UI):** تعمل عبر وظائف خلفية متوازنة ومؤقتات مستقلة، مما يضمن بقاء الواجهة الاستجابة بنسبة 100% أثناء الفحص الشامل.
* **إجهاد منخفض جداً للأقراص:** صُممت بتوقفات ميكروية ذكية بين المجلدات لمنع استهلاك القرص بنسبة 100% أو إجهاد الأقراص الميكانيكية.
* **فحص موجه وحاد:** تركز مسبقاً على مناطق التراكم الكبيرة (Downloads، Program Files، مجلدات المستخدمين، مكتبات Steam، ومسارات مودات الألعاب مثل *FIFA14 mods*)، مع تجنب مجلدات النظام المكررة مثل `WinSxS`.
* **فلترة ذكية للحجم:** تقوم بتصفية واستخراج الملفات التي يتجاوز حجمها **100 ميجابايت** وترتيبها تنازلياً للتعرف على الملفات الضخمة فوراً.
* **تحكم تفاعلي مباشر:**
* 📂 **Open Location:** فتح موقع الملف المSelected فوراً.
* 📦 **Smart Move:** نقل الملفات الضخمة بأمان إلى قرص آخر مع تحديث القائمة تلقائياً.
* 🗑️ **Force Delete:** حذف الحشو والمخلفات نهائياً مع رسالة تأكيد لحماية البيانات.


* **جاهزة للعلامة التجارية والتشغيل المباشر:** تدعم إدراج اللوجو الشخصي، والعمل كبرنامج مستقل مع سجل تدقيق لحظي (`Storage_Sentinel_Log.txt`).

---

### ⚙️ المتطلبات والتشغيل

* **نظام التشغيل:** Windows 10 / 11 (تتطلب PowerShell 5.1 أو أحدث).
* **الصلاحيات:** تعمل تلقائياً بصلاحيات المسؤول (Administrator) لضمان الوصول للقطاعات المحمية.
* **شعار البرنامج:** ضع ملف اللوجو الخاص بك باسم `logo.png` (يُفضل صيغة PNG شفافة بمقاس `128x128` بكسل) في نفس مجلد السكربت أو الملف التنفيذي.

---

### 📥 التحميل والاستخدام

#### 🚀 الخيار 1: التحميل السريع (ملف EXE جاهز)

1. توجه إلى قسم **[Releases](https://www.google.com/search?q=../../releases)** على اليمين في هذا المستودع.
2. قم بتحميل الملف المضغوط `Amar_Storage_Sentinel_v1.8.zip`.
3. فك الضغط (تأكد من وجود `Amar_Storage_Sentinel.exe` و `logo.png` في نفس المجلد).
4. شغل `Amar_Storage_Sentinel.exe` كمسؤول مباشرة.

#### 🛠️ الخيار 2: التجميع من الكود المصدري (.PS1)

إذا كنت تفضل تشغيل السكربت أو تجميعه بنفسك:

1. قم بتنزيل ملف `Amar_Storage_Sentinel.ps1`.
2. اجمع السكربت باستخدام أداة `ps2exe` بدون نافذة كنسول مع إرفاق الأيقونة الخاصة بك:

```powershell
Invoke-PS2EXE -InputFile "Amar_Storage_Sentinel.ps1" `
              -OutputFile "Amar_Storage_Sentinel.exe" `
              -iconFile "app_icon.ico" `
              -noConsole `
              -requireAdmin `
              -title "Amar Storage Sentinel" `
              -version "1.8.0.0"

```

---

## 📜 License / الترخيص

Developed with precision by **Amar**. Free for personal and professional systems optimization use.

*تم التطوير بدقة بواسطة **عمار**. مجاني للاستخدام الشخصي والمهني في تحسين أنظمة التشغيل.*

```

```
