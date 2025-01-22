## Strategies for Stabilizing Tomato Prices in Nepal


### Project Motivation


The tomato industry plays a crucial role in Nepal’s economy, particularly for smallholder farmers who depend on year-round cultivation to support rural employment and meet market demands. Tomatoes are a key part of the Nepali diet, offering essential nutrients and contributing to food security due to their adaptability to various growing conditions.

However, tomato production in Nepal faces significant challenges, including price fluctuations, seasonal changes, and post-harvest losses caused by an inefficient supply chain and unpredictable weather. These challenges affect different types of tomatoes—Big Tomatoes and Small Tomatoes—in unique ways, as their prices and market dynamics often diverge. For instance, Big Tomatoes tend to have higher prices but are more volatile, while Small Tomatoes are relatively stable but may experience lower demand. Understanding these differences is essential for more accurate price forecasting and targeted interventions.

Improvements in price forecasting models can help stabilize incomes for farmers by reducing the uncertainty surrounding price trends for both Big and Small Tomatoes. Additionally, investments in infrastructure and technology can enhance supply chain efficiency, minimize post-harvest losses, and ensure better price stability for both varieties.

Despite these challenges, tomatoes—both Big and Small—hold significant export potential, particularly to neighboring countries. By addressing inefficiencies and improving market systems, Nepal can leverage this valuable crop to promote food security, enhance rural livelihoods, and drive economic stability.


### Project Objective

The goal of this project is to create a reliable framework for forecasting tomato prices in Nepal, specifically for Big Tomatoes and Small Tomatoes. By reducing price volatility, improving market predictability, and examining the relationships between tomato varieties, this project seeks to equip farmers, policymakers, and other stakeholders with the insights to make informed decisions and support key players in the Nepalese agricultural market.

Tomato prices in Nepal fluctuate unpredictably due to seasonality, external shocks, and supply chain inefficiencies, impacting farmer incomes, consumer affordability, and overall food market stability. Through accurate price forecasting and volatility analysis, this project aims to mitigate uncertainty, enabling farmers to plan production and harvest schedules effectively. Additionally, by supporting policymakers in developing market stabilization strategies, this study strives to establish a more secure and stable food market in Nepal.


### Methodology

To achieve these objectives, this study will employ a structured and multifaceted approach that combines exploratory data analysis (EDA), statistical forecasting models, and volatility analysis.

The project begins with data collection and preparation, using historical tomato price data obtained from local agricultural markets. This data includes average, minimum, and maximum prices, categorized by date, tomato type (Big and Small), and variety (e.g., Nepali, Local). The dataset will be cleaned and organized to ensure it is complete, accurate, and ready for analysis.

The next phase involves Exploratory Data Analysis (EDA) to uncover insights into price dynamics:
Historical price trends will be visualized to identify patterns, cycles, and seasonal fluctuations for Big and Small Tomatoes.
Correlation analysis will examine relationships between price metrics (e.g., minimum, maximum, and average prices) for different tomato types.
Principal Component Analysis (PCA) will reduce dimensionality and identify the most significant factors driving price variations across tomato categories and varieties.

Building on these insights, the study will apply a range of statistical forecasting models to predict future tomato prices, considering both short-term and long-term trends:

Linear Regression Models: Models will analyze average prices across categories (Big and Small), interactions, and varieties to determine the influence of date, volatility, and categorical factors on price behavior.
<br/>
<br/>
Time Series Models: ARIMA (AutoRegressive Integrated Moving Average) and SARIMA (Seasonal ARIMA) models will capture trends, seasonality, and autocorrelations within the price data.
<br/>
<br/>
VECM (Vector Error Correction Model): VECM will analyze the cointegrated relationship between Big Tomato and Small Tomato prices, identifying their long-run equilibrium and short-term adjustments. Cointegration tests will first confirm this relationship before applying the VECM.
<br/>
<br/>
GARCH (Generalized Autoregressive Conditional Heteroskedasticity) Models: GARCH will capture and forecast price volatility, highlighting clustering effects and short-term risks in price fluctuations.

To ensure robust evaluation, the dataset will be split into training (80%) and testing (20%) subsets. Forecast accuracy will be evaluated using key error metrics including
Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), Mean Squared Error (MSE) and Mean Absolute Percentage Error (MAPE).

Forecasts will be compared to actual prices, with results visualized to highlight model performance and reliability. Additionally, volatility forecasts from the GARCH model will quantify short-term price risks, supporting stakeholders in managing uncertainties.

### Dataset

Kaggle: https://www.kaggle.com/datasets/ramkrijal/agriculture-vegetables-fruits-time-series-prices

This dataset provides a comprehensive overview of vegetable and fruit prices in Nepal from 2013 to 2021. It contains 197,161 entries with daily price information for a wide range of produce, including the minimum, maximum, and average prices recorded. 

Sourced from official figures, this dataset offers valuable insights into the price dynamics of essential agricultural commodities in Nepal, making it a useful resource for researchers, policymakers, and anyone interested in agricultural market analysis.

### Results and Findings

The performance of various forecasting models for predicting tomato prices in Nepal was evaluated using RMSE, MAE, MSE, and MAPE metrics. These models encompassed linear regression (including Combined, Category, Interaction, and Variety models), ARIMA, SARIMA, VECM, and GARCH, offering a range of statistical and volatility-based techniques.  

Among the linear regression models, the Combined model (incorporating Date, Category, Variety, and Volatility) outperformed the others, exhibiting the lowest RMSE (16.76) and MAPE (35.03%). The Category, Interaction, and Variety models also demonstrated reasonable performance; however, the Combined model's inclusion of multiple explanatory variables enhanced its accuracy.

The ARIMA and VECM models effectively captured the price trends and seasonality for both tomato types. The ARIMA models for both Big and Small Tomatoes delivered identical results with RMSE of 14.08 and MAPE of 20.59%, outperforming linear regression models across all metrics. The VECM (Vector Error Correction Model) exhibited significant improvements with an RMSE of 10.56 and MAPE of 22.19% for both Big and Small Tomatoes. The results highlight the importance of capturing the cointegrated relationship between Big and Small Tomato prices, as VECM effectively models both the short-term deviations and long-term equilibrium between the two price series.

Despite being designed for seasonality, the SARIMA model, which extends ARIMA to handle seasonality, did not outperform ARIMA, indicating that seasonal patterns may already be well captured by the ARIMA model. SARIMA showed slightly higher error metrics with an RMSE of 15.42 and MAPE of 25.79%.

The GARCH models showed the best performance in terms of error reduction, particularly for Big Tomatoes. With an RMSE of 7.35, MAE of 4.95, and MAPE of 12.24%, the GARCH model effectively captured volatility clustering and provided highly accurate forecasts. However, for Small Tomatoes, the GARCH model produced higher errors, with an RMSE of 10.75 and MAPE of 58.19%, indicating that price fluctuations for Small Tomatoes are more unpredictable compared to Big Tomatoes.

### Conclusion

The results demonstrate that advanced time series models like VECM and GARCH provide superior performance in forecasting tomato prices compared to linear regression and SARIMA models. VECM excels at capturing the long-run equilibrium between Big and Small Tomato prices, achieving consistent error reductions across both categories. Meanwhile, GARCH models effectively handle volatility, particularly for Big Tomatoes, where price variations exhibit strong clustering behavior.

The performance of ARIMA models highlights their robustness in capturing general trends and seasonality in both price series. However, the SARIMA models offered no significant advantage over ARIMA, suggesting limited seasonal influence beyond what ARIMA already captures.
The findings suggest that:
GARCH models are most suitable for price volatility forecasting, particularly for commodities like Big Tomatoes with significant price fluctuations.
VECM models are ideal for analyzing and forecasting interdependent price dynamics, capturing both short-term adjustments and long-term trends between related price series.

For stakeholders in Nepal’s tomato industry, these models provide valuable tools for price prediction and risk management. By leveraging these insights, farmers can plan their production cycles more effectively, and policymakers can address market inefficiencies to stabilize prices and reduce post-harvest losses. This study highlights the importance of combining traditional models with volatility-focused techniques to achieve reliable and actionable price forecasts for agricultural commodities in Nepal.


