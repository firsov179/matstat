# <img src="https://github.com/fodof91/fodof91/blob/main/data-analysis.png" width="40" height="40"/> Отчет о ДЗ по математической статистике 
### Вариант 2 Калабай Михаил, Порфирьеа Антон, Фирсов Федор

<img src="https://github.com/devicons/devicon/blob/master/icons/python/python-original.svg" title="Python" alt="Python" width="30" height="30"/> Для выполнения расчетов мы использовали язык Python с библиотеками pandas, numpy, sklearn, statsmodels и т.д. и среды Google Colab. Так как они максимально удобные и созданя для подобных вычислений.
## <img src="https://github.com/fodof91/fodof91/blob/main/data.png" width="20" height="20"/> Задание 6
## <img src="https://github.com/fodof91/fodof91/blob/main/data.png" width="20" height="20"/> Задание 7
## <img src="https://github.com/fodof91/fodof91/blob/main/data.png" width="20" height="20"/> Задание 8
## <img src="https://github.com/fodof91/fodof91/blob/main/data.png" width="20" height="20"/> Задание 9
## <img src="https://github.com/fodof91/fodof91/blob/main/data.png" width="20" height="20"/> Задание 10

Для исследования пороговых значений, logit-модели были использованы следующие термины:

<img src="https://media.springernature.com/lw685/springer-static/image/art%3A10.1186%2Fs13174-018-0087-2/MediaObjects/13174_2018_87_Fig4_HTML.png"/> 

В данных терминах, предложенные в задачах метрики буду иметь следуюший вид:

**Чувствительность** = $\frac{TP}{TP + FN}$

**Специфичность** = $\frac{TN}{TN + FP}$

Сделав перебор пороговых значений между 0 и 1 с шагом 0.01, были получены следующие результаты:
![download](https://github.com/fodof91/matstat/assets/90344389/773b49f3-5221-423b-b060-1e7ba0311062)

Эти графики выглядят достаточно правдоподобно, ведь из определений очевидно, что если рассмотреть наши метрики как функции от порогов, то они будут обладать следующими свойствами:

+ Чувствительность
  - Монотонно убывающая (не строго)
  - В 0 имеет значение 1
  - В 1 имеет значение 0
 
+ Специфичность
  - Монотонно возрастающая (не строго)
  - в 0 имеет значение 0
  - в 1 имеет значение 1

Эти свойства подтверждается графиками выше.

Также выделив те пороги, где чувствительность не ниже 80%, был выделен порог с максимальным значением специфичности.

Этот порог имеет значение 0.33. Чувствительность $\approx$ 80.21%. Специфичность $\approx$ 35.60%
