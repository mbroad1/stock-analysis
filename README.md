# Module 2 VBA Challenge: Analyzing Stocks
---
## Overview of Project
### Background:
Steve is helping his parents in choosing the right green energy stocks to invest in by using data evaluating the stocks' performances in previous years. He believes that there are two factors to look for when deciding whether to invest in a stock: 1) a high total daily volume meaning that the stock is traded on a regularly (the prices of stocks that are traded more frequently are thought to be more accurate than those of stocks traded rarely) and 2) the stock's price increased by the end of the year in comparison to the start of the year. Using VBA, we can help Steve evaluate these factors in two different fiscal years, 2017 and 2018, for twelve green energy stocks.
### Purpose:
The purpose of this analysis is to evaluate the yearly trends in stocks with code that is refactored so that it is more efficient and faster in executing the analysis. With the code that was originally made in Module 2, it is good for analyzing a relatively small number of stocks which means that if more stocks were to be analyzed, then the analysis would take much longer. Therefore, refactoring the code will reduce the analysis time and make the analysis more efficient to be used in the future. We will analyze the differences in timing to execute the code using the timer function in VBA on both modules created.

Likewise, we want to evaluate the differences in stock performances between 2017 and 2018 and see which stocks are steady in their increase and the stocks that are declining in price from 2017 to 2018. This information will help inform Steve and his parents on which green energy stocks are the best to invest in.

---
## Results
### Refactoring:
The code was refactored so that data from both 2017 and 2018 could be accessed without having to repeat the code made initially in the module.
#### yearValue Variable Example 1:
![Refactoring #1.1](https://github.com/mbroad1/stock-analysis/blob/main/VBA%20Challenge%20Resources/Refactoring%20%231.1.png)
#### yearValue Variable Example 2:
![Refactoring #1.2](https://github.com/mbroad1/stock-analysis/blob/main/VBA%20Challenge%20Resources/Refactoring%20%231.2.png)
As you can see in the above images of code, initializing the variable "yearValue" makes it so that the user can input either 2017 and 2018 to generate the analysis specifically for that year. Unlike this refactored code, the original code activated the 2018 worksheet so that all analyses were done with just that worksheet; therefore, in order to analyze the 2017 worksheet, we would have to copy and paste the code activating the 2017 worksheet for this piece of code. However, copying and pasting this code causes a longer analysis time because VBA would have to run through this same code block for 2017 and 2018 meaning that it is running through it twice.
#### Original Code Time for 2017:
![VBA_Challenge_Original_2017](https://github.com/mbroad1/stock-analysis/blob/main/VBA%20Challenge%20Resources/VBA_Challenge_2017_Original.png)
#### Original Code Time for 2018:
![VBA_Challenge_Original_2018](https://github.com/mbroad1/stock-analysis/blob/main/VBA%20Challenge%20Resources/VBA_Challenge_2018_Original.png)
The above images are the times that it took for the original code to run for 2017 and 2018, respectively.
#### Refactored Code Time for 2017:
![VBA_Challenge_2017](https://github.com/mbroad1/stock-analysis/blob/main/VBA%20Challenge%20Resources/VBA_Challenge_2017.png)
#### Refactored Code Time for 2018:
![VBA_Challenge_2018](https://github.com/mbroad1/stock-analysis/blob/main/VBA%20Challenge%20Resources/VBA_Challenge_2018.png)
Differently from the original code times, the refactored code times are faster. Originally, it took about 0.59 seconds to run the analysis for the 2017 worksheet. With the refactored code, the 2017 analysis can be done in 0.56 seconds. Likewise, the original code made to analyze the stock performance in 2018 was about 0.59 seconds. Differently, with the refactored code, the 2018 analysis can be done in about 0.55 seconds. Although the time difference may seem insignificant, if there were more than 12 stocks being analyzed (such as over 1000 stocks), this refactored code would save a significant amount of time.

### Stock Analysis:
Shown below are the analyses done for the stock performances in 2017 and 2018, respectively.
#### 2017 Stock Analysis:
![VBA_2017_Stock_Result](https://github.com/mbroad1/stock-analysis/blob/main/VBA%20Challenge%20Resources/VBA_2017_Stock_Result.png)
#### 2018 Stock Analysis:
![VBA_2018_Stock_Result](https://github.com/mbroad1/stock-analysis/blob/main/VBA%20Challenge%20Resources/VBA_2018_Stock_Result.png)

In 2017, all of the stocks, except TERP, increased in value relative to their starting price that year. The stock that increased the greatest in price at its end of year was DQ with a growth of 199.4%. However in terms of total daily volume, the most traded stock was SPWR with a total daily volume of 782,187,000. TERP, the only stock that decreased in value relative to its starting price in 2017, decreased by 7.2%.

However, the 2018 analysis reveals a drastic shift in pattern from the 2017 analysis. In 2018, only two stocks, ENPH and RUN, increased in price at the end of the year relative to their price at the start of the year, with increases of 81.9% and 84%, respectively. Unlike in 2017, DQ was the stock that decreased the most in value by the end of the year with a 62.6% overall decrease in selling price. Interestingly, in 2018, the stock with the greatest total daily volume was ENPH with 607,473,500 as the total daily volume. 

Looking at the data, we can see that stocks like ENPH and RUN have greater total daily volumes in 2018 than those of 2017, and their stock prices positively correlate with an increase in total daily volume as their stock prices increased by the end of 2018. Differently, stocks that had smaller total daily volumes in 2017 than 2018 like SPWR and AY decreased in stock price by the end of 2018 in comparison to 2017 when they were increasing relative to the start of the year. Therefore, we can conclude that there is a strong relationship between total daily volume and return.

---
## Summary

### 1) What are the advantages and disadvantages of refactoring code in general?

#### Advantages:
- Refactoring code makes the code more efficient and maintainable.
- The function of the code remains the same making it very convenient to use in multiple applications.
- Refactoring helps avoid "code rot" which can result in duplicate code and programming discrepancies that can be hard to debug.
- Refactoring helps to clean up the code, and thus improves the presentability and quality of the code itself.

#### Disadvantages:
- If you are trying to refactor code that was taken from an outside source, you may not understand the code and thus could mess up the function of the code during refactoring.
- Refactoring, in general, could affect the testing outcomes.

### 2) What are the advantages and disadvantages of the original and refactored VBA scripts?

Although the refactored code is faster than the original code, one advantage of the original code is that since it directly refers to one dataset, the one of 2018, it may be easier to interpret and follow since only one worksheet is involved. However, the fact that the 2018 worksheet is the only dataset included in the original VBA script makes it so that it is disadvantageous since deeper data analysis like also analyzing the 2017 dataset is unable to be executed in the script. Another disadvantage of the original VBA script is that if more stocks were to be analyzed, like over 1000 stocks, then the code would execute much more slowly than the refactored VBA script.

On the other hand, one advantage of refactoring the original VBA script was that the function of the original code stayed the same, but the refactored code made it so that either the 2017 or 2018 datasets could be accessed, not just the 2018 dataset like in the original VBA script. Another advantage of refactoring the VBA script is that the code reads cleaner and is more succinct in its function. However, a disadvantage of the refactored VBA script could be that when looked at at a later time point, the refactored adjustments in the script may not make sense so when trying to add or change the script, the code's function may change or may not work in general. Therefore, one must be careful and diligent in making comments in their code, especially when refactoring, so that they can understand the function behind the code at a later time point.
