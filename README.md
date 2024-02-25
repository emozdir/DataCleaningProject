
![](./images/data_cleaning.png)
# <center> Очистка данных на Python </center>
## Оглавление
1. [Описание проекта](#Описание-проекта)
2. [Описание данных](#Описание-данных)
3. [Зависимости](#Зависимости)
4. [Установка проекта](#Установка-проекта)
5. [Использование проекта](#Использование-проекта)
6. [Авторы](#Авторы)
7. [Выводы](Использование-проекта)

## Описание проекта

> **Очистка данных (data cleaning)** – это процесс обнаружения и удаления (или исправления) поврежденных, ложных или неинформативных записей таблицы или целой базы данных. Процесс состоит из двух этапов: поиск и ликвидация (или редактирование).

Основные этапы очистки данных:
* Работа с пропущенными значениями.
* Очистка данных от пропусков.
* Удаление признаков и записей, которые не несут полезной информации.

**Цель очистки данных** — избавиться от «мусора», который может помешать моделированию или исказить его результаты. Во многих задачах очистка данных — это самая главная часть этапа подготовки данных к построению модели, которая нередко занимает большую часть времени работы над задачей.


Рассмотрим пример того, как «мусор» может влиять на результат. На графиках ниже представлены две диаграммы рассеяния и две одинаковые линейные модели (прямые, которые пытаются повторить данные). На левом графике модель построена на «грязных» данных, содержащих аномалии, а на правом модель обучена на очищенных данных. 

![](./images/example_outliers.png)

**Данный проект** направлен на демонстрацию применения различных методов очистки данных на каждом из ее этапов на примере датасета о квартирах в Москве от Сбербанка.

**О структуре проекта:**
* [data](./data) - папка с исходными табличными данными
* [images](./images) - папка с изображениями, необходимыми для проекта
* [outliers_lib](./outliers_lib) - папка со вспомогательными модулями для обработки выбросов 
* [data_cleaning_example.ipynb](./data_cleaning_example.ipynb) - jupyter-ноутбук, содержащий основной код проекта, в котором демонстрируются методы и подходы решения задач очистки данных


## Описание данных
В этом проекте используются данные с соревнования [Sberbank Russian Housing Market](https://www.kaggle.com/c/sberbank-russian-housing-market/data) от Сбера (бывш. Сбербанк).

Требования Сбера состояли в построении модели, которая бы прогнозировала цены на жильё в Москве, опираясь на параметры самого жилья, а также состояние экономики и финансового сектора в стране.

Исходный датасет представляет собой набор данных из таблицы с информацией о параметрах жилья в Москве и Московской области, а также таблицы, в которой содержатся 292 признака о состоянии экономики России на момент продажи недвижимости. 

Для упрощения демонстрации техники очистки данных мы будем отрабатывать на урезанном датасете. Он содержит информацию о 61 признаке, описывающих жилье. Файл с данными можно найти [здесь](./data/sber_data.csv).

## Используемые зависимости
* Python (3.9):
    * [numpy (1.20.3)](https://numpy.org)
    * [pandas (1.3.4)](https://pandas.pydata.org)
    * [matplotlib (3.4.3)](https://matplotlib.org)
    * [seaborn (0.11.2)](https://seaborn.pydata.org)

## Установка проекта

```
git clone https://github.com/SkillfactoryDS/DataCleaningProject
```

## Использование
Вся информация о работе представлена в jupyter-ноутбуке data_cleaning_example.ipynb.

## Авторы

* [Екатерина](https://github.com/emozdir)

## Выводы

>Мы определили основные проблемы "грязных данных" и способы их решения.

В данном проекте мы рассмотрели:
- работу с пропущенными значениями;
- методы поиска выбросов;
- методы выявления и ликвидации дубликатов и неинформативных признаков.

Для наглядности каждую проблему мы расматривали отдельно. Но, каждая из них может косвенно влиять на другую. Поэтому очистка данных должна предполагать комплексное исследование. Более того, не существует конкретного решения для каждого случая: каждый набор данных индивидуален. Необходимо помнить об этом и всегда рационально смотреть не только на данные, но и на результаты методов их очистки.