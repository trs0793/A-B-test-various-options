# A-B-test (English)
### 1) Goal and Task Statement:

During the testing of one hypothesis, a new post recommendation algorithm was applied to the target group, while the control group retained the basic algorithm. The main hypothesis posits that the new algorithm in the 2nd group will lead to an increase in CTR. **My task was to analyze the experiment's outcomes using various methods and make a conclusion about launching the post recommendation algorithm for all users**.

 ### 2) Tools Used:
 - Python (Pandas, Numpy, Seaborn, Matplotlib, Scipy.stats, Pingouin, Bootstrap libraries)
 - SQL queries in ClickHouse

 ### 3) Results:
   
1) The T-test resulted in a p-value > 0.05 for the regular CTR, suggesting no significant differences, possibly due to the non-normal distribution in the test group.

2) Conversely, the Mann-Whitney test yielded a p-value < 0.05 for the regular CTR, indicating significant differences.

3) The T-test for smoothed CTR produced a p-value of 0.0516, suggesting potential significant differences, likely because of the smoothing effect akin to logarithmic transformation, reducing the standard deviation.

4) The Mann-Whitney test for smoothed CTR continued to highlight significant and considerable differences.

5) Bootstrap analysis indicated intersecting confidence intervals between both groups, implying no statistical disparity.

6) The Poisson bootstrap suggested statistical disparities.

7) The Mann-Whitney test post-Bucket transformation revealed discernible differences.

8) Similarly, the t-test post-Bucket transformation revealed differences.

In most cases, the tests demonstrated statistically significant differences. **Since the CTR decreased in the test group, it is not advisable to launch the new algorithm**. Understanding its cause and rectifying it could significantly improve our algorithm, making it deployable in the future.


# A-B-test (Russian)
### 1)Цель и условие задачи:

 В ходе тестирования одной гипотезы целевой группой был использован новый алгоритм рекомендации постов, у контрольной группы оставался базовый алгоритм. Основная гипотеза заключается в том, что новый алгоритм во 2-й группе приведет к увеличению CTR. **Мне необходимо было проанализировать итоги эксперимента разными методами и сделать вывод о запуске алгоритма рекомендаций постов на всех пользователях**. 

 ### 2)Во время выполнения проекта я применял следующе инструменты:
 - Python (библиотеки Pandas, Numpy, Seaborn, Matplotlib, Scipy.stats, Pingouin, Bootstrap);
 - SQL-запрос в ClickHouse

 ### 3)Результат:
   
1) В результате T-теста pvalue>0,05  для обычного CTR и значимых различий нет, это может быть из-за того , что в распределение в тестовой группе ненормальное.

2) В результате теста Манна-Уитни pvalue<0,05  для обычного CTR и значимые различия есть.
 
3) Т-тест сглаженного CTR  показывает что pvalue=0.0516 , можно предположить что значимое различие есть, может быть потому что сработало сглаживание как если бы мы прологорифмировали и тем самым, уменьшили стандартное отклонение.
 
4) Тест Манна-Уитни сглаженного CTR по-прежнему говорит нам о том, что различия есть и очень большое и значимое.
 
5) Метод bootsrap показывает нам , что доверительные интервалы обеих групп пересекаются , значит стат различий нет.
 
6) Пуассоновский бутстреп говорит нам о том, что статистические различия есть.
 
7) Тест Манна-Уитни при Бакетном преобразовании видит отличие.
    
8) И t-тест тоже  при Бакетном преобразовании видит отличие.

В большестве случаев тесты показывают , что стат значимые различия есть, а так как CTR уменьшился в тестовой группе, **значит запускать 
новый алгоритм не стоит**. Когда поймём, что её вызвало и как её поправить - тогда, возможно, мы сделаем наш алгоритм гораздо лучше и уже сможем его выкатить.
