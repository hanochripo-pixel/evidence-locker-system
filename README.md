# evidence-locker-system

יש לך כבר טוקן? מעולה. הנה הדרך הכי קצרה להתקדם.

## 1) לשמור את הטוקן כמשתנה זמני (בטרמינל)
> מחליפים את `<YOUR_GITHUB_TOKEN>` בטוקן שיצרת.

```bash
export GH_TOKEN='<YOUR_GITHUB_TOKEN>'
```

## 2) לוודא שהריפו מחובר ל-GitHub הנכון
```bash
git remote set-url origin https://github.com/hanochripo-pixel/evidence-locker-system.git
git remote -v
```

## 3) לבדוק שהטוקן עובד
```bash
gh auth status
```

אם מתקבלת שגיאה, אפשר להתחבר ידנית עם הטוקן:
```bash
echo "$GH_TOKEN" | gh auth login --with-token
```

## 4) להעלות שינויים ל-GitHub
```bash
git add .
git commit -m "update"
git push -u origin work
```

## 5) אם `git push` מבקש הרשאות
השתמש בשם משתמש GitHub שלך, ובסיסמה הדבק את ה-token (לא את סיסמת החשבון).

---

## חשוב: הרשאות טוקן
מומלץ שה-token יכלול לפחות:
- `repo`
- `workflow` (אם יש GitHub Actions)
