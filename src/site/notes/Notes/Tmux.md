---
{"dg-publish":true,"dg-path":"Tmux.md","permalink":"/tmux/","contentClasses":"rtl"}
---



![Tmux Banner.png](/img/user/Assets/Banners/Tmux%20Banner.png)

# Tmux
ה- Tmux הוא Terminal Multiplexer המאפשר להריץ כמה סשנים של טרמינל בחלון אחד, והוא מציע פיצ'רים מגוונים לארגן את הטרמינל כמו למשל לפצל חלון אופקית/אנכית או להגדיר חלונות טרמינל נוספים שניתן לעבור ביניהם בקלות.

### מושגים בסיסים

#### ה- Session
ניתן לחשוב על Session כמו על "פרויקט" שפותחים ב- [[Notes/Integrated Development Environment\|IDE]]. כל Session יכול להכיל כמה [[Notes/Tmux#ה- Window\|Windows]].

##### פקודות רלוונטיות
- יצירת Session חדש - `tmux new-session -s SESSION_NAME`.
- התנתקות (detach) מ- Session (כשאנחנו בתוכו) - `Ctrl+b` ואז `d`.
- התחברות ל- Session קיים - `tmux attach-session -t SESSION_NAME`.

#### ה- Window
כל חלון יכול להכיל כמה [[Notes/Tmux#ה- Pane\|Panes]].

##### פקודות רלוונטיות
- יצירת חלון חדש - `Ctrl+b` ואז `c`.
- מעבר בין חלונות - `Ctrl+b` ואז `0-9` כדי לעבור חלון ספציפי, או `Ctrl+b` ואז `n` או `p` (בשביל next או prev).
- שינוי שם של חלון - `Ctrl+b` ואז `,`.

#### ה- Pane
ה- Panes הם תתי יחידות בתוך חלון, וכל אחד מהם מריץ טרמינל שניתן לעבוד מולו. כל [[Notes/Tmux#חלון (Window)\|חלון]] מכיל Pane אחד או יותר.

##### פקודות רלוונטיות
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

{ .block-language-dataview}

### מאמרים קשורים
| תאריך | שם הפתק |
| ----- | ------- |

{ .block-language-dataview}

