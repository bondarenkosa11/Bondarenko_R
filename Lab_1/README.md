# Практическая работа №1 Бондаренко С.А.


# Lab1

## Цель

1.  Развить практические навыки использования языка программирования R
    для обработки данных
2.  Развить навыки работы в Rstudio IDE
3.  Закрепить знания базовых типов данных языка R и простейших операций
    с ними

## Исходные данные

1.  Windows 11
2.  Rstudio
3.  Github

## План

1.  Установить программный пакет swirl
2.  Запустить задание с помощью swirl::swirl()
3.  Выбрать из меню курсов 1. R Programming: The basics of programming
    in R
4.  Составить отчет и выложить его и исходный qmd/rmd файл в свой
    репозиторий

### Шаг 1. Установка программного пакет swirl.

![](https://github.com/bondarenkosa11/Bondarenko_R/blob/main/Lab_1/img/install%20swirl.png)

### Шаг 2. Запуск swirl и выбор обучения

![](https://github.com/bondarenkosa11/Bondarenko_R/blob/main/Lab_1/img/запуск%20swirl.png)

### Шаг 3. Выполнение курсов

-   базовые структурные блоки (Basic Building Blocks)

``` r
5 + 7
```

    [1] 12

``` r
x <- 5 + 7
```

``` r
x
```

    [1] 12

``` r
y <- x - 3
```

``` r
y
```

    [1] 9

``` r
z <- c(1.1, 9, 3.14)
```

``` r
?c
```

    запускаю httpd сервер помощи... готово

``` r
z
```

    [1] 1.10 9.00 3.14

``` r
c(z,555, z)
```

    [1]   1.10   9.00   3.14 555.00   1.10   9.00   3.14

``` r
z * 2 + 100
```

    [1] 102.20 118.00 106.28

``` r
my_sqrt <- sqrt(z - 1)
```

``` r
my_sqrt
```

    [1] 0.3162278 2.8284271 1.4628739

``` r
 my_div <- z / my_sqrt
```

``` r
my_div
```

    [1] 3.478505 3.181981 2.146460

``` r
c(1, 2, 3, 4) + c(0, 10)
```

    [1]  1 12  3 14

``` r
c(1, 2, 3, 4) + c(0, 10, 100)
```

    Warning in c(1, 2, 3, 4) + c(0, 10, 100): длина большего объекта не является
    произведением длины меньшего объекта

    [1]   1  12 103   4

``` r
z * 2 + 1000
```

    [1] 1002.20 1018.00 1006.28

``` r
my_div
```

    [1] 3.478505 3.181981 2.146460

-   рабочие пространства и файлы (Workspace and Files)

``` r
getwd()
```

    [1] "C:/Users/bonda/Documents/R/Bondarenko_R/Lab_1"

``` r
ls()
```

    [1] "my_div"  "my_sqrt" "x"       "y"       "z"      

``` r
x <- 9
```

``` r
ls()
```

    [1] "my_div"  "my_sqrt" "x"       "y"       "z"      

``` r
dir()
```

    [1] "img"              "mytest2.R"        "mytest3.R"        "readme.html"     
    [5] "readme.qmd"       "readme.rmarkdown" "readme_files"     "testdir"         

``` r
?list.files
```

``` r
args(list.files)
```

    function (path = ".", pattern = NULL, all.files = FALSE, full.names = FALSE, 
        recursive = FALSE, ignore.case = FALSE, include.dirs = FALSE, 
        no.. = FALSE) 
    NULL

``` r
old.dir <- getwd()
```

``` r
dir.create("testdir")
```

    Warning in dir.create("testdir"): 'testdir' уже существует

``` r
setwd("testdir")
```

``` r
file.create("mytest.R")
```

    [1] TRUE

``` r
ls()
```

    [1] "my_div"  "my_sqrt" "old.dir" "x"       "y"       "z"      

``` r
list.files()
```

    [1] "img"              "mytest.R"         "mytest2.R"        "mytest3.R"       
    [5] "readme.html"      "readme.qmd"       "readme.rmarkdown" "readme_files"    
    [9] "testdir"         

``` r
file.exists("mytest.R")
```

    [1] TRUE

``` r
file.info("mytest.R")
```

             size isdir mode               mtime               ctime
    mytest.R    0 FALSE  666 2024-12-17 22:39:11 2024-12-17 22:39:11
                           atime exe
    mytest.R 2024-12-17 22:39:11  no

``` r
file.rename("mytest.R", "mytest2.R")
```

    [1] TRUE

``` r
file.copy("mytest2.R", "mytest3.R")
```

    [1] FALSE

``` r
file.path("mytest3.R")
```

    [1] "mytest3.R"

``` r
file.path("folder1", "folder2")
```

    [1] "folder1/folder2"

``` r
?dir.create
```

``` r
dir.create(file.path('testdir2', 'testdir3'), recursive = TRUE)
```

``` r
unlink('testdir2', recursive = TRUE)
```

``` r
setwd(old.dir)
```

-   последовательности чисел (Sequences of Numbers)

``` r
1:20
```

     [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20

``` r
pi:10
```

    [1] 3.141593 4.141593 5.141593 6.141593 7.141593 8.141593 9.141593

``` r
15:1
```

     [1] 15 14 13 12 11 10  9  8  7  6  5  4  3  2  1

``` r
?':'
```

``` r
seq(1,20)
```

     [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20

``` r
seq(0, 10, by=0.5)
```

     [1]  0.0  0.5  1.0  1.5  2.0  2.5  3.0  3.5  4.0  4.5  5.0  5.5  6.0  6.5  7.0
    [16]  7.5  8.0  8.5  9.0  9.5 10.0

``` r
my_seq <- seq(5, 10, length=30)
```

``` r
length(my_seq)
```

    [1] 30

``` r
1:length(my_seq)
```

     [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25
    [26] 26 27 28 29 30

``` r
seq(along.with = my_seq)
```

     [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25
    [26] 26 27 28 29 30

``` r
seq_along(my_seq)
```

     [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25
    [26] 26 27 28 29 30

``` r
rep(0, times=40)
```

     [1] 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
    [39] 0 0

``` r
rep(c(0, 1, 2), times = 10)
```

     [1] 0 1 2 0 1 2 0 1 2 0 1 2 0 1 2 0 1 2 0 1 2 0 1 2 0 1 2 0 1 2

``` r
rep(c(0, 1, 2), each = 10)
```

     [1] 0 0 0 0 0 0 0 0 0 0 1 1 1 1 1 1 1 1 1 1 2 2 2 2 2 2 2 2 2 2

-   векторы (Vectors)

``` r
num_vect <- c(0.5, 55, -10, 6)
```

``` r
tf <- (num_vect < 1)
```

``` r
tf <- num_vect < 1
```

``` r
tf
```

    [1]  TRUE FALSE  TRUE FALSE

``` r
num_vect >= 6
```

    [1] FALSE  TRUE FALSE  TRUE

``` r
my_char <- c("My", "name", "is")
```

``` r
my_char
```

    [1] "My"   "name" "is"  

``` r
paste(my_char, collapse = " ")
```

    [1] "My name is"

``` r
my_name <- c(my_char, "Johnny")
```

``` r
my_name
```

    [1] "My"     "name"   "is"     "Johnny"

``` r
paste(my_name, collapse = " ")
```

    [1] "My name is Johnny"

``` r
paste("Hello", "world!", sep = " ")
```

    [1] "Hello world!"

``` r
paste(1:3, c("X", "Y", "Z"), sep = "")
```

    [1] "1X" "2Y" "3Z"

``` r
paste(LETTERS, 1:4, sep = "-")
```

     [1] "A-1" "B-2" "C-3" "D-4" "E-1" "F-2" "G-3" "H-4" "I-1" "J-2" "K-3" "L-4"
    [13] "M-1" "N-2" "O-3" "P-4" "Q-1" "R-2" "S-3" "T-4" "U-1" "V-2" "W-3" "X-4"
    [25] "Y-1" "Z-2"

-   пропущенные значения (Missing Values)

``` r
x <- c(44, NA, 5, NA)
```

``` r
x * 3
```

    [1] 132  NA  15  NA

``` r
y <- rnorm(1000)
```

``` r
 z <- rep(NA, 1000)
```

``` r
my_data <- sample(c(y, z), 100)
```

``` r
my_na <- is.na(my_data)
```

``` r
my_na
```

      [1] FALSE  TRUE FALSE FALSE  TRUE FALSE  TRUE  TRUE  TRUE  TRUE FALSE  TRUE
     [13]  TRUE  TRUE  TRUE FALSE FALSE  TRUE  TRUE FALSE FALSE FALSE  TRUE  TRUE
     [25]  TRUE  TRUE FALSE FALSE FALSE FALSE FALSE FALSE  TRUE FALSE  TRUE FALSE
     [37]  TRUE FALSE  TRUE FALSE FALSE  TRUE FALSE FALSE  TRUE  TRUE FALSE FALSE
     [49] FALSE  TRUE  TRUE FALSE FALSE  TRUE  TRUE FALSE  TRUE  TRUE FALSE  TRUE
     [61]  TRUE  TRUE FALSE  TRUE  TRUE FALSE FALSE FALSE  TRUE  TRUE  TRUE FALSE
     [73] FALSE FALSE  TRUE FALSE FALSE FALSE  TRUE FALSE  TRUE FALSE  TRUE FALSE
     [85] FALSE FALSE FALSE  TRUE FALSE  TRUE  TRUE FALSE FALSE FALSE  TRUE  TRUE
     [97]  TRUE FALSE FALSE  TRUE

``` r
my_data == NA
```

      [1] NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA
     [26] NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA
     [51] NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA
     [76] NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA NA

``` r
sum(my_na)
```

    [1] 48

``` r
my_data
```

      [1]  0.962209857           NA -0.064032263  0.829646866           NA
      [6]  1.120732723           NA           NA           NA           NA
     [11]  1.121418998           NA           NA           NA           NA
     [16] -1.287078474  0.375698737           NA           NA -2.088896198
     [21] -0.474154624  0.365759836           NA           NA           NA
     [26]           NA  0.941930248 -0.543915363 -0.010944576  0.134838078
     [31]  0.670596629  0.249357582           NA  1.206401896           NA
     [36]  0.265990645           NA  0.788891749           NA -0.519712555
     [41] -0.886473139           NA -0.353540276  1.775423796           NA
     [46]           NA -0.492102436 -0.002547985  1.104948306           NA
     [51]           NA  0.437115608 -0.162051252           NA           NA
     [56]  0.304259262           NA           NA  0.326177032           NA
     [61]           NA           NA  0.354346609           NA           NA
     [66] -0.198893800  0.204853747  0.363900299           NA           NA
     [71]           NA  0.370148579 -0.261055046  0.678721742           NA
     [76]  0.565376748  1.289518081 -0.804445665           NA  2.100044558
     [81]           NA  3.102916977           NA  0.830886513  0.380787817
     [86] -1.068188514 -0.204491576           NA  2.115379569           NA
     [91]           NA  0.502926954 -0.926409923 -0.528902204           NA
     [96]           NA           NA -1.281020861  0.548557927           NA

``` r
0 / 0
```

    [1] NaN

``` r
Inf - Inf
```

    [1] NaN

## Оценка результата

В результате работы была установлена библиотека swirl, а также были
пройдены 5 подкурсов в рамках обучения “R Programming: The basics of
programming in R”

## Вывод

Были изучены базовые команды и функции языка R - работа с переменными,
векторами, файлами, циклами и NA.
