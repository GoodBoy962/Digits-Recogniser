##1. Временные затраты
Время измеряется в тактах процессора

#### 42000 экземпляров на обучение

### Сводная таблица результатов 1

|Классификатор|Такты процессора
|---|---|
Decision Tree classifier| 14.493245
Random forest classifier| 30.909819

##2. Точность результатов

Точность (precision) и полнота (recall) являются метриками которые используются при оценке большей части алгоритмов извлечения информации. Иногда они используются сами по себе, иногда в качестве базиса для производных метрик, таких как F-мера или R-Precision. Суть точности и полноты очень проста.

Точность системы в пределах класса – это доля документов действительно принадлежащих данному классу относительно всех документов которые система отнесла к этому классу. Полнота системы – это доля найденных классфикатором документов принадлежащих классу относительно всех документов этого класса в тестовой выборке.

Эти значения легко рассчитать на основании таблицы контингентности, которая составляется для каждого класса отдельно.

#### Таблица контингентности

В таблице содержится информация сколько раз система приняла верное и сколько раз неверное решение по документам заданного класса. А именно:

**TPTP** — истино-положительное решение;  
**TNTN** — истино-отрицательное решение;  
**FPFP** — ложно-положительное решение;  
**FNFN** — ложно-отрицательное решение.  
Тогда, точность и полнота определяются следующим образом:  

$$Precision = TPTP+FP$$
$$Precision = TPTP+FP$$
$$Recall = TPTP+FN$$
$$Recall = TPTP+FN$$

Рассмотрим пример. Допустим, у вас есть тестовая выборка в которой 10 сообщений, из них 4 – спам. Обработав все сообщения классификатор пометил 2 сообщения как спам, причем одно действительно является спамом, а второе было помечено в тестовой выборке как нормальное. Мы имеем одно истино-положительное решение, три ложно-отрицательных и одно ложно-положительное. Тогда для класса “спам” точность классификатора составляет 1212 (50% положительных решений правильные), а полнота 1414 (классификатор нашел 25% всех спам-сообщений).

### Для проверки точности будет взято для предсказывания результата

1. **34.000** представлений цифр - __точность 1__
2. **21.000** представлений цифр - __точность 2__
3. **1.000** представлений цифр - __точность 3__

Для оценки точнности работы классификаторов были использованы следующие характеристики:

$$Accuracy(x)=(TP+TN)/(TP+TN+FP+FN)$$

$$Precision = TP / (TP + FP) $$ 
$$Recall = TP / (TP + FN)$$
 , где 
True positive **(TP)** - верное предсказание положительного результата  
False positive **(FP)** - ошибочное предсказание положительного результата  
True negative **(TN)** - верное предсказание отрицательного результата  
False negative **(FN)** - ошибочное предсказание отрицательного результата  

В таблице ниже приведены лучшие точнности результов работы алгоритмов при определенном
количестве тестовых данных.

### Свобная таблица результатов 2

|Классификатор|Точность 1(%)|Точность 2(%)|Точность 3(%)|
|---|---|---|---|
|Decision Tree|85.25|83.79|67.63|
|Random Forest|93.53|92.74|79.81|
|kNN|-|-|87.61|

![Accuracy charts](sections/accuracy_charts.png)





    