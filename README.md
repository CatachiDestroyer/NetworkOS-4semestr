# NetworkOS-4semestr
## Лекционные материалы
Репозиторий создан с целью практической реализации некоторых программ, разбираемых на лекциях в течение учебного семестра.

Оглавление:

Операционные системы, подходящие для установки и запуска программ:
- GNU/Linux.

Программные коды, которые находятся в папках с лекциями, можно скомпилировать с помощью make-файла или использовать компилятор gcc. Используя ручную компиляцию, необходимо перейти в папку с программным кодом и вызвать компилятор, написав команду `gcc program_filename.c -o executable_filename.out`. Однако рекомендуется пользоваться Makefile'ом, где все шаги уже предусмотрены. Для того, чтобы использовать make-файл необходимо находиться в корневой папке репозитория.

Структура Makefile:
- all
  - Lec2_Lec3_1
  - Lec2_Lec3_2
  - Lec2_Lec3_3
  - Lec4_1
  - Lec4_2
  - Lec4_3

## Обзор программ и результов их работы
___
## Лекции 2-3
#### <a name="Program_№1">Program №1</a>  
Пример программы динамического выделения памяти для массива.

Программа запрашивает длину массива. Затем выделяется память с помощью функции malloc. При выделении памяти возвращается указатель, который будет равен NULL, если память не выделилась. Если массив инициализирован, то выделенная память осовобождается.  

Тестирование 1 
```
Enter length of array: 1  
All fine 
```
Тестирование 2 
```
Enter length of array: -10  
Error: can't allocate memory 
```
___ 
#### <a name="Program_№2">Program №2</a>  
Пример программы для чтения данных из файла.  

В начале выделяем память для массива чаров с помощью функции calloc. Затем создаем дескриптор и открываем файл для чтения, если файла не будет, то он будет создан. Выводим значение дескриптора файла. После читаем из файла 10 байт и записываем в переменную sz количество байт, которое удалось прочитать. Далее обязательно записываем в конец массива, в который записывали прочитанную информацию, символ конца строки (терминальный ноль). В конце программы закрываем файл.  

Тестирование 
```
fd = 3  
called read( 3, c, 10). returned that 0 bytes were read.  
closed the fd.  
```
___
