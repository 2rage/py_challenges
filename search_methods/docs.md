## Структуры данных, используемые для заданных методов организации таблиц идентификаторов

### Простое рехэширование:

* **Массив (Array):** Основной структурой данных для реализации хеш-таблицы с простым рехэшированием является массив фиксированного размера, элементы которого хранят пары ключ-значение.
* **Хеш-функция**: Функция для вычисления индекса в массиве на основе ключа.
Бинарное дерево:

### Бинарное дерево
**Бинарное дерево поиска (Binary Search Tree):** Динамическая структура данных, в которой каждый узел содержит ключ, значение и указатели на левое и правое поддеревья.
Узлы дерева (Tree Nodes): Каждый узел содержит данные (ключ-значение) и ссылки на дочерние узлы.
Сравнение структур данных:

**Массивы:** Просты в использовании и обеспечивают быстрый доступ по индексу. Однако могут требовать перехеширования при заполнении и не обеспечивают упорядоченное хранение данных.
Бинарные деревья: Обеспечивают упорядоченное хранение данных и позволяют эффективно выполнять операции вставки, удаления и поиска при сбалансированном дереве. Однако имеют сложную структуру и требуют больше памяти на хранение указателей.

## Результат работы:

1. **Производительность при малом количестве данных (45 идентификаторов):**

Простое рехеширование показывает лучшее время вставки (0.000012 с против 0.000025 с у бинарного дерева).
Бинарное дерево показывает лучшее время поиска (0.000018 с против 0.000026 с у простого рехеширования).

2. **Производительность при среднем количестве данных (90 идентификаторов):**

Простое рехеширование демонстрирует значительно лучшее время вставки (0.000014 с против 0.000916 с у бинарного дерева).
Поиск также быстрее у простого рехеширования (0.000014 с против 0.000046 с у бинарного дерева).

3. **Производительность при большом количестве данных (223 идентификатора):**

Простое рехеширование снова быстрее при вставке (0.000044 с против 0.000145 с у бинарного дерева).
Поиск также быстрее у простого рехеширования (0.000043 с против 0.000125 с у бинарного дерева).

4. **Производительность при очень большом количестве данных (300 идентификаторов):**

Простое рехеширование продолжает демонстрировать лучшее время вставки (0.000057 с против 0.000229 с у бинарного дерева).
Поиск также быстрее у простого рехеширования (0.000056 с против 0.000192 с у бинарного дерева).

## Общий вывод:

1. **Простое рехеширование** показывает лучшую производительность как при вставке, так и при поиске на всех уровнях заполнения таблицы, представленных в тестах (45, 90, 223, 300 идентификаторов). Это особенно заметно при увеличении количества данных, где разница в производительности увеличивается в пользу простого рехеширования.
2. **Бинарное дерево** демонстрирует сравнительно стабильное время вставки и поиска, но оно значительно уступает простому рехешированию при увеличении размера данных. Это связано с тем, что бинарное дерево может становиться несбалансированным, что приводит к увеличению времени выполнения операций.
3. При небольшом размере данных (45 идентификаторов) бинарное дерево показывает лучшее время поиска, но это преимущество нивелируется с увеличением числа идентификаторов.

## Рекомендации:

* **Простое рехеширование** рекомендуется для сценариев с небольшим и средним количеством идентификаторов, так как оно демонстрирует лучшую производительность как при вставке, так и при поиске.
* **Бинарное дерево** может быть полезным в специфических ситуациях, когда важна структура данных или требуется дополнительная функциональность, связанная с упорядоченностью данных. Однако для больших объемов данных и частых операций вставки и поиска простое рехеширование является предпочтительным методом.

Этот анализ показывает, что простое рехеширование является более эффективным методом для большинства случаев, особенно когда количество идентификаторов превышает 90.

