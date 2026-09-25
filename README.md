# AEO Skill ליועץ אופטימיזציה למנועי AI

סקיל ל-Claude Code שבודק אתרים ובונה תוכנית כדי שמנועי AI כמו ChatGPT, Gemini, Claude ו-Perplexity יציגו ויצטטו את התוכן שלכם. עובד בעברית ובאנגלית, לפי שפת הפנייה.

יש לו שלושה מצבים. ביקורת (audit) בודקת אתר ומחזירה ציון AEO, בעיות קריטיות, שיפורים ושלושה צעדים ראשונים, כולל בדיקת llms.txt. תוכנית (plan) בונה מפת דרכים לאופטימיזציה לעסק. תוכן (content) מציע אסטרטגיית תוכן, שאלות ותשובות ו-Schema.

## התקנה כתוסף (מומלץ)

בתוך Claude Code:

```
/plugin marketplace add guycoful/aeo-skill
/plugin install aeo@aeo-skill
```

## התקנה ידנית

```bash
mkdir -p ~/.claude/skills/aeo
curl -o ~/.claude/skills/aeo/SKILL.md \
  https://raw.githubusercontent.com/guycoful/aeo-skill/main/skills/aeo/SKILL.md
```

## שימוש

אפשר לכתוב "תבדוק את האתר שלי" עם כתובת, "רוצה להופיע ב-ChatGPT" או "מה לכתוב כדי שיצטטו אותי", והסקיל יזהה את המצב לבד. אפשר גם להפעיל ישירות עם audit, plan או content.

## English

AEO/GEO advisor for Claude Code. Audits a website for visibility in AI answer engines, builds an optimization roadmap, and plans content that gets cited. Install with `/plugin marketplace add guycoful/aeo-skill` and then `/plugin install aeo@aeo-skill`.

## רישיון

MIT. ראו את הקובץ LICENSE.

נבנה על ידי [גיא כהן](https://github.com/guycoful).
