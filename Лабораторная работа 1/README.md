## Задание 1  
Проверяем что лежит в текущей директории.  
ls - она выводит имена файлов, лежащих в данной директории. Видим, что здесь имеется файл diary.txt.   
Выводим его содержимое на экран терминала при помощи команды cat.  
ZGFpejZhaFJhZVNhZXhhaWJ1YWYK  
## Задание 2  
cat ./* - отображение всей информации  
dGhlaWxpM2FoWm9odGFpM2VldzMK  
## Задание 3  
Так как кроме ls нет никаких команд, прочитал по строчно нужный файл в данной директории
while read $LINE; do echo $LINE; done <./-diary.txt-;
Y284ZWlxdXVlMmllTDNpZXBoNWUK
## Задание 14   
cd перемещение по каталогам
cd .. - на позицию вверх
d2FodmFoMWFlV2FpYmVlaG9vMmIK
## Задание 15   
pwd (present working directory - текущий рабочий каталог)  
TWVlMXdvaDJ6YWVoZWoyamllNm8K  
## Задание 16  
id - показывает информацию о user'е  
ZXVsb29naG91MFBob2g4T2hkYWkK  
## Задание 17  
тут скрытый файл, поэтому прописать просто ls ничего не произойдет, поэтому нужно сделать через  
ls -a который выводит скрытые файлы  
bmVlNm1lMEhhaU11M2thaGVpNmEK  
## Задание 18  
man diary - вручную считывает  
Y2hpZWNoM2VpRzRJZWtlaXNlbGUK  
## Задание 19  
mkdir - создание директории  
mkdir -p - создание сразу нескольких вложенных    
cd - переходим в директории для создания следующей  
K3kzZUJWMHUvZHFqRnlUZ2NpZ3V2SkZYWjl2ZUl5SElpZkZ3NG0wQmpVST0K  
  
V2VpMGNvaHNoZWlxdWE0YWhnaG8K - верный  
## Задание 20  
rm -R (рекурсивное удаление директории и всех вложенных директорий)  
YW1pZWhpaW0yb2h5NW9vRjZlaXcK  
## Задание 21  
1)rm *[0-9]*.txt  
2)rm *[a-z]*.png  
3)rm test-*.log (удаляем все не архивированные)  
ls  
aWU0b29XdWxlaXBodXBpZWZveW8K  
## Задание 22  
Использовал цикл и touch для создания файла  
dXI2dXNhaDNvaFQxaWV2MGNobzgK  
## Задание 23  
Использовали ls / cd и mv (для перемещения и изменения названия каталога/файла)  
dmVlc2VpQzVBb2dlaXI1cmVlM2YK  
## Задание 24  
Использовали ls, cd и cp -r (для копирования каталога)  
YWVnaG9venVvejd2b292OHNvaEwK    
## Задание 25  
Использовали ls и cat (выводи содержимого файла)  
dGhlZThhcXVpZUNpTGFpdGhlZTkK  
## Задание 26  
Использовали less для отображения содержимого файла по страницам  
После использовали /SECOND, /THIRD для поиска флага  
WWVpc2gxYWlndXVrZWl5ZWloaWUK  
## Задание 27  
Нужно использовать tail -f diary, но в данном задании баг  
dGVlMUtleThhUXVvaDFnZTFiaWkK  
## Задание 28  
Вставляем весь текст из 27 задания, кроме последней строчки.  
cat >diary <<end  
далее через echo -n '11:32pm: Нассал под кресло. Еееееееее!' >> diary  
ZWV4b1g1WnVkMm9oZnVjYWhkdTMK  
## Задание 29   
Нужно узнать историю, для этого нажимаем стрелочку вверх и ищем флаг.
