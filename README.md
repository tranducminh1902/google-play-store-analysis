# Google Play Store Analysis
An analysis on how to be successful when developing app on Google Play Store

## About the data:
Data source - Kaggle:
- [Google Play Store Apps](https://www.kaggle.com/gauthamp10/google-playstore-apps): 645.13 MB - 24 columns - 2,312,944 rows
- [Google Play Store User Review](https://www.kaggle.com/lava18/google-play-store-apps): 7.31 MB - 5 columns -  64,296 row

According to the author, the data was collected with the help of Python and Scrapy running on a cloud vm instance on June 2021.

## About the notebook:
[Google_Play_Store_Analysis.ipynb](https://github.com/tranducminh1902/google-play-store-analysis/blob/main/Google_Play_Store_Analysis.ipynb)

The notebook was used to clean data and analyse whether to focus on Game or Application on Play Store.

### Cleaning Dataset:
1. Remove Unwanted Data
- Drop columns ['Installs', 'Minimum Installs','Minimum Android','Developer Website','Developer Email', 'Privacy Policy']
2. Check/Change Data Type
- Change column 'Size' datatype to float and sync Size unit
- Change column 'Released' and 'Last Updated' to timestamp
- Change all boolean value to 0 & 1 (False/True)
- Change Scrapped time datatype and calculate App Age
3. Working With Missing Values
- App name: 2 null values
- Rating/ and Rating Count: 22883 null values
- Currency: 135 null values
- Size: 74973 null values
- Developer ID: 33 null values
- Released: 71053 null values
4. Handling Duplicated Values
- Remove 4418 duplicated values
5. Handle Mislabeled & Corrupted Data
- Create more precise main category column
- Currency column
- 'Unrated' values in 'Content Rating'
- Fix Release and Last Update date
- Fix those app Price = 0 but not free app
- Calculate App Age column and Install Per Year column
6. Descriptive Statistics, detect and handle outliers
- Dealing with pre-installed apps (with external info get from Wikipedia, stored as excel file: [Play Store Pre-installed apps.xlsx](https://github.com/tranducminh1902/google-play-store-analysis/blob/main/Play%20Store%20Pre-installed%20apps.xlsx))
7. Data Cleaning - User Review
### Exploratory Data Analysis:
- Application
- Game
- User Review
### Report - Choosing between App or Game
Criteria to compare:
- Install/App Count Ratio
- Median Rating	
- Ad Supported Rate	
- Paid percentage

Conclusion: All the criteria are better when developing a Game compared to Application

## About the report:
[Google_Game_Report.pdf](https://github.com/tranducminh1902/google-play-store-analysis/blob/main/Google_Game_Report.pdf)

From the result of the notebook, we focus on Game sector on Google Play Store, to analyse how to be more successful when developing a game.

The report was prepared using Google Data Studio. Link to the report platform: https://datastudio.google.com/s/kSbHtt5XPME

## Contributions and References:
Contributions:
- Minh Tran: https://github.com/tranducminh1902
- Tam_Tran: https://github.com/tamtridung
- Thi-Quang: https://github.com/Thi-Quang
- Trung Nguyen: https://github.com/nguyenZzzz

References:
- Gautham Prakash: https://www.kaggle.com/gauthamp10
- Lavanya: https://www.kaggle.com/lava18
