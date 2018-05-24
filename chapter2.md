---
title: Выборочные характеристики
description: >-
  Insert the chapter description here


---
## Знакомство с датасетом

```yaml
type: NormalExercise

xp: 100

key: 4a2d497748
```

Перед работой с любым датасетом его необходимо обработать и ознакомиться с ним. Датасет candy уже загружен в Ваше рабочее пространство.

`@instructions`
- Загрузите библиотеку psych с помощью функции library()
- Проанализируйте данный датасет.
- Выгрузите первые 10 наблюдений.

`@hint`
- Используйте функции describe() и head()

`@pre_exercise_code`
```{r}
candy <- read.csv(url("https://raw.githubusercontent.com/fivethirtyeight/data/master/candy-power-ranking/candy-data.csv"))
```
`@sample_code`
```{r}
# подключите библиотеку psych
___(psych)

# проанализируйте данный датасет
___(___)

# выгрузите первые 10 наблюдений
___(___, 10)
```
`@solution`
```{r}
# подключите библиотеку psych
library(psych)

# проанализируйте данный датасет
describe(candy) 

# выгрузите первые 10 наблюдений
head(candy, 10)
```
`@sct`
```{r}
#first instruction
test_student_typed("library(psych)", not_typed_msg = "Вы не подгрузили библиотеку psych. Внимательно прочтите инструкцию")

#second instruction
test_student_typed("describe(candy)", not_typed_msg = "Возникла проблема с анализом датасета. Внимательно прочтите инструкцию.")

#third instruction
test_student_typed("head(candy, 10)", not_typed_msg = "Возникла проблема с выгрузкой первых 10 наблюдений. Внимательно прочтите инструкцию.")

#General
test_error()
success_msg("Отлично! Пришло время проверить, как хорошо Вы познакомились с датасетом.")
```



