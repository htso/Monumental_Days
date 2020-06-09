# A Monumental Day in the Stock Market
## -- Jun 5, 2020

### Introduction

Today is a monumental day in the history of stock market. The Nasdaq 100 index, which represents some of the biggest companies in the world, has just completed a round trip. Starting from a record high on Feb 20, it crashed 28% into a bear market, troughed on Mar 19, and rose all the way back to a new record high today. All that happened in 76 days. That's just a little longer than one quarter, and crossed over the reporting period of a typical money manager. With the economy in the dump and corporate earnings disappearing, how could this happen?

![Fig1](plots/NDX_jun2020.png)

Let's not worry about fundamentals for a moment[1] and focus on one "technical" aspect : the fundamental law of bear market progression.

A month ago there was a chorus of bears calling for the market to fall; they were made with a degree of conviction rarely seen in the investment advisory business. One headline reads "_The Crash Has Only Just Begun_(Apr 28)"[2]. Another told investors "_How To Trade a Second Coronavirus Stock Market Crash_(May 5)"[3]. And their reasons are well articulated -- "_4 Reasons Why The Market Will Dive Again_(May 4)"[4]. 

All of these pieces relied on one central belief that a bear market must have three phases. It starts with a sharp decline of more than 20%, to be followed by an equally sharp rebound, then drifts lower until the previous low is "retested". It is only after this "retesting" phase fully played out could a bear market end. Up till now we definitely do not have the last part.

So, is this really unprecedented? 

### No Historic Precedent

Let's look at the data. I coded a R script that searches for similar pattern in historic data. I ran it on the major market indices available on [yahoo finance](https://finance.yahoo.com/), including the amazing 92 years of S&P 500 since 1927, 49 years of Nasdaq Composite, the history of the British market, the German market, and 10 other stock markets around the world [5]. 

Finding : Nothing like this has happened before. No previous example of a drop and then a complete recovery inside four months. There has been some highly volatile trajectories in Nasdaq. The closest ever to a round trip was the path in second half of 2001, during Dot-com Bubble. I'll discuss some coding detail in the last section.

### How is it possible?

I have three observations/hypotheses that I find useful to make sense of what's been happening in the stock market. 

This coronavirus pandemic has created some highly visible damage to the economy. Unlike the subprime crisis in 2008 where the initial impact showed up in some obscure corner of Wall Street, this crisis feels very real. People all over the world could see their neighborhood shops and restaurants closed down. Many people lost their jobs. The fear generated by the shutdown is felt in a broad spectrum of the society. 

As human we have this cognitive mechanism that responds to visible stimulus by taking action. With convenient access to brokerage account, it's so easy to sell everything. One push of a button and you are all in cash and you feel safe. 

So, my first hypothesis is that behavorial bias played a role. Many long term investors might have sold into the decline in the March. As economic data continue to show the enormous damage in the real economy, few of them have moved back into stocks. The market is going up to make sure these people would buy back at some point, at higher prices. 

The second hypothesis is about the changing mix of stock market participants. It is well documented that as much as 90% of the volume in a typical day is from HFT algorithms taking advantge of some nanosecond price movements. These algorithms don't know and don't care about long term price patterns based on century-old theory of market cycle. An index level such as the 61.8% Fibonacci retracement has no significance to these machine learning models trained on level-agnostic return data. Very few machine learning models could learn directly from level data because stock prices are inherently nonstationary and are therefore difficult to learn.

However, I do not dismiss the usefulness of level data. With enough level data, a good model could be trained to make long term prediction. 

And that brings me to my third observation : the belief about how a bear market should behave has very little statistically support. And that is because we have very few data points available to evaluate any hypothesis of the sort akin to the Dow theory. Over the last one hundred years, there were just six bear markets ever occurred in the US, and less than 20 over the developed world[5]. Many of the bear markets lasted a very short time, such as the stock market crash in 1987. And some of them are double-counts. Any model built from 10 or 20 data points would have little statistical signficance and a large margin of error. 

Therefore, as we're witnessing at the moment, a bear market does not need a third leg down to retest the previous low. Any stretegy relying on such a pattern would suffer enormous variance.



### Pattern Search Algorithm


 
### Data Sources
Yahoo finance.  

### Install Software
To install R, press Ctrl+Alt+T to open a terminal

    sudo apt-get update 
    sudo apt-get install r-base

### Dependencies
Code has been tested on 
* R 3.6.0
* Ubuntu 18.04 


### Contact
To ask questions or report issues, please open an issue on the [issues tracker](https://github.com/htso/Monumental_Day/issues).


References

[1] For a fundamental perspective, I refer the reader to the [piece](https://github.com/htso/bear_market) I wrote during the darkest days of the March selloff.

[1] https://seekingalpha.com/article/4340437-crash-only-just-begun

[2] https://seekingalpha.com/article/4342960-how-to-trade-second-coronavirus-stock-market-crash

[3] https://seekingalpha.com/article/4342645-4-reasons-why-market-will-dive-again

[4] https://seekingalpha.com/article/4342157-continued-selling-for-next-week-losses-set-next

[5] The `quantmod` package in R is amazing; it has the capability to pull large amount of historic time series with one function call. In R command line, type `?getSymbols`.

[6] https://en.wikipedia.org/wiki/List_of_stock_market_crashes_and_bear_markets



