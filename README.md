# GREEN STOCK ANALYSIS FOR THE YEAR 2017 AND 18

## OVERVIEW OF THE PROJECT
This analysis is done in order to determine which stock out of a list of green stocks is the best one to invest in by finding the yearly return on the stocks for the year 2017 and 2018. The purpose of this challenge is to refactor the code and make it more efficient so that it would take less time to run this code and it would consume less of memory.

## RESULT
### STEPS THROUGH THE CODE
In this analysis we determined the total daily volume and the yearly return for each stocks by looping over each row to get the data for each day of the year. In the beginning of the code and at the end we used the timer to measure the total time it took to ran the code. 

1. We formed an array for ticker values:

> ![image](https://user-images.githubusercontent.com/86074187/124403768-edda1700-dd05-11eb-8f79-074f410831d5.png)

2. The tickerindex count is set to 0. This is used as the index value for ticker array to add total daily volume for the each ticker. And also tickerindex is used to find the ticker starting price and ticker ending price for each ticker.

> ![image](https://user-images.githubusercontent.com/86074187/124404430-e6683d00-dd08-11eb-8b87-9841588623be.png)


3. We also initiated a tickerVolume array with 12 elements in it and set the initial  tickervolume counter for each element to 0. This is done so as the code is looping through the rows, it would add the daily volume for that row to the total calculated daily volume so far.

> ![image](https://user-images.githubusercontent.com/86074187/124404469-0b5cb000-dd09-11eb-994a-638f16876fc4.png)
> ![image](https://user-images.githubusercontent.com/86074187/124404524-4b239780-dd09-11eb-9d0e-e93f9d9dddf5.png)


4. To calculate the ticker starting price, we used if condition to check if the ticker value for the previous row is equal to the ticker value of the current row or not. If it is not equal then the close value in cells(i,6) will be equal to tickerStartingPrice.

> ![image](https://user-images.githubusercontent.com/86074187/124404543-5d9dd100-dd09-11eb-9c39-0058f5654d30.png)


5. To calculate the ticker ending price, we used if condition to check if the ticker value for the next row is equal to the ticker value of the current row or not. If it is not equal then the close value in cells(i,6) will be equal to tickerEndingPrice.

> ![image](https://user-images.githubusercontent.com/86074187/124404559-6ee6dd80-dd09-11eb-8d02-7dfd16c5e7d9.png)

6. Next step is to increase the tickerIndex by 1. For that we used the if condition to check if the ticker value for the current row is the same as ticker value for the previous row by using the same tickerIndex and also check if ticker value for the next row is equal to the ticker value of the current row or not. If not, it would increase the ticker index by 1 and if it is the same, it will iterate over the next row adding in the total daily volume and searching for the ticker ending price.

> ![image](https://user-images.githubusercontent.com/86074187/124404574-7e662680-dd09-11eb-9695-67e9736c0205.png)

7. Once the code has ran through all the rows, we printed the Ticker values in column A, Total Daily Volume in Column B and Yearly Return in Column C.

> ![image](https://user-images.githubusercontent.com/86074187/124404595-8f169c80-dd09-11eb-8f9e-5775703c9b9d.png)

8. Finally, we used formatting to made the headers bold, add borders to the  headers, autofit the text in cells, color the interior of cells green for positive yearly return and red for negative yearly return.

> ![image](https://user-images.githubusercontent.com/86074187/124404698-0b10e480-dd0a-11eb-8b6d-cbd18f0064bd.png)

### OUTPUT
**Analysis**

<img width="411" alt="Output analysis Refactored" src="https://user-images.githubusercontent.com/86074187/124404998-47911000-dd0b-11eb-9a98-42d26c607ae1.png">

**Code Performance for Refactored Code**

<img width="347" alt="Code performance refactored" src="https://user-images.githubusercontent.com/86074187/124405106-ab1b3d80-dd0b-11eb-9c40-0804f3356798.png">

**Code Performance for Initial Code**

<img width="320" alt="Code Performance original" src="https://user-images.githubusercontent.com/86074187/124405367-6d6ae480-dd0c-11eb-9799-3caa5bf952aa.png">

## SUMMARY


