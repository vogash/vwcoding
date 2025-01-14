# Приборная панель

### Тест стрелок при включении зажигания 
При включении зажигания стрелки тахометра и спидометра совершают ход от минимального до максимального положения.   
Функционал никакой, зато смотрится эффектно!   
```
17 блок → адаптация → 
> канал «indicator_celebration» → выбираем «active» → выполнить 
```
 
### Показ свободного месте в бензобаке в литрах 
Остаток места в баке – приблизительное значение литров, которые можно залить в бак. Шаг шкалы – 5 литров.   
При полностью заправленном баке отображается «---». Показания приблизительные и могут варьироваться ±10 л.
```
17 блок → адаптация → 
> канал «Volume to be replenished» → выставить значение «yes» → выполнить 
```
 
### Отключение звукового сигнала и индикации о не пристегнутом ремне 
По умолчанию на некоторых автомобилях включен контроль ремня водителя и переднего пассажира.   
Если кто любит кататься без ремня безопасности, эту функцию можно отключить. 
```
17 блок → кодирование → длинное кодирование → 
> 1 Байт → 1 бит → выключить 
```
 
### Корректировка показаний спидометра 
В соответствии с нормами безопасности показания спидометра слегка завышены относительно реальной скорости.   
Для разных автомобилей предусмотрены различные уровни завышения показаний.   
Число импульсов от Skoda Octavia (01) завышает показание при 100 км/ч ≈ на 8 км/ч, от Skoda Fabia (02) ≈ на 15 км/ч.   
Самое точное показание на колёсах размерности 215/65 R16 при установке числа импульсов от VW Golf (07).   
```
17 блок → кодирование → длинное кодирование → 
> 0 Байт → 0-3 бит → 07 Distance Impulse Number 7 
```
 
### Корректировка показаний уровня топлива 
Датчик уровня топлива в баке имеет погрешность, из-за чего неточность в показаниях может достигать ±10 л. 
```
17 блок → адаптация → 
> канал "Display correction of fuel gauge" → подбираем значение (от -10 до 10) → выполнить 
```

Чтобы скорректировать показания, нужно точно знать, сколько бензина в баке или дождаться загорания лампочки.  
Ёмкость бака – 64 л, цена деления – 4 л. Контрольная лампа низкого уровня топлива загорается при остатке 7 л в баке. 
 
 