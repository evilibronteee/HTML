# Практическая работа №5 #

### Тема: Решение циклических задач

#### Ход работы

#### Задача:


### 8. В последовательности чисел определить предпоследнее четное число и произведение его цифр


```
# Инициализация переменных
last_even = None
second_last_even = None
product = 1

print("Введите последовательность чисел (0 для завершения):")

while True:
    number = int(input())
    if number == 0:
        break
    if number % 2 == 0:
        # Обновление предпоследнего и последнего четных чисел
        second_last_even, last_even = last_even, number

# Вычисление произведения цифр, если есть предпоследнее четное число
if second_last_even:
    temp = second_last_even
    while temp > 0:
        product *= temp % 10
        temp //= 10
    print(f"Предпоследнее четное число: {second_last_even}")
    print(f"Произведение его цифр: {product}")
else:
    print("Четные числа в последовательности не найдены.")
```



### Результат работы программы: 

![](https://github.com/evilibronteee/HTML/blob/main/PR5_YP/Python%20-%20Replit%20-%20Google%20Chrome%2008.04.2024%2013_07_34.png?raw=true)
