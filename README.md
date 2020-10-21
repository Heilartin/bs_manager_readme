# Documentation BS Manager

# Кратко и ясно:

1. Сработал монитор на бш, запустили рафл и ты это увидел.
2. !me сделал и посмотрел все ли окей у тебя, если не окей, делаешь окей, ок?
3. Делаешь !sizes ["38 EU", "39 EU", "40 EU"] и отправляешь эту команду, размеры добавляются к тебе.
4. Вводишь !activate и кайфуешь,
 через несколько минут в твой канал по твоему вебхуку посыпятся заказы, сиди и плати в свое удовольствие
 > https://sun9-66.userapi.com/FjjVttBV5Lvw6MgeGbl-3F1Nc70iLH54GE-USA/MfMTms7-A4w.jpg
5. По окончанию розыгрыша Дима проверит наличие победителей и отправит в дм информацию о победе.

## Commands

### Users
- !me
   > Информация о пользователе
- !auth guild_id ship url
   > Аутентификация пользователя <br>
   Params: guild_id - ID сервера, ship - метод доставки, url - вебхук <br>
* Поддерживается и slack, и discord вебхук
   
   
    Example:  !auth 14000000000000 dhl https://hooks.slack.com/services/url

### Update
-  !up url [value]
   > Обновление вебхука    
   value = новая ссылка <br>
 
 
     Example:  !up url https://hooks.slack.com/newurl
     
-  !up ship [value]
   > Обновление метода доставки.<br>
   Доступные методы: ``dhl, cdek, pickup, flat`` - в зависимости от релиза <br>
   value = новый метод <br>
   
  
     Example:  !up ship cdek
### Get
- !get accounts
  > Выгрузить все свои аккаунты. <br>
 
    Example: !get accounts

- !get orders [pid]
  > Выгрузить всю информацию о заказах по определенному релизу


    Example: !get orders 1234566
    
### Load
- !load [attached file]
  > Загрузить свои профиля. Профиля в закрелепенном файле.
 
 
    Example: !load <прикрепленный файл>
    FORMAT: 
            {
                "login": "qwe123",
                "password": "test123",
                "shipping_id": "1234567"
            } 
- !shipping_ids [format] [attached file]
  > Получить свои shipping ids можно через эту команду
    
    
    Example: !shipping_ids txt <прикрепленный файл>
    FORMAT: login:password
    
    Example: !shipping_ids json <прикрепленный файл>
    FORMAT:     
            {
               "login": "qwe123",
               "password": "test123"
            } 
    
### Settings
- !sizes ["41 EU"]
  > Добавление размеров для запуска
  
  
    Example: !sizes ["41 EU", "42 EU", "43 EU"]

- !activate
  > Подтверждение готовности к раффлу. Если activated = No - ваши профиля не ранятся <br>
  Готовность нужно подтверждать перед каждым релизом

###  Drop
- !drop [setting]
  > Удалит метод доставки, вебхук


    Example: !drop setting
    
- !drop [sizes]
  > Удалит все размеры
  
  
    Example: !drop sizes

- !drop [user]
  > Деактивирует аккаунт и удалит всю инфорацию. Включая аккаунты.
  
  
    Example: !drop user

- !drop [accounts]
  > Удаление аккаунтов
   
  
    Example: !drop accounts
