#  приложение microservices-pack

## Описание

microservices-pack    представляет  из себя 
набор приложений, которые предоставляют микросервисы и объединены в виртуальное “облако” (cloud) – таким образом работают как единое приложение.

Модули в приложении могут:
* работать и вызываться независимо друг от друга (если один сервис “упадет”, остальные будут работать)
* вызывать друг друга при необходимости
* быть частью бoльшего функционала
* ничего не знать о других микросервисах

## Модуль  Eureka Server
Модуль, который представляет из себя контейнер для регистрации и публикации микросервисов.


## Модуль Api Gateway
API Gateway (AG) является шлюзом, который обрабатывает входящие запросы и “перекидывает” их на нужный мс (с логированием, кешированием, безопасностью
и тд.

## Модуль Spring Cloud Config
Основная цель – вынести файлы настроек (например, *.properties) из приложения в облако и хранить их отдельно от приложений.
Можно использовать одни и те же настройки для определенных приложений (чем дублировать в файле properties их внутри самого приложения)
Тем самым достигается гибкость – можно изменять настройки без перезапуска микросервисов

## Модуль zoo

 Модуль zoo хранит в себе два  реактивных микросервиса, которые общаются между собой, используя технологии Spring cloud. 
