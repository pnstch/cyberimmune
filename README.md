# Secure update
---
***Отредактирован app-update.py*** 

В get update digest файла requests.rest file отправить GET request, из request скопировать sha256 и вставить в update POST request в раздел manager section в requests.rest

Красными стрелками выделены **возможные векторы атак**
![scheme3 drawio (3)](https://user-images.githubusercontent.com/85806007/209093229-9f9d7cf9-070d-4735-8faa-dd5bc7e92ba2.png)

---
## Имплементация защиты
---
Данный способ защиты от представленных выше атак заключается в том, чтобы "*подписать*" данные. В случае успешной проверки происходит обнолвение, иначе отрабатывается логика, которая запрещает обновление
![scheme3 drawio](https://user-images.githubusercontent.com/85806007/209565570-19f10584-9b1a-4ae2-b137-7396471e74fe.png)
