---
{"dg-publish":true,"dg-path":"Tmux.md","permalink":"/tmux/","contentClasses":"rtl"}
---



![Tmux Banner.png](/img/user/Assets/Banners/Tmux%20Banner.png)

# Tmux
Tmux (או Terminal Multiplexer) הוא [[Notes/תכנות\|תוכנה]] המוסיפה יכולות שונות לטרמינל הפשוט. בעזרת ה- Tmux ניתן למשל להריץ כמה [[Notes/Tmux#Session\|Sessions]] של טרמינל [[Notes/Tmux#Window\|בחלון]] אחד, לפצל [[Notes/Tmux#Window\|חלון]] אופקית/אנכית לכמה [[Notes/Tmux#Pane\|Panes]], ולהגדיר [[Notes/Tmux#Window\|חלונות]] טרמינל נוספים שניתן לעבור ביניהם בקלות.
**דבר שימושי נוסף שניתן לעשות בעזרת ה- Tmux או לאפשר למשהו לרוץ בתוך Session של Tmux גם כאשר ה- Session של הטרמינל הפשוט נסגר. בכך ניתן לחזור להמשיך מאותה נקודה שהפסקנו, גם אם בטעות סגרנו את הטרמינל.**

### אובייקטים בסיסים
ה- Tmux בנוי מכמה אובייקטים:
- [[Notes/Tmux#Session\|#Session]]
- [[Notes/Tmux#Window\|#Window]]
- [[Notes/Tmux#Pane\|#Pane]]

#### Session
ניתן לחשוב על Session כמו על "פרויקט" שפותחים ב- [[Notes/Integrated Development Environment\|IDE]] במובן הזה שכל החלונות/לשוניות שבתוך הפרויקט שפתחנו שייכות לאותו הפרויקט/משימה. כל Session יכול להכיל כמה [[Notes/Tmux#Window\|Windows]].

הנה כנה פקודות רלוונטיות:
- יצירת Session חדש - `tmux new-session -s SESSION_NAME`.
- התנתקות (detach) מ- Session (כשאנחנו בתוכו) - `Ctrl+b` ואז `d`.
- התחברות ל- Session קיים - `tmux attach-session -t SESSION_NAME`.

#### Window
כל חלון יכול להכיל כמה [[Notes/Tmux#Pane\|Panes]].

הנה כמה פקודות רלוונטיות:
- יצירת חלון חדש - `Ctrl+b` ואז `c`.
- מעבר בין חלונות - `Ctrl+b` ואז `0-9` כדי לעבור חלון ספציפי, או `Ctrl+b` ואז `n` או `p` (בשביל next או prev).
- שינוי שם של חלון - `Ctrl+b` ואז `,`.

#### Pane
ה- Panes הם תתי יחידות בתוך חלון, וכל אחד מהם מריץ טרמינל שניתן לעבוד מולו. כל [[Notes/Tmux#Window\|חלון]] מכיל Pane אחד או יותר.

הנה כמה פקודות רלוונטיות:
- פיצול חלון בצורה אנכית - `Ctrl+b` ואז `%`.
- פיצול חלון בצורה אופקית - `Ctrl+b` ואז `"`.
- מעבר בין Panes שונים - `Ctrl+b` ואז `←`, `→`, `↑`, `↓`.
- סגירת ה- Pane הנוכחי - `Ctrl+b` ואז `x`.
- שינוי גודל ה- Pane הנוכחי - `Ctrl+b` ואז `Ctrl+Arrow(up/down/left/right)`.

### מבנה ההיררכי של ה- Tmux
![Tmux Hierarchy.png](/img/user/Assets/Tmux%20Hierarchy.png)

 

--- 

### פתקים קשורים

| תאריך      | שם הפתק                                                                             |
| ---------- | ----------------------------------------------------------------------------------- |
| 2023/06/30 | [[Notes/Integrated Development Environment\|Integrated Development Environment]] |
| 2022/01/19 | [[Notes/תכנות\|תכנות]]                                                           |

{ .block-language-dataview}

### מאמרים קשורים
| תאריך | שם הפתק |
| ----- | ------- |

{ .block-language-dataview}

