Battery stats module.

##Changelog:
##v5.0.1: RU🇷🇺 : Обычный багфикс, ничего нового.
EN🇬🇧 : small bugfix, Nothing new 

##v5.0.0: RU🇷🇺 : В этой версии очень много изменений, итак, во первых больше нет выбора bms или battery, данные подтягиваются с двух мест одновременно. Из основного и самого важного: модуль теперь поддерживает устройства со старым андроидом (тестировано на Android 6-9) при поддержке rtr456304(rtr456304 сделал модуль для старых устройств на основе этого модуля, за что ему большое спасибо), но главное не ставить версию для старых устройств имея новое устройство, ибо можно получить невозможный запуск системы. Выбор типа устройства осуществляется при установке модуля, изначально советую выбирать new/modern, если не будет работать или явно врать, то пробуйте вариант для старых устройств.

EN🇬🇧 : There are a lot of changes in this version, so, first of all, there is no more choice of bms or battery, data is pulled from two places at the same time. From the main and most important: the module now supports devices with old android (tested on Android 6-9) with the support of rtr456304 (rtr456304 made a module for old devices on the basis of this module, for what he thanks a lot), but the main thing is not to put the version for old devices having a new device, because you can get an impossible start of the system. The choice of device type is made when installing the module, initially I advise you to choose new/modern, if it will not work or obviously lie, then try the version for old devices.


##v4.4.1: Ru🇷🇺: Изменен формат лога состояния акб, теперь он пишет не только здоровье, но и дату изменения здоровья, время(вплоть до секунд) и температуру в момент изменения здоровья
EN🇬🇧: The format of the battery status log has been changed, now it writes not only health, but also the date of health change, time (up to seconds) and temperature at the time of health change

##v4.4.0: Ru🇷🇺: Теперь модуль пишет лог о состоянии батареи для того чтобы вы могли следить за изменениями состояния, лог сохраняется в /data/adb/modules/battery_stats, важно учесть что лог обновляется только при изменении состояния здоровья батареи, тоесть просто так лоо перезаписываться не будет. Также теперь существует система ошибок, тоесть например если у вас не отображается какая то статистика, то модуль запишет проблему в лог файл (лог находится в /data/adb/modules/battery_stats/) который вы сможете дать мне для исправления вашей проблемы, в описание и action также будет сообщение об ошибке, но доступные файлы продолжать отображаться, при ошибке также будет выведен текст что есть проблемы в описание модуля. Также при установке вы не сможете выбрать несуществующий путь, вам просто выдаст ошибку установки и скрипт перестанет работать(ниже предоставлю пример)

En🇬🇧: Now the module writes a log about the state of the battery so that you can keep track of changes in the state, the log is saved in /data/adb/modules/battery_stats, it is important to note that the log is updated only when the state of health of the battery, ie just so loo will not be overwritten. Also now there is a system of errors, that is, for example, if you do not display some statistics, the module will record the problem in a log file (the log is located in /data/adb/modules/battery_stats/), which you can give me to fix your problem, in the description and action will also be a message about the error, but the available files will continue to be displayed, when the error will also display the text that there are problems in the description of the module. Also when installing you will not be able to select a path that does not exist, you will just get an installation error and the script will stop working (I will provide an example below).


##v4.3.9: RUru Ничего нового, перенос и востановление репозитория
EN: Nothing new: repository migration and restoration.


##v4.3.8: RU🇷🇺 : Вся логика, расчёты и прочее перенесено в lib.sh, из за чего вес файла стал меньше почти в 2 раза. Теперь подсчет времени с зарядки хранится не temp, а в папке самого модуля. /|\ EN🇬🇧 : All logic, calculations, and other things have been transferred to lib.sh, which is why the file weight has become almost 2 times less. Now the charging time is stored not temp, but in the folder of the module itself.


##v4.2.0: RU🇷🇺 : наконец-то Добавлено 2 пути, sys/class/power_supply/battery и sys/class/power_supply/bms, выбор осуществляется при установке, если выбрали не то и все значения по нулям то переустаровите модуль выбрав другой путь, также теперь если нет данных, то описание не ломается, а ставит нули там где не видит информации.
EN🇬🇧 : Finally, 2 paths have been added, sys/class/power_supply/battery and sys/class/power_supply/bms, the choice is made during installation, if you selected the wrong thing and all the values are zero, then re-outdate the module by choosing another path, also now if there is no data, then the description does not break, but puts zeros where it does not see the information.


##v4.1.3: Исправлен баг с отображением времени с последней зарядки
Fixed a bug with displaying the time since the last charge
