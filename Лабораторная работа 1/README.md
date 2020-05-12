## Задание 1  
Проверяем что лежит в текущей директории.  
ls - она выводит имена файлов, лежащих в данной директории. Видим, что здесь имеется файл diary.txt.   
Выводим его содержимое на экран терминала при помощи команды cat.  
ZGFpejZhaFJhZVNhZXhhaWJ1YWYK 
## Задание 2  
cat ./* - отображение всей информации  
dGhlaWxpM2FoWm9odGFpM2VldzMK  
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/2.jpg)  
## Задание 3  
Так как кроме ls нет никаких команд, прочитал по строчно нужный файл в данной директории
while read $LINE; do echo $LINE; done <./-diary.txt-;
Y284ZWlxdXVlMmllTDNpZXBoNWUK
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/3.jpg)  
## Задание 14   
cd перемещение по каталогам
cd .. - на позицию вверх
d2FodmFoMWFlV2FpYmVlaG9vMmIK  
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/14.jpg)  
## Задание 15   
pwd (present working directory - текущий рабочий каталог)  
TWVlMXdvaDJ6YWVoZWoyamllNm8K  
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/15.jpg)  
## Задание 16  
id - показывает информацию о user'е  
ZXVsb29naG91MFBob2g4T2hkYWkK  
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/16.jpg)  
## Задание 17  
тут скрытый файл, поэтому прописать просто ls ничего не произойдет, поэтому нужно сделать через  
ls -a который выводит скрытые файлы  
bmVlNm1lMEhhaU11M2thaGVpNmEK  
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/17.jpg)  
## Задание 18  
man diary - вручную считывает  
Y2hpZWNoM2VpRzRJZWtlaXNlbGUK  
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/18.jpg)  
## Задание 19  
mkdir - создание директории  
mkdir -p - создание сразу нескольких вложенных    
cd - переходим в директории для создания следующей   
V2VpMGNvaHNoZWlxdWE0YWhnaG8K  
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/19.jpg)  
## Задание 20  
rm -R (рекурсивное удаление директории и всех вложенных директорий)  
YW1pZWhpaW0yb2h5NW9vRjZlaXcK  
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/20.jpg)  
## Задание 21  
1)rm *[0-9]*.txt  
2)rm *[a-z]*.png  
3)rm test-*.log (удаляем все не архивированные)  
ls  
aWU0b29XdWxlaXBodXBpZWZveW8K  
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/21.jpg)  
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/21_1.jpg)  
## Задание 22  
Использовал цикл и touch для создания файла  
dXI2dXNhaDNvaFQxaWV2MGNobzgK  
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/22.jpg)  
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/22_1.jpg)  
## Задание 23  
Использовали ls / cd и mv (для перемещения и изменения названия каталога/файла)  
dmVlc2VpQzVBb2dlaXI1cmVlM2YK  
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/23.jpg)  
## Задание 24  
Использовали ls, cd и cp -r (для копирования каталога)  
YWVnaG9venVvejd2b292OHNvaEwK    
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/24.jpg)  
## Задание 25  
Использовали ls и cat (выводи содержимого файла)  
dGhlZThhcXVpZUNpTGFpdGhlZTkK  
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/25.jpg)  
## Задание 26  
Использовали less для отображения содержимого файла по страницам  
После использовали /SECOND, /THIRD для поиска флага  
WWVpc2gxYWlndXVrZWl5ZWloaWUK  
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/26.jpg)  
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/26_1.jpg) 
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/26_2.jpg) 
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/26_3.jpg) 
## Задание 27  
Нужно использовать tail -f diary, но в данном задании баг  
dGVlMUtleThhUXVvaDFnZTFiaWkK  
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/27.jpg)  
![Картинка](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%201/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/27_1.jpg)  
## Задание 28  
Вставляем весь текст из 27 задания, кроме последней строчки.  
cat >diary <<end  
далее через echo -n '11:32pm: Нассал под кресло. Еееееееее!' >> diary  
ZWV4b1g1WnVkMm9oZnVjYWhkdTMK  
## Задание 29   
Нужно узнать историю, для этого нажимаем стрелочку вверх и ищем флаг.
