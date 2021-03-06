---
title       : "vizualizeReturns:"
subtitle    : R/Shiny application for vizualization of stocks and bonds performance (1871 - 2012)
author      : Sergey Bushmanov
job         : Coursera / JHU Data Products Project
framework   : io2012    # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [bootstrap, quiz]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Who <span style="color:CadetBlue"> vizualizeReturns </span> application is for:

- Everybody interested in long term performance of stocks and bonds
- Especially:  
  - Individuals making financial plans for retirement  
  - Financial advisors  
  - Pension funds  
  - Trusts and endowments  
  - Economists and financial journalists  

--- &twocol

## Why stocks and bonds?

- Stocks and Bonds are two distinct asset classes that usually form a significant part of any long-term investment portfolio

- Asset allocation between Stocks and Bonds is a cumbersome process (sometimes referred to as "investment art"), which among others relies on the following characteristics of the assets classes:

*** {name: left}
### Bonds 

- lower risks
- lower rewards

*** {name: right}
### Stocks  

- higher risks (measured by return volatility)
- higher reward (measured by average long-term returns)


--- 

## Stocks and Bonds exibit significant volatility


```r
load("./returnData.RData"); library(ggplot2)
qplot(data=subset(returnData, year %in% 2000:2009), x=year, y=return, 
      color=variable, geom="line") + labs(title = "Value of $1 invested in 2000 through 2009")
```

![plot of chunk unnamed-chunk-1](assets/fig/unnamed-chunk-1.png) 


---

## What's my next step?

- Try <span style="color:CadetBlue; font-weight: bold"> vizualizeReturns </span> application live together with accompanying **documentation** at
http://sbushmanov.shinyapps.io/returns/  

- Find reproducible code for shiny application at 
https://github.com/sbushmanov/shiny

- Find Github repository for this slide deck at
https://github.com/sbushmanov/shinyApp_slideDeck
