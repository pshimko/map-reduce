# Document Storage Apache Hadoop

## Framework

Хранилище документов из 2-х узлов вычислительного кластера, построенное с использованием Apache Hadoop (HDFS + Hive). 

## Description

+ Построение над коллекцией документов инвертированного, k-граммного индексов для полнотекстового поиска
+ Реализации поисковых запросов на кластере в парадигме Map-Reduce
+ Реализация двух типов динамических индексов: «перестройка заново» и «вспомогательный индекс»
+ Сравнение времени работы индексов
+ Оценка качества информационного поиска в созданной системе


Имя файла        | Содержимое файла
-----------------|-------------------------------------
inv_index.py     | построение инвертированного индекса
kgramm_index.py  | построение k-граммного индекса
query.py         | реализация поискового запроса
source.py        | построение динамических индексов
report.pdf       | результаты

### Metrics used for assessment:

+ точность и полнота; 
+ f-мера; 
+ кривая точность – полнота; 
+ средняя (интерполированная) точность; 
+ макро(микро)усреднение; MAP; 
+ точность на уровне k; 
+ R-точность; 
+ порог отсечения; 
+ ROC-кривая; 
+ показатель AUC; 
+ совокупная выгода в обычном и нормированном виде.

## Input

1) число кластеров: 1 кластер, состоящий из 2-ух вычислительных узлов и одного главного узла;
2) число элементов данных: 16597;
3) объем данных: 996 Кбайт, 16597 записей;
4) время заполнения коллекции данными: 6,5 с.

