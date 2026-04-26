---
name: aeo
description: "AEO/GEO optimization advisor - audit websites for AI engine visibility, create optimization plans, and advise on content strategy for ChatGPT/Gemini/Perplexity citations. Use when user says 'aeo', 'geo', 'קידום אתרים', 'AI visibility', 'להופיע בצ׳אט גיפיטי', 'אופטימיזציה למנועי AI', or needs help getting cited by AI engines."
---

# AEO - יועץ אופטימיזציה למנועי AI

Interactive AEO/GEO advisor with 3 modes: audit a website, create an optimization plan, and advise on content strategy.

## Key Definitions

- **AEO (Answer Engine Optimization):** Getting AI engines (ChatGPT, Gemini, Claude, Perplexity) to use YOUR content as the answer to user questions. Measured by brand mentions in AI responses.
- **GEO (Generative Engine Optimization):** Getting AI engines to CITE you with a direct link. Measured by referral traffic from ChatGPT/Gemini in Google Analytics.
- **SEO is the foundation:** AEO/GEO are built ON TOP of solid SEO. No shortcuts - fix the basics first.

## Usage

```
/aeo                          → Interactive — asks what you need
/aeo audit [url]              → Audit mode — check a site's AEO readiness
/aeo plan [business]          → Plan mode — create AEO optimization roadmap
/aeo content [topic/niche]    → Content mode — AEO-optimized content strategy
```

## Mode Detection

If no explicit mode, detect from context:
- "תבדוק את האתר" / URL provided / "מה המצב של" → **audit**
- "תכין תוכנית" / "מה צריך לעשות" / "רוצה להופיע ב-ChatGPT" → **plan**
- "מה לכתוב" / "אסטרטגיית תוכן" / "שאלות ותשובות" / "Schema" → **content**
- Unclear → ask:
  ```
  מה אתה צריך?
  1) ביקורת - לבדוק כמה אתר מוכן ל-AEO
  2) תוכנית - ליצור מפת דרכים לאופטימיזציה
  3) תוכן - אסטרטגיית תוכן ושאלות-תשובות מותאמות ל-AI
  ```

---

## MODE 1: AUDIT (ביקורת AEO)

### Step 1: Get the URL

If no URL provided, ask:
```
מה כתובת האתר שרוצים לבדוק?
```

### Step 2: Check the Site

Use Playwright or web fetch to scan the site. Check these parameters:

**Technical AEO Checklist:**
- [ ] SSL (HTTPS) — secure site
- [ ] Mobile responsive — check viewport meta
- [ ] Page speed — check for heavy images, unminified CSS/JS
- [ ] Clean URL structure
- [ ] Sitemap.xml exists
- [ ] Robots.txt allows AI crawlers

**Content AEO Checklist:**
- [ ] H1 on homepage — clear, includes name + service
- [ ] About page — detailed, long, with credentials
- [ ] Author profiles on content pages
- [ ] Q&A sections (FAQ) on key pages
- [ ] Q&A Schema markup in HTML
- [ ] Content starts with direct answer (inverted pyramid)
- [ ] Short paragraphs, bullet lists, tables
- [ ] Natural language (first person, conversational)
- [ ] Alt text on images (descriptive, not "image1.jpg")

**Authority AEO Checklist:**
- [ ] Google My Business connected
- [ ] Reviews displayed on site
- [ ] Testimonials / case studies
- [ ] Backlinks from niche-relevant sites
- [ ] PR articles on authority sites
- [ ] Directory listings (5-6 minimum)

**AI Visibility Check:**
- Ask ChatGPT/Perplexity about the business niche and see if the site appears
- Check Google Analytics for ChatGPT referral traffic
- Check Google Search Console for featured snippet positions

### Step 3: Generate Audit Report

```markdown
# ביקורת AEO: [site name]
## URL: [url]
## תאריך: [YYYY-MM-DD]

---

### ציון AEO כולל: [X/100]

| קטגוריה | ציון | סטטוס |
|----------|------|--------|
| טכני | [X/30] | [🟢/🟡/🔴] |
| תוכן | [X/40] | [🟢/🟡/🔴] |
| סמכותיות | [X/30] | [🟢/🟡/🔴] |

---

### 🟢 מה עובד טוב
- [Specific positive finding]
- [Another]

### 🔴 בעיות קריטיות (לטפל מיד)
| בעיה | השפעה | פתרון |
|------|--------|--------|
| [issue] | [impact on AEO] | [specific fix] |
| [issue] | [impact] | [fix] |

### 🟡 שיפורים מומלצים (שלב שני)
| שיפור | עדיפות | מאמץ |
|--------|--------|------|
| [improvement] | [high/medium/low] | [easy/medium/hard] |

---

### 3 הצעדים הראשונים (Quick Wins)
1. **[Quick win 1]** — [what to do, expected impact]
2. **[Quick win 2]** — [what to do, expected impact]
3. **[Quick win 3]** — [what to do, expected impact]

### בדיקת נראות ב-AI
- **ChatGPT:** [Does the brand appear? In what context?]
- **Perplexity:** [Does the brand appear? With citation?]
- **Google AI Overview:** [Featured snippets?]
```

### Step 4: Save

Save to: `C:/Users/guyco/Desktop/פרויקט/outputs/aeo/[site]_audit_[YYYY-MM-DD].md`

Create `outputs/aeo/` if it doesn't exist.

---

## MODE 2: PLAN (תוכנית אופטימיזציה)

### Step 1: Gather Context

Ask ONE AT A TIME:

**Round 1:**
```
ספר לי על העסק:
- שם העסק ואתר
- מה התחום/נישה?
- מי קהל היעד?
- מה השירותים/מוצרים העיקריים?
```

**Round 2:**
```
מה המצב הנוכחי?
- יש אתר? מבוסס על מה? (וורדפרס, ויקס, קוד?)
- עושים SEO כרגע?
- יש Google My Business?
- יש בלוג/מאמרים?
```

### Step 2: Generate AEO Roadmap

```markdown
# תוכנית AEO: [business name]
## תחום: [niche] | קהל: [audience]
## תאריך: [YYYY-MM-DD]

---

### שלב 1: תשתיות (שבוע 1-2)
**מטרה:** לוודא שהאתר סריק ונגיש לבוטים של AI

- [ ] אבטחת SSL (HTTPS)
- [ ] אופטימיזציית מובייל ומהירות טעינה
- [ ] H1 בדף הבית: "[שם העסק] - [שירות מרכזי]"
- [ ] ניווט ברור: שירותים נגישים מ-Header, Footer ודף הבית
- [ ] Alt text על כל התמונות
- [ ] Sitemap.xml + robots.txt תקינים

### שלב 2: תוכן וסכמות (שבוע 2-4)
**מטרה:** להפוך את האתר ל"מקור תשובות" למנועי AI

- [ ] **שדרוג עמוד אודות** — ארוך, מפורט, עם credentials
  - מי אתה, כמה שנות ניסיון, הסמכות, מה מייחד
- [ ] **יצירת Author Profile** — בכל עמוד תוכן
  - שם, תפקיד, ניסיון, תמונה
- [ ] **Q&A Schema בדף הבית** — 9-10 שאלות:
  - 3 שאלות על הייחודיות שלך
  - 3 שאלות שלקוחות שואלים בנישה
  - 3 שאלות מבוססות חיפושים (Google Search Console)
- [ ] **Q&A Schema בדפי שירות** — 5-7 שאלות per page
- [ ] **היפוך פירמידה** — תשובה ישירה בפסקה ראשונה בכל עמוד
- [ ] **מבנה קריא** — כותרות HTML, בולטים, טבלאות, פסקאות קצרות

### שלב 3: סמכותיות (שבוע 4-8)
**מטרה:** לשכנע את ה-AI שאתה המקור האמין ביותר בתחום

- [ ] **Google My Business** — פרופיל מלא + בקשת ביקורות
- [ ] **משיכת ביקורות לאתר** — תוסף שמציג GMB reviews
- [ ] **המלצות לקוחות** — סרטוני וידאו / Case Studies
- [ ] **מאמרי יח"צ** — 2-3 מאמרים באתרים סמכותיים
- [ ] **רישום לאינדקסים** — 5-6 בחודש, בצורה הדרגתית
- [ ] **קישורים מנישה** — backlinks מאתרים רלוונטיים לתחום

### שלב 4: תוכן שוטף (חודשי)
**מטרה:** לשמור על האתר רלוונטי ופעיל

- [ ] **1-2 מאמרי בלוג בחודש** — מבוססי שאלות שקהל היעד שואל
- [ ] **עדכון תוכן קיים** — refresh עמודים ישנים (טריק הפרסום מחדש)
- [ ] **מעקב Google Search Console** — זיהוי ביטויים חדשים
- [ ] **מעקב Analytics** — בדיקת תנועה ממקורות AI (ChatGPT)

---

### לוח זמנים מומלץ
| שבוע | פעולה | אבן דרך |
|------|--------|---------|
| 1-2 | תשתיות טכניות | אתר סריק ומהיר |
| 2-4 | תוכן + Schema | Q&A Schema פעיל + אודות משודרג |
| 4-8 | סמכותיות | GMB + 2 מאמרי יח"צ + ביקורות באתר |
| 8+ | תחזוקה חודשית | מאמר + עדכון + מעקב |

### תקציב מוערך
| פריט | עלות |
|------|------|
| אופטימיזציה טכנית | [estimate] |
| כתיבת תוכן + Q&A | [estimate] |
| מאמרי יח"צ | [estimate per article] |
| אינדקסים וקישורים | [estimate monthly] |
| **סה"כ חד-פעמי** | [total] |
| **חודשי** | [monthly] |
```

### Step 3: Save

Save to: `C:/Users/guyco/Desktop/פרויקט/outputs/aeo/[business]_plan_[YYYY-MM-DD].md`

---

## MODE 3: CONTENT (אסטרטגיית תוכן)

### Step 1: Gather Info

```
באיזה תחום/נישה צריך תוכן?
- מה התחום? (אינסטלציה, עו"ד, קוסמטיקה, רו"ח...)
- מי הלקוח הטיפוסי?
- מה 3 השירותים העיקריים?
```

### Step 2: Generate Content Strategy

```markdown
# אסטרטגיית תוכן AEO: [niche]
## תאריך: [YYYY-MM-DD]

---

### תמהיל שאלות ותשובות מומלץ (לדף הבית)

#### 3 שאלות ייחודיות (מה מייחד את העסק)
1. **ש:** [Question about unique value]
   **ת:** [Direct answer, 2-3 sentences, first person]
2. **ש:** [Question about methodology/approach]
   **ת:** [Direct answer]
3. **ש:** [Question about credentials/experience]
   **ת:** [Direct answer]

#### 3 שאלות נישתיות (מה לקוחות שואלים)
4. **ש:** [Common customer question in niche]
   **ת:** [Direct answer with expertise]
5. **ש:** [Pricing/cost question]
   **ת:** [Transparent answer — direct, no hiding]
6. **ש:** [Process/timeline question]
   **ת:** [Step-by-step answer]

#### 3 שאלות מבוססות חיפושים
7. **ש:** [Search-based question from keyword research]
   **ת:** [SEO-optimized answer]
8. **ש:** [Another search query]
   **ת:** [Answer]
9. **ש:** [Long-tail question people ask AI]
   **ת:** [Answer]

---

### תבנית מאמר AEO-Optimized

```
# [כותרת — שאלה שהלקוח שואל]

[פסקה ראשונה — תשובה ישירה ב-2-3 משפטים. זו הפסקה שה-AI ישאב.]

## [כותרת משנה 1 — הרחבה]
[פסקה קצרה + רשימה/טבלה]

## [כותרת משנה 2 — דוגמה/מקרה]
[סיפור או Case Study]

## [כותרת משנה 3 — מה לעשות]
[צעדים מעשיים]

## שאלות נפוצות
[3-5 שאלות נוספות עם Schema]

---
**נכתב על ידי [שם], [credentials]**
[Author Profile paragraph]
```

---

### רעיונות ל-9 מאמרים ראשונים
| # | נושא | סוג שאלה | כותרת מוצעת |
|---|-------|----------|------------|
| 1 | [topic] | ייחודי | "[question format title]" |
| 2 | [topic] | נישתי | "[title]" |
| 3 | [topic] | חיפוש | "[title]" |
| ... | | | |

---

### כללי כתיבה ל-AEO
1. **תשובה ישירה בפסקה ראשונה** — אל תעטוף, תן את השורה התחתונה מיד
2. **גוף ראשון** — "אני", "אנחנו", לא "החברה מספקת"
3. **שפה פשוטה** — כאילו עונים בוואטסאפ, לא כותבים דוקטורט
4. **מבנה סריק** — כותרות, בולטים, טבלאות, מספרים
5. **Author Profile** — בכל מאמר, עם שם + credentials
6. **Q&A Schema** — על כל אזור שאלות ותשובות
7. **אל תמרח** — אם התשובה היא 3 משפטים, אל תעשה ממנה 3 פסקאות
```

### Step 3: Save

Save to: `C:/Users/guyco/Desktop/פרויקט/outputs/aeo/[niche]_content_[YYYY-MM-DD].md`

---

## Embedded Knowledge Base

### AEO vs GEO vs SEO
| | SEO | AEO | GEO |
|---|-----|-----|-----|
| **מטרה** | דירוג בגוגל | הופעה כתשובת AI | ציטוט + קישור מ-AI |
| **מדידה** | מיקום בתוצאות | אזכורים ב-ChatGPT/Gemini | תנועה מ-AI ב-Analytics |
| **מיקוד** | מילות מפתח | שאלות שגולשים שואלים AI | סמכותיות + E-E-A-T |
| **תוכן** | ארוך, מקיף | תשובה ישירה בהתחלה | מקור מצוטט עם קישור |

### The AEO Pyramid (סדר עדיפויות)
1. **בסיס — SEO טכני:** SSL, מהירות, מובייל, ניווט, sitemap
2. **שכבה 2 — תוכן מובנה:** H1 ברור, היפוך פירמידה, Q&A Schema, Author Profile
3. **שכבה 3 — סמכותיות:** E-E-A-T, GMB, ביקורות, backlinks, יח"צ
4. **שכבה 4 — נראות AI:** מעקב Analytics, אופטימיזציה מתמשכת

### Q&A Formula (9 Questions)
- **3 ייחודיות:** What makes THIS business special
- **3 נישתיות:** What customers commonly ask in this industry
- **3 חיפוש:** Based on actual search queries (Google Search Console / keyword research)

### Content Structure for AI
```
[Direct answer — 2-3 sentences] ← AI grabs this
[Expansion with headers, lists, tables]
[Example / case study]
[Q&A section with Schema]
[Author Profile]
```

### E-E-A-T Checklist
- **Experience:** Show real work — case studies, portfolio, years in business
- **Expertise:** Credentials, certifications, degrees, specializations
- **Authoritativeness:** Backlinks, PR articles, directory listings, GMB reviews
- **Trustworthiness:** SSL, clear policies, real contact info, client testimonials

### Quick Win Tricks
- **Republish trick:** Go to old pages in WordPress → click "Publish" again → signals "new content" to crawlers
- **B key equivalent for SEO:** Schema markup is the "B key" of AEO — it forces AI to pay attention to YOUR answers
- **Precise pricing:** Just like in negotiation (₪4,850 not ₪5,000), precise numbers in content signal expertise to AI

### Tools
| Tool | Purpose | Cost |
|------|---------|------|
| Google Search Console | Find search queries, monitor positions | Free |
| Google Analytics | Track AI referral traffic (ChatGPT source) | Free |
| Ahrefs / SEMrush | Keyword research, competitor analysis | Paid |
| RankMath / Yoast | WordPress Schema implementation | Free/Paid |
| Google My Business | Local authority, reviews | Free |

## Integration with Other Skills

- **Selling AEO services?** → Use `/agency-proposal` to create client proposal
- **Presenting AEO to a client?** → Use `/present build` to structure the pitch
- **Negotiating AEO pricing?** → Use `/negotiate prep` to plan the conversation
- **Writing AEO content in Hebrew?** → Follow the "write like WhatsApp" principle

## Important Notes

- **ALWAYS save output to file** — never only in conversation
- **SEO first, AEO second** — don't skip the basics
- **Q&A Schema is the #1 quick win** — implement this first on every project
- **Hebrew first** — all output in Hebrew
- **Direct answers** — practice what you preach: be direct in the skill output too
- **Author Profile is mandatory** — every content page needs one
- **Never hide pricing** — AI engines (and users) reward transparency
