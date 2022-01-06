
Отчет по лаб. работе №1 : простой микросервис, реализующий CRUD.
Лабораторная работа №1: создание микросервиса на Spring Boot с базой данных
Дисциплина: Технологии разработки программного обеспечения
Выполнил: студент гр. МБД2131 Харлиева Л.Ц.
Цель работы: знакомство с проектированием многослойной архитектуры Web-API (веб-приложений, микро-сервисов).

ЗАПУСК ПРОЕКТА
- склонировать проект с репозитория:
$ git clone
https://github.com/LiubaKh/ReportLaboratornayaRabota

- для того,чтобы запустить проект через Docker:
1. сборка приложения в Maven из командной строки:
$ mvnw package
2. перейти в директорию проекта SimpleApi:
$ cd ../SimpleApi
3. собрать Docker-image :
$ docker build --tag simpleapi:lates
4. запустить c Docker-container:
$ docker run -p 8080:8080 simpleapi
- работа приложения
1.обращение к ендпоинту, возвращающему hostname:
http://localhost:8080/api/v1/status
2. по запросу GET -> вывод таблицы product из БД:
http://localhost:8080/api/v1/products
3.по запросу GET -> вывод строки c id 1  из таблицы  product в БД:
http://localhost:8080/api/v1/products/1
4. приложение также через запросы DELETE и POST удалять по id и изменять параметры.
