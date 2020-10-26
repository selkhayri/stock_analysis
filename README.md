# Stock Analysis

# Aim
The aim of this project is to refactor an existing stock analysis process in order to optimize the code and make it run faster.

In order to achieve this goal, an AB test was setup. Two excel sheets were compared, with one having the pre-existing code and one with the refactored code. The code from the two sheets is run, capturing the execution time of each sheet.

## Additional functions
<ul>
    <li>AllStocksAnalysis_v2</li>
    <li>ClearStockAnalysisWorksheets</li>
    <li>ProcessYear</li>
    <li>getTickerCount</li>
</ul>


## Description of new processing
## AllStocksAnalysis_v2

### Refactored pseudocode

<pre>
Determine tickerCount = number of ticker symbols
Define ticker, startingPrice, endingPrice, and totalVolume arrays of size tickerCount 
Define ticker_index = 0

For each row in the data set
    if the current ticker symbol <> the row ticker symbol
        if the row <> 2, which has no previous ticker symbol
            endingPrice(ticker_index) = price from the previous row
            increment the ticker_index counter by 1
        end if

        ticker symbol(ticker_index) = symbol of the current row
        starting price(ticker_index) = price of the current row
    end if

    increment the totalVolume of the current ticker symbol
next
</pre>

## ClearStockAnalysisWorksheets
Clear the sheets "All Stock Analysis" and "All Stock Analysis 2"

## ProcessYear

* Prompts the user for the year to process
* Runs both AllStockAnalysis and AllStockAnalysis_V2
* Determines the elapsed time for each and record it on the respective
worksheets
* Calls Formatting to format each of the worksheets
</pre>

## Results

<table>
    <tr>
        <th>Code</th>
        <th>Processing time (seconds)</th>
    </tr>
    <tr>
        <td>Old</td><td>0.53125</td>
    </tr>
    <tr>
        <td>Refactored</td><td>0.046875</td>
    </tr>
</table>
