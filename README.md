# HLC15
Highload Course. Ex 15

1. Типи сторінок на сайті 
    - Сторінка з інфою про матчі, які проходять в даний момент
    - Історичні дані про матчі (ліги, кубки, турнірні таблиці і тд)
    - Футбольні новини
    - Статті (лайфстайл, гайди по покупкам, тощо)
    - Статичні сторінки (полісі, інфо і тд)
 
2. Можливі джерела пікових навантажень

    а) Важливий матч (фінал змагання/якісь унікальні події) спричинить навантаження на ріалтайм сторінку спражніми користувачами, які прийшли самі/або з пуш повідомленням
 
    б) Атака ботів. Виділю такі можливі мотиви. 
           
              1. Читають інфу по матчам, щоб агрегувати дані
           
              2. Лонгпулять рахунки
 
    в) Важлива подія в новинах/Екслюзивний матеріал і як наслідок - навантаження на сторінку з новиною/новинами

    г) DDOS атака

3. Можливі рішенння

   В першу чергу беремо за факт, що система написана з оглядом на можливе навантаження (використовується кеш, оптимальне зберігання даних, можливість скейлінгу окремих 
частин, тощо)


 а) Нам відомий час матчу та події - попередньо робимо наступне
   - Збільшуємо к-ть реплік (ми знаємо +- потрібну к-ть з проведених тестів та попереднього досвіду)
   - Прогріваємо кеш
   
   
 б) 
   - Аналізуємо трафік, щоб знайти закономірності
   - Блокуємо конкретні іп, якщо боти користуються статичними
   - Аналізуємо поведінку звичайних користувачів та вводимо відповідні обмеження на к-ть запитів на одиницю часу
   
 в) 
 
   - автоскейлінг за наперед визначеними метриками
   - якщо подія очікувана (пуш, аналітично зрозуміло, що новина спричинить навантаження) - використати дії з пункту а)

 г) Проаналізувати тип атаки та вжити відповідних заходів
   
