# Лабораторная работа по информатике
### Тема: Команда grep в Linux
## Введение
Команда ``grep (Global Regular Expression Print)`` используется для поиска текста в файлах с помощью регулярных выражений. Это мощный инструмент, который широко используется в системах Linux и Unix для фильтрации и анализа текстовой информации.

В рамках лабораторной работы мы будем изучать основные возможности команды grep, ее синтаксис и применение, а также выполнять практические задания. 

## Задание, разобранное по шагам ( теоретическая база ) 
1. Создание тестового файла \
   Создаем текстовый файл ``employees.txt`` со следующим содержимым:

   ```
   James, 29, Web Developer
   Sophia, 33, Data Analyst
   Lucas, 25, Graphic Designer
   Olivia, 40, Full Stack Developer
   Liam, 31, Product Manager
   ```
2. Использование команды ``grep`` : \
   Найдем все строки, содержащие слово ``Developer``:

   ```
   grep "Developer" employees.txt
   ```
   Результат:

   ```
   James, 29, Web Developer
   Olivia, 40, Full Stack Developer
   ```
   Найдем все строки, содержащие слово ``manager``, игнорируя регистр: 

   ```
   grep -i "manager" employees.txt
   ```
   Результат:

   ```
   Liam, 31, Product Manager
   ```
   Отобразим строки, не содержащие слово ``Analyst``:

   ```
   grep -v "Analyst" employees.txt
   ```
   Результат:
   
   ```
   James, 29, Web Developer
   Lucas, 25, Graphic Designer
   Olivia, 40, Full Stack Developer
   Liam, 31, Product Manager
   ```
   Найдем все строки, где возраст больше или равен 30:

   ```
   grep -E "\b[3-9][0-9]\b" employees.txt
   ```
   Результат:
   ```
   Sophia, 33, Data Analyst
   Olivia, 40, Full Stack Developer
   Liam, 31, Product Manager
   ```
   Найдем строки, которые содержат либо ``Developer``, либо ``Manager``:

   ```
   grep -E "(Developer|Manager)" employees.txt
   ```
   Результат:
   ```
   James, 29, Web Developer
   Olivia, 40, Full Stack Developer
   Liam, 31, Product Manager
   ```

## Практические задания 
#### 1 - Работа с датами и временными метками
1. Создайте лог-файл с датами и событиями, например:

   ```
   2024-12-01 12:30:45 ERROR user1 login failed
   2024-12-01 12:31:00 INFO user1 login successful
   2024-12-01 12:36:30 ERROR user2 login failed
   2024-12-01 12:40:00 INFO user2 login successful
   ```
2. Найдите все строки с ошибками `ERROR`
3. Найдите все события, произошедшие в интервале между ``12:30`` и ``12:35``

#### 2 - Анализ логов веб-сервера с использованием grep и регулярных выражений
1. Сначала создайте файл server_logs.txt с примерными данными:

   ```
   192.168.1.1 - - [12/Dec/2024:10:01:23 +0000] "GET /index.html HTTP/1.1" 200 532
   192.168.1.2 - - [12/Dec/2024:10:01:55 +0000] "GET /about.html HTTP/1.1" 404 1024
   192.168.1.3 - - [12/Dec/2024:10:02:10 +0000] "POST /login HTTP/1.1" 500 2048
   192.168.1.1 - - [12/Dec/2024:10:02:45 +0000] "GET /contact.html HTTP/1.1" 200 512
   192.168.1.4 - - [12/Dec/2024:10:03:05 +0000] "GET /index.html HTTP/1.1" 200 532
   192.168.1.1 - - [12/Dec/2024:10:03:22 +0000] "GET /notfound.html HTTP/1.1" 404 1024
   192.168.1.5 - - [12/Dec/2024:10:04:30 +0000] "POST /login HTTP/1.1" 500 2048
   192.168.1.2 - - [12/Dec/2024:10:06:12 +0000] "GET /index.html HTTP/1.1" 200 532
   192.168.1.1 - - [12/Dec/2024:10:06:45 +0000] "GET /index.html HTTP/1.1" 200 532
   ```
3. Найдите все запросы от IP-адреса ``192.168.1.1`` \
4. Подсчитайте количество строк с ошибками ``404`` и ``500`` и выведите эти запросы \
5. Извлечьте только IP-адреса, игнорируя остальные части строки (время, запросы и коды ошибок) \
6. Найдите все запросы, сделанные в промежутке между ``10:00`` и ``10:05`` (включая только код ошибки ``404``) \
7. Подсчитайте количество уникальных IP-адресов, которые сделали GET-запросы на страницы ``.html``

## Как успешно сдать работу?

Создайте свой репозиторий из этого шаблона. Как это делается - ``Use this template -> Create a new repository`` и сделайте его ``public``. 

Находясь уже в своем репозитории - создайте новый файл формата ``.md`` и там оформляйте отчет. В отчете опишите все шаги и приложите скриншоты, которые вы делали, чтобы получить финальный результат работы.

## Что вам нужно знать, чтобы успешно защитить работу?
Как работает команда ``grep`` и что она делает на практике? 

Что такое регулярные выражения и как они помогают улучшить поиск с помощью ``grep``? 

В каких реальных сценариях и для каких типов задач можно использовать ``grep``?

## Источники
1. Официальная документация ``grep``: https://man7.org/linux/man-pages/man1/grep.1.html

2. https://regexr.com/ - онлайн-инструмент для тестирования регулярных выражений с подсказками. 

3. https://regex101.com/ - отличный ресурс для проверки регулярных выражений с пояснениями.
   
4. Книга "Mastering Regular Expressions" Дж. Э. Фримана (вы можете найти ее онлайн для изучения регулярных выражений в контексте различных языков программирования).





   


   





