![](bg1.png)

Authors
--------------------------------------------------------

David Kane, dave.kane at gmail.com

Ziqi Lu, ziqi.lu at williams.edu

Karan Tibrewal, karan.tibrewal at williams.edu

Fan Zhang, fan.zhang at williams.edu

Miller Zijie Zhu, zijie.zhu at williams.edu

About
-----------------------------------------------------------------------

`backtestGraphics` package creates an interactive graphical interface to visualize backtest results
for different financial instruments, including but not limited to equities, futures, and credit default swaps. The package does
not run backtests, but instead displays the backtest results graphically. Available summary statistics include average gross market value, cumulative profit and loss, sharpe ratio, top three drawdowns, etc. Available plots include cumulative and point-in -time profit and loss, and gross and net market value, etc. `backtestGraphics` also support backtest results with different strategies, substrategies, and overlapping portfolios, if the necessary columns are provided. 

Installation
----------------------------------------------------------------------------------------------------
You can easily install `backtestGraphics` by typing:

    install.packages("backtestGraphics")
or

    library(devtools)
    install_github("knightsay/backtestGraphics")

Usage
----------------------------------------------------------------------------------------------------
The package comes with three sample data frames: `commodity`, `equity`, and `credit`. These are backtest results for commodity futures, equities, and credit default swaps (CDS), respectively. We use these data frames to demonstrate the capabilities of the `backtestGraphics` package. (Note: The user may also use her own data frame, as long as it adheres to the format specified in the documentation).

As an example, let us look at `backtestGraphics` at work for the `commodity` data frame. Type the following command, and click the "Visualize" button on the Shiny interface returned by the function call. 


    library(backtestGraphics)
    backtestGraphics(x = commodity)


Maintainer
----------------------------------------------------------------------------------------------------
Miller Zijie Zhu, zijie.zhu at williams.edu

