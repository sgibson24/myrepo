HW 2, CS 625, Fall 2022
================
Shawn Gibson
Sep 22, 2022

## R Markdown

# Homework 2 Part 1: Data Cleaning

Steps Taken to Clean the Data

1.  What kind of pet is this column.

<!-- -->

1)  Text Facet Opened

<!-- -->

    1) This provided an overview of the 83 choices that had been selected for this column. It was easy to see misspellings of words, space and capitalization errors to clean the category. These actions cut the total down to 56 but there should only be 4, (Dog, Cat, Bird, Other).

2)  Edit Cells\> Cluster and Edit

<!-- -->

    1) This provides the fastest means to take all entries that are not Dog, Cat, or Bird, and enter the value as Other. 

    2) This provides each cluster of multiple entries and allows the new value of Other to be entered into the New Value field.

3)  Text Filter Opened

<!-- -->

    1) This is another option but more time consuming due to the volume of the data. It provides a filtered view of each of the 4 options for this column. 

4)  White space or spaces before/after entries are creating separate
    entries for the filed.

<!-- -->

    1) Select Edit Cells> Common Transforms> Trim Leading/Trailing White space

      a) This operation quickly cleaned the extra spaces entered. 

5)  Transform

<!-- -->

    1) 42 different entries are left and there should only be 4. The transform command was used on each entry that wasn't within the 4 prescribed entries was changed to other with this entry into the transform command.

      a) value.replace("Fish" , "Other").

2.  Pet’s full name column. 1703 Names to start.

<!-- -->

1)  Edit Cells\> Common Transforms\> Trim Leading/Trailing White space

<!-- -->

    1) 1479 Names after executing this action.

2)  Edit Cells\> Common Transforms\> To Uppercase

<!-- -->

    1) 1465 Names after executing this action.

3.  Pet’s everyday name. 1367 Names to start.

<!-- -->

1)  Edit Cells\> Common Transforms\> Trim Leading/Trailing White space

<!-- -->

    1) 1328 Names after executing this action.

2)  Edit Cells\> Common Transforms\> To Uppercase

<!-- -->

    1) 1309 Names after executing this action.

4.  Pet’s age. 220 different entries to start.

<!-- -->

1)  Edit Cells\> Common Transforms\> Trim Leading/Trailing White space

<!-- -->

    1) 204 Names after executing this action.

2)  Edit Cells\> Common Transforms\> To Number

<!-- -->

    1) 1499 cells contained text

    2) 278 non-numeric entries listed in the facet

3)  Edit\> Cluster and Edit

<!-- -->

    1) Used to clean the entries by comparing to similar values. Removing such things as question marks and other non-representative numeric entries.

      a) 18 clusters found - 712 cells edited through execution

5.  Pet’s Breed. 827 different entries to start.

<!-- -->

1)  Edit Cells\> Common Transforms\> Trim Leading/Trailing White space

<!-- -->

    1) 734 Names after executing this action.

2)  Edit Cells\> Common Transforms\> To Uppercase

<!-- -->

    1) 640 Names after executing this action.

3)  Edit\> Cluster and Edit

<!-- -->

    1) 13 clusters found - 231 cells edited through execution, 622 Names.

4)  Facet\> Text Facet

<!-- -->

    1) Used to skim through all cluster counts to look for anomalies or errors.

      a) Several numbers entered or non-sense entries - deleted.
      

``` r
summary(cars)
```

    ##      speed           dist       
    ##  Min.   : 4.0   Min.   :  2.00  
    ##  1st Qu.:12.0   1st Qu.: 26.00  
    ##  Median :15.0   Median : 36.00  
    ##  Mean   :15.4   Mean   : 42.98  
    ##  3rd Qu.:19.0   3rd Qu.: 56.00  
    ##  Max.   :25.0   Max.   :120.00

## Including Plots

# Homework 2 Part 2: Analyze Cleaned Data

1.  How many types (kinds) of pets are there?

There are only 4 categories for this column. Dogs, Cats, Birds, and
Others were what I interpreted as acceptable answers to the question.
There is 153 types of pets listed as Other.

2.  How many dogs?

1,123

3.  How many breeds of dogs?

445

4.  What’s the most popular dog breed?

Golden Retriever at 156

5.  What’s the age range of the dogs?

6 weeks to 16 yrs

6.  What’s the age range of the guinea pigs?

Because of my choice to change everything other than dog, cat, and bird
to other, there are only 4 guinea pig entries listed under pet’s breed.
The range is 1-4 years old.

7.  What is the oldest pet?

24 year old cat named Bruce

8.  Which are more popular, betta fish or goldfish? How many of each?

BETTA FISH 11 and GoLDFISH 5

9.  What’s the most popular everyday name for a cat?

KITTY 7

10.What’s the most popular full name for a dog?

MAGGIE and SADIE with 7 Each

## Summary

The week two assignment to clean the Pet Names data set proved to be a
challenge. The data contained many errors that would test the limited
knowledge learned over the past week of class instruction.

My interpretation of the pet type column led me to believe that any
animal listed that wasn’t a dog, cat, or bird should be listed as other.
Looking forward to part two of the assignment this made answering a few
of the questions difficult. It is my belief that there is a more
efficient way to clean the data than the multiple methods I employed to
this column. In attempting to find a way to execute a transform through
value.replace, where all entries would be changed to Other, with the
exception of dog, cat, and bird. It is my belief that this would be a
useful command in future data cleaning but I could not find a way to
execute a command in that manner.

The remainder of the assignment employed many of the same techniques
used on the first column.

The cleaning decisions made change the outcome for many of the answers
to the questions listed in part two of the homework 2 assignments. The
Pet’s Age column is one instance of several different possibilities.
This column was messy and contained nearly 1500 cells containing text.
Using Common Transform to Number for this column may have given
different results than others may receive from cleaning. Many entries
listed by months so without the ability to distinguish between years and
months the totals may end differently through this cleaning execution.

Overall, this assignment was informative and helpful with taking learned
cleaning strategies and executing them hands on. It provided a means of
taking several learned techniques and employing them to a real world
scenario.

## References

-   Golbeck, Jennifer (2019) “A Messy Dataset of Pet Names”. Social
    Intelligence Lab Tech Report 19722. University of Maryland, College
    Park.
-   Open Refine Data Cleaning,
    <https://www.youtube.com/watch?v=ChNEIKxL3Yg>
-   Clean Your Data: Getting Started with OpenRefine \[workshop\],
    <https://www.youtube.com/watch?v=wGVtycv3SS0>