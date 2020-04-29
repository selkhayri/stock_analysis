# stock_analysis_challange
Stock Analysis Challenge

# Challenge
## Unchanged Subroutines (from course material)
<ul>
    <li>AllStocksAnalysis</li>
    <li>DQAnalysis</li>
    <li>checkerboard</li>
    <li>Formatting</li>
    <li>MacroCheck</li>
    <li>Ones_A1_to_J10</li>
    <li>Sums_A1_to_J10</li>
    <li>Sums_A1_to_MN</li>
</ul>

## New Subroutines
<ul>
    <li>AllStocksAnalysis_v2</li>
    <li>ClearStockAnalysisWorksheets</li>
    <li>ProcessYear</li>
    <li>getTickerCount</li>
</ul>


## Description of new processing
## AllStocksAnalysis_v2
<p>  
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
<pre>
Prompts the user for the year to process
Run both AllStockAnalysis and AllStockAnalysis_V2
Determine the elapsed time for each and record it on the respective
worksheets
Calls Formatting to format each of the worksheets
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
        <td>Refactored</td><td></td>
    </tr>
</table>