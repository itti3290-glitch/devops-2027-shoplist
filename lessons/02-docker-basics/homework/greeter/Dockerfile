

# בוחרים תמונת בסיס עם גרסת Python מוגדרת
FROM python:3.12.10-slim

# מגדירים את תיקיית העבודה בתוך ה-Container
WORKDIR /app

# מעתיקים את קובץ התלויות לפני העתקת קוד התוכנה
COPY requirements.txt .

# מתקינים את הספריות שהתוכנה צריכה
RUN pip install --no-cache-dir -r requirements.txt

# מעתיקים את קובץ התוכנה לתוך תיקיית העבודה
COPY app.py .

# מצהירים שהאפליקציה משתמשת בפורט 8000 בתוך ה-Container
EXPOSE 8000

# מפעילים את אפליקציית Python באמצעות תחביר exec
CMD ["python", "app.py"]

