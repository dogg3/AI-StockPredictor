
[![github](https://cloud.githubusercontent.com/assets/17016297/18839843/0e06a67a-83d2-11e6-993a-b35a182500e0.png)][1][![linkedin](https://cloud.githubusercontent.com/assets/17016297/18839848/0fc7e74e-83d2-11e6-8c6a-277fc9d6e067.png)][3]


# AI-StockPredictor

AI-StockPredictor is an attempt to predict the stockmarket (S&P 500) with machine learning.

The dataset used was found on ‘Kaggle’. (https://www.kaggle.com/dgawlik/nyse) It is called “S&P 500 companies historical prices with fundamental data” and is posted by Dominik Gawlik, student at AGH, Krakow, Poland. 
The dataset consists of 4 different subsets. These are ‘prices.csv’, ‘prices-split-adjusted.csv’, ‘sequrities.csv’ and ‘fundamentals.csv’. The subsets we are concerned with are the ‘fundamentals.csv’ and ‘prices-split-adjusted.csv’. The fundamentals set is extracted from annual SEC 10K filings (2012-2016) and each entry has: the company ticker symbol, year and 76 key metrics such as gross margin, cash ratio and so on. The prices-split-adjusted entries are a company's daily prices adjusted for splits. Each entry consists of a date, ticker symbol, opening price, closing price, lowest price, highest price and the price volume. The entries In both subsets, except ‘ticker symbol’ and ‘date’, are continuous. 

## Year on Year price change
The price changes to predict are continuous in nature, but we have encoded the changes into labels of the intervals [min,-18], [-18,8], [-8,4], [4,max], so our task becomes a classification problem. As our dataset is small, we had to make sure that the amount of samples in each label was as close to equal as possible, because otherwise we would risk bias.


## Daily price change
The intention is to try to predict a price change between a day’s opening and closing price of the S&P 500. The target of the model is the next day’s price change. The prediction of the model is aimed to enhance trading with 1 day interval. Traders that hold positions over a day often bet in both directions: a price increase or a price decrease. As it is more interesting to predict in what direction the price goes, we will use the encoded version of the price change: negative and positive. Therefore, the problem becomes a classification problem.



## Installation

Jupyter notebook is needed to run.
Use the package manager [pip](https://pypi.org/project/jupyter/) to install foobar.

```bash
pip install jupyter
```

## Usage

To open the preprocessing files run.

```bash
jupyter notebook preprocessing_daily_prices_newest_.ipynb
jupyter notebook preprocessing_fundamentals_newest.ipynb
```

To open the machine learning files run.

```bash
jupyter notebook classification_fundamentals_newest.ipynb 
jupyter notebook daily_prices_RNN.ipynb
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)


[1]: http://www.github.com/dogg3
[2]: https://www.linkedin.com/in/doggeland
