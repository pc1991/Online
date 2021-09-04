# Online Shoppers Purchasing Intention Dataset 

(Courtesy: Akash Patel of Kaggle)

# Context Data Set Information:

The dataset consists of feature vectors belonging to 12,330 sessions. The dataset was formed so that each session would belong to a different user in a 1-year period to avoid any tendency to a specific campaign, special day, user profile, or period.

# Content: 

The dataset consists of 10 numerical and 8 categorical attributes. The 'Revenue' attribute can be used as the class label.

"Administrative", "Administrative Duration", "Informational", "Informational Duration", "Product Related" and "Product Related Duration" represent the number of different types of pages visited by the visitor in that session and total time spent in each of these page categories. The values of these features are derived from the URL information of the pages visited by the user and updated in real time when a user takes an action, e.g. moving from one page to another. The "Bounce Rate", "Exit Rate" and "Page Value" features represent the metrics measured by "Google Analytics" for each page in the e-commerce site. The value of "Bounce Rate" feature for a web page refers to the percentage of visitors who enter the site from that page and then leave ("bounce") without triggering any other requests to the analytics server during that session. The value of "Exit Rate" feature for a specific web page is calculated as for all pageviews to the page, the percentage that were the last in the session. The "Page Value" feature represents the average value for a web page that a user visited before completing an e-commerce transaction. The "Special Day" feature indicates the closeness of the site visiting time to a specific special day (e.g. Mother’s Day, Valentine's Day) in which the sessions are more likely to be finalized with transaction. The value of this attribute is determined by considering the dynamics of e-commerce such as the duration between the order date and delivery date. For example, for Valentina’s day, this value takes a nonzero value between February 2 and February 12, zero before and after this date unless it is close to another special day, and its maximum value of 1 on February 8. The dataset also includes operating system, browser, region, traffic type, visitor type as returning or new visitor, a Boolean value indicating whether the date of the visit is weekend, and month of the year.

# Acknowledgements: 

Sakar, C.O., Polat, S.O., Katircioglu, M. et al. Neural Comput & Applic (2018).

Inspiration Education is the most powerful weapon which you can use to change the world. 😃

https://github.com/pc1991/Math-Adventures/projects/1#card-67733963

https://github.com/pc1991/Math-Adventures/blob/ecdcc8423413436fb81b0137d2b45a89882cdea4/Fitted%20vs%20Residuals%20in%20Original%20Linear%20Model%20for%20Online.png

# Fitted vs. Residuals on Online Linear Model

For the original linear model, the majority of the fitted values are not dispersed within the line. A general linear model may be more favorable.

![Fitted vs Residuals in Original Linear Model for Online](https://user-images.githubusercontent.com/87962854/131275135-58c3271d-0da4-470b-802b-10ce17d4f756.png)

# QQ Plot for Residuals in Online Linear Model

![QQ Plot for Residuals in Online Linear Model](https://user-images.githubusercontent.com/87962854/131276620-790e86c4-b948-41a1-84f0-3705a20788d9.png)

For the quantile-quantile plot with this original model, the fit is mainly accurate throughout.

# Half-Normal Plot of the Online Linear Model

![Half-Norm Of The Online Linear Model](https://user-images.githubusercontent.com/87962854/131276648-51f9c129-e2aa-406c-9a1c-f3e4113e2f5e.png)

The half-normal probability graph basically proves the importance of how viable this model is.

# Box-Cox Method of Online Linear Model

![Box-Cox Method Of Online Linear Model](https://user-images.githubusercontent.com/87962854/131277794-7e87247f-4939-49d9-bb05-d0ae19185223.png)

The Box-Cox graph shows that many of the fitted values are not dispersed within the line.

# Half-Normal Plot for the First Online General Linear Model

![Half-Norm for 1st Online GLM](https://user-images.githubusercontent.com/87962854/131412251-92a8803f-7751-45aa-8379-e02eb1c69447.png)

The Half-Normal plot shows how accurate the original online general linear model is.

# Box-Cox Method of First Online General Linear Model

![Box-Cox for 1st Online GLM](https://user-images.githubusercontent.com/87962854/131423671-934fe31e-6db4-4f38-8d8e-6bdbf800dc6c.png)

For this Box-Cox graph, this first general linear model has more accuracy than the original online linear model.

# Quantile-Quantile Plot for the First Online General Linear Model

![QQ Plot for 1st Online GLM](https://user-images.githubusercontent.com/87962854/131423702-f882b806-dd78-48d2-a0f5-44d5a4e6c6c5.png)

This fit for this first general linear model is accurate throughout.

# Half-Normal Plot for the Second Online General Linear Model

![Half-Norm for Second Online GLM](https://user-images.githubusercontent.com/87962854/131423758-4f176960-068d-4809-bfc1-657fe1a692f5.png)

This Half-Normal plot shows how accurate the first original online general linear model is.

# Quantile-Quantile Plot for the Second Online General Linear Model

![QQ Plot for 2nd Online GLM](https://user-images.githubusercontent.com/87962854/131423971-9cd3cd00-c27e-4281-a174-940af9fb8c2d.png)

This fit for this second general linear model is accurate throughout.

# Correlation Matrix of the Relationship b/w Administrative Duration & Informational Duration

![Correlation Matrix of relationship between AD   ID](https://user-images.githubusercontent.com/87962854/131424006-e3186fca-2c1e-42fe-9e88-ebbd89cbb666.png) 

Please take note of the p-values in the next two scatter plots below.

# Scatter Plot Showing the Relationship b/w Administrative Duration & Informational Duration

![GG stats plot between AD   ID](https://user-images.githubusercontent.com/87962854/131424032-e7938bfc-0939-43da-88fc-4aaf7d9107e6.png)

# Correlation Matrix of the Relationship b/w Administrative & Informational

![Correlation Matrix of relationship between Informational and Administrative](https://user-images.githubusercontent.com/87962854/131424045-4ec20abe-7542-4063-bfe0-0fdf900cb6a9.png)

# Scatter Plot Showing the Relationship b/w Administrative & Informational

![GG Stats Plot between Informational and Administrative](https://user-images.githubusercontent.com/87962854/131424057-17750dfd-5ff8-4e59-ac57-3a305d577f8c.png)

# Now..... The Question Is.... Which Model Is The Most Efficient To Rely On To Predict The Future Trends?

We need to find the RMSE of each model.

>#Checking the linear and logarithmic root mean square errors of all the linear models#
>
> rmse <- function(x,y) sqrt(mean(x-y)^2)
> 
> rmse(g$fitted.values,online$Administrative_Duration)
> 
[1] 2.427661e-14

> rmse(g2$fitted.values,online$Administrative_Duration)
> 
[1] 7.759004e-08

> rmse(g3$fitted.values,online$Administrative_Duration)
> 
[1] 78.50344

> rmse(log(g$fitted.values),log(online$Administrative_Duration))
> 
[1] NaN

Warning message:

In log(g$fitted.values) : NaNs produced

> rmse(log(g2$fitted.values),log(online$Administrative_Duration))
> 
[1] Inf

> rmse(log(g3$fitted.values),log(online$Administrative_Duration))
> 
[1] Inf

# Conclusion

Overall, given the models that are ran, the original linear model is the most efficient with minimal error.

# Citations
> citation(package = 'readr')

  Hadley Wickham and Jim Hester (2020). readr: Read
  Rectangular Text Data. R package version 1.4.0.
  https://CRAN.R-project.org/package=readr

A BibTeX entry for LaTeX users is

  @Manual{,
    title = {readr: Read Rectangular Text Data},
    author = {Hadley Wickham and Jim Hester},
    year = {2020},
    note = {R package version 1.4.0},
    url = {https://CRAN.R-project.org/package=readr},
  }

> citation(package = 'faraway')


  Julian Faraway (2016). faraway: Functions and
  Datasets for Books by Julian Faraway. R package
  version 1.0.7.
  https://CRAN.R-project.org/package=faraway

A BibTeX entry for LaTeX users is

  @Manual{,
    title = {faraway: Functions and Datasets for Books by Julian Faraway},
    author = {Julian Faraway},
    year = {2016},
    note = {R package version 1.0.7},
    url = {https://CRAN.R-project.org/package=faraway},
  }

ATTENTION: This citation information has been
auto-generated from the package DESCRIPTION file and
may need manual editing, see ‘help("citation")’.

> citation(package = 'MASS')



  Venables, W. N. & Ripley, B. D. (2002) Modern
  Applied Statistics with S. Fourth Edition.
  Springer, New York. ISBN 0-387-95457-0

A BibTeX entry for LaTeX users is

  @Book{,
    title = {Modern Applied Statistics with S},
    author = {W. N. Venables and B. D. Ripley},
    publisher = {Springer},
    edition = {Fourth},
    address = {New York},
    year = {2002},
    note = {ISBN 0-387-95457-0},
    url = {https://www.stats.ox.ac.uk/pub/MASS4/},
  }

> citation(package = 'jmv')


  Ravi Selker, Jonathon Love and Damian Dropmann
  (2020). jmv: The 'jamovi' Analyses. R package
  version 1.2.23.
  https://CRAN.R-project.org/package=jmv

A BibTeX entry for LaTeX users is

  @Manual{,
    title = {jmv: The 'jamovi' Analyses},
    author = {Ravi Selker and Jonathon Love and Damian Dropmann},
    year = {2020},
    note = {R package version 1.2.23},
    url = {https://CRAN.R-project.org/package=jmv},
  }

ATTENTION: This citation information has been
auto-generated from the package DESCRIPTION file and
may need manual editing, see ‘help("citation")’.

Copyright (c) 2021 Robert (Christian) Paul & Akash Patel

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
