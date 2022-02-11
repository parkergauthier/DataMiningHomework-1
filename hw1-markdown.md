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

\#\#Trim 350 analysis \#\#\# Splitting the dataset and making
predictions

    ## [1] 9652.476

    ## [1] 8702.561

    ## [1] 9151.221

    ## [1] 11418.08

    ## [1] 22434.62

Above are the RMSE outputs, in order, of arbitrarily selected values of
K (2, 10, 25, 100, and 300 respectively).

    ##    trim mileage  price k2_price_pred k10_price_pred k25_price_pred
    ## 2   350   17770  60900       53445.0        56860.2       57203.72
    ## 3   350   29108  54995       60445.0        51160.3       53879.44
    ## 6   350   19567  59977       50947.5        57455.4       57118.24
    ## 18  350  117683  12900       12196.0        14570.8       12811.56
    ## 23  350    2384  75900       71929.5        72394.8       79351.56
    ## 29  350   11862  76878       67245.5        63191.4       65558.12
    ## 39  350   31782  52999       49727.5        56911.1       55179.00
    ## 44  350   18748  59995       57379.0        56832.5       57148.60
    ## 45  350    9300 103410       77589.5        69292.7       67501.16
    ## 47  350   80511  15991       29197.5        20251.5       18731.68
    ##    k100_price_pred k300_price_pred
    ## 2         59166.49        50193.70
    ## 3         54131.49        50193.70
    ## 6         57978.50        50193.70
    ## 18        20202.58        43194.97
    ## 23        66154.25        50193.70
    ## 29        62701.38        50193.70
    ## 39        52957.61        50193.70
    ## 44        58206.73        50193.70
    ## 45        66154.25        50193.70
    ## 47        24872.37        43616.80

This table shows our testing set with the predictions of each model
associated with a value of k. For brevity we added only the first 10
observations.

### Plotting RMSE vs K

![](hw1-markdown_files/figure-markdown_strict/Trim%20350s%20RMSE%20Based%20on%20the%20Value%20of%20K-1.png)

### Finding Optimal K and Plotting the Model

    ## [1] 12

![](hw1-markdown_files/figure-markdown_strict/Finding%20Optimal%20K%20and%20Plotting%20the%20Model%20-1.png)

Trim 65 AMG analysis
--------------------

### Splitting the data and making predictions

    ## [1] 28111.88

    ## [1] 21909.88

    ## [1] 21653.99

    ## [1] 43878.5

    ## [1] 74786.53

Above are the predicted RMSE values for different values of K (2, 10,
25, 100, and 200 respectively).

    ##      trim mileage  price k2_price_pred k10_price_pred k25_price_pred
    ## 16 65 AMG   55730  78992       58492.5        61371.5       54115.68
    ## 25 65 AMG   48579  77444       61387.5        57643.2       57388.92
    ## 32 65 AMG   52951  64999       48645.0        55144.9       57861.12
    ## 40 65 AMG   15512 114998      125694.0       112700.6      103428.60
    ## 43 65 AMG       8 224765      230345.0       229504.5      229117.80
    ## 58 65 AMG   44075  50037       59870.5        63039.0       61112.04
    ## 63 65 AMG       7 227865      230184.0       229458.8      228462.81
    ## 65 65 AMG   79713  45888       32497.0        33256.0       39876.28
    ## 73 65 AMG   67604  44777       61943.5        44210.4       44605.12
    ## 76 65 AMG   32115  50999       69888.0        61009.6       75957.00
    ##    k100_price_pred k200_price_pred
    ## 16        53993.36        110095.8
    ## 25        60942.53        110858.0
    ## 32        57844.02        110095.8
    ## 40       174489.00        131982.1
    ## 43       201123.84        131982.1
    ## 58        65208.30        112002.5
    ## 63       201123.84        131982.1
    ## 65        49890.20        111721.3
    ## 73        51300.97        112069.4
    ## 76        77726.29        131982.1

This table shows our testing set with the predictions of each model
associated with a value of k. For brevity we added only the first 10
observations.

### Plotting RMSE vs K

![](hw1-markdown_files/figure-markdown_strict/Plotting%20RMSE%20vs%20K-1.png)

### Finding Optimal K and Plotting the Model

    ## [1] 18

![](hw1-markdown_files/figure-markdown_strict/Finding%20Optimal%20K%20and%20Plotting%20the%20Model-1.png)
\#\# Discussion

It would appear that, with repeated trials, Trim 350’s optimal value of
k is generally higher. This is due to Trim 350’s larger sample size.
Generally, higher values of k will reduce the variation of our model but
at the cost of greater bias. With larger sample sizes, we can afford to
use larger values of k as these values will have a lesser effect on the
model’s bias.
