Linear Model on mtcars for an outcome of your choice 
========================================================
author: Hassan
date: 21-06-2014

Linear models can be confusing
========================================================


```r
data(mtcars)
library(caret)
my_model<- train(mtcars$mpg~., data = mtcars, method = "lm")
summary(my_model)
```

```

Call:
lm(formula = modFormula, data = data)

Residuals:
   Min     1Q Median     3Q    Max 
 -3.45  -1.60  -0.12   1.22   4.63 

Coefficients:
            Estimate Std. Error t value Pr(>|t|)  
(Intercept)  12.3034    18.7179    0.66    0.518  
cyl          -0.1114     1.0450   -0.11    0.916  
disp          0.0133     0.0179    0.75    0.463  
hp           -0.0215     0.0218   -0.99    0.335  
drat          0.7871     1.6354    0.48    0.635  
wt           -3.7153     1.8944   -1.96    0.063 .
qsec          0.8210     0.7308    1.12    0.274  
vs            0.3178     2.1045    0.15    0.881  
am            2.5202     2.0567    1.23    0.234  
gear          0.6554     1.4933    0.44    0.665  
carb         -0.1994     0.8288   -0.24    0.812  
---
Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

Residual standard error: 2.65 on 21 degrees of freedom
Multiple R-squared:  0.869,	Adjusted R-squared:  0.807 
F-statistic: 13.9 on 10 and 21 DF,  p-value: 3.79e-07
```



========================================================

Notice that it can be difficult to decipher all the information in above summary. Graphs, may be?

![plot of chunk unnamed-chunk-2](shiny_assignment-figure/unnamed-chunk-2.png) 

```
numeric(0)
```



What we need is a fancy app that does all of this on a single click
========================================================
The App uses

- the mtcars dataset
- caret package
- AppliedPredictiveModeling
- base Plot package



Voila!
========================================================

The App allows the user to

- choose an outcome from the list
- look at the predicted vs observed graph
- RMSE values for models
 
With the App, you can see all these relationships on the go, using any variable as an outcome from the database. 

