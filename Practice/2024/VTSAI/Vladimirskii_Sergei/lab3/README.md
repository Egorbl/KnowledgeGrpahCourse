# Среда Taxi #

Существует 4 местоположения на сетке: R, G, Y, B. При начале эпизода такси появляется на случайной клетке,
и пассажир в случаном месте. Такси должно подъехать к месту нахождения пассажира, забрать его, и поехать к месту 
назначения пассажира и затем его высадить.

## Actions Space ##

6 дискретных состояний:

1) Вниз
2) Вверх
3) Влево
4) Вправо
5) Подобрать пассажира
6) Высадить пассажира

## Observation Space ##

Состояние представляет собой 4-мерный вектор:

(x, y, z, w)

x, y - координаты такси

z - состояние пассажира (0-4)

w - пункт назначения (0-3)

## Награда ##

-1 за шаг, если нет других наград
+20 за доставку пассажира
-10 за подбор/высадку в незаконное место

## Вывод ##

В ходе выполнения данной лабораторной работы были проведены несколько экспериментов с разными значениями learning rate и discount factor.
При повышении learning rate модель совершала неправильные действия, которые приводили к терминальному состоянию. При повышении discount factor модель учитывает будущие вознаграждения, что может способствовать формированию более долгосрочных стратегий, при уменьшении модель
будет более склоненна к учету только мгновенных вознаграждений, что может привести к формированию краткосрочных стратегий.

Рассмотренные коомбинации параметров в экспериментах не привели к успешному прохождению Taxi-v3, скорей всего, нужно использовать другой алгоритм.
