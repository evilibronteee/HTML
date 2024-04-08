# Практическая работа №7 #

### Тема: Использование двумерных массивов
#### Ход работы

#### Задача:


### 8. Задан двухмерный массив вещественных чисел. Найти максимальную сумму абсолютных значений элементов по строкам и номер строки с такой суммой;


```
# Функция для создания двумерного массива
def create_2d_array(rows, cols):
    return [[float(input(f"Введите элемент [{i}][{j}]: ")) for j in range(cols)] for i in range(rows)]

# Функция для нахождения максимальной суммы абсолютных значений элементов по строкам
def find_max_sum_and_row(matrix):
    max_sum = 0
    row_number = -1
    for i, row in enumerate(matrix):
        sum_row = sum(abs(x) for x in row)
        if sum_row > max_sum:
            max_sum = sum_row
            row_number = i
    return max_sum, row_number + 1  # Добавляем 1, так как индексация начинается с 0

# Задание размерности массива и его создание
rows = int(input("Введите количество строк: "))
cols = int(input("Введите количество столбцов: "))
matrix = create_2d_array(rows, cols)

# Находим максимальную сумму и номер строки
max_sum, row_number = find_max_sum_and_row(matrix)
print(f"Максимальная сумма абсолютных значений элементов по строкам: {max_sum}")
print(f"Номер строки с такой суммой: {row_number}")

```



### Результат работы программы: 

![](https://github.com/evilibronteee/HTML/blob/main/PR7_YP/Python%20-%20Replit%20-%20Google%20Chrome%2008.04.2024%2013_55_34.png?raw=true)
