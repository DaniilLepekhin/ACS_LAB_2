# Архитектура вычислительных систем. Лабораторная 2.   
## Лепёхин Даниил. ИС-841  
### Задание: Реализовать программу для оценки производительности процессора (benchmark).

 1) Написать программу(ы) (benchmark) на языке С/С++/C# для оценки производительности
процессора. В качестве набора типовых задач использовать либо минимум 3 функции
выполняющих математические вычисления, либо одну функцию по работе с матрицами и
векторами данных с несколькими типами данных. Можно использовать готовые функции
из математической библиотеки (math.h) [3], библиотеки BLAS [4] (англ. Basic Linear Algebra Subprograms — базовые подпрограммы линейной алгебры) и/или библиотеки LAPACK [5]
(LinearAlgebra PACKage).Обеспечить возможность подать на вход программы общее число
испытаний для каждой типовой задачи (минимум 10). Входные данные для типовой задачи
сгенерировать случайным образом.

 2) С помощью системного таймера (библиотека time.h, функции clock() илиgettimeofday()) или
с помощью процессорного регистра счетчика TSC реализовать оценку в секундах среднего
времени испытания каждой типовой задачи. Оценить точность и погрешность (абсолютную
и относительную) измерения времени (рассчитать дисперсию и среднеквадратическое
отклонение). 

 3) Результаты испытаний в самой программе (или с помощью скрипта) сохранить в файл в
формате CSV со следующей структурой:
[PModel;Task;OpType;Opt;LNum;InsCount;Timer;AvTime;AbsErr;RelErr;TaskPerf], где
PModel – Processor Model, модель процессора, на котором проводятся испытания;
Task – название выбранной типовой задачи (например, sin, log, saxpy, dgemv, sgemm и др.);
OpType – Operand Type, тип операндов используемых при вычислениях типовой задачи;
Opt – Optimisations, используемы ключи оптимизации (None, O1, O2 и др.);
LNum – Launch Numer, число испытаний типовой задачи.
InsCount – Instruction Count, оценка числа инструкций при выполнении типовой задачи;
AvTime – Average Time, среднее время выполнения типовой задачи в секундах;
AbsError – Absolute Error, абсолютная погрешность измерения времени в секундах;
RelError – Relative Error, относительная погрешность измерения времени в %;
TaskPerf – Task Performance, производительность (быстродействие) процессора при
выполнении типовой задачи. 
