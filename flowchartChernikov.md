# Блок-схема алгоритма решения квадратного уравнения

## Диаграмма

```mermaid
flowchart TD
    Start([Начало]) --> Input[/"Введите a, b, c"/]
    Input --> CheckA{a == 0?}
    CheckA -- Да --> Error["Вывод: 'Не квадратное уравнение'"]
    CheckA -- Нет --> CalcD["Вычисление D = b² – 4ac"]
    CalcD --> ConditionD{D < 0?}
    ConditionD -- Да --> NoRoots["Вывод: 'Нет действительных корней'"]
    ConditionD -- Нет --> ConditionZero{D == 0?}
    ConditionZero -- Да --> OneRoot["x = -b / (2a)"]
    ConditionZero -- Нет --> TwoRoots["x1 = (-b - √D)/(2a), x2 = (-b + √D)/(2a)"]
    OneRoot --> Output1[/"Вывод x"/]
    TwoRoots --> Output2[/"Вывод x1, x2"/]
    NoRoots --> Stop([Конец])
    Error --> Stop
    Output1 --> Stop
    Output2 --> Stop

