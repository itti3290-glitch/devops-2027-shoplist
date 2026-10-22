איזו פקודה תבנה מה-Dockerfile שלכן image בשם greeter עם התגית v1? (מהתיקייה הראשית של הריפו.)
איזו פקודה תריץ אותו ברקע, בשם greeter, כך שבדפדפן נגיע אליו דרך http://localhost:9000?
מה צריך להוסיף לפקודה משאלה 2 כדי שהברכה תהיה Shalom במקום Hello?
מה תחזיר הכתובת http://localhost:9000/hello/Rivka אחרי השינוי משאלה 3?
שיניתן שורה ב-app.py ובניתן שוב. אילו שלבים ב-build יסומנו CACHED, ואילו ירוצו מחדש? למה?

תשובה 1: docker build -t greeter:v1 lessons/02-docker-basics/homework/greeter
תשובה 2:docker run -d -p 9000:8000 --name greeter greeter:v1
תשובה 3: docker run -d -p 9000:8000 --name greeter -e GREETING=Shalom greeter:v1
תשובה 4:{"message":"Shalom, Rivka!"}
תשובה 5:FROM, WORKDIR, COPY
