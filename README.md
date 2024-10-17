# Лабораторная работа 2

В данной лабораторной работе требуется написать скрипт, который на вход принимает IPv4-адрес в десятичном формате, а на выходе обеспечивает данный IP-адрес в двоичном формате.

##Ход работы

Для выполнения задания я совершила следующие действия:

1. Создала новый файл под названием `info_lab2.bash` и написала скрипт для перевода IP-адрес в бинарную систему:

   ![image](https://github.com/user-attachments/assets/deac1224-98ad-4867-808b-b651a4a574d6)
   
2. Сам скрипт имеет такой вид:
   
![image](https://github.com/user-attachments/assets/6d71b3b2-c57d-4e7e-8fe7-d5bd3178644e)

Рассмотрим его поподробнее.
1. Для ввода данных используется `read`, чтобы соответсвовать примеру входа данных. Я решила написать цикл, с помощью которого будет перебираться каждый байт IP-адреса, после чего будет записываться в строку `ip`, которая и будет является выходными данными.
2. Для перевода байта из десятичной системы в двоичную я использую массив `bin`. В нем 8 символов так как каждый байт IP-адреса имеет 8 битов (0 или 1 соответственно). В данной записи создается массив, в котором перебираются все двоичные числа в десятичном значении от 0 по 255, т.е.: `00000000 00000001 00000010 ... 11111101 11111110 11111111`. Таким образом, указав заданное байтом десятичное число как индекс в данном массиве, мы получим его соответсвтующее значение в двоичной системе счисления.
3. Далее я делаю вывод данных (`|`, то же что и стандартный вывод) из переменной `ip1` в команду `tr` (truncate), которая заменяет все точки в записи IP-адреса на пробелы и создает массив, состоящий из байтов IP-адреса.
4. После этого, я запускаю цикл `for`, который перебирает каждый из эдементов массива `ip_bytes`. Внутри цикла к пустой строке `ip` добавляется элемент из массива bin, найденный по индексу. Таким образом составляется бинарная запись IP-адреса.
5. После выполнения цикла я вывожу результат, сделав срез первого символа `:1` (так как он является точкой).
6. Готово! IP-адрес теперь представлен в двоичной форме записи.

![image](https://github.com/user-attachments/assets/b1a69581-1800-491b-875e-11e8b3ea20ab)

##Вывод

Для выполнения этой лабораторной работы мне пришлось изучить массивы и циклы. Также я изучила функции и действия с правами доступа, но если они не были задействованы в выполнении задания лабораторной работы. Я получила опыт работы с циклами и массивами, закрепила знания о пременных. 
