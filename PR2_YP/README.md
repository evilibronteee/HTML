# Практическая работа №2 #

### Тема: Решение линейных задач и работа в среде программирования Питон

#### Ход работы

#### Задача:


### 8.	Дано время запуска ракеты в часах, минутах и секундах,  и время полета в секундах. Определите время возвращения ракеты на Землю


```
from datetime import datetime, timedelta

# Ввод времени запуска ракеты
launch_time_str = input("Введите время запуска ракеты (HH:MM:SS): ")
flight_duration_seconds = int(input("Введите продолжительность полета в секундах: "))

# Преобразование ввода в объект datetime
launch_time = datetime.strptime(launch_time_str, '%H:%M:%S')

# Вычисление времени возвращения
return_time = launch_time + timedelta(seconds=flight_duration_seconds)

# Форматирование и вывод результата
print("Время возвращения ракеты:", return_time.strftime('%H:%M:%S'))


```



### Результат работы программы: 

![](https://github.com/evilibronteee/HTML/blob/main/PR2_YP/Python%20-%20Replit%20-%20Google%20Chrome%2007.04.2024%2016_54_23.png?raw=true)
