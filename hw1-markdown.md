1) Data visualization: flights at ABIA
======================================

![](hw1-markdown_files/figure-markdown_strict/Airline%20Delays%20(1)-1.png)

How did departures for Austin-Bergstrom International Airport vary in
2008? According to this chart, across all airlines, the greatest average
departure delays occur in the morning, with Southwest delays being the
most severe. If you’re flying United, you want to avoid early afternoon
departures, as there is a huge spike in average delays in the hours
between 11:00 am and 4:00 pm.

\#2) Wrangling the Billboard Top 100

\#\#Part A:

    ## # A tibble: 10 x 3
    ## # Groups:   performer [10]
    ##    performer                              song                             count
    ##    <chr>                                  <chr>                            <int>
    ##  1 Imagine Dragons                        Radioactive                         87
    ##  2 AWOLNATION                             Sail                                79
    ##  3 Jason Mraz                             I'm Yours                           76
    ##  4 The Weeknd                             Blinding Lights                     76
    ##  5 LeAnn Rimes                            How Do I Live                       69
    ##  6 LMFAO Featuring Lauren Bennett & Goon~ Party Rock Anthem                   68
    ##  7 OneRepublic                            Counting Stars                      68
    ##  8 Adele                                  Rolling In The Deep                 65
    ##  9 Jewel                                  Foolish Games/You Were Meant Fo~    65
    ## 10 Carrie Underwood                       Before He Cheats                    64

\#\#Part B:

![](hw1-markdown_files/figure-markdown_strict/Musical%20Diversity%20(2B)-1.png)

Song diversity on the Billboard Top 100 peaked in the mid-1960’s, then
steadily dropped until it hit a low in the early 2000’s. Since the early
2000’s, however, song diversity has increased sharply, with
almost-record high numbers for 2020.

\#\#Part C:

    ## # A tibble: 19 x 2
    ##    performer             count
    ##    <chr>                 <int>
    ##  1 Elton John               52
    ##  2 Madonna                  44
    ##  3 Kenny Chesney            42
    ##  4 Tim McGraw               39
    ##  5 Keith Urban              36
    ##  6 Stevie Wonder            36
    ##  7 Taylor Swift             35
    ##  8 Michael Jackson          34
    ##  9 Rod Stewart              33
    ## 10 The Rolling Stones       33
    ## 11 Billy Joel               32
    ## 12 Chicago                  31
    ## 13 Drake                    31
    ## 14 Rascal Flatts            31
    ## 15 Brad Paisley             30
    ## 16 Daryl Hall John Oates    30
    ## 17 George Strait            30
    ## 18 Jason Aldean             30
    ## 19 Neil Diamond             30

![](hw1-markdown_files/figure-markdown_strict/19%20Artists%20that%20are%20Built%20Different%20(2C)-1.png)

\#3) Wrangling the Olympics

\#\#Part A:

    ## # A tibble: 132 x 2
    ##    event                                 topheight
    ##    <chr>                                     <dbl>
    ##  1 Basketball Women's Basketball              198.
    ##  2 Volleyball Women's Volleyball              193 
    ##  3 Athletics Women's Shot Put                 192.
    ##  4 Swimming Women's 200 metres Freestyle      191 
    ##  5 Athletics Women's Heptathlon               189.
    ##  6 Athletics Women's Discus Throw             188.
    ##  7 Athletics Women's High Jump                188 
    ##  8 Rowing Women's Coxed Eights                188 
    ##  9 Rowing Women's Double Sculls               188.
    ## 10 Athletics Women's Triple Jump              187.
    ## # ... with 122 more rows

Female competitors across all athletic events in the top 20 Olympic
sports. The Women’s Basketball team has the highest (and therefore
tallest) percentiles among all female sports. The Women’s Triple Jump
has the lowest.

\#\#Part B:

    ## # A tibble: 1 x 2
    ##   event                      height_variation
    ##   <chr>                                 <dbl>
    ## 1 Rowing Women's Coxed Fours             10.9

Rowing Women’s Coxed Fours has the most variation in height among
competitors, with a standard deviation of 10.9 cm.

\#\#Part C:

![](hw1-markdown_files/figure-markdown_strict/Average%20Age%20of%20Olympic%20Swimmers%20(3C)-1.png)

The average age of Olympic swimming medalists spiked in 1924, but
dropped to an average age of about 20 for men and 17 for women until the
1980s, when there began a gradual increase in age for both sexes.

\#4.) K-nearest Neighbors

Trim 350 Analysis
-----------------

### Making predictions

    ## [1] 11508.67

    ## [1] 10075.39

    ## [1] 10391.73

    ## [1] 10778.91

    ## [1] 19714.24

Above are the RMSE outputs, in order, of arbitrarily selected values of
K (2, 10, 25, 100, and 300 respectively).

    ##    trim mileage price k2_price_pred k10_price_pred k25_price_pred
    ## 5   350   66689 37995       42495.0        21458.9       22821.08
    ## 9   350   23677 61001       52883.5        53833.3       55598.92
    ## 13  350   26183 49990       62975.5        55593.8       56484.76
    ## 17  350   61676 35900       17989.5        25369.0       27366.00
    ## 28  350   41075 53981       50918.0        47357.5       48562.40
    ## 34  350   11076 59900       68931.0        68000.5       67190.84
    ## 36  350   32290 48789       60945.5        54661.9       54990.40
    ## 38  350   40755 46995       52987.0        47260.0       48212.56
    ## 49  350    7000 82000       66449.0        70463.7       71699.52
    ## 52  350   10721 62988       70397.5        68000.5       67950.96
    ##    k100_price_pred k300_price_pred
    ## 5         28140.06        44803.73
    ## 9         56145.84        50366.44
    ## 13        55585.96        50366.44
    ## 17        32021.85        45190.07
    ## 28        48507.90        50366.44
    ## 34        65235.85        50366.44
    ## 36        53072.02        50366.44
    ## 38        48839.34        50366.44
    ## 49        67537.10        50366.44
    ## 52        66760.92        50366.44

This table shows our testing set with the predictions of each model
associated with a value of k. For brevity we added only the first 10
observations.

### Plotting RMSE vs K

![](hw1-markdown_files/figure-markdown_strict/Trim%20350s%20RMSE%20Based%20on%20the%20Value%20of%20K-1.png)

### Finding Optimal K and Plotting the Model

    ## [1] 16

![](hw1-markdown_files/figure-markdown_strict/Finding%20Optimal%20K%20and%20Plotting%20the%20Model%20-1.png)

Trim 65 AMG analysis
--------------------

### Making predictions

    ## [1] 22546.56

    ## [1] 20029.15

    ## [1] 21279.01

    ## [1] 29408.13

    ## [1] 74830.28

Above are the predicted RMSE values for different values of K (2, 10,
25, 100, and 200 respectively).

    ##      trim mileage  price k2_price_pred k10_price_pred k25_price_pred
    ## 4  65 AMG   73415  54981       27450.0        39906.1       41018.20
    ## 11 65 AMG       5 216510      229455.0       229046.2      228783.48
    ## 14 65 AMG   69652  42982       34416.0        45870.9       41759.80
    ## 15 65 AMG   79795  41995       34443.5        33455.0       38831.12
    ## 16 65 AMG   55730  78992       58492.5        66883.0       56679.88
    ## 22 65 AMG      11 235365      228518.8       228754.5      228755.60
    ## 25 65 AMG   48579  77444       61387.5        57453.2       57114.36
    ## 26 65 AMG      17 225681      231141.2       231814.5      230223.20
    ## 35 65 AMG   51670  59995       64745.5        60855.6       59273.28
    ## 49 65 AMG   61560  47888       47935.5        43688.6       50065.12
    ##    k100_price_pred k200_price_pred
    ## 4         49561.42        111771.8
    ## 11       195782.70        128742.1
    ## 14        49671.93        111771.8
    ## 15        48781.46        108684.7
    ## 16        52842.13        109782.9
    ## 22       195782.70        128742.1
    ## 25        60966.99        110524.4
    ## 26       195782.70        128742.1
    ## 35        57979.62        110112.5
    ## 49        51159.93        112113.8

This table shows our testing set with the predictions of each model
associated with a value of k. For brevity we added only the first 10
observations.

### Plotting RMSE vs K

![](hw1-markdown_files/figure-markdown_strict/Plotting%20RMSE%20vs%20K-1.png)

### Finding Optimal K and Plotting the Model

    ## [1] 5

![](hw1-markdown_files/figure-markdown_strict/Finding%20Optimal%20K%20and%20Plotting%20the%20Model-1.png)

Discussion
----------

It would appear that, with repeated trials, Trim 350’s optimal value of
k is generally higher. This is due to Trim 350’s larger sample size.
Generally, higher values of k will reduce the variation of our model but
at the cost of greater bias. With larger sample sizes, we can afford to
use larger values of k as these values will have a lesser effect on the
model’s bias.
