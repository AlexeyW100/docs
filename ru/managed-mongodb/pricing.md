---
editable: false
---

# Правила тарификации для [!KEYREF MG]

[!INCLUDE [currency-choice](../_includes/pricing/currency-choice.md)]

## Из чего складывается стоимость использования [!KEYREF mmg-short-name] {#rules}

Расчет стоимости использования [!KEYREF mmg-name] учитывает:

* тип и объем хранилища (дискового пространства);

* [класс хостов](concepts/instance-types.md), выбранный для кластера;

* количество хостов БД в кластерах;

* настройки и количество резервных копий;

* объем исходящего трафика.


[!INCLUDE [pricing-gb-size](../_includes/pricing-gb-size.md)]

### Использование хостов БД {#rules-hosts-uptime}

Стоимость начисляется за каждый час работы хоста в соответствии с его классом. Точные характеристики классов приведены в разделе [[!TITLE]](concepts/instance-types.md).

Минимальная единица тарификации — час (например, стоимость 1,5 часов работы хоста равна стоимости 2 часов). Время, когда хост [!KEYREF MG] не может выполнять свои основные функции, не тарифицируется.

### Использование дискового пространства {#rules-storage}

Оплачивается:

* Объем хранилища, выделенный для кластеров БД.

    * Хранилище на быстрых локальных дисках (NVMe) можно заказывать только для кластеров более чем с 3 хостами, с шагом 100 ГБ.


* Объем, занимаемый резервными копиями баз данных сверх заданного хранилища для кластера.

    * Хранение резервных копий не тарифицируется пока сумма размера БД и всех резервных копий остается меньше выбранного объема хранилища.

    * При автоматическом резервном копировании [!KEYREF mmg-short-name] не создает новую копию, а сохраняет изменения БД по сравнению с предыдущей копией. Поэтому потребление хранилища автоматическими резервными копиями растет только пропорционально объему изменений.

    * Количество хостов кластера не влияет на объем хранилища и, соответственно, на бесплатный объем резервных копий.



Цена указывается за 1 месяц использования.  Минимальная единица тарификации — ГБ в час (например, стоимость хранения 1 ГБ в течение 1,5 часов равна стоимости хранения в течение 2 часов).

## Цены {#prices}

### Хосты MongoDB {#prices-mongodb-hosts}

---

**[!TAB За месяц работы хоста]**

Класс хостов | Цена за месяц, вкл. НДС 
----- | ----- 
| **Intel Broadwell** |  |
[!KEYREF b1.nano]| 775 ₽
[!KEYREF b1.micro] | 1 138 ₽
[!KEYREF b1.medium] | 2 124 ₽
[!KEYREF m1.micro] | 7 221 ₽
[!KEYREF m1.small] | 14 442 ₽
[!KEYREF m1.medium]| 21 662 ₽
[!KEYREF m1.large] | 28 883 ₽
[!KEYREF m1.xlarge] | 43 324 ₽
[!KEYREF m1.2xlarge] | 57 765 ₽
[!KEYREF m1.3xlarge] | 86 648 ₽
[!KEYREF m1.4xlarge] | 115 531 ₽
[!KEYREF s1.nano]| 2 160 ₽
[!KEYREF s1.micro] | 4 327 ₽
[!KEYREF s1.small] | 8 647 ₽
[!KEYREF s1.medium] | 17 302 ₽
[!KEYREF s1.large] | 34 597 ₽
[!KEYREF s1.xlarge] | 69 201 ₽
**Intel Cascade Lake** | | 
[!KEYREF b2.nano]| 775 ₽
[!KEYREF b2.micro] | 1 138 ₽
[!KEYREF b2.medium] | 2 124 ₽
[!KEYREF m2.micro] | 7 221 ₽
[!KEYREF m2.small] | 14 442 ₽
[!KEYREF m2.medium]| 21 662 ₽
[!KEYREF m2.large] | 28 883 ₽
[!KEYREF m2.xlarge] | 43 324 ₽
[!KEYREF m2.2xlarge] | 57 765 ₽
[!KEYREF m2.3xlarge] | 86 648 ₽
[!KEYREF m2.4xlarge] | 115 531 ₽
[!KEYREF m2.5xlarge] | 144 413 ₽
[!KEYREF m2.6xlarge] | 173 296 ₽
[!KEYREF s2.micro] | 4 327 ₽
[!KEYREF s2.small] | 8 647 ₽
[!KEYREF s2.medium] | 17 302 ₽
[!KEYREF s2.large] | 26 095 ₽
[!KEYREF s2.xlarge] | 34 597 ₽
[!KEYREF s2.2xlarge] | 52 192 ₽
[!KEYREF s2.3xlarge] | 69 201 ₽
[!KEYREF s2.4xlarge]| 86 986 ₽
[!KEYREF s2.5xlarge]| 104 382 ₽

**[!TAB За 1 час работы хоста]**

Класс хостов | Цена за час, вкл. НДС 
----- | ----- 
| **Intel Broadwell** | 
[!KEYREF b1.nano]| 1,0770 ₽
[!KEYREF b1.micro] | 1,5800 ₽
[!KEYREF b1.medium] | 2,9500 ₽
[!KEYREF m1.micro] | 10,0296 ₽
[!KEYREF m1.small] | 20,0580 ₽
[!KEYREF m1.medium]| 30,0864 ₽
[!KEYREF m1.large] | 40,1148 ₽
[!KEYREF m1.xlarge] | 60,1728 ₽
[!KEYREF m1.2xlarge] | 80,2296 ₽
[!KEYREF m1.3xlarge] | 120,3444 ₽
[!KEYREF m1.4xlarge] | 160,4592 ₽
[!KEYREF s1.nano] | 3,0000 ₽ | 
[!KEYREF s1.micro] | 6,0102 ₽ | 
[!KEYREF s1.small] | 12,0102 ₽ | 
[!KEYREF s1.medium] | 24,0305 ₽ | 
[!KEYREF s1.large] | 48,0508 ₽ | 
[!KEYREF s1.xlarge] | 96,1119 ₽ 
**Intel Cascade Lake** |  
[!KEYREF b2.nano]| 1,0770 ₽
[!KEYREF b2.small] | 1,5800 ₽
[!KEYREF b2.medium] | 2,9500 ₽
[!KEYREF m2.micro] | 10,0296 ₽
[!KEYREF m2.small] | 20,0580 ₽
[!KEYREF m2.medium]| 30,0864 ₽
[!KEYREF m2.large] | 40,1148 ₽
[!KEYREF m2.xlarge] | 60,1728 ₽
[!KEYREF m2.2xlarge] | 80,2296 ₽
[!KEYREF m2.3xlarge] | 120,3444 ₽
[!KEYREF m2.4xlarge] | 160,4592 ₽
[!KEYREF m2.5xlarge] | 200,5740 ₽
[!KEYREF m2.6xlarge] | 240,6888 ₽
[!KEYREF s2.micro] | 6,0102 ₽
[!KEYREF s2.small] | 12,0102 ₽
[!KEYREF s2.medium] | 24,0305 ₽
[!KEYREF s2.large] | 36,2436 ₽
[!KEYREF s2.xlarge] | 48,0508 ₽
[!KEYREF s2.2xlarge] | 72,4884 ₽
[!KEYREF s2.3xlarge] | 96,1119 ₽
[!KEYREF s2.4xlarge]| 120,8136 ₽
[!KEYREF s2.5xlarge]| 144,9756 ₽

---


### Хосты mongocfg {#prices-mongocfg-hosts}

---

**[!TAB За месяц работы хоста]**

Класс хостов | Цена за месяц, вкл. НДС 
----- | ----- 
| **Intel Broadwell** |  |
[!KEYREF b1.nano]| 775 ₽
[!KEYREF b1.micro] | 1 138 ₽
[!KEYREF b1.medium] | 2 124 ₽
[!KEYREF s1.nano]| 2 160 ₽
[!KEYREF s1.micro] | 4 327 ₽
[!KEYREF s1.small] | 8 647 ₽
[!KEYREF s1.medium] | 17 302 ₽
[!KEYREF s1.large] | 34 597 ₽
[!KEYREF s1.xlarge] | 69 201 ₽
**Intel Cascade Lake** | | 
[!KEYREF b2.nano]| 775 ₽
[!KEYREF b2.micro] | 1 138 ₽
[!KEYREF b2.medium] | 2 124 ₽
[!KEYREF s2.micro] | 4 327 ₽
[!KEYREF s2.small] | 8 647 ₽
[!KEYREF s2.medium] | 17 302 ₽
[!KEYREF s2.large] | 26 095 ₽
[!KEYREF s2.xlarge] | 34 597 ₽
[!KEYREF s2.2xlarge] | 52 192 ₽
[!KEYREF s2.3xlarge] | 69 201 ₽
[!KEYREF s2.4xlarge]| 86 986 ₽
[!KEYREF s2.5xlarge]| 104 382 ₽

**[!TAB За 1 час работы хоста]**

Класс хостов | Цена за час, вкл. НДС 
----- | ----- 
| **Intel Broadwell** | 
[!KEYREF b1.nano]| 1,0770 ₽
[!KEYREF b1.micro] | 1,5800 ₽
[!KEYREF b1.medium] | 2,9500 ₽
[!KEYREF s1.nano] | 3,0000 ₽ | 
[!KEYREF s1.micro] | 6,0102 ₽ | 
[!KEYREF s1.small] | 12,0102 ₽ | 
[!KEYREF s1.medium] | 24,0305 ₽ | 
[!KEYREF s1.large] | 48,0508 ₽ | 
[!KEYREF s1.xlarge] | 96,1119 ₽ 
**Intel Cascade Lake** |  
[!KEYREF b2.nano]| 1,0770 ₽
[!KEYREF b2.small] | 1,5800 ₽
[!KEYREF b2.medium] | 2,9500 ₽
[!KEYREF s2.micro] | 6,0102 ₽
[!KEYREF s2.small] | 12,0102 ₽
[!KEYREF s2.medium] | 24,0305 ₽
[!KEYREF s2.large] | 36,2436 ₽
[!KEYREF s2.xlarge] | 48,0508 ₽
[!KEYREF s2.2xlarge] | 72,4884 ₽
[!KEYREF s2.3xlarge] | 96,1119 ₽
[!KEYREF s2.4xlarge]| 120,8136 ₽
[!KEYREF s2.5xlarge]| 144,9756 ₽

---


### Хосты mongos {#prices-mongos-hosts}

---

**[!TAB За месяц работы хоста]**

Класс хостов | Цена за месяц, вкл. НДС 
----- | ----- 
| **Intel Broadwell** |  |
[!KEYREF b1.nano]| 775 ₽
[!KEYREF b1.micro] | 1 138 ₽
[!KEYREF b1.medium] | 2 124 ₽
[!KEYREF s1.nano]| 2 160 ₽
[!KEYREF s1.micro] | 4 327 ₽
[!KEYREF s1.small] | 8 647 ₽
[!KEYREF s1.medium] | 17 302 ₽
[!KEYREF s1.large] | 34 597 ₽
[!KEYREF s1.xlarge] | 69 201 ₽
**Intel Cascade Lake** | | 
[!KEYREF b2.nano]| 775 ₽
[!KEYREF b2.micro] | 1 138 ₽
[!KEYREF b2.medium] | 2 124 ₽
[!KEYREF s2.micro] | 4 327 ₽
[!KEYREF s2.small] | 8 647 ₽
[!KEYREF s2.medium] | 17 302 ₽
[!KEYREF s2.large] | 26 095 ₽
[!KEYREF s2.xlarge] | 34 597 ₽
[!KEYREF s2.2xlarge] | 52 192 ₽
[!KEYREF s2.3xlarge] | 69 201 ₽
[!KEYREF s2.4xlarge]| 86 986 ₽
[!KEYREF s2.5xlarge]| 104 382 ₽

**[!TAB За 1 час работы хоста]**

Класс хостов | Цена за час, вкл. НДС 
----- | ----- 
| **Intel Broadwell** | 
[!KEYREF b1.nano]| 1,0770 ₽
[!KEYREF b1.micro] | 1,5800 ₽
[!KEYREF b1.medium] | 2,9500 ₽
[!KEYREF s1.nano] | 3,0000 ₽ | 
[!KEYREF s1.micro] | 6,0102 ₽ | 
[!KEYREF s1.small] | 12,0102 ₽ | 
[!KEYREF s1.medium] | 24,0305 ₽ | 
[!KEYREF s1.large] | 48,0508 ₽ | 
[!KEYREF s1.xlarge] | 96,1119 ₽ 
**Intel Cascade Lake** |  
[!KEYREF b2.nano]| 1,0770 ₽
[!KEYREF b2.small] | 1,5800 ₽
[!KEYREF b2.medium] | 2,9500 ₽
[!KEYREF s2.micro] | 6,0102 ₽
[!KEYREF s2.small] | 12,0102 ₽
[!KEYREF s2.medium] | 24,0305 ₽
[!KEYREF s2.large] | 36,2436 ₽
[!KEYREF s2.xlarge] | 48,0508 ₽
[!KEYREF s2.2xlarge] | 72,4884 ₽
[!KEYREF s2.3xlarge] | 96,1119 ₽
[!KEYREF s2.4xlarge]| 120,8136 ₽
[!KEYREF s2.5xlarge]| 144,9756 ₽

---


### Хранилище и резервные копии {#prices-storage}

Услуга | Цена за ГБ в месяц, вкл. НДС 
----- | -----
Стандартное сетевое хранилище | 2,2881 ₽ | 
Быстрое сетевое хранилище | 8,1356 ₽ | 
Быстрое локальное хранилище | 8,1356 ₽ | 
Резервные копии сверх размера хранилища | 2,5424 ₽ 

### Исходящий трафик {#prices-traffic}

[!INCLUDE-NOTITLE [pricing-egress-traffic](../_includes/pricing/pricing-egress-traffic.md)]
