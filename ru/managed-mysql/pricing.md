---
editable: false
---

# Правила тарификации для [!KEYREF mmy-name]

[!INCLUDE [currency-choice](../_includes/pricing/currency-choice.md)]

## Из чего складывается стоимость использования [!KEYREF mmy-short-name] {#rules}

Расчет стоимости использования [!KEYREF mmy-name] учитывает:

* тип и объем хранилища (дискового пространства);

* [класс хостов](concepts/instance-types.md), выбранный для кластера;

* количество хостов БД в кластерах;

* настройки и количество резервных копий;

* объем исходящего трафика.


[!INCLUDE [pricing-gb-size](../_includes/pricing-gb-size.md)]

### Использование хостов БД {#rules-hosts-uptime}

Стоимость начисляется за каждый час работы хоста в соответствии с его классом. Точные характеристики классов приведены в разделе [[!TITLE]](concepts/instance-types.md).

Минимальная единица тарификации — час (например, стоимость 1,5 часов работы хоста равна стоимости 2 часов). Время, когда хост [!KEYREF MY] не может выполнять свои основные функции, не тарифицируется.

### Использование дискового пространства {#rules-storage}

Оплачивается:

* Объем хранилища, выделенный для кластеров БД.

    * Хранилище на быстрых локальных дисках (NVMe) можно заказывать только для кластеров более чем с 3 хостами, с шагом 100 ГБ.


* Объем, занимаемый резервными копиями баз данных сверх заданного хранилища для кластера.

    * Хранение резервных копий не тарифицируется пока сумма размера БД и всех резервных копий остается меньше выбранного объема хранилища.

    * Количество хостов кластера не влияет на объем хранилища и, соответственно, на бесплатный объем резервных копий.

Цена указывается за 1 месяц использования. Минимальная единица тарификации — 1 ГБ в час (например, стоимость хранения 1 ГБ в течение 1,5 часов равна стоимости хранения в течение 2 часов).


## Цены {#prices}

### Хосты {prices-hosts}

---

**[!TAB За месяц работы хоста]**

Класс хостов | Цена за месяц, вкл. НДС
----- | -----
**Intel Broadwell** | 
[!KEYREF b1.nano]| 508 ₽
[!KEYREF b1.micro] | 858 ₽
[!KEYREF b1.medium] | 1 581 ₽
[!KEYREF m1.micro] | 5 372 ₽
[!KEYREF m1.small] | 10 745 ₽
[!KEYREF m1.medium]| 16 116 ₽
[!KEYREF m1.large] | 21 489 ₽
[!KEYREF m1.xlarge] | 32 232 ₽
[!KEYREF m1.2xlarge] | 42 976 ₽
[!KEYREF m1.3xlarge] | 64 465 ₽
[!KEYREF m1.4xlarge] | 85 952 ₽
[!KEYREF s1.nano] | 1 926 ₽
[!KEYREF s1.micro] | 3 547 ₽
[!KEYREF s1.small] | 7 094 ₽
[!KEYREF s1.medium] | 14 189 ₽
[!KEYREF s1.large] | 28 377 ₽
[!KEYREF s1.xlarge] | 56 755 ₽
**Intel Cascade Lake** | 
[!KEYREF b2.nano]| 508 ₽
[!KEYREF b2.micro] | 858 ₽
[!KEYREF b2.medium] | 1 581 ₽
[!KEYREF m2.micro] | 5 372 ₽
[!KEYREF m2.small] | 10 745 ₽
[!KEYREF m2.medium]| 16 116 ₽
[!KEYREF m2.large] | 21 489 ₽
[!KEYREF m2.xlarge] | 32 232 ₽
[!KEYREF m2.2xlarge] | 42 976 ₽
[!KEYREF m2.3xlarge] | 64 465 ₽
[!KEYREF m2.4xlarge] | 85 952 ₽
[!KEYREF m2.5xlarge] | 107 440 ₽
[!KEYREF m2.6xlarge] | 128 929 ₽
[!KEYREF s2.micro] | 3 547 ₽
[!KEYREF s2.small] | 7 094 ₽
[!KEYREF s2.medium] | 14 189 ₽
[!KEYREF s2.large] | 21 284 ₽
[!KEYREF s2.xlarge] | 28 377 ₽
[!KEYREF s2.2xlarge] | 42 567 ₽
[!KEYREF s2.3xlarge] | 56 755 ₽
[!KEYREF s2.4xlarge]| 70 945 ₽
[!KEYREF s2.5xlarge]| 85 133 ₽

**[!TAB За 1 час работы хоста]**

Класс хостов | Цена за час, вкл. НДС
----- | ----- 
**Intel Broadwell** | 
[!KEYREF b1.nano]| 0,7056 ₽
[!KEYREF b1.micro] | 1,1916 ₽
[!KEYREF b1.medium] | 2,1960 ₽
[!KEYREF m1.micro] | 7,4616 ₽
[!KEYREF m1.small] | 14,9232 ₽
[!KEYREF m1.medium]| 22,3836 ₽
[!KEYREF m1.large] | 29,8452 ₽
[!KEYREF m1.xlarge] | 44,7672 ₽
[!KEYREF m1.2xlarge] | 59,6892 ₽
[!KEYREF m1.3xlarge] | 89,5344 ₽
[!KEYREF m1.4xlarge] | 119,3784 ₽
[!KEYREF s1.nano] | 2,6748 ₽
[!KEYREF s1.micro] | 4,9260 ₽
[!KEYREF s1.small] | 9,8532 ₽
[!KEYREF s1.medium] | 19,7064 ₽
[!KEYREF s1.large] | 39,4128 ₽
[!KEYREF s1.xlarge] | 78,8268 ₽
**Intel Cascade Lake** | 
[!KEYREF b2.nano]| 0,7056 ₽
[!KEYREF b2.micro] | 1,1916 ₽
[!KEYREF b2.medium] | 2,1960 ₽
[!KEYREF m2.micro] | 7,4616 ₽
[!KEYREF m2.small] | 14,9232 ₽
[!KEYREF m2.medium]| 22,3836 ₽
[!KEYREF m2.large] | 29,8452 ₽
[!KEYREF m2.xlarge] | 44,7672 ₽
[!KEYREF m2.2xlarge] | 59,6892 ₽
[!KEYREF m2.3xlarge] | 89,5344 ₽
[!KEYREF m2.4xlarge] | 119,3784 ₽
[!KEYREF m2.5xlarge] | 149,2224 ₽
[!KEYREF m2.6xlarge] | 179,0676 ₽
[!KEYREF s2.micro] | 4,9260 ₽
[!KEYREF s2.small] | 9,8532 ₽
[!KEYREF s2.medium] | 19,7064 ₽
[!KEYREF s2.large] | 29,5608 ₽
[!KEYREF s2.xlarge] | 39,4128 ₽
[!KEYREF s2.2xlarge] | 59,1204 ₽
[!KEYREF s2.3xlarge] | 78,8268 ₽
[!KEYREF s2.4xlarge]| 98,5344 ₽
[!KEYREF s2.5xlarge]| 118,2408 ₽

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
