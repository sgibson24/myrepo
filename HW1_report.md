HW 1, CS 625, Fall 2022
================
Shawn Gibson
Sep 07, 2022

## Git, GitHub

1.  \*What is your GitHub username? sgibson24

2.  \*What is the URL of your remote GitHub repo (created through
    Mr. Kennedy’s exercises)? <https://github.com/sgibson24/myrepo.git>

## R

The command below will load the tidyverse package. If you have installed
R, RStudio, and the tidyverse package, it should display a list of
loaded packages and their versions.

``` r
library(tidyverse)
```

    ## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.2 ──
    ## ✔ ggplot2 3.3.6      ✔ purrr   0.3.4 
    ## ✔ tibble  3.1.8      ✔ dplyr   1.0.10
    ## ✔ tidyr   1.2.0      ✔ stringr 1.4.1 
    ## ✔ readr   2.1.2      ✔ forcats 0.5.2 
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()

## R Markdown

1.  *Create a bulleted list with at least 3 items*

-   Bulleted list item 1
-   Bulleted list item 2
-   Bulleted list item 3

2.  *Write a single paragraph that demonstrates the use of italics,
    bold, bold italics, code, and includes a link. The paragraph does
    not have to make sense.*

This is my *paragraph* that **demonstrates** the use of text formatting.
It will show the abilty to *italic* **bold** and to combine both with
***bold italic***. Code is enclodes between two backticks. Insert the
code `R_code`.

3.  *Create a level 3 heading*

### 3rd Level Heading

## R

#### Data Visualization Exercises

1.  (Q2) *How many rows are in mpg? How many columns?*

There are 234 rows and 11 columns.

1.  (Q4) *Make a scatterplot of hwy vs cyl.*

ggplot(mpg, aes(x = cyl, y = hwy)) + geom_point()

#### Workflow: basics Exercises

1.  (Q2) *Tweak each of the following R commands so that they run
    correctly (`library(tidyverse)` is correct):*

``` r
library(tidyverse)
ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy))

filter(mpg, cyl = 8)

filter(diamonds, carat > 3)
```

## Google Colab

1.  *What are the URLs of your Google Colab notebooks (both Python and
    R)?*

<https://colab.research.google.com/drive/1ORgjSoFoDWa_x9p2OycyMkjsjs6awRTR?usp=sharing>

<https://colab.research.google.com/drive/1bXWJqXF9S4I3fjjrUC8J7FD002lC-P6D?usp=sharing>

## Tableau

*Insert your the image of your final bar chart here*

![Tableau Sales in West.](Sales%20in%20the%20West.png)

1.  *What conclusions can you draw from the chart?*

There isn’t any obvious conclusions from the chart. These sales seem all
over from year to year. The one thing that stood out was that technology
grew as the years went along.

## Observable and Vega-Lite

### A Taste of Observable

1.  *In the “New York City weather forecast” section, try replacing
    `Forecast: detailedForecast` with `Forecast: shortForecast`. Then
    press the blue play button or use Shift-Return to run your change.
    What happens?*

It now displays a shorter forecast description instead of the detailed
forecast.

1.  *Under the scatterplot of temperature vs. name, try replacing
    `markCircle()` with `markSquare()`. Then press the blue play button
    or use Shift-Return to run your change. What happens? How about
    `markPoint()`?*

The circle is now gone and replaced by sqaures. markPoint draws an open
circle.

1.  *Under “Pick a location, see the weather forecast”, pick a location
    on the map. Where was the point you picked near?*

2.  *The last visualization on this page is a “fancy” weather chart
    embedded from another notebook. Click on the 3 dots next to that
    chart and choose ‘Download PNG’. Insert the PNG into your report.*

### Charting with Vega-Lite

`markCircle()`

1.  *Pass an option of `{ size: 200 }` to `markCircle()`.*
2.  *Try `markSquare` instead of `markCircle`.*
3.  *Try `markPoint({ shape: 'diamond' })`.*

`vl.x().fieldQ("Horsepower")`, …

1.  *Change `Horsepower` to `Acceleration`*
2.  *Swap what fields are displayed on the x- and y-axis*

`vl.tooltip().fieldN("Name")`

1.  *Change `Name` to `Origin`.*

Another example, `count()`

1.  *Remove the `vl.y().fieldN("Origin")` line.*
2.  *Replace `count()` with `average("Miles_per_Gallon")`.*

## References

*Every report must list the references that you consulted while
completing the assignment. If you consulted a webpage, you must include
the URL.*

-   Insert Reference 1, <https://www.example.com>
-   Insert Reference 2,
    <https://www.example.com/reallyreallyreally-extra-long-URI/>
