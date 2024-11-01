### 1. Insertion sort

Insertion sort - это простой алгоритм сортировки, который работает, как люди сортируют карты в руках. Он последовательно берет каждый элемент из неотсортированной части и вставляет его на нужное место в отсортированной части массива.

```c++
void InsertionSort(int arr[],int n) {
    for (int i = 1; i < n;i++) {
        int j = i-1;
        while (j >= 0 && arr[j] > arr[j + 1]) {
            swap(arr[j], arr[j + 1]);
            j--;
        }
    }
}
```

### Асимптотика по времени:

    Лучший случай: когда все элементы частично/полностью отсортированы, **O(n)**, тк просто фором пройдем все элементы и будем заходить в вайл супер редко.

    Средний и худший случаи: **O(n^2)**, тк зайдем в вайл и будем перебирать элементы в отсортированном массиве

### Асимптотика по памяти:

    Все случаи: O(n), тк работаем только с переменными

### Когда использовать:

    Когда массивы частично/полностью отсортированы, тк время выполнения будет меньше, чем у Merge/Quick Sort

    Когда данные поступают в режиме реального времени и нужно поддерживать массив в отсортированном состоянии по мере поступления новых элементов. Каждый новый элемент можно легко вставить на нужное место, не требуя полной перестановки массива
