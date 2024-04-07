# Практическая работа №6 #

### Тема: Использование одномерных массивов 

#### Ход работы

#### Задача:


### 8.Дана последовательность a1,a2,...,a15.Расположить элементы на четных местах по убыванию.
### Код программы:


```
def sort_even_indices_descending_simple(arr):

  # Сортируем только элементы на четных индексах в порядке убывания
  arr[1::2] = sorted(arr[1::2], reverse=True)
  return arr

# Пример массива
arr = [5, 3, 2, 8, 9, 7, 1, 6, 0, 4, 11, 15, 13, 10, 12]
sorted_arr = sort_even_indices_descending_simple(arr)
print(sorted_arr)

```




### Результат работы программы: 

![задание2](https://github.com/evilibronteee/HTML/blob/main/PR6_YP/Python%20-%20Replit%20-%20Google%20Chrome%2007.04.2024%2013_37_02.png?raw=true)
