
---
- title: "Backtest Graphics"   
- authors: 
  - name: David Kane
    email: david.kane@gmail.com
    affiliation: Harvard University
  - name: Ziqi Lu
    email: ziqi.lu@williams.edu
    affiliation: Williams College
  - name: Karan Tibrewal
    email: karan.tibrewal@williams.edu
    affiliation: Williams College
  - name: Fan Zhang
    email: fan.zhang@williams.edu
    affiliation: Williams College
  - name: Miller Zijie Zhu
    email: zijie.miller.zhu@gmail.com
    affiliation: Williams College    
- date: 30th May 2016
- bibliography: paper.bib    

---

![](bg1.png)

###Summary

Backtesting is the process of testing trading strategies on prior time horizons to measure the effectiveness of a given strategy. It helps investors understand and optimize their trading strategies. The **Backtest Graphics** package provides an interactive **Shiny** interface to visualize backtest results for a variety of financial instruments (equities, futures , and credit defualt swaps, among others). These visualizations enable users to employ their human perception to process a lot of backtest data quickly and approximately. 

It is important to note here that **Backtest Graphics** doesn't run backtests, but instead provides graphical visualization of backtest results. To illustrate this subtle distinction, consider a simple trading strategy that buys the top 10 shares of the S&P 500, and shorts the bottom 10. Now, to test how the strategy performs historically, the user may use backtesting software like **Quantopia**, or even  R packages like **backtest**.The output from such backtesting is generally in the form of large dataframes which are difficult to interpret. As of such, the user may feed these dataframes, i.e. the holding data, to **backtestGraphics**. The package then constructs interactive **dygraph** plots, and calculates essential summary statistics which are easy to interpret and explore. 

The **Shiny** interface returned by the package consists of a sidebar panel that includes a "Summary" and a "Detail" tab. The former provides the user with summary statistics, such as average gross market value (GMV), number of instruments, cumulative and annualized profit and loss (P&L), Sharpe ratio and best and worst performing months. The "Detail" tab provides information about the best and worst performers, as well as the biggest drawdowns. 

The main panel of the **Shiny** interface houses interactive plots for cumulative and point-in-time P&L, NMV, GMV and number of contracts. The user can learn the response variable at a given point in time for any of these plots by hovering the mouse on the specified point in time. Additionally, the user can also zoom into a time period by dragging the mouse. Radio buttons at the bottom of the plots allow the user to seamlessly switch between plots. Below is a screen shot of the plots: 

![](vignettes/img/plots.png)

Additionally, to accomodate for more complex backtests, **Backtest Graphics** allows the user to subset seamlessly between overlapping portfolios, and multiple strategies and sub-strategies. For example, suppose the user splits his portfolio into two halves: the first half trades using the aforementioned trading strategy on a weekly basis, while the second uses the same strategy on a bi-weekly basis. Although these strategies overlap every other week, the user may want to explore how a particular strategy does in isolation. In order to do so, the user simply has to select the appropriate options from the dropdown menus, and click visualize. 

![](vignettes/img/dropdown.png)

In order to see **Backtest Graphics** in action, please visit [here](https://backtestgraphics.shinyapps.io/backtestGraphics)!

###Installation

You can easily install backtestGraphics by typing:

    install.packages("backtestGraphics")
or

    library(devtools)
    install_github("knightsay/backtestGraphics")

