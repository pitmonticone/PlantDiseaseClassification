---
title: Template for preparing your research report submission to Royal Society Open Science using RMarkdown
author:
  - name: Alice Anonymous
    affiliation: "1,2"
  - name: Bob Security
    affiliation: "2"
address:
  - code: "1"
    address: Some Institute of Technology, Department, Street, City, State, Zip
  - code: "2"
    address: Another University Department, Street, City, State, Zip

corresp_author_name:  "B. Security"
corresp_author_email: "bob@email.com"

subject:
  - "subject 1"
  - "subject 2"
  - "subject 3"

keywords:
  - one
  - two
  - optional
  - optional
  - optional

abstract: |
  The abstract text goes here. The abstract text goes here. The abstract text goes here. The abstract text goes here. The abstract text goes here. The abstract text goes here. The abstract text goes here. The abstract text goes here.

## Remove this if not required
ethics: |
  Please provide details on the ethics.
  
data_accessibility: |
  Please provide details on the data availability.

author_contributions: |
  Please provide details of author contributions here.

## Remove this if not required
conflict_of_interest: |
  Please declare any conflict of interest here.

## Remove this if not required
funding: |
  Please provide details on funding

## Remove this if not required
disclaimer: |
  Please provide disclaimer text here.

## Remove this if not required
acknowledgements: |
  Please include your acknowledgments here, set in a single paragraph. Please do not include any acknowledgments in the Supporting Information, or anywhere else in the manuscript.

bibliography: sample.bib

## change to true to add optional line numbering
lineno: false

site: bookdown::bookdown_site
output: 
  bookdown::pdf_book:
    base_format: rticles::rsos_article
---

# Insert A head here

This demo file is intended to serve as a "starter file"" for articles submitted to the [Royal Society Open Science](http://rsos.royalsocietypublishing.org/) journal using `RMarkdown`.

Place `\EndFirstPage` at the point where the plain text on the first page stops. Warning: excess text will be hidden behind the copyright box. The example below contains line 1 to 19 in the code. Lines 14 to 17 are hidden behind the copyright box.

## Insert B head here

Subsection text here.

### Insert C head here

Subsubsection text here.

Line 1

Line 2

Line 3

Line 4

Line 5

Line 6

Line 7

Line 8

Line 9

Line 10

Line 11

Line 12

Line 13

Line 14

Line 15

Line 16

Line 17

Line 18

Line 19

\EndFirstPage

# Lists

* one
* two
* three

* fruits
    + apples
        - macintosh
        - red delicious
    + pears
    + peaches
* vegetables
    + broccoli
    + chard

## Citations

Blabla \cite{Lannes} blabla. Blabla \cite{HJ2} blabla. Blabla \cite{BF, Lannes} blabla. Blabla \cite{Benjamin1967, HJ2, HJ3, HP2} blabla.

### Headling level 3

Subsubsection text here.

# R code

R code can be added as usual. Note that syntax highlighting is not available. Fig. \@ref(fig:nice-plot) is a an example.


```text
#23456789012345678901234567890123456789012345678901234567890123456789012345
#       10        20        30        40        50        60        70     
summary(lm(mpg ~ disp, data = mtcars))
```

```
## 
## Call:
## lm(formula = mpg ~ disp, data = mtcars)
## 
## Residuals:
##     Min      1Q  Median      3Q     Max 
## -4.8922 -2.2022 -0.9631  1.6272  7.2305 
## 
## Coefficients:
##              Estimate Std. Error t value Pr(>|t|)    
## (Intercept) 29.599855   1.229720  24.070  < 2e-16 ***
## disp        -0.041215   0.004712  -8.747 9.38e-10 ***
## ---
## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
## 
## Residual standard error: 3.251 on 30 degrees of freedom
## Multiple R-squared:  0.7183,	Adjusted R-squared:  0.709 
## F-statistic: 76.51 on 1 and 30 DF,  p-value: 9.38e-10
```


```
##       mpg             cyl             disp             hp       
##  Min.   :10.40   Min.   :4.000   Min.   : 71.1   Min.   : 52.0  
##  1st Qu.:15.43   1st Qu.:4.000   1st Qu.:120.8   1st Qu.: 96.5  
##  Median :19.20   Median :6.000   Median :196.3   Median :123.0  
##  Mean   :20.09   Mean   :6.188   Mean   :230.7   Mean   :146.7  
##  3rd Qu.:22.80   3rd Qu.:8.000   3rd Qu.:326.0   3rd Qu.:180.0  
##  Max.   :33.90   Max.   :8.000   Max.   :472.0   Max.   :335.0  
##       drat             wt             qsec             vs        
##  Min.   :2.760   Min.   :1.513   Min.   :14.50   Min.   :0.0000  
##  1st Qu.:3.080   1st Qu.:2.581   1st Qu.:16.89   1st Qu.:0.0000  
##  Median :3.695   Median :3.325   Median :17.71   Median :0.0000  
##  Mean   :3.597   Mean   :3.217   Mean   :17.85   Mean   :0.4375  
##  3rd Qu.:3.920   3rd Qu.:3.610   3rd Qu.:18.90   3rd Qu.:1.0000  
##  Max.   :4.930   Max.   :5.424   Max.   :22.90   Max.   :1.0000  
##        am              gear            carb      
##  Min.   :0.0000   Min.   :3.000   Min.   :1.000  
##  1st Qu.:0.0000   1st Qu.:3.000   1st Qu.:2.000  
##  Median :0.0000   Median :4.000   Median :2.000  
##  Mean   :0.4062   Mean   :3.688   Mean   :2.812  
##  3rd Qu.:1.0000   3rd Qu.:4.000   3rd Qu.:4.000  
##  Max.   :1.0000   Max.   :5.000   Max.   :8.000
```

\begin{figure}

{\centering \includegraphics{RoyalSocietyOpenScience_files/figure-latex/nice-plot-1} 

}

\caption{The caption}(\#fig:nice-plot)
\end{figure}

