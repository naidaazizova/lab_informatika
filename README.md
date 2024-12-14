# Лабораторная работа по информатике
### Тема: Команда grep в Linux
## Введение
Команда grep (Global Regular Expression Print) используется для поиска текста в файлах с помощью регулярных выражений. Это мощный инструмент, который широко используется в системах Linux и Unix для фильтрации и анализа текстовой информации.

В рамках лабораторной работы мы будем изучать основные возможности команды grep, ее синтаксис и применение, а также выполнять практические задания. 

## Пример задания ( теоретическая база ) 
1. Создание тестового файла \
   Создаем текстовый файл ``employees.txt`` со следующим содержимым:

   ```
   James, 29, Web Developer
   Sophia, 33, Data Analyst
   Lucas, 25, Graphic Designer
   Olivia, 40, Full Stack Developer
   Liam, 31, Product Manager
   ```
2. Использование команды ``grep`` : 
   Найдем все строки, содержащие слово "Developer":

   ```
   grep "Developer" employees.txt
   ```
   Результат:

   ```
   James, 29, Web Developer
   Olivia, 40, Full Stack Developer
   ```
   Найдем все строки, содержащие слово "manager", игнорируя регистр: 

   ```
   grep -i "manager" employees.txt
   ```
   Результат:

   ```
   Liam, 31, Product Manager
   ```
   Отобразим строки, не содержащие слово "Analyst":

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
   Найдем строки, которые содержат либо "Developer", либо "Manager":

   ```
   grep -E "(Developer|Manager)" employees.txt
   ```
   Результат:
   ```
   James, 29, Web Developer
   Olivia, 40, Full Stack Developer
   Liam, 31, Product Manager
   ```

## Задание





   


   





