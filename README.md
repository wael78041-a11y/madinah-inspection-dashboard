<p align="center"><b>العربية</b> · <a href="#english-version">English</a></p>

# لوحة الزيارات الرقابية — أمانة منطقة المدينة المنورة

لوحة Power BI تفاعلية تحلّل الزيارات الرقابية لأمانة منطقة المدينة المنورة في النصف الأول من 2023 — قرابة 80 ألف زيارة و438 ألف مخالفة — وتترجمها إلى صورة واضحة تدعم قرارات الرقابة والتحصيل.

*بيانات المشروع مولّدة اصطناعيًا لأغراض العرض، والأرقام توضيحية.*

## أبرز ما تكشفه اللوحة

- الامتثال العام لا يتجاوز **19.9%**، ويبقى ثابتًا طوال الأشهر الستة دون تحسّن يُذكر.
- الالتزام يتراجع كلما ارتفعت خطورة النشاط: نحو **6%** للأنشطة الأعلى خطورة مقابل **50%** للأدنى.
- قطاع الأغذية هو الأضعف التزامًا — التموينات **96%** مخالفات والبقالة **95%**.
- أبرز خلل في التحصيل: **2.8% فقط** من إجمالي الغرامات (833 مليون ريال) جرت فوترته فعليًا، ولم يُحصّل منه سوى جزء يسير.
- الغرامات تتركّز زمنيًا في يناير (**31%** من غرامات النصف الأول) وجغرافيًا في بلديات قباء والعوالي والعقيق.

تشير هذه المؤشرات إلى ثلاث أولويات: معالجة خط الفوترة أولًا، ثم ربط كثافة التفتيش بدرجة الخطورة، وحملة تفتيش وتوعية موجّهة لقطاع الأغذية.

## كيف بُنيت

جاء المصدر كملف إكسل بورقتين على مستويين مختلفين (الزيارة والمخالفة)، فأعدت هيكلته في **نموذج نجمي** يفصل الحقائق عن الأبعاد: جدولا حقائق (الزيارات والمخالفات) وستة أبعاد — التاريخ والمنشأة والنشاط والموقع والمراقب — مع 23 مقياس DAX وست علاقات نشطة.

أهم قرار في التحليل كان احتساب الغرامات من مستوى المخالفة لا مستوى الزيارة؛ الخلط بينهما يعطي 109 مليون ريال بدل 833 مليون — فارق يقلب كل استنتاج لاحق.

## الصفحات

خمس صفحات تتدرّج من العام إلى التفصيلي:

1. **ملخص تنفيذي** — أبرز النتائج والتوصيات في صفحة قرار واحدة
2. **نظرة عامة** — حجم النشاط الرقابي ومستوى الامتثال
3. **المخالفات والغرامات** — اتجاه الغرامات وحالة التحصيل وأعلى الأنشطة
4. **أداء المراقبين** — الأحمال وساعات الذروة والإنتاجية
5. **المنشآت والأنشطة** — أعلى المنشآت والأحياء، ومصفوفة الخطورة مقابل الامتثال

التصميم عربي (RTL) بثيم موحّد، مع عناوين بيانات على الرسوم وترتيب زمني للأشهر وأيام الأسبوع.

## التشغيل

افتح `visits_dashboard.pbip` في Power BI Desktop؛ ستُحمَّل البيانات من مجلد `data/`. اضغط Refresh عند أول فتح، وإن ظهر خيار ترقية صيغة التقرير فاختر **Don't upgrade**.

## الأدوات

Power BI · DAX · Power Query · نمذجة نجمية (Star Schema) · Python

---

<a id="english-version"></a>
<p align="center"><a href="#لوحة-الزيارات-الرقابية--أمانة-منطقة-المدينة-المنورة">العربية</a> · <b>English</b></p>

# Madinah Municipality — Inspection Visits Dashboard

An interactive Power BI dashboard analyzing regulatory inspection visits for the Madinah Region Municipality across the first half of 2023 — around 80,000 visits and 438,000 violations — turning them into a clear picture that supports enforcement and collection decisions.

*The project data is synthetically generated for demonstration; the figures are illustrative.*

## Key findings

- Overall compliance sits at just **19.9%** and stays flat across all six months, with no real improvement.
- Compliance drops as activity risk rises: around **6%** for the highest-risk activities versus **50%** for the lowest.
- Food retail is the weakest — convenience stores at **96%** violations, groceries at **95%**.
- The biggest gap is in collection: only **2.8%** of total fines (SAR 833M) were actually invoiced, and only a fraction of that was ever collected.
- Fines concentrate in January (**31%** of H1 fines) and in the Quba, Al-Awali, and Al-Aqiq municipalities.

Together these point to three priorities: fix the invoicing pipeline first, tie inspection frequency to risk level, and run a targeted campaign for the food sector.

## How it was built

The source was an Excel workbook with two sheets at different grains (visit and violation), which I restructured into a **star schema** separating facts from dimensions: two fact tables (visits and violations) and six dimensions — date, establishment, activity, location, and inspector — with 23 DAX measures and six active relationships.

The key analytical decision was reading fines from the violation grain rather than the visit grain; mixing the two returns SAR 109M instead of 833M — a gap that flips every downstream conclusion.

## Pages

Five pages, from overview to detail:

1. **Executive summary** — key findings and recommendations on a single decision page
2. **Overview** — inspection volume and compliance
3. **Violations & fines** — fine trends, collection status, top activities
4. **Inspector performance** — workload, peak hours, productivity
5. **Establishments & activities** — top establishments and districts, plus a risk-vs-compliance matrix

The design is Arabic (RTL) with a consistent theme, data labels on the charts, and chronological sorting for months and weekdays.

## Running it

Open `visits_dashboard.pbip` in Power BI Desktop; the data loads from the `data/` folder. Click Refresh on first open, and if prompted to upgrade the report format, choose **Don't upgrade**.

## Tools

Power BI · DAX · Power Query · Star schema modeling · Python
