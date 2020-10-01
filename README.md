# HighloadServices
## Задание: 
написать сервис, слушающий определённый порт и возвращающий текущий прогноз погоды или прогноз погоды на выбранный день
## Prerequirements:
* Установленная среда python3
* Установленные библиотеки Flask и requests
## Установка и запуск:
1. Создайте переменную среды с названием SERV_PORT, которая будет определять какой порт будет прослушивать сервис. если переменная не существует, по умолчанию прослушивается 5000 порт;
2. Склонируйте репозиторий в выбранную папку;
3. выполните команду **export FLASK_APP=Main.py**;
4. Выполните команду *flask run*;
## Использование:
Для получения текущего прогноза погоды используйте запрос <Хост:Порт>/v1/current/?city=*Город*, где *Город* это название города на английском
Прогноз будущей погоды доступен на 10 дней вперёд, для этого введите запрос <Хост:Порт>/v1/weather/?city=*Город*&dt=*день*, где *Город* это название города на английском, а *день* это количество дней после сегодняшнего. Так при вводе 1 будет возвращена погода на завтра, при 2 - на послезавтра и так далее. Так же возможно обращение по маршрутам через curl
Получение погоды за прошлые дни недоступно в бесплатной версии используемого API 
если город не найден или произошла внутренняя ошибка, будет возвращен код ошибки 400 BadRequest с сообщением "Sorry, no matching location found or an internal server error occured, try again later"


