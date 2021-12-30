# Market Basket Analysis : Bakery Product

## Business Understanding
* Problem : A small bakery in Korea sells they products through an online platform called 'Bea Min'. According to sales data from July 2019 to June 2020, some products had no sales at all, while others had very few sales. Bakeries want to understand their customers' purchasing habits so that they can implement marketing strategies such as product recommendations to increase the number of product sales through their online platform.
* Goals : Make product recommendations and bundling product using association rules to increase the number of product purchases.
* Objective : Conduct investigations to find associative rules in a product combination.
* Business Metrics : Product recommendations

## Data Understanding
This dataset contains detailed information about transactions and product shipped to customers between July 2019 and June 2020. There are 2654 transactions in this dataset. 
Transaction information consists of date time (order time), day of week (day of the week. The bakery usually closes Tuesday), total (total amount), and place (customer’s place). The products in this bakery are angbutter, plain bread, jam, americano, croissant, caffe latte, tiramisu croissant, cacao deep, pain au chocolat, almond croissant, croque monsieur, mad garlic, milk tea, gateau chocolat, pandoro, cheese cake, lemonade, orange pound, wiener, vanila latte, berry ade, tiramisu, and merinque cookies.

Data Source : https://www.kaggle.com/hosubjeong/bakery-sales

## Data Cleaning and Feature Engineering
* Remove unuseful columns and rows
* Filling missing value
* Create new feature. This new feature will be used to get business insights from product sales.

## Data Insights
* Angbutter is the best selling product followed by Croissant, Plain Bread, Tiramisu croissant, and Pain au chocolat.
* The Bakery makes up most of their sales (70%) at noon (10 - 13 o'clock). Sales fell sharply at other times.
* Sunday is the bakery's most productive day in sales. Followed by Saturday, Thursday, Wednesday, Friday, and Monday. This bakery is usually closed on Tuesdays.

## Modeling
Market Barket Analysis is a methodology that investigates purchasing behavior by analyzing the items in the buyer's shopping cart. The investigation is carried out by determining which products are selling well. What products are purchased together? The investigation's findings are then used to develop cross-selling and upselling strategies, which are expected to encourage buyers to purchase multiple products and increase purchase transactions.

The following question is, "How do we investigate this purchasing behavior?" The solution is to use Apriori. What exactly is apriori? The term apriori refers to an algorithm or technique for determining the relationship between items or products in a shopping cart. This a priori result is known as the Association Rule.

Within the association rules there are several important metrics:

* Support. Support is an indication of how often the itemset appears in the dataset. In other words, an indication is how often items X and Y appear in the dataset.
* Confidence. Confidence is an indication of how often the rule proves to be true. That is an indication of how often items X and Y appear together, keeping in mind the number of times X occurs.
* Lift. The following ratio of support observations can be said to explain the strength of the emergence of a rule X and Y.

## Model Insights
The insights model is derived from the outcomes of association rules. These are some of the most interesting dataset-derived associations.
*	If the jam is purchased, there is an 87 percent chance (confidence) that plain bread will be purchased as well. 
*	If plain bread is purchased, there is a 22 percent chance (confidence) that jam will be purchased as well. 
*	If angbutter and jam are purchased, there is an 86 percent chance (confidence) that plain bread will be purchased as well. 
*	If the jam is bought, there is a 58 percent chance (confidence) that plain bread and angbutter will be bought. 
*	There is a 39 percent chance (confidence) that croissants will be purchased if pain au chocolat is purchased. 
*	If the wiener is bought, there is a 34% possibility (confidence) that the croissant will be bought. 
*	If a croissant is purchased, there is a 36% possibility (confidence) that plain bread will be purchased. 
*	If pain au chocolat is purchased, there is a 35% possibility (confidence) that plain bread will then be purchased. 
*	If an angbutter and a pain au chocolat are purchased, there is a 37% possibility (confidence) that croissants will be purchased. 

## Business Recommendations
Several strategies can be applied by bakeries to increase product sales transactions:
*	Provide recommendations on the product detail page (PDP) of the Customs Min platform. Recommendations that can be given are:
*	When customers open PDP jam, then we can recommend plain bread to customers
*	When the customer puts the jam into the “basket”, then we can recommend plain bread to the customer
*	When customers open PDP pain au chocolat, then we can recommend croissants to customers
*	When the customer puts the pain au chocolat into the “basket”, then we can recommend the croissant to the customer
*	When the customer opens the PDP wiener, then we can recommend the croissant to the customer
*	When the customer put the wiener into the “basket”, then we can recommend the croissant to the customer
*	When the customer opens the PDP croissant, then we can recommend plain bread to the customer
*	When the customer puts the croissant into the “basket”, then we can recommend plain bread to the customer
*	When customers open PDP pain au chocolat, then we can recommend plain bread to customers
*	When customers put pain au chocolat into the "basket", then we can recommend plain bread to customers
*	When customers put angbutter and jam into the "basket", then we can recommend plain bread to customers
*	When customers put angbutter and pain au chocolat into the “basket”, then we can recommend croissants to customers
The most potential products for bundling are:
*	Bundling of two products: Jam - Plain bread
*	Bundling of three products: Angbutter - Jam - Plain bread

Other recommendations: This recommendation is based on a business insight: Remove Croque monsieur and Mad garlic from the sales platform's product list because the two products are not creating any sales. 
