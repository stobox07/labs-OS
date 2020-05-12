# Лабораторная работа № 2  
В ходе выполенения лабораторной работы было использовано следующее:  
| Параметр  | Значение  | Количество |
| ------------ | ------------ | ---- |
| Операционная система | Debian 10.3 | 1 |
| SSD  | 8/10 gb | 2/2 соотв.|
| HDD | 16 gb | 2|
| SATA контроллер | - | 4 порта  |

## Часть первая  
Здесь мы устанавливаем и настраиваем операционную систему(debian 10.3.0).Занимаемся настройкой LVM, RAID.  
![1](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/1.png "1")  
Настроили RAID.  
![2](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/2.png "2")  
Настроили LVM.  
![3](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/3.png "3")  
Разметили и выбрали соответствующие точки монтирования.  
![4](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/4.png "4")  
Информация о дисках после копирования /boot с sda на sdb и установки grub.  
Команда lsblk показала нам 2 диска на 8G и сопутствующую информацию.  
![5](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/5.png "5")  
Информация о текущем RAID с помощью команды cat /proc/mdstat. Здесь мы увидели активный RAID1 на sda2 и sdb2.
![6](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/6.png "6")  
После выполнения задания 1 у нас появилась виртуальная машина с дисками ssd1, ssd2, а также настроенный RAID и LVM.  
  
## Часть вторая  
Нам требуется восстановить работу диска, который вышел из строя.  
![7](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/10.png "lsbk")  

Как мы видим, у нас всего лишь один диск, вместо двух.  
А вот что показывает cat /proc/mdstat после перезагрузки.  
![8](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/12.png "raid info")  
  
Создаем в нашей виртуальной машине новый диск и называем его, как сказано в задании, ssd3 <br>
  
![9](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/13.png "VM")  
  
С помощью команды ``fdisk -l`` убедились, что диск был успешно добавлен.  

![10](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/14.png "fdisk")  
  
Cкопировали таблицу разделов со старого диска на новый с помощью ``sfdisk -d /dev/sda | sfdisk /dev/sdb``  
и добавили raid в sdb2 c помощью команды ``mdadm --manage /dev/md0 --add /dev/sdb2``  

![11](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/15.png "copy table")  
Скопировали /boot, установили grup и выполнили перезагрузку виртуальной машины.  
В итоге все было успешно восстановлено.  
![12](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/17.png "finish task 2")  

## Часть Третья  
После отказа диска.  
Состояние RAID-массива и дисков после отказа еще одного диска.  
![13](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/17.png)  	
Состояние дисков после добавления нового ssd4 на 10GB.  
 ![14](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/20.png)  
Скопировали файловую таблицу со старого диска на новый.  
 ![15](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/22.png)  
Информация о RAID и дисках после создания нового RAID-массива, установки grub, перемонтировки /boot и копирования данных на новый диск.  
![16](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/27.png)  
Информация о дисках и физических томах после создания нового физического тома.  
![17](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/28.png)  
Информация о физических томах после увеличения размера Volume Group system.  
 ![18](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/29.png)  
Информация о системе после перемещения данных со старого диска на новый.  
 ![19](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/32.png)  
Окончательная информация о дисках после удаления старого диска из группы system.  
![20](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/32.png)  
Состояние дисков после добавлнения одного нового ssd на 10GB и двух hdd на 16GB.  
![21](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/35.png)  
Состояние дисков после копирования таблицы разделов на новый диск.  
 ![22](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/37.png)    
Информация о дисках после копирования /boot, установки grub, и изменения размера второго раздела диска sde.  
![23](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/40.png)  
Информация о дисках после добавления нового диска к RAID-массиву и расширения массива до 2-х дисков.  
![24](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/41.png)  
Информация о дисках после увеличения размера раздела на sdb.  
![25](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/43.png)  
Информация о дисках после расширения размера RAID.  
 ![26](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/44.png)  
Информация о размерах vg root, var, log до и после их увеличения.  
![27](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/46.png)  
Информация о дисках после создания нового RAID-массива, нового PV и группы, а также нового логического тома и отформатирования раздела в ext4.  
![28](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/49.png)  
Информация о дисках после переноса данных логов со старого раздела на новый.  
![29](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/54.png)  
Информация о дисках после перезагрузки.  
 Исправили файл /etc/fstab.  
 ![30](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/55.png)  
Информация о дисках и RAID-массивах после перезгарузки.  
![31](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/57.png)  
Все остальные скриншоты каждого действия находятся в папке screens.  
 ![32](https://raw.githubusercontent.com/stobox07/labs-OS/master/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%202/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/58.png)  
