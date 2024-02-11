נעזרתי והתבססתי על הטמפלייט בשיטת בוטסטרפ מאתר https://themewagon.com/themes  - ישנו קישור בתחתי האתר היכן שהזכויות יוצרים
הורדתי פונקציות וסקשנים לא רצויים
הוספת פונקציות לחיצה על כפתור
הפנייה לסקשנים השונים עח פי תפריט nav
שיניתי את הmax-size ל 700px עבור מצב של מובייל
ישנו תפריט ניווט למצב מובייל ותפריט למסכים גדולים
כמו כן אפקטים וכפתורים של פתיחה וסיגרה של התפריט - הוספה בקובץ ה css של הבוסטראפ
הערה ** ה nav מוגדר להיות fixed ולא sticky משום שרציתי שישאר קבוע על המסך מעל הכל - בצורה שקופה , כחלק מהעיצוב ואילו עם סטיקי לא עבד
#mynav {
  z-index: 10;
  padding: 0;
  position: fixed;
  background-color: transparent;
  box-shadow: 3px 3px 5px rgba(0, 0, 0, 0.2);
}

#mynav ul {
  width: 100%;
  list-style: none;

  display: flex;
  justify-content: flex-start;
  align-items: center;
}

#mynav li,
.sidebar li {
  height: 50px;
}

.sidebar a,
#mynav a {
  height: 100%;
  padding: 0 30px;
  text-decoration: none;
  display: flex;
  align-items: center;
  color: black;
}
#mynav a:hover {
  background-color: #f0f0f0;
}
#mynav li:first-child {
  margin-right: auto;
}
.sidebar {
  padding: 0;
  display: none;
  position: fixed;
  top: 0;
  right: 0;
  height: 100vh;
  width: 250px;
  z-index: 999;

  backdrop-filter: blur(10px);
  background-color: rgba(255, 255, 255, 0.2);
  box-shadow: -10px 0 10px rgba(0, 0, 0, 0.1);

  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
}
.sidebar ul {
  list-style: none;
}
.sidebar li {
  width: 100%;
}
.sidebar a {
  width: 100%;
}
.menu-button {
  display: none;
}
@media (max-width: 700px) {
  .hideOnMobile {
    display: none;
  }
  .menu-button {
    display: block;
  }
}
@media (max-width: 400px) {
  nav.sidebar {
    width: 100%;
  }
}
