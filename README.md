# Crypto-Market-Watch-Dashboard
A simple and dynamic web App to track Crypto Pair changes

![Crypto Market Watch Image](https://user-images.githubusercontent.com/90919070/183308101-486438f5-e12d-4204-a81b-a190c6fb77e1.JPG)

## Objective

As there are numerous opportunities in the Cryptocurrency sphere today, it is highly important to have the ability to track value crypto pairs. A good User Interface(UI) will make it more likely to have insights quickly at our fingertips. It is in light of these, I decided to create a Simple Web App or a Modern Dashboard Tool with elements of Neumorphism and Light/dark Mode Capability to cater for any colour deficiencies.

## Data Source

Dataset is the cryptocurrency pairs from Yahoo Finance. Tool used is Power BI fetching daily and historical data from Yahoo Finance using https://finance.yahoo.com/cryptocurrencies/

## Data Cleansing, Modelling and Visualization Steps:

Step 1. Open a new Power BI File and connect to https://finance.yahoo.com/cryptocurrencies/ via the web

![Data](https://user-images.githubusercontent.com/90919070/183308245-679b99c6-47c6-4684-8efb-799d2908f73f.JPG)

Step 2. I tinkered with the url with the final url looking like https://finance.yahoo.com/cryptocurrencies?offset=0&count=100 to fetch first Top 100 pairs

Step 3. I decided to use the link below https://finance.yahoo.com/cryptocurrencies?offset=0&count=25 when the data seems to be taking forever to load. Making it just the Top 25 Pairs daily metrics.
I also used the link below https://finance.yahoo.com/quote/ETH-USD/history?p=ETH-USD to get the Top 25 Pairs Historical Metrics. I only had to adjust the pairs for all the 25 currencies.
I loaded Calendar Table using M in Power Query which acn also be loaded using DAX in Power BI Model using CALENDAR and CALENDARAUTO fx.

So we now have Three Tables. A. Top 25 Pairs — Daily Metrics B. Top 25 Pairs — Historical Metrics. B. Calendar Table

Step 4. I Filtered out “chart” and “52 week range” column to limit to only relevant data for our scope

Step 5. I Extracted the Last Characters in Market Cap, Volume of Currency(24hrs) and Circulating Supply and create a new columns for each of them so as to capture the actual figures without the abbreviated Trillion, Billion and Million. This will allow for proper analysis and building of metrics.

Step 6. Dealing with Data Format of the three columns listed above to account for consistent Data Type within columns using DAX Formulas

![Data Cleansing images_1](https://user-images.githubusercontent.com/90919070/183308280-79443d33-ca9e-4f62-8dea-0b8e2981f620.JPG)

Step 7. Created a Refresh Date and Metrics Table in Power Query in addition to the three(3) tables created ab-initio to aid Data Modelling when transformed data is imported into Power Data Model

Step 8. Created Data Model using Relationships(One-to-Many relationship between Calendar and Top 25 Pairs Historical Metrics and a Many-to-One relationship between Top 25 Pairs Daily Metrics and Top 25 Pairs Historical Metrics) for accurate Metrics Calculation.

![Data Mode Image_2](https://user-images.githubusercontent.com/90919070/183308309-d5cf3f70-8ac9-4cd8-8b15-1edc5821ea80.JPG)

Step 9. A Colour Mode Table was created to properly build the Light-dark Mode Functionality A. Visual Background. B. Font Colour C. Page Background

![Page Background Image_4](https://user-images.githubusercontent.com/90919070/183308359-a5ebe864-3b16-41a7-8895-a0878a217180.JPG)
![Visual Background Image_3](https://user-images.githubusercontent.com/90919070/183308366-8e94e414-a8cb-4fc0-8dcd-f4a1308536ce.JPG)
![Font Color Image_4](https://user-images.githubusercontent.com/90919070/183308373-3c5e82e1-6ab6-4304-93da-d9905cc10bcb.JPG)

Step 10. Button Switch for Light-Dark Mode was imported from the Visual Market Place. Advanced Toggle Switch TME AG

Step 11. Background Design was done in Power Point, with a combo of Shapes, Textboxes, shadow and glow effects and gradient colour scheme

![Background Image](https://user-images.githubusercontent.com/90919070/183308393-c76b1e3e-1fd4-45aa-b8e5-c165cc52e044.JPG)

Step 12. Metrics and Visuals Definition, Design and Development in Power BI

You can interacte with the Tool by suing this url: [Crypto Market Watch](https://app.powerbi.com/view?r=eyJrIjoiMzkzMTAwN2MtMWIyOC00NWU3LThjNTQtNDM4YzhmNTRjNDQzIiwidCI6IjNiZGFjNmEwLWVlNDYtNDQzMC05OGFiLWZiNTJmYTI2MWMyOCIsImMiOjl9)

![Crypto Market Watch Image](https://user-images.githubusercontent.com/90919070/183308433-81a65dc6-5817-4025-9dd8-633cd48f987e.JPG)
  
Thank you for taking out time to go through this piece, I hope it has been a time well spent. Thank you once again.

You can reach me via [Olatkem@gmail.com](Olatkem@gmail.com)

