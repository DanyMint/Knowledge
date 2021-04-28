# Ubuntu linux

История, настройка и разные команды

## Смена тайм зоны:

~~~bash
sudo dpkg-reconfigure tzdata
~~~



## Смена размера шрифта в консоли:

~~~bash
sudo dpkg-reconfigure console-setup
~~~

Здесь нужно выбрать UTF-8,  Termius а потом размер. Так консоль выглядит приятнее.



## Archives ERROR

Часто выскакивала ошибка Unable fetch to come archives 

Решается она часто так:

~~~ bash
sudo apt clear && sudo apt-get clear
~~~

Она возникает достаточно часто. Особенно при установке i3. 