# практична робота 3
## алгоритми сортування на мові piton
![alt](https://www.pngall.com/wp-content/uploads/5/Python.png "shih-tzu" )
* елемент 
* елемент 
    * вкладений елемент 
    * вкладений елемент 
* елемент 
	+ вкладений елемент 
	+ вкладений елемент 
	    - вкладений елемент 
	    - вкладений елемент
```py
def capitalize(String):
    return String.title()
capitalize("shop") # [Shop]
capitalize("python programming") # [Python Programming]
capitalize("how are you!") # [How Are You!]

```
# бульбашка
```py
def bubble_sort(array):
    length = len(array)
    for i in range(0, length):
        for j in range(0, length - i - 1):
            if array[j] > array[j + 1]:
                temp = array[j]
                array[j] = array[j + 1]
                array[j + 1] = temp

print("Сортировка пузырьком")
arr = []
n = int(input("Введите длину массива: ")) 
for i in range(0, n): 
    element = int(input("arr[" + str(i + 1) + "] = "))   
    arr.append(element)
bubble_sort(arr) 
print("Отсортированный массив: ") 
print(arr)
```
# вставки
```py
def insertion_sort(array): 
    length = len(array) 
    for i in range(1, length):
        key = array[i]
        j = i
        while (j - 1 >= 0) and (array[j - 1] > key):
            array[j - 1], array[j] = array[j], array[j - 1]
            j = j - 1
        array[j] = key

print("Сортировка вставками")
arr = []
length = int(input("Введите длину массива: ")) 
for i in range(0, length): 
    element = int(input("arr[" + str(i + 1) + "] = "))   
    arr.append(element)
insertion_sort(arr) 
print("Отсортированный массив: ") 
print(arr)
```
# шейкерна
```py
def shaker_sort(array): 
    length = len(array) 
    swapped = True
    start_index = 0
    end_index = length - 1
    
    while (swapped == True): 
        
        swapped = False
          
        # проход слева направо
        for i in range(start_index, end_index): 
            if (array[i] > array[i + 1]) : 
                # обмен элементов
                array[i], array[i + 1] = array[i + 1], array[i] 
                swapped = True
  
        # если не было обменов прерываем цикл
        if (not(swapped)): 
            break

        swapped = False

        end_index = end_index - 1
  
        #проход справа налево
        for i in range(end_index - 1, start_index - 1, -1): 
            if (array[i] > array[i + 1]): 
                # обмен элементов
                array[i], array[i + 1] = array[i + 1], array[i] 
                swapped = True
 
        start_index = start_index + 1

print("Шейкерная сортировка")
arr = []
length = int(input("Введите длину массива: ")) 
for i in range(0, length): 
    element = int(input("arr[" + str(i + 1) + "] = "))   
    arr.append(element)
shaker_sort(arr) 
print("Отсортированный массив: ") 
print(arr)
```
