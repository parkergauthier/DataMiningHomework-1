1.) Data visualization: flights at ABIA
---------------------------------------

![](hw1-markdown_files/figure-markdown_strict/Airline%20Delays%20(1)-1.png)

How did departures for Austin-Bergstrom International Airport vary in
2008? According to this chart, across all airlines, the greatest average
departure delays occur in the morning, with Southwest delays being the
most severe. If you’re flying United, you want to avoid early afternoon
departures, as there is a huge spike in average delays in the hours
between 11:00 am and 4:00 pm.

2.) Wrangling the Billboard Top 100
-----------------------------------

### Part A:

<table>
<caption>Top 10 Most Popular Songs since 1958</caption>
<thead>
<tr class="header">
<th style="text-align: left;">Performers</th>
<th style="text-align: left;">Songs</th>
<th style="text-align: right;">Total # of Weeks on Billboard</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Imagine Dragons</td>
<td style="text-align: left;">Radioactive</td>
<td style="text-align: right;">87</td>
</tr>
<tr class="even">
<td style="text-align: left;">AWOLNATION</td>
<td style="text-align: left;">Sail</td>
<td style="text-align: right;">79</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Jason Mraz</td>
<td style="text-align: left;">I’m Yours</td>
<td style="text-align: right;">76</td>
</tr>
<tr class="even">
<td style="text-align: left;">The Weeknd</td>
<td style="text-align: left;">Blinding Lights</td>
<td style="text-align: right;">76</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LeAnn Rimes</td>
<td style="text-align: left;">How Do I Live</td>
<td style="text-align: right;">69</td>
</tr>
<tr class="even">
<td style="text-align: left;">LMFAO Featuring Lauren Bennett &amp; GoonRock</td>
<td style="text-align: left;">Party Rock Anthem</td>
<td style="text-align: right;">68</td>
</tr>
<tr class="odd">
<td style="text-align: left;">OneRepublic</td>
<td style="text-align: left;">Counting Stars</td>
<td style="text-align: right;">68</td>
</tr>
<tr class="even">
<td style="text-align: left;">Adele</td>
<td style="text-align: left;">Rolling In The Deep</td>
<td style="text-align: right;">65</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Jewel</td>
<td style="text-align: left;">Foolish Games/You Were Meant For Me</td>
<td style="text-align: right;">65</td>
</tr>
<tr class="even">
<td style="text-align: left;">Carrie Underwood</td>
<td style="text-align: left;">Before He Cheats</td>
<td style="text-align: right;">64</td>
</tr>
</tbody>
</table>

### Part B:

![](hw1-markdown_files/figure-markdown_strict/Musical%20Diversity%20(2B)-1.png)

Song diversity on the Billboard Top 100 peaked in the mid-1960’s, then
steadily dropped until it hit a low in the early 2000’s. Since the early
2000’s, however, song diversity has increased sharply, with
almost-record high numbers for 2020.

### Part C:

![](hw1-markdown_files/figure-markdown_strict/19%20Artists%20that%20are%20Built%20Different%20(2C)-1.png)

As shown above, there are 19 artists who had at least 30 songs on
Billboard’s Top 100 for 10 weeks or more. We can see that Elton John
dominates this category, with the most songs of this classification.

3.) Wrangling the Olympics
--------------------------

### Part A:

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

### Part B:

    ## # A tibble: 1 x 2
    ##   event                      height_variation
    ##   <chr>                                 <dbl>
    ## 1 Rowing Women's Coxed Fours             10.9

Rowing Women’s Coxed Fours has the most variation in height among
competitors, with a standard deviation of 10.9 cm.

### Part C:

![](hw1-markdown_files/figure-markdown_strict/Average%20Age%20of%20Olympic%20Swimmers%20(3C)-1.png)

The average age of Olympic swimming medalists spiked in 1924, but
dropped to an average age of about 20 for men and 17 for women until the
1980s, when there began a gradual increase in age for both sexes.

4.) K-nearest Neighbors
-----------------------

### Trim 350 Analysis

#### Making predictions

    ## [1] 12207.97

    ## [1] 11497.31

    ## [1] 11784.88

    ## [1] 12557.48

    ## [1] 21098.94

Above are the RMSE outputs, in order, of arbitrarily selected values of
K (2, 10, 25, 100, and 300 respectively).

<table>
<caption>Our Testing Data with Price Predictions Based on Differing Values of k (data arranged by mileage</caption>
<colgroup>
<col style="width: 4%" />
<col style="width: 7%" />
<col style="width: 6%" />
<col style="width: 15%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 17%" />
<col style="width: 17%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Trim</th>
<th style="text-align: right;">Mileage</th>
<th style="text-align: right;">Price</th>
<th style="text-align: right;">k = 2 Prediction</th>
<th style="text-align: right;">k = 10 Prediction</th>
<th style="text-align: right;">k = 25 Prediction</th>
<th style="text-align: right;">k = 100 Prediction</th>
<th style="text-align: right;">k = 300 Prediction</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">350</td>
<td style="text-align: right;">10</td>
<td style="text-align: right;">106010</td>
<td style="text-align: right;">87108.5</td>
<td style="text-align: right;">89769.2</td>
<td style="text-align: right;">82319.80</td>
<td style="text-align: right;">67296.21</td>
<td style="text-align: right;">50788.05</td>
</tr>
<tr class="even">
<td style="text-align: left;">350</td>
<td style="text-align: right;">2325</td>
<td style="text-align: right;">74899</td>
<td style="text-align: right;">72947.5</td>
<td style="text-align: right;">72304.3</td>
<td style="text-align: right;">80004.44</td>
<td style="text-align: right;">67296.21</td>
<td style="text-align: right;">50788.05</td>
</tr>
<tr class="odd">
<td style="text-align: left;">350</td>
<td style="text-align: right;">2747</td>
<td style="text-align: right;">67995</td>
<td style="text-align: right;">68495.0</td>
<td style="text-align: right;">70380.1</td>
<td style="text-align: right;">78417.92</td>
<td style="text-align: right;">67296.21</td>
<td style="text-align: right;">50788.05</td>
</tr>
<tr class="even">
<td style="text-align: left;">350</td>
<td style="text-align: right;">2951</td>
<td style="text-align: right;">69995</td>
<td style="text-align: right;">68991.0</td>
<td style="text-align: right;">69870.5</td>
<td style="text-align: right;">76643.60</td>
<td style="text-align: right;">67296.21</td>
<td style="text-align: right;">50788.05</td>
</tr>
<tr class="odd">
<td style="text-align: left;">350</td>
<td style="text-align: right;">3524</td>
<td style="text-align: right;">70900</td>
<td style="text-align: right;">72441.5</td>
<td style="text-align: right;">70162.0</td>
<td style="text-align: right;">75310.20</td>
<td style="text-align: right;">67296.21</td>
<td style="text-align: right;">50788.05</td>
</tr>
<tr class="even">
<td style="text-align: left;">350</td>
<td style="text-align: right;">4978</td>
<td style="text-align: right;">69990</td>
<td style="text-align: right;">66991.0</td>
<td style="text-align: right;">72245.2</td>
<td style="text-align: right;">73184.24</td>
<td style="text-align: right;">67296.21</td>
<td style="text-align: right;">50788.05</td>
</tr>
<tr class="odd">
<td style="text-align: left;">350</td>
<td style="text-align: right;">5404</td>
<td style="text-align: right;">81895</td>
<td style="text-align: right;">75991.0</td>
<td style="text-align: right;">72946.4</td>
<td style="text-align: right;">73551.44</td>
<td style="text-align: right;">67296.21</td>
<td style="text-align: right;">50788.05</td>
</tr>
<tr class="even">
<td style="text-align: left;">350</td>
<td style="text-align: right;">6655</td>
<td style="text-align: right;">59991</td>
<td style="text-align: right;">78447.5</td>
<td style="text-align: right;">71864.0</td>
<td style="text-align: right;">71735.56</td>
<td style="text-align: right;">67296.21</td>
<td style="text-align: right;">50788.05</td>
</tr>
<tr class="odd">
<td style="text-align: left;">350</td>
<td style="text-align: right;">7116</td>
<td style="text-align: right;">69998</td>
<td style="text-align: right;">72450.0</td>
<td style="text-align: right;">71864.0</td>
<td style="text-align: right;">71171.48</td>
<td style="text-align: right;">67296.21</td>
<td style="text-align: right;">50788.05</td>
</tr>
<tr class="even">
<td style="text-align: left;">350</td>
<td style="text-align: right;">7342</td>
<td style="text-align: right;">53900</td>
<td style="text-align: right;">72450.0</td>
<td style="text-align: right;">75805.9</td>
<td style="text-align: right;">71011.48</td>
<td style="text-align: right;">67296.21</td>
<td style="text-align: right;">50788.05</td>
</tr>
</tbody>
</table>

This table shows our testing set with the predictions of each model
associated with a value of k. For brevity we added only the first 10
observations.

#### Plotting RMSE vs K

![](hw1-markdown_files/figure-markdown_strict/Trim%20350s%20RMSE%20Based%20on%20the%20Value%20of%20K-1.png)

#### Finding Optimal K and Plotting the Model

    ## [1] 4

![](hw1-markdown_files/figure-markdown_strict/Finding%20Optimal%20K%20and%20Plotting%20the%20Model%20-1.png)

### Trim 65 AMG analysis

#### Making predictions

    ## [1] 26014.64

    ## [1] 28139.07

    ## [1] 27966.32

    ## [1] 37749.66

    ## [1] 75474.28

Above are the predicted RMSE values for different values of K (2, 10,
25, 100, and 200 respectively).

<table>
<caption>Our Testing Data with Price Predictions Based on Differing Values of k (data arranged by mileage</caption>
<colgroup>
<col style="width: 6%" />
<col style="width: 7%" />
<col style="width: 6%" />
<col style="width: 15%" />
<col style="width: 15%" />
<col style="width: 15%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Trim</th>
<th style="text-align: right;">Mileage</th>
<th style="text-align: right;">Price</th>
<th style="text-align: right;">k = 2 Prediction</th>
<th style="text-align: right;">k = 10 Prediction</th>
<th style="text-align: right;">k = 25 Prediction</th>
<th style="text-align: right;">k = 100 Prediction</th>
<th style="text-align: right;">k = 200 Prediction</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">65 AMG</td>
<td style="text-align: right;">3</td>
<td style="text-align: right;">224625</td>
<td style="text-align: right;">225667.5</td>
<td style="text-align: right;">225693.5</td>
<td style="text-align: right;">228186.8</td>
<td style="text-align: right;">194877.1</td>
<td style="text-align: right;">127029</td>
</tr>
<tr class="even">
<td style="text-align: left;">65 AMG</td>
<td style="text-align: right;">5</td>
<td style="text-align: right;">228825</td>
<td style="text-align: right;">225458.3</td>
<td style="text-align: right;">226603.5</td>
<td style="text-align: right;">228186.8</td>
<td style="text-align: right;">194877.1</td>
<td style="text-align: right;">127029</td>
</tr>
<tr class="odd">
<td style="text-align: left;">65 AMG</td>
<td style="text-align: right;">6</td>
<td style="text-align: right;">224975</td>
<td style="text-align: right;">228858.3</td>
<td style="text-align: right;">227874.0</td>
<td style="text-align: right;">228290.4</td>
<td style="text-align: right;">194877.1</td>
<td style="text-align: right;">127029</td>
</tr>
<tr class="even">
<td style="text-align: left;">65 AMG</td>
<td style="text-align: right;">7</td>
<td style="text-align: right;">226620</td>
<td style="text-align: right;">229797.5</td>
<td style="text-align: right;">229516.2</td>
<td style="text-align: right;">228401.5</td>
<td style="text-align: right;">194877.1</td>
<td style="text-align: right;">127029</td>
</tr>
<tr class="odd">
<td style="text-align: left;">65 AMG</td>
<td style="text-align: right;">8</td>
<td style="text-align: right;">226965</td>
<td style="text-align: right;">229611.7</td>
<td style="text-align: right;">229408.5</td>
<td style="text-align: right;">229145.8</td>
<td style="text-align: right;">194877.1</td>
<td style="text-align: right;">127029</td>
</tr>
<tr class="even">
<td style="text-align: left;">65 AMG</td>
<td style="text-align: right;">8</td>
<td style="text-align: right;">224351</td>
<td style="text-align: right;">229611.7</td>
<td style="text-align: right;">229408.5</td>
<td style="text-align: right;">229145.8</td>
<td style="text-align: right;">194877.1</td>
<td style="text-align: right;">127029</td>
</tr>
<tr class="odd">
<td style="text-align: left;">65 AMG</td>
<td style="text-align: right;">9</td>
<td style="text-align: right;">226625</td>
<td style="text-align: right;">228966.5</td>
<td style="text-align: right;">228966.5</td>
<td style="text-align: right;">229414.4</td>
<td style="text-align: right;">194877.1</td>
<td style="text-align: right;">127029</td>
</tr>
<tr class="even">
<td style="text-align: left;">65 AMG</td>
<td style="text-align: right;">11</td>
<td style="text-align: right;">225525</td>
<td style="text-align: right;">230743.8</td>
<td style="text-align: right;">228987.4</td>
<td style="text-align: right;">229137.9</td>
<td style="text-align: right;">194877.1</td>
<td style="text-align: right;">127029</td>
</tr>
<tr class="odd">
<td style="text-align: left;">65 AMG</td>
<td style="text-align: right;">11</td>
<td style="text-align: right;">226465</td>
<td style="text-align: right;">230743.8</td>
<td style="text-align: right;">228987.4</td>
<td style="text-align: right;">229137.9</td>
<td style="text-align: right;">194877.1</td>
<td style="text-align: right;">127029</td>
</tr>
<tr class="even">
<td style="text-align: left;">65 AMG</td>
<td style="text-align: right;">12</td>
<td style="text-align: right;">232475</td>
<td style="text-align: right;">227157.5</td>
<td style="text-align: right;">229356.0</td>
<td style="text-align: right;">228998.1</td>
<td style="text-align: right;">194877.1</td>
<td style="text-align: right;">127029</td>
</tr>
</tbody>
</table>

This table shows our testing set with the predictions of each model
associated with a value of k. For brevity we added only the first 10
observations.

#### Plotting RMSE vs K

![](hw1-markdown_files/figure-markdown_strict/Plotting%20RMSE%20vs%20K-1.png)

#### Finding Optimal K and Plotting the Model

    ## [1] 2

![](hw1-markdown_files/figure-markdown_strict/Finding%20Optimal%20K%20and%20Plotting%20the%20Model-1.png)

### Discussion

It would appear that, with repeated trials, Trim 350’s optimal value of
k is generally higher. This is due to Trim 350’s larger sample size.
Generally, higher values of k will reduce the variation of our model but
at the cost of greater bias. With larger sample sizes, we can afford to
use larger values of k as these values will have a lesser effect on the
model’s bias.
