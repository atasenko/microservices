### Задание 1. Обеспечить разработку  
Предлагаю использовать GitLab. Он соответствует всем необходимым условиям:  
- есть облачная версия (или локальная если по каким-то причинам данные нужно держать на своем оборудовании)  
- система контроля версий Git  
- репозиторий на каждый сервис  
- доступен запуск сборки по по событию из VCS или вручную, кнопкой с указанием параметров  
- возможность настройки каждой сборки  
- создание шаблонов для конфигураций сборок  
- безопасное хранение секретных данных в защищенных переменных  
- наличие нескольких конфигураций для сборки из одного репозитория  
- возможность писать кастомные шаги для сборки  
- выбор собственных докер-образов для сборки проектов  
- возможность использования общих облачных "раннеров"(агентов) или развернуть свои на локальных серверах  
- параллельный запуск нескольких сборок и тестов

### Задание 2. Логи  
Предлагаю использовать связку Vector, ClickHouse, Graylog.  
Vector позволяет собирать и модицифировать при необходимости логи с большого количества хостов с минимальными системными требованиями. Поддерживает работу по TCP, что гарантирует надежную доставку в отличие от UDP.  
ClickHouse обеспечивает долговременное хранение с хорошим сжатием позволяя экономить место в сравнении с Logstash, например.  
Graylog обеспечивает поиск, фильтрацию, сохранение и загрузку параметров поиска. Доступ к пользовательскому интерфейсу можно удобно организовать и автоматизировать используя встроенный функционал групп и возможности LDAP/AD.  

### Задание 3. Мониторинг  
В качестве сервиса для сбора, хранения и визуализации метрик предлагаю использовать Prometheus, InfluxDb, Grafana.  
Prometheus позволяет собирать метрики состояния ресурсов для хостов и сервисов на них работающих.  
InfluxDb хранит, а Grafana предоставляет пользовательский интерфейс с возможностью делать запросы, агрегировать информацию и настраивать различные дашборды для отслеживания состояния системы.  
