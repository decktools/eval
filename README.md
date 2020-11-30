# Deck's forecast & model evaluations

:wave:&nbsp;&nbsp;Hi there! [Deck](https://deck.tools) is a product that helps Democratic campaigns run more efficient and effective programs. 

Toward that end, we make predictions about which voters will turnout to vote in a given election, support a given candidate, make financial contributions, and more. We also use these predictions to predict a range of likely outcomes.

We plan to use this repo to share evaluations of our predictions. And this README will explain the files we've included.

### Table of contents:
- Forecast accuracy (`forecast-error.csv`)
- Score accuracy (`survey_validation_nc_2020.csv`)


## Forecast accuracy

In `forecast-error.csv`, we share the forecasts we've published since 2019 alongside actual results and the mean absolute error of our forecasts. On average, our forecasts have been off by 3.7% and 95% of our forecasts have fallen within our 95% confidence interval.

One common question we get is whether our forecasts are more accurate in larger districts. Our evaluation data shows us that district size is not a factor in our accuracy:

**Mean absolute forecast error by district size**
| District type  | Mean absolute error |
| --- | :---: |
| Statewide  | 3.6%  |
| US House  | 3.9%  |
| State Senate  | 3.5%  |
| State House  | 3.7%  |

However, there are races where our forecasts perform better! For example, here's a breakdown by the size of the margin of victory:

| Margin size  | Mean absolute error |
| --- | :---: |
| Less than 5%  | 3.3%  |
| 5% to 10%  | 3.4%  |
| 11% to 20%  | 3.5%  |
| 21% to 40%  | 3.9%  |
| More than 40%  | 4.1%  |

Often, when our forecasts miss badly, it's because of a bug in the data we're applying our forecasting models to -- such as mislabled media data or mismatched finance data. If you see any interesting patterns while inspecting this evaluation data, please let us know!

More details on our blog: 
- [The role we played in the 2020 election](https://medium.com/obso-deck/the-role-we-played-in-the-2020-election-d7cc772d10c7?source=friends_link&sk=c289145d2f8c850e6ccda840c50f9593)
- [Is Deck accurate?](https://medium.com/obso-deck/is-deck-accurate-bcd250a243d2?source=friends_link&sk=c200616db031075fffc835f0d52d760f)

## Score accuracy

In `survey_validation_nc_2020.csv`, we share data from a validation exercise we did with data from a YouGov survey of voters in North Carolina re: who they would vote for in the 2020 contests for US President, US Senate, and US House.

Below, you can see which share of survey respondents in one of five Deck support score buckets indicated support for a given Democratic candidate. In most cases (except in very low sample size buckets, as indicated by the parenthetical), the share of survey respondents indicating support falls squarely within the expected Deck probability range.

![](https://miro.medium.com/max/662/1*-zrU-jXw7e93y8ThTrxHNg.png)

We also took a look at how our scores predicting support for Cal Cunningham compared with survey-based Democratic Party support scores from another vendor. As shown in the area under the curve and gains charts below, we found that our scores were more precise.

Against the YouGov responses, our scores had an area under the curve of 0.96, mean squared error of 0.10, accuracy of 0.87, sensitivity of 0.91, and specificity of 0.84.

More details on our blog: 
- [How we predict which candidates a voter will support](https://medium.com/obso-deck/how-we-predict-which-candidates-a-voter-will-support-6b4f489b36b8?source=friends_link&sk=94de8e58286deaa1ac5a6fa47fb7428c)
- [Our 2020 VBM models](https://medium.com/obso-deck/our-2020-vbm-models-8b6384722a5e?source=friends_link&sk=88ecc37d79f859f3c7d87313de69fd03)
