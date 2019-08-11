Learning Text Analytics in R
================

# Learning TextAnalytics in R

If you work in data science or analytics, then you can’t survive without
data. At a basic level, you would be using Excel to create adhoc reports
or charts for better business understanding. If you know some coding
skills, then you would also use R or Python to solve your business
problem at scale. In doing so, most of the time you have to deal with
data in tabular or matrix format. This is known as structured data.

But about a situation when you have to deal with the text data. This
data is too growing at a rapid speed along with other types of business
data which is in structured format. If this un-structured data in used
properly, then business can gain invaluable insights for itself and for
its competition.

Today we will talk about this data and what all we can do with it.

## This Tutorial will cover following topics in R

  - Text data manipulation
  - Sentiment Analysis
  - Term Frequency - Inverse Document Frequency
  - N-grams
  - Tidying Data
  - Topic Modeling
  - Text Analysis Application

\#1. Text Data Manipulation \#\# Tidy text

Tiday text format is defined as a table with one-token-per-row

1.1: Three ways text data is stored

  - String: Text is stored as strings, i.e., character vectors, within R
  - Corpus: Contain raw strings annotated with additional metadata
  - Document term matrix: Collection (i.e., a corpus) of documents with
    one row for each document and one column for each term

1.2: The unnest\_tokens function

[Emily Dickinson](https://en.wikipedia.org/wiki/Emily_Dickinson), An
American poiet, wrote some lovely text in her time

``` r
text <- c("Because I could not stop for Death -",
          "He kindly stopped for me -",
          "The Carriage held but just Ourselves -",
          "and Immortality")

text
```

    ## [1] "Because I could not stop for Death -"  
    ## [2] "He kindly stopped for me -"            
    ## [3] "The Carriage held but just Ourselves -"
    ## [4] "and Immortality"
