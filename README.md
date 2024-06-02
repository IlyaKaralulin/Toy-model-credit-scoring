# Toy-model-credit-scoring
##Описание
Эта модель для предсказания кредитного риска написана на языке С и обучена на игрушечном наборе данных. Это учебный проект, и его нельзя использовать для реальных задач. В основе лежит модель логистической регрессии и метод L-BFGS для минимизации функции потерь. 

##Запуск
Для того что бы ее обучить и протестировать нужно запустить файл make.bat (для Windows) или make.sh (для Linux)
> В начале соберется исполнительный файл, который подберет нужные веса для каждого параметра и min/max значение каждого параметра для нормализации данных, затем запишет их в конфигаруционный файл.
> Затем соберется файл и запуститься файл, который, используя эти данные, предскажет риск дефолта для тестового набора данных и запишет результат в файл prediction.txt
> После этого составится оцениться количество ошибок по 4 параметрам: true positiv, true negativ, false positiv, false negativ.
> 
##Итог
После тестирования получаем следующие показатели:
TP - 0.153300
FP - 0.074860
TN - 0.558540
FN - 0.213300

Верных предсказаний 70%, ложных 30%. Модель не одобрила бы кредит 20% заемщикам, которые могли бы выплатить (метрика false negativ). И одобрила 7% заемщиков, которые по итогу объявили дефолт.
