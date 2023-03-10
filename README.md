# smartfara 
# Плата управления поворотниками/стоп-сигналами для мотоцикла Honda

<img src= "https://user-images.githubusercontent.com/93090351/220214213-8454c857-e380-4cd6-8bec-6d5210063901.JPG" alt="diagram" width="650"/>


#### Firmware for board "SmartFara T-01"

Плата имеет защиту от переполюсовки клемм АБ на входе; 
Цепи питания АБ и цепи питания MCU гальванически развязаны Ирбисом.
DC/DC преобразователь защищен самовостанавливающимся предохранителем.

###### Плата детектирует

- срабатывания концевика педали тормоза
- включения левого поворотника 
- включения правого поротника

Эти входы на схеме также оптически развязанны от цепей питания байка.

###### Плата по прерыванию выходит из спящего режима и запускает соответсвущ. ф-ю:

- стробирование стоп-сигнала
- бегущий огонь поворотников

Все светодиодные группы управляются LED-драйверами для защиты LED от экстреальных режимов работы (высокого тока, импульсов напряжения до 50В, температуры).  

###### DIP-переключатель на плате:

- устанавливает режим "строб. сигнал" стоп-огней либо непрерывный (switch 4);
- устанавливает режим (один и 8-ми) бегущего огня поворников (switch 1..3). 

###### На плате 6 контактных площадок для подключения:

 - светод. групп светодиодов стоп-сигнала и габаритов 
 - светод. групп лев. поворотника к LED-драйверам;
 - светод. групп прав. поворотника к LED-драйверам;
 - cигнала тормоза, сигналов поворотника
 - минуса АБ (-Ubat)  
 - плюса АБ  (+Ubat)
 
###### Представлены два файла:

 - [smartfara_13A_t01.c](./smartfara_13A_t01.c) (для AVR ATTiny 13A)
 - [smartfara_2313A_t01.c](./smartfara_2313A_t01.c) (для AVR ATTiny 2313A)
 
