# Как оптимизировать циклы
[//]: # (Version:1.0.0)
Иногда вы будете сталкиваться циклами или рекурсивными функциями, которые занимают много времени при выполнении и являются узким местом в вашем продукте. Прежде чем пытаться сделать цикл немного быстрее, попробуйте потратить несколько минут и обдумать способ, при котором можно удалить цикл. Будет ли другой алгоритм оптимальней работать? Не могли бы вы предположить, будет ли расчитываться(вычисляться) что-то еще? Если Вы не можете отказаться от цикла, то Вы можете оптимизировать его. Это просто; Нужно перенести некоторые вещи из цикла во внешний код. В конце концов, для этого потребуется не только сообразительность, но и понимание расхода при использовании каждого вида операторов и выражений. Вот некоторые рекомендации:

- Удалить операции с плавающей запятой.
- Не выделять новые блоки памяти без надобности.
- Сложить(произвести конкатенацию, если это строки) константы вместе.
- Переместить операции ввода/вывода в буфер.
- Стараться не использовать операцию деления.
- Постарайтесь не делать приведениe типов(это дорогая операция).
- Перемещайте указатель, а не перерасчитывайте показатели.

Стоимость каждой из этих операций зависит от специфики Вашей системы. В некоторых системах компиляторы и оборудования сделать эти вещи за Вас. Но бесспорно, что эффективный код лучше, чем код, который требует понимания конкретной платформы.

Далее [Как справиться с издержками при операциях ввода-вывода](08-How-to-Deal-with-IO-Expense.md)
