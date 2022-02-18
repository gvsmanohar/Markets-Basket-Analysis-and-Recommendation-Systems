# Markets-Basket-Analysis-and-Recommendation-Systems

**Market Basket Analysis and**

**Recommendation Systems**

### Abstract

In recent times, data, especially data mining has played an crucial role in transforming various
industries. Market Basket Analysis is known as an old data mining area, which can be used
as the best example for association rules. Market Basket Analysis(MBA), also known as
association rule mining or affinity analysis, is a technique that may be used in a variety of
areas such as marketing, bio-informatics, education industry, nuclear research and in several
other areas. In the past there have been many mining rules or algorithms which have been
developed by the researchers and currently there are a lot of researchers working on these
rules to develop new ones in order to make it easy for the retailers to reach their target.
The primary goal of Market Basket Analysis in marketing is to give information to retailers
in order for them to better understand the purchasing behaviour of their customers. This
information can then be used to assist the retailer in making more efficient decisions. The
current methods are designed to operate with static data and do not account for changes
in data over time. Rather than mining static data, the suggested association rules offer a
novel approach of taking into account changes occurring in the data. The ability to make
decisions and comprehend the behavior of customers has become an increasingly important
and difficult issue for businesses seeking to maintain their position in highly competitive
marketplaces. Technological advancements have opened the way for breakthroughs in query
processing speed and response time in the sub-second range. For evaluating large amounts of
data and making accurate choices, data mining technologies have emerged as the most reliable
technology available in the market. In order to demonstrate the superiority of Market Basket
Analysis over traditional methods, an experimental study was conducted utilizing association
rules. This project covers the data mining method known as association rule mining, as well as
the algorithms: Apriori and FP-Growth that may be useful in examining customer behaviour
and assisting the retailers to increase the sales and customer experience.

```
ii
```

## Contents






- 1 Introduction
   - 1.1 Aims and Objectives
   - 1.2 Overview of the Report
- 2 Literature Review
   - 2.1 Market Basket Analysis
      - 2.1.1 Market Basket Analysis In Large Database Network
      - 2.1.2 Market Basket Analysis in Multiple Store Environment
      - 2.1.3 Market Basket Analysis Using Fast Algorithms
   - 2.2 Association Rules
      - 2.2.1 Item Sets
      - 2.2.2 Support Count
      - 2.2.3 Confidence
      - 2.2.4 Lift
      - 2.2.5 Frequent Item Generation
      - 2.2.6 Extracting rules from frequent item sets
   - 2.3 Recommendation Systems
      - 2.3.1 Types of Recommendation Systems
      - 2.3.2 Product Recommendation Using Association Rule
   - 2.4 Related Work
- 3 Analysis
   - 3.1 Project Requirements
      - 3.1.1 Data Collection
      - 3.1.2 Pandas
      - 3.1.3 NumPy
      - 3.1.4 Matplotlib
      - 3.1.5 Seaborn
   - 3.2 Methodology & Implementation
      - 3.2.1 Data Description
      - 3.2.2 Feature Extraction
      - 3.2.3 Apriori Algorithm
      - 3.2.4 FP-Growth Algorithm CONTENTS iv
      - 3.2.5 Collaborative Filtering
   - 3.3 Ethical, Professional and Legal Issues
- 4 Results & Discussion
   - 4.1 Exploratory Data Analysis Results
      - 4.1.1 How many orders in a week per day?
      - 4.1.2 How many orders in a day per hour?
      - 4.1.3 How many orders day vs hour?
      - 4.1.4 What are the popular products ordered?
      - 4.1.5 What are the top aisles that the products from?
      - 4.1.6 What are the popular products that were reordered?
      - 4.1.7 What is the reorder ratio of departments?
      - 4.1.8 What are the popular departments that the products reordered from?
         - reorder ratio 4.1.9 Relationship between how adding a product to the cart affects the
      - 4.1.10 Heatmap for Reorder ratio (Day vs Hour)
   - 4.2 Association Rule Mining Results
      - 4.2.1 Apriori Algorithm
      - 4.2.2 FP-Growth Algorithm
      - 4.2.3 Collaborative Filtering Results
- 5 Conclusion & Future Work
   - 5.1 Conclusion
   - 5.2 Future Work
- 2.1 Machine Learning Stages List of Figures
- 3.1 DBMS Schema of the Data Set
- 3.2 Statistics of Products Data Set
- 3.3 Statistics of Orders Data Set
   - prior 3.4 Merged result OrdProdTr(order products train) and OrdProdPr(order products
   - als(aisles), depts(departments) 3.5 Merged result OrdProdPr(order products prior) with ords(orders), prds(products),
   - als(aisles), depts(departments) 3.6 Merging OrdProdTr(order products train) with ords(orders), prds(products),
- 3.7 Products Data set
- 3.8 Product names corresponding to the Orderid
- 3.9 Number of times each product frequency occurs
- 3.10 Filtered products with minimum support of 0.01
- 3.11 Data frame containing products with minimum support 0.01
- 3.12 Number of times each order size occurs
- 3.13 Snippet of Code Block
- 3.14 FP-Tree
- 3.15 Basket Data frame (orderid & products)
- 3.16 Frequent Patterns
- 4.1 Orders in a week per day
- 4.2 Orders in a day per hour
- 4.3 Day vs Hour
- 4.4 Time Interval of the orders
- 4.5 Popular Products
- 4.6 Top Aisles
- 4.7 Popular Products that were reordered
- 4.8 Department reorder ratio
- 4.9 Popular departments that the products were reordered from
- 4.10 Reorder Ration of a product added to the cart
- 4.11 Reorder ratio Day vs Hour LIST OF FIGURES vi
- 4.12 Combination Occurrences
- 4.13 Rules with minimum support 0.01
- 4.14 Rules with minimum support 0.05 & maximum length of
- 4.15 Rules with minimum support 0.002 & maximum length of
- 4.16 Rules with minimum support 0.001 & maximum length of
- 4.17 Antecedent & Consequent with minimum support of 0.01
- 4.18 Actual vs Predicted products with minimum support of 0.01
- 4.19 Antecedent & Consequent with minimum support of 0.005
- 4.20 Actual vs Predicted products with minimum support of 0.005
- 4.21 Antecedent & Consequent with minimum support of 0.002
- 4.22 Actual vs Predicted products with minimum support of 0.002
- 4.23 Antecedent & Consequent with minimum support of 0.001
- 4.24 Actual vs Predicted products with minimum support of 0.001
- 4.25 Model AUC without features
- 4.26 Model AUC with features
- 4.27 Result of Customer
- 4.28 Result of Customer
- 3.1 Transactions of Customers for Apriori Algorithm List of Tables
- 3.2 C1:Candidates, One frequent item sets
- 3.3 L1:Filtered one frequent item sets
- 3.4 C2:Two frequent item sets
- 3.5 L2:Filtered two frequent item sets
- 3.6 Transactions of Customers for FP-Growth Algorithm
- 3.7 Items Support Count
- 3.8 Items Support Count in Descending order
- 3.9 Frequent Patterns
- 3.1 Merging of order products train & order products prior Listings
- 3.2 Merging of order products prior with orders, aisles,departments
- 3.3 Merging of order products train with orders, aisles, departments
- 3.4 Merging of products, aisles, departments
- 3.5 Product Names
- 3.6 list of users function
- 3.7 list of products function
- 3.8 function for ID mappings
- 3.9 function of user product interaction
- 3.10 Function for Matrix interaction
- 3.11 funtion for product feature interaction
- 3.12 Function for combining train, test sets & retraining the model


## Chapter 1

# Introduction

From the 1980s, database engineering has been defined by the widespread worldwide adoption
of the relational model, along with a dramatic shift in the focus of research and innovation
towards the creation of new and efficient database systems. These database systems make
use of a sophisticated data architecture. As a result of the rapid evolution in information
technology services and operating system technologies over the last 30 years, there has been
an abundant supply of efficient and cost-effective processors, data collecting devices, and
storage media available for purchase. There has been a significant boost in the databases and
knowledge business as a result of these technologies, which makes a large range of databases
and information archives accessible for transaction processing, information extraction, and
data processing.

Advancements in information and communication technology has made it possible for
businesses to collect and keep financial and statistical data on individual consumers at a
lower cost. Obtaining valuable insights from massive customer databases in order to obtain
a competitive edge is one of the most difficult problems faced by businesses that have made
significant investments in data gathering. Customer buying patterns may be discovered via
market basket analysis (also known as association rule mining), which extracts associations
or from the past transaction data of retail businesses.

In the case of two non-overlapping subsets of product items, P1 and P2 , an association
rule in the form of P1⇒P2 implies that a purchasing pattern exists in which customers
who buy P1 also buy P2. The selection of association rules is often guided by two factors:
support and confidence. A rule’s support and confidence are both metrics of the rule’s
accuracy, defined as the ratio of the number of transactions with both P1 and P2 to the
number of transactions with only P1. Support and confidence are both measured by how
frequently transactions in the data consists of both P1 and P2. In the field of association rules
mining, the Apriori algorithm is by far the most well-known method for mining association
rules from transactions data that meet the minimal support and confidence levels set by users.

##### 1


##### CHAPTER 1. INTRODUCTION 2

In today’s business, it is typical for a firm to have subsidiaries or branches in various
geographical areas, as well as dealers or franchisees. For example, Insta-Cart, has over 5500
locations in more than 100 countries. It may be beneficial for a business with numerous shops
to identify buying trends that may change over time and present in all or a selection of the
locations. This information can then be used to develop advertising, sales, servicing, and
operating plans in the corporate, local, and retail sectors.

In order to automatically extract association rules from a store environment, an Apriori-like
algorithm and an FP-Growth algorithm are being developed. The rules are written in a
manner that is comparable to that of the conventional rules. The regulations, on the other
hand, provide information about the shop (location) and the time when the rules are in effect.
If the suggested approach is successful, the findings may include rules that are applicable
to the whole chain without any regard to time or rules that are applicable to a subset of
shops at specified time periods. In addition to general or specialized marketing tactics, these
principles may be applied to product sourcing, inventory management, and distribution plans
throughout the whole retail chain. A further feature is that an item is let to have numerous
selling time periods; in other words, an item may be placed on the shelf and removed off
the shelf more than once. Furthermore, we consider that various shops may have different
product mixtures during different times of the year, and vice versa. In other words, each
shop may have its own product mix, and the product mix inside a store can be modified on
a dynamic basis over time.

### 1.1 Aims and Objectives

The primary goal of the project is to enable Instacart merchants to understand their existing
customers’ buying behavior better and to anticipate the purchase behavior of their prospective
customers. The use of customer transaction data can assist businesses in understanding their
customers’ purchasing behavior, offering the appropriate bundles and promotions, assortment
planning, and inventory management, thereby helping them to retain customers, increase
sales, and extend their customer relationship.
**The Goals of the project are as follows:**

1. To get an understanding of the buying patterns of the items that are included in the
    customer’s basket.
2. To do research on a wide range of goods that are often bought by customers.
3. To research the most probable goods that consumers will buy, as well as the most likely
    product categories that customers will acquire.
4. To provide product recommendations and suggestions to the customers.


##### CHAPTER 1. INTRODUCTION 3

### 1.2 Overview of the Report

The technological age in which we live has made it possible for commercial organizations to
amass vast amounts of data on their customers and suppliers. Currently, database technology
innovation has developed enough to maintain these information stacks stable; nevertheless, it
is important not only to retain that information, but also to evaluate the information in order
to enhance the value of the organization. Business must develop appropriate and low-cost
advertising methods that can respond to changes in customer perceptions and requests for
goods in today’s customer-centered marketplaces. Moreover, it may aid businesses in the
identification of a whole new market approach that may be targeted successfully. All together,
reliable, as much as possible, and protected proof-based data is required in order to make
important decisions about market strategy. Data Mining has received probably the greatest
answer to this need as a result of technological advancement. It is the process of identifying
and refining significant data from massive databases, and it covers a wide range of statistical
and computational techniques, such as neural network analysis and clustering, classification,
and summarization of information. This project includes the development of association rules,
which is one of the Data Mining methods used by Market Basket Research and is one of the
techniques used by Market Basket Research. The analysis is carried out on the transaction
data collected from grocery shop, with the use of Apriori and FP-Growth algorithms, the
main aim is to examine the category of products that are most likely to be promoted in
combination with one another and also to recommend the products to the customers.


## Chapter 2

# Literature Review

### 2.1 Market Basket Analysis

The process of Market Basket Analysis was first introduced by (Agrawal & Srikant, 1994)[5],
they performed various tasks by collecting data sets from different retail stores, this data set
has past transactions of customers which includes the bar code data and customer receipt’s
data. From this process they have found new rules which helped retail stores, businesses
and industries to maximize their profits, this method is also used as standard method by
many other bodies. Singh and Sinwar (Singh & Sinwar, 2017)[17] discovered that using
Market Basket Analysis has benefited the researchers who are working for different marketing
companies to develop other methods using the past results[5] like making decisions when
purchasing the products. So this method helped customers by giving them a good experience
when they shop, like if we place a product and the recommended product both in the same
place then the customers will buy both the products instead of buying only one.

#### 2.1.1 Market Basket Analysis In Large Database Network

Market basket analysis is developed to take decisions on what products to place on a department
and an aisle, the placement of the products in an aisle will maximize the profits. An analysis
is performed on the past transaction data of the customers to find the trends in what products
are bought. Up to now we only have historic data about the transactions during some hours
of the day or days of the week. However the progress in the time made easy with new bar
code technology to store the data on a transaction basis, so due to this technology, we are
able to collect large amounts of data.So, we can make rules from this data to enhance the
customer experience and also to help the stores to maximise the profits, like:

1. Banana as a result of the regulations. For example, knowing what can be done to
    propose a list of items or increase banana sales may be helpful.
2. Trying to find a rule that has ”Organic produce” as its antecedent. For example, if
    the business decided to discontinue selling organic products, these regulations may be
    useful.

```
4
```

##### CHAPTER 2. LITERATURE REVIEW 5

#### 2.1.2 Market Basket Analysis in Multiple Store Environment

These days, many of the corporations and organizations have many locations. Many businesses
are expanding in size in order to keep up with the efficiency of sales. In the United Kingdom,
for example, Tesco is by far the biggest retailer. Time and place have an impact on determining
the varied purchase habits in these shops. When there are many stores, the simple rules of
association aren’t applicable.

#### 2.1.3 Market Basket Analysis Using Fast Algorithms

Using the Apriori method, it is possible to uncover association rules using market basket
analysis which are hard to find normally. As a result, the Apriori algorithm has a lot of
trouble finding rules, and we must utilize better techniques to determine the rules.

### 2.2 Association Rules

An essential Data Mining approach utilized in Market Basket Analysis is the association rule.
For example, let us say all vegetables are placed and sorted in the same aisle and all produce
products are placed in another aisle, so the time taken for the customers to shop the required
product is reduced and also helps the customers to purchase the required products along
with the first product(Kanagawa et al., 2009)[11]. Some customers like to combine products
in their basket, this is also called product bundles. Support, confidence, and lift are three
factors that can be used to compute an associative rule.
As one of the oldest algorithms, the Apriori method is used to identify the most common
patterns of Logical rules. The concept of quantitative rules in mining for large relational
tables or databases was elaborated by Ramakrishnan Skrikant and Rakesh Agrawal(Agrawal
& Srikant, 1994)[5].
By creating association rules, it will be easy for the companies to find out what products
are most purchased by the customers and also it can be used to analyse the percentage of
product purchase by the customers and revenue produced by the same product. It is also
important to place the leading product in the area where the customers buy the essential
products so that it will be an easy process for the customer to select the recommended
products along with the products bought previously. Even the aisles and departments play
a major role in this process, like the product that is recommended should be placed in the
right aisle or department for an east shopping and also increase the customer experience.
This process is of generating association rules for the leading products has been researched
and analysed by Julander (Julander, 1992)[10].
Analysing the process of data mining, lead to some exceptional results and clusters in
data by modelling it as a product network. From this process, it is clear that the products
have a greater relationship between them, which made the aggregate rules to be simpler.
The relationship between the products has to lead to a successful process for networking the
data and exposed good links between combinations of rules. From the past transactional


##### CHAPTER 2. LITERATURE REVIEW 6

data provided by the companies, one can extract the purchasing patterns and rules for these
patterns. For example, customers who bought a meat product will buy meat-related products
like fruits, vegetables and spices. So we can see how important to place the right products
near the product bought by the customer so that it will be easy for the customers to shop for
the preferred product. Placing the product group in the same area benefits the customers so
that they knew these are grouped items for any products they are going to buy.
New plans and rules have been developed for store restocking problems with association
rules and multidimensional scaling evaluation, this problem was solved by taking the important
information from the product barcode and customer receipt details which holds an important
position in the retail sector. The collected then analyses using the Apriori algorithm using
the association process. Ibrahim, Cil(Cil, 2012)[7], then stated that a new plane has been
developed for the stores based on the resulting rules. The Apriori and FP-Growth algorithms
are the most used algorithms for the development of new association rules or to research
more on the existing rules. These algorithms are then used on the data collected from the
stores (past transactional data) to recommend the products or to automate the process of
recommending. Using these algorithms some researchers have found out that the FP-Growth
algorithm is more accurate than Apriori because of the speed on the data set, FP-Growth is
faster than the Apriori in the case of large data sets.
Every data set contains missing values and outliers, to build a good model these constraints
need to be taken care of. Few algorithms are suggested on dynamic data which connects to
the association rule mining. So these algorithms are helped to find the outliers and in finding
the future association rules. This research was carried by Kaur and Kang (Kaur & Kang,
2016)[12]. Every customer plans to take all the products in a single visit to save time, so the
word called shopping basket was proposed for this use by Cachon and Kok (Cachon & K ̈ok,
2007)[6]. This even helps the stores to gather data easily, if a customer takes multiple trips
to a store the transactional data will also be according to the visits which mean more data
which leads to more storage. To overcome this problem researchers developed an approach
where it tests the use of shopping baskets and contributing to stores for a higher projected
profit.
**Summary** :It is also important to place the leading product in the area where the
customers buy the essential products so that it will be an easy process for the customer to
select the recommended products along with the products bought previously. Even the aisles
and departments play a major role in this process, like the product that is recommended
should be placed in the right aisle or department for easy shopping and also increase the
customer experience. Analysing the process of data mining, lead to some exceptional results
and clusters in data by modelling it as a product network. The relationship between the
products has led to a successful process for networking the data and exposed good links
between a combination of rules. New plans and rules have been developed for store restocking
problems with association rules and multidimensional scaling evaluation, this problem was
solved by taking the important information from the product barcode and customer receipt
details which holds an important position in the retail sector. The collected data is then


##### CHAPTER 2. LITERATURE REVIEW 7

analysed using the Apriori algorithm. The Apriori and FP-Growth algorithms are the most
used for the development of new association rules or to research more on the existing rules.
These algorithms are then used on the data collected from the stores (past transactional
data) to recommend the products or to automate the process of recommending.

#### 2.2.1 Item Sets

Each of these item sets is a combination of all the products that fill up a market basket.
T = t1, t2,..tn, is a set which include all the transactions.
It’s important to note that each transaction is unique and represents a group of things from
item I. Item sets with n items are known as n item sets. In the case of banana, strawberries,
and raspberries, it is referred to as a three item set. Item sets with no items are named
null sets or empty sets. More than one product in the item set increases the probability of
additional rules being included.

#### 2.2.2 Support Count

One of the most significant components of a data item is its supporting counts, that relates
to the amount of transactions that have been performed on the item set. This will be the
percentage of transactions in the collection of data that contain a large number of that given
product compared to a total number of transactions that is supported by the item or group of
items. An item’s support gives us an estimate of how often it’s been used in the transaction’s
overall history. For example, a retail outlet with 100 users who came in here to purchase
items, users bought Fifty of P1, Forty of P2 and 25 of them purchased both P1 and P2 out
of a total of 100 customers. There is 50 percent support for Product P1, 40 percent support
for Product P2, and 25 percent support for the both Products P1 and P2, value of Support
is a useful tool for determining what rules are worth examining further in terms of product
association with other items in the market. Support = 0.005, for example, if we want to keep
a record of item sets that appear at least 50 times in 10,000 transactions, without enough
information on how the items are interrelated to one another, we would be unable to detect
”hidden” connections.

```
Support P1=Number of Transactions that consists of P
Total Transactions
```
#### 2.2.3 Confidence

In other words, it’s the probability that even a buyer who buys a certain item will also
buy another item. This means that the statement (item set P1)⇒(item set P2) is a rule of
association, where P1 is the antecedent and P2 is the consequence. With confidence, you may
be sure that Consequences will occur if there are antecedents that already exist. Regardless
of whatever the consumer has in the Antecedent, the Consequence will occur. There will


##### CHAPTER 2. LITERATURE REVIEW 8

always be excellent value in the confidence placed in an Association rule. For example,

```
Conf idenceP 1 ⇒ P 2 = PP^1
P 2
```
```
=Number of transactions that consists of both P1 and P
Total transactions that contains P
```
50 people bought item P1 and item P2, and 25 of them purchased both. By purchasing P
and P2, a person has a 50 percentage probability of purchasing P2.

#### 2.2.4 Lift

Compared to something like a random selection of a transaction, the proportion determines
how good the rule is at identifying consequences. More than one lift implies that perhaps the
guideline is effective in practice. Having a lift greater than one indicates that presence of P
in this transaction had increased the chance that P2 will be obtained. Lift value just under
one means that the role of product P2 is less likely to take place.

```
Lif tP 1 ⇒ P 2 =
```
```
Conf idenceP 1 ⇒ P 2
SupportP 2
```
lift score of 1.25 indicates that the likelihood of acquiring product P2 has increased by
25 percentage. The occurrence of one thing and the addition of another is granted by
fundamental laws of association. The following steps are involved in the process of attempting
to discover association rules using Data Analytics:
Step 1: Assemble the data for the transactions display. tx = i1, i2, i3 seems to be the
transaction kind required for an association method.
Step 2: A checklist of items that commonly occur. Item groups are a kind of data collection
that uses large items ets as a component. When using an association algorithm, the most
frequent objects are evaluated, and the least frequently happening ones are eliminated,
making an important rule which will be carried to the next stage is even more crucial.
Step 3: From the frequent item sets, build any appropriate association rules. So it develops
and analyzes rules based on the data being updated.

#### 2.2.5 Frequent Item Generation

**n** item sets may be broken down into null item sets and 2n-1 item sets. In relation to the
increase in the number of items, the number of frequent item sets rises significantly. This
means choosing and establishing a minimum support level for frequent item sets that appear
very frequently in the transaction world is critical. Exactly why is frequent item extraction
such a problem?. To use a simple force of nature technique, all probable item sets will
be collected and calculated over all transactions for each contender, calculating how many
instances the item-set meets the required support count for each contender. So, a typical
store may have over 10,000 different products to choose from!.


##### CHAPTER 2. LITERATURE REVIEW 9

#### 2.2.6 Extracting rules from frequent item sets

Developing the mining association’s regulations with support and confidence would be a
difficult task to deal with.
_R_ = 3 _I_ − 2 _I_ +^1 + 1

Data sets of n items include R rules. All rules having a confidence level greater than a
given threshold may be found using this approach. Even for a handful of objects, generating
frequent items and separating stages enables for the construction of thousands of rules. A
minimal support and confidence level is therefore essential in order to filter out less common
and less acceptable rules in your search area. Support, confidence, and lift measures may also
be used to assess the generated rules. There is a substantial difference in computation time
between finding all the frequent item sets and obtaining the rules from frequent item sets. To
be much more precise, R must be null if the entire set of possible rules is not even on either
one side of the rule. In terms of quantifying frequent pattern collections, there are very few
algorithmic approaches that are successful. Algorithms used for the association analysis are
Apriori and Frequent Pattern (FP)-Growth are two of the most commonly used methods.

### 2.3 Recommendation Systems

This system, as per Anna Gatzioura and Miquel Snchez(Gatzioura & S`anchez-Marr`e, 2015)[9],
is designed to offer appropriate and beneficial material (items) to the customer who is now
logged in. In recent times, recommendation systems have grown increasingly widespread.
Early within the 1990s, the very first article on collaborative filtering published and the
recommendation systems became a popular study topic. In order to sort and retrieve
information, recommendation systems utilize a technology known as recommendation systems
(RS). Purchases of e-commerce companies as well as other retailers are also boosted by these
methods. Most of the time, these platforms are indeed a technological tool that allows a
customer locate a product or service that piques their attention. Nowadays it’s used to
describe a service that’s personalized for the customer’s preferences and needs. This is a
machine learning method that belongs to unsupervised learning models in which information
is not labelled, as per K. Shah, A. k Salunke, and S. Dongare and K. Antala(Shah et al.,
2017)[16].
Recommendation systems are of two types, Personalized and non-personalized. Personalized
recommendation systems are those in which the group of different users is receive different
suggestions where as in nonpersonalized recommender systems all users get same suggestions.
According to J. Ben Schafer, Joseph Konstan, John, Non-personalized recommendation
systems are automatic because in these systems recommendations are not based on customers
so these systems doesn’t recognized the users from one session to another and these systems
requires a physical storage. Recommendation systems are grouped into these categories-
Content Based Filtering, Collaborative Filtering and Hybrid Systems. All the techniques are
using in different platforms and they have their advantages and disadvantages. The paper


##### CHAPTER 2. LITERATURE REVIEW 10

```
Figure 2.1: Machine Learning Stages
```
will describe all the techniques with their advantages and limitations in the following sections.
Recommendation systems are used to filter the information that analyses the user behaviour
data from the historic data and also used to predict the suggestions for the customers based
on their previous purchase data. We have other recommendation systems such as movie,
music, books, articles etc., generally, the data sets for these recommendations are very large,
contains a lot of missing values and outliers.
Five stages of recommendation systems are demo-graphical, content-based, hybrid systems,
collaborative filtering (CF) and knowledge-based. The association rules are also used in many
other industries as it used in the financial services, stock market sector to manage the portfolio
of the customers. In this sector, the rules are used to predict what stocks have a high margin
of profit and what stocks should be neglected to decrease the margin of loss. This was
proposed by Paranjape-Voditel and Deshpande (Paranjape-Voditel & Deshpande, 2011)[15],
later this method has been used as a base for all the models built in the stock market sector.
Yazgan and Kusakci (Yazgana & Kusakci, 2016)[18] concentrated on improving order
collection in a pharmaceutical warehouse. For this situation, when the objects to be processed
are small in size, the order stacking approach was proposed (Cil, 2012)[7]. We used a genetic
technique to compute stacking of client orders that were similar in order to accommodate
them across different pharmaceutical warehouses. In the occupation or job, there was a
decline in the number of passes for multiple orders placed in one phase, saving time.
This system, as per Anna Gatzioura and Miquel Snchez(Gatzioura & S`anchez-Marr`e,
2015)[9], is designed to offer appropriate and beneficial material (items) to the customer
who is now logged in. In recent times, recommendation systems have grown increasingly
widespread. Early within the 1990s, the very first article on collaborative filtering published


##### CHAPTER 2. LITERATURE REVIEW 11

and recommendation systems became a popular study topic. In order to sort and retrieve
information, recommendation systems utilize a technology known as recommendation systems
(RS). Purchases of e-commerce companies as well as other retailers are also boosted by these
methods. Most of the time, these platforms are indeed a technological tool that allows a
customer locate a product or service that piques their attention. Nowadays it’s used to
describe a service that’s personalized for the customer’s preferences and needs. This is a
machine learning method that belongs to unsupervised learning models in which information
is not labelled, as per K. Shah, A. k Salunke, and S. Dongare and K. Antala(Shah et al.,
2017)[16].

#### 2.3.1 Types of Recommendation Systems

**Collaborative Filtering**

One way to put it is that when a user has shown previous patterns of behavior or interests, he
or she will likely demonstrate such traits in the future. The notion of collaborative filtering
hinges on this main concept. For collaborative filtering, you need a data set that includes
user interactions with the items to be recommended, as well as a means of taking advantage
of that data set to categorize users by their tastes and interests. You also need an algorithm
to compare users who are alike to one another while filtering out those who are not. We’ll
be covering each of these topics for a short period of time. The information will include
user activity, such as buying information, movies rating, search history, and publications.
Thus, for any particular customer, it will include the total of all feedback that is accessible to
them. In certain cases, the system architect requires external data to gather input. Feedback
may be given in many ways, including being explicit, having an implicit effect, or ideally,
both. There are no hard-and-fast rules for collecting data. Regardless of how the data was
acquired, though, it is almost always better to input it into a matrix structure in which rows
represent distinct customer and columns represent products and each cell’s value indicates
a given customer’s relationship with a given product. The feedback they provide is clear or
implicit, depending on what it is trying to communicate. Explicit feedback is an expression of
preference; that is, if a customer rates a product with a rating of 4 stars and another product
with a rating of 3 stars, we know that the user prefers the first product over the second.
Essentially, profiles in the memory-based method are nothing more than vectors with
many ratings provided by many people. An algorithm determines whether or not a customer
would enjoy a product by adding the scores of many comparable customers to get an aggregate
score for the product, typically after accounting for individual consumer bias. It has many
inherent problems, all of which need to be solved quickly. How should the system identify
customers who are similar? If the data set is very large, evaluating customers pair-by-pair
may be costly in terms of computing effort. Even in practice, the online computing of this
calculation never occurs. Systems administrators utilize the online computation of projected
scores as part of teaching each customer’s neighborhood of similar customer’s. When should
you deal with new customer’s or things? While a new customer will be new to the service, he


##### CHAPTER 2. LITERATURE REVIEW 12

will not be comparable to any previous customers due to the lack of previous encounters to
be used as a basis of comparison. An product, however, has no ratings but will be examined
for suggestion in every situation. While it’s obvious that resolving this specific issue would
involve re-training the program, this specific issue is a basic problem of the memory-based
method, since the only way to solve it is to re-train the system.
Not only can memory-based systems grow inadequately, but another drawback is that they
may be more difficult to use. The majority of customers will engage with a limited number
of things whereas each customer will deal with thousands of products. Because the resultant
customer-product interaction matrix is extremely sparse, adaptation will be hindered and
learning duration’s will be long. Now that we’ve spoken about model-based methods, we’re
entering into a discussion of it. Both model-based and memory-based collaborative filtering
systems utilize matrix factorization techniques to help with the customer-product interaction
matrix. Matrix factorization was among the most popular methods for dimensionality reduction.
The combined reduced matrices capture almost all of the essential information in the original
matrix. Like the customer-product matrix, the reduced matrices are neither sparse nor
accessible to individuals. These new, simpler matrices include what’s been described as
latent factors for every particular person or object. Any two products or any two customers
have in common the essence that may be expressed in the most concise way by latent factors.
In a model-based collaborative filtering system, these parameters are utilized to generate
recommendations. In a memory-based model, the same parameters are used to produce
recommendations.

**Content Based Recommendation Systems**

It is the basic premise of content-based recommendation systems that things or material
that have piqued your interest in the past and/or present will continue to be indicative of
your interests in the future. This assumption is incorrect. Based on your visiting and buying
history (if this is accurate), a content-based recommendation system will construct a customer
profile based on your preferences. This is often accomplished by creating a representation of
objects and customer’s as vectors in a high-dimensional vector space. Rather of representing
the conventional length, width, and height of a three-dimensional space, the dimensions of
the vector space will each reflect an attribute of the object or an area of interest to the user.
Consider the following example: a vector space for a movie recommendation system could
include attributes such as ”fantasy,” ”romance,” and ”starring Britney spears,” each of which
is taken from the characteristics of the movies contained in the area. These characteristics
are distinct, and only a handful of them will be applicable to any given film or television
show. Continuing with the movie example, ”Blade Runner” may contain the ”Sci-Fi” and
”Thriller” elements, but it does not feature Britney Spears in any way. In the event that
such a vector space has been created, the system may begin creating customer profiles by
utilizing either explicit or a real value near to zero for a feature that the customer hates or
has shown no interest in, and the opposite for an attribute that the user is interested in.
As soon as a vector has been produced, metrics such as the cosine similarity are used to


##### CHAPTER 2. LITERATURE REVIEW 13

determine whether or not a specific movie should be suggested to the viewer, with higher
values suggesting greater probability of favourable reception than lower ones.

**Hybrid Recommendation Systems**

Hybrid systems include elements of both content-based and collaborative filtering systems in
an effort to leverage the advantages of one method while compensating for the disadvantages
of the other, as described above. In order to integrate two recommendation systems, there
are many approaches that may be used. Taking a weighted average of their predictions for a
given product is one method, and using the outcome of one method as the feedback to the
next is another. However, the hybrid methods which are most appropriate to our discussion
are those that transfer smoothly through using content-based information in the absolute
lack of collaborative information and using a pure collaborative filtering system whenever a
product completely lacks metadata.

#### 2.3.2 Product Recommendation Using Association Rule

For a model to recommend a set of products it needs historical data to start building the
model and we should take care that the model can adapt to new problems or situations. The
important role of data mining is to build a good accurate model. We can discover purchase
patterns and unknown patterns from the historic data using data mining techniques. We
can use Machine learning methods in the recommendation systems to train a model and also
to recommend products. The process of a recommendation system can be divided into four
steps:

1. Collecting the data and performing the pre-processing steps like dealing with missing
    values, checking outliers and Exploratory Data Analysis
2. Once the data is ready then we can use this data to prepare for the model by extracting
    the features or by training the data using Apriori and FP-Growth algorithms with
    required association rules to find the trends in the data.
3. Now build the model from the processed data, model building includes steps like
    parameter tuning, error, accuracy and feature importance.
4. At last, use the previously developed association rules to recommend the products to
    the customer.

### 2.4 Related Work

An algorithm is developed for the Apriori association rules using genetic methods(Mostafa,
2015)[14] by Shanta Rangaswamy and G.Shobha[8], this algorithm predicts the rules using
this genetic algorithm, this algorithm contains negative parameters. The main role of this
algorithm is to reduce the time taken to load large data sets, increase in the computational


##### CHAPTER 2. LITERATURE REVIEW 14

speed and also increases the effectiveness of gaining the database log-files. Market Basket
Analysis can be used to place the products in the correct aisle and department, by this way
the vendor can benefit more. This method is based in the customer support and trust when
purchasing related products. To improve the probability of placing the product in correct
aisle or department we use data mining tools.
The data mining tools are even used in the education industry and association rules are
used to analyse the performance in their exams and to predict what the output of the next
exam(Madani, 2009)[13]. This will help not only the teachers but also students to know what
mistake they made, teachers can benefit by giving the feedback and on what subjects the
students need to improve for the next exam.


## Chapter 3

# Analysis

### 3.1 Project Requirements

#### 3.1.1 Data Collection

The data set for this project is obtained from an open source website[4], Kaggle. The
data consists of six separate data sets, **orders.csv, products.csv, departments.csv,
aisles.csv, orderproductsprior.csv, orderproductstrain.csv**. From these data sets
there are a total of 206,200 customers or users, over 3 million orders (3.2M), so that is
approximately 16 orders per customer. Total number of products available in the store are
around 49,700 and number of total ordered products are 3.4 million, so 652 orders for a single
product.

1. **Orders:**
    Orders data set consists of seven columns and 3.4m rows, which are total orders. The
    shape of the orders data set is (3421083,7).
       - orderid: Order ID of the customer orders
       - userid: User ID of the customers or customer ID
       - ordernumber: Unique number for the customer order
       - evalset: train or test or prior
       - orderdow: orders in a day of a week (Sunday(0) - Saturday(6))
       - orderhourofday: orders placed during hour of a day (0-23)
       - daysincepriororder: the days since a customer placed a reorder (ranges from 1
          - 30)
2. **Products:**
    Products data set consists of four columns and 49.6k rows (which are total products).
    The shape of the products data set is (49688,4)
       - productsid: ID of the products, every product has a unique product ID

```
15
```

##### CHAPTER 3. ANALYSIS 16

- productname: name of the products, every product has unique product name
- aisleid: Unique ID for each aisle
- departmentid: Unique ID for each department
3. **Aisles:**
Aisles dataset has two columns and 134 rows (which are total aisles). The shape of the
aisles dataset is (134,2)
- aisleid: Unique ID for each aisle
- aislename: names for each aisle
4. **Departments:**
Departments dataset has two columns and 21 rows (which are total departments). The
shape of the aisles dataset is (21,2)
- departmentid: Unique ID for each department
- departmentname: names for each department
5. **orderproductsprior:**
Orderproductsprior consists of four columns and 32434489 rows (total orders). The
shape is (32434489,4).
- orderid: Unique ID for each customer order
- productid: Unique ID for each product
- addtocartorder: Order in which each product was addedd to the cart
- reordered: if a product is reordered or not (Boolean), 1 if a product is reordered
otherwise 0.
6. **orderproductstrain:**
Orderproductstrain consists of four columns and 1384617 rows (total orders). The
shape is (1384617,4).
- orderid: Unique ID for each customer order
- productid: Unique ID for each product
- addtocartorder: Order in which each product was addedd to the cart
- reordered: if a product is reordered or not (Boolean), 1 if a product is reordered
otherwise 0.

So, the aisles data set and departments data set are merged with the products data set,
because the aisles and products data sets have aisleid as a common column. Merging
along this column we can identify the products according to their respective aisles and for
departments and products data sets we have departmentid as a common column, merging
along this column will result in the department names of all the products.


##### CHAPTER 3. ANALYSIS 17

```
Figure 3.1: DBMS Schema of the Data Set
```
#### 3.1.2 Pandas

”Pandas is a library written for the python programming language”[1]. Pandas library is
mainly used for data analysis and data manipulation which includes reading the data, creating
data frames, manipulating the data and even for cleaning the data.
**Main Features**

1. Reading the data with different file formats, which includes column changing, indexing.
2. Writing the data to an output file in different file formats, saving images and saving
    some pickled data.
3. Pandas are used to deal with the missing values by replacing the none values with a
    suitable value.
4. Also used to subset a large data files, ”slicing data frames, fancy indexing, reshaping
    and pivoting the data.”[1]
5. One main feature which is widely used is merging data with pandas, this is the most
    useful tool and also a important part in this project, which is used to merger six different
    data sets into useful data sets.


##### CHAPTER 3. ANALYSIS 18

#### 3.1.3 NumPy

”NumPy is a library for the python programming, which is used in adding support for
large, multi-dimensional arrays and matrices, along with a large collection of high-level
mathematical functions to operate on these arrays.”[2]
**Features:** ”Array creation, Basic operations, Linear algebra, Universal functions, Tensors”[2].

#### 3.1.4 Matplotlib

”Matplotlib is a graphical representation library for python programming. Matplotlib extends
it’s use to numerical representation using NumPy and Pandas”[3]. Matplotlib library consists
of basic charts like bar chart, line, stacked bar, histogram (horizontal and vertical) and scatter
plots. This library also extends to 3D plots and image plots, these kind of plots are mainly
used for medical data sets or any in depth statistical related data. One can easily infer or
summarize important points from these graphs.

#### 3.1.5 Seaborn

Seaborn library works same like a matplotlib library, but seaborn library consists different
plots (a lot of graphs and options to plot data), which ranges from basic to statistical data.
Seaborn library consists of different graphs like, line plot, scatter plot, cat plot (categorical
plot), count plot, kde plots and heat maps. Seaborn is a good library to style a plot, because
this library consists of a lot of parameters like, color, style, aplha (visibility of a color).
Seaborn library is used load pre-loaded dat sets. One can easily plot the data from a large
data sets or using a subset from the large data and also used in merging two different data
sets. Most of the plots will accept values for both X and Y axis which a good because it helps
to plot the easily. In this project seaborn library is used to plot the data and matplotlib for
basic editing like, title, X and Y labels, changing the figure size.

### 3.2 Methodology & Implementation

#### 3.2.1 Data Description

**Analyzing Orders and Products data sets**

**Products:**

From the figure 3.2, all the numeric columns have the same count, which is equal to the
number of rows indicating that there are no missing values. The minimum is 1 and the
maximum is equal to the last entry for each category (product, aisle or department), which
suggest, for productif, that all ids are indeed unique and given sequentially and for aisleid
and departmentid, that they are consistent with the previous, corresponding, data frames.


##### CHAPTER 3. ANALYSIS 19

```
Figure 3.2: Statistics of Products Data Set
```
**Orders:**

From the figure 3.3, All columns have the same count (which is equal to the number of
rows in the prior split, indicating no missing values), except column dayssincepriororder.
The difference is probably due to those NaN values. If userid is given sequentially, there
are 206,209 users. ordernumber goes from 1 to 99, meaning all clients included purchased
at least once, and none made more than 99 orders. orderdow contains values from 0 to
6, corresponding to the 7 days of the week. orderhourofday goes from 0 to 23, which
corresponds to the 24 hours of a day. dayssincepriororder goes from 0 to 30, meaning that
some orders were made in the same day of the previous order, while the longest interval is 30


##### CHAPTER 3. ANALYSIS 20

```
days.
```
```
Figure 3.3: Statistics of Orders Data Set
```
#### 3.2.2 Feature Extraction

```
Feature Extraction
Concatenate the OrdProdTr(order products train) and OrdProdPr(order products prior)
data sets as both contains purchased products order of customers.
```
1 ord_prds_all = pd.concat ([OrdProdTr , OrdProdPr], axis =0)
2 ord_prds_all = pd.merge(ord_prds_all , prds , on=’product_id ’, how=’left’)
3 ord_prds_all = pd.merge(ord_prds_all , ords , on=’order_id ’, how=’left’)
4 ord_prds_all = pd.merge(ord_prds_all , als , on=’aisle_id ’, how=’left’)
5 ord_prds_all = pd.merge(ord_prds_all ,depts ,on=’department_id ’,how=’left’)

```
Listing 3.1: Merging of order products train & order products prior
```
```
Figure 3.4: Merged result OrdProdTr(order products train) and OrdProdPr(order
products prior
Merging the prds(products), ords(orders), als(aisles) and depts(departments) data sets
with the OrdProdPr(order products prior) data set. Ords(orders) and OrdProdPr(order
products prior) data sets are merged on orderid, using left merge, prds(products) and
OrdProdPr(order products prior) are merged on productid, als(aisles) and OrdProdPr(order
products prior) are merged on aisleid, depts(departments) and OrdProdPr(order products
prior) are merged on departmentid.
```

##### CHAPTER 3. ANALYSIS 21

1 OrdProdPr = pd.merge(OrdProdPr , prds , on=’product_id ’, how=’left’)
2 OrdProdPr = pd.merge(OrdProdPr , ords , on=’order_id ’, how=’left’)
3 OrdProdPr = pd.merge(OrdProdPr , als , on=’aisle_id ’, how=’left’)
4 OrdProdPr = pd.merge(OrdProdPr , depts , on=’department_id ’, how=’left’)

```
Listing 3.2: Merging of order products prior with orders, aisles,departments
```
```
Figure 3.5: Merged result OrdProdPr(order products prior) with ords(orders),
prds(products), als(aisles), depts(departments)
Merging the prds(products), ords(orders), als(aisles) and depst(departments) data sets
with the OrdProdTr(order products train) data set. ords(Orders) and OrdProdTr(order
products train) data sets are merged on orderid, using left merge, prds(products) and
OrdProdTr(order products train) are merged on productid, als(aisles) and OrdProdTr(order
products train) are merged on aisleid, depts(departments) and OrdProdTr(order products
train) are merged on departmentid.
```
1 OrdProdTr = pd.merge(OrdProdTr , ords , on=’order_id ’, how=’left’)
2 OrdProdTr = pd.merge(OrdProdTr , prds , on=’product_id ’, how=’left’)
3 OrdProdTr = pd.merge(OrdProdTr , als , on=’aisle_id ’, how=’left’)
4 OrdProdTr = pd.merge(OrdProdTr , depts , on=’department_id ’, how=’left’)

```
Listing 3.3: Merging of order products train with orders, aisles, departments
```
```
Figure 3.6: Merging OrdProdTr(order products train) with ords(orders), prds(products),
als(aisles), depts(departments)
Merging als(aisles), depts(departments) and prds(products) data sets because the als(aisles)
and prds(products) have aisleid as a common column where as depts(departments) and
prds(products) have departmentid as a common column.
```
1 products= pd.merge(left =pd.merge(left=prds , right=depts ,how=
2 ↪’left’),right=als , how=’left’)

```
Listing 3.4: Merging of products, aisles, departments
```

##### CHAPTER 3. ANALYSIS 22

```
Figure 3.7: Products Data set
Creating a data frame ”orderproducts” with each row corresponding to one order. First
column is the orderid and the second column is the name of the products corresponding to
the orderid.
```
1 prds=OrdProdPr[’product_name ’]
2 product_name_with_no_space =[]
3 for product in prds:
4 product=product.replace(" ","_")
5 product_name_with_no_space.append(product)
6 OrdProdPr[’product_name_with_no_space ’]=
7 ↪product_name_with_no_space
8
9 name_list =[]
10 for p_name in OrdProdPr.groupby(’order_id ’)[’product_name_with_no_space ’]:
11 name_list.append(’ ’.join(p_name [1]))
12
13 ord_id=OrdProdPr.groupby(’order_id ’)
14 ↪[’product_name_with_no_space ’].agg(’count ’).index
15 ord_prds=pd.DataFrame ({’order_id ’:ord_id ,’products ’:name_list })

```
Listing 3.5: Product Names
```
```
Figure 3.8: Product names corresponding to the Orderid
```

##### CHAPTER 3. ANALYSIS 23

#### 3.2.3 Apriori Algorithm

For this process first a small subset is taken to perform the tasks and to create different
functions, because the original data set has around 3.2M orders. Once the required tasks and
functions are created the rules are generated on the whole data set.
Apriori algorithm is useful in the process of Association rule mining. Association rule mining
can be viewed as a two step process:

1. Finding all the frequent item sets
    - Apriori method
    - FP-Growth method
2. Generating strong association rules from the frequent item sets, by definition these rules
    must satisfy minimum support and minimum confidence

Apriori employs an iterative approach known as a level-wise search, where k-items sets
are used to explore (k+1) item sets. For this process we are going to use a subset from
the OrdProdPr(order products prior) data set, the subset consists of 977 order and 4511
products. After getting the subset the product frequency is calculated, minimum product
frequency is 0.001 and maximum product frequency is 0.15.

**Mathematical Explanation:**

```
Customer Transactions List of Product ID’s
X1 P1,P2,P5
X2 P2,P4
X3 P2,P3
X4 P1,P2,P4
X5 P1,P3
X6 P2,P3
X7 P1,P3
X8 P1,P2,P3,P5
X9 P1,P2,P3
```
```
Table 3.1: Transactions of Customers for Apriori Algorithm
```
First set the minimum support as 2 and then generate a table(3.2) for count of each
candidate(item) from the transactions data(table:3.1). Once the table(3.2) is formed filter
the table(3.2) with the minimum support count and construct another table(3.3). After
forming the one frequent item sets, then build a table with two frequent item sets using the
candidates from the table(3.2) after this scan the database and calculate the support count of
the item sets(table:3.4) and filter them according to the minimum support count(table:3.5).
Carry this process until all the frequent item sets are formed.


##### CHAPTER 3. ANALYSIS 24

```
Items Support Count
P1 6
P2 7
P3 6
P4 2
P5 2
```
```
Table 3.2: C1:Candidates, One frequent item
sets
```
```
Items Support Count
P1 6
P2 7
P3 6
P4 2
P5 2
```
```
Table 3.3: L1:Filtered one frequent item sets
```
```
Items Support Count
P1,P2 4
P1,P3 4
P1,P4 1
P1,P5 2
P2,P3 4
P2,P4 2
P2,P5 2
P3,P4 0
P3,P5 1
P4,P5 0
```
```
Table 3.4: C2:Two frequent item sets
```
```
Items Support Count
P1,P2 4
P1,P3 4
P1,P5 2
P2,P3 4
P2,P4 2
P2,P5 2
```
```
Table 3.5: L2:Filtered two frequent item sets
```
```
Figure 3.9: Number of times each product frequency occurs
From the figure 3.9, in order to avoid including the products purchased only rarely, the
```

##### CHAPTER 3. ANALYSIS 25

minimum support is set to 0.01, which stands for the products bought at least 4 times. Filter
the products that fit this threshold and create a new data frame.

Figure 3.10: Filtered products with minimum support of 0.01
From the figure 3.10, there are 125 products remaining, it means a 95% reduction in
the relevant data amount, which will clearly make computations easier. After filtering these
products, a new transactions data frame containing only these products is created (3.11) and
the number of times a product ordered in a customer order is plotted (3.12).

```
Figure 3.11: Data frame containing products with minimum support 0.01
```

##### CHAPTER 3. ANALYSIS 26

Figure 3.12: Number of times each order size occurs
From the figure 3.12, it is clear that most of the orders have 1 or 2 products. Since it makes
no sense to make association rules with only 1 product, these can be neglected.If the minimum
length is set to 4 then orders with 3 or less products will be exclude, so the minimum length
is set to 2, so that it is easy to draw strong association rules. After setting the minimum
length to 2 there is reduction in the total order which is to 567 (39% reduction). Making
all possible combinations, group purchases by orderid, followed by retrieving the order list
that contains the variable productid. This will allow to generate all possible combinations
of each order by limiting it to 2. The below result is all possible combinations for orderid 2
&3.

```
Figure 3.13: Snippet of Code Block
```

##### CHAPTER 3. ANALYSIS 27

The Orderid number 3 contains 3 products which are mentioned in orderlist, with these
3 products, there are 3 possible combinations which are mentioned in Products combinations.
All the combinations from all orders are concatenated and then count the number of occurrences.
This way it is easy to call and iterate through the generator which prints out the combinations.
The beauty of generators is that, they keep track of their internal state which are different
from regular functions. So that, when next function is called again it will spit out the second
combination, this way the generator produces all the possible product combinations. After
performing the required tasks, from 2615 transactions, there are 60,633 possible combinations.

#### 3.2.4 FP-Growth Algorithm

Finding frequent item sets without candidate generation. First compress the database representing
frequent items into a frequent-pattern tree or fp-tree, which retains the item set association
information. Then divide the compressed database into a set of conditional databases (a
special kind of projected database), each associated with one frequent item or ”pattern
fragment” and mines each such database separately.

**Mathematical Explanation:**

Set the Minsupport for the example(3.6) as 2, then construct the fp-tree and generate the
rules from the tree. To build a fp-growth tree the items should be arranged in descending

```
Transaction ID (TID) List of Item ID’s
X1 P1,P2,P5
X2 P2,P4
X3 P2,P3
X4 P1,P2,P4
X5 P1,P3
X6 P2,P3
X7 P1,P3
X8 P1,P2,P3,P5
X9 P1,P2,P3
```
```
Table 3.6: Transactions of Customers for FP-Growth Algorithm
```
order according to their support count(table 3.8).


##### CHAPTER 3. ANALYSIS 28

```
Items Support Count
P1 6
P2 7
P3 6
P4 2
P5 2
```
```
Table 3.7: Items Support Count
```
```
Items Support Count
P2 7
P1 6
P3 6
P4 2
P5 2
```
Table 3.8: Items Support Count in Descending
order
Start the FP-tree by taking null as a root node, from the table 3.6, take the first
transaction X1, the corresponding items are _P1,P2,P5_ and arrange these items according
to the support count table(3.8). So. the order will be _P2,P1,P5_. Starting from the root node
take a left node for _P2_ and it’s count from the transactions table(3.6, which is followed by
_P1_ and it’s count, _P5_ and it’s count.

For the second transaction _X2_ (table,3.6, the items are _P2,P4_. Arrange these items in
descending order according to the support count table(3.8, the descending order according
to the table(3.8) is _P2,P4_. Start the steps for the fp-tree from the root node, then check if
_P2_ has any node from the root node, if it has a node then add the count to _P2_ node else
create a new node for _P2_. Then check for _P4_ , if it has any node then add the count to _P4_
node, else start a new node from _P2_ node because the _P2,P4_ are from the same transaction
and _P4_ is followed by _P2_.

```
Figure 3.14: FP-Tree
```

##### CHAPTER 3. ANALYSIS 29

After completing the FP-tree (figure 3.14), build a table from the tree to derive frequent
patterns for each item. The table consists of four columns: items, conditional patterns base,
conditional fp-tree and frequent patterns generated. The table is arranged starting with least
support count item.

```
Item Conditional Pattern Base Conditional FP-tree Frequent Patterns Generated
P5 [(P2,P1:1),(P2,P1,P3:1)] (P2:2, P1:2) (P2,P5:2),(P1,P5:2),(P2,P1,P5:2)
P4 [(P2,P1:1),(P2:1)] (P2:2) (P2,P4:2)
P3 [(P2,P1:1),(P2:2),(P1:2)] (P2:4,P1:2),(P1:2) (P2,P3:4),(P1,P3:4),(P2,P1,P3:2)
P1 [(P2:4)] (P2:4) (P2,P1:4)
```
```
Table 3.9: Frequent Patterns
```
For each item. calculate the conditional pattern base, conditional fp-tree and frequent
patterns. Consider item _P5_ from the table(3.9), the conditional pattern base for this item is
_[(P2,P1:1),(P2,P1,P3:1)]_ , this is obtained from the fp-tree by calculating the path travelled
to reach the item _P5_ from the root node and taking the count of nodes in the way. So, for
_P5_ we have two sets _(P2,P1:1)_ with support count 1, _(P2,P1,P3:1)_ with support count 1 for
each item. Next columns is conditional fp-tree in this the total count of each item from the
column conditional pattern base is calculated. This will be _(P2:2,P1:2)_ which is item and it’s
total support count. The minimum support count is set to 2 so, the items with less than this
minimum support count are excluded. In this case _P3_ has support count less than 2 so, it
is excluded from the calculation. In the frequent patterns generated column, the result from
the column conditional fp-tree and item column are joined to generate frequent patterns and
their support count. In this case for the support count if both the items have same support
count then take the count of any one of the item else if, the support count is different for
both the items then take the minimum support of the that items.

**FP-Growth Implementation**

Pyspark is used for this implementation because there are SQL steps included in extracting
data frames which will be used to build the fp-growth model. Creata a data frame with
orderid and items. If we compare this data frame with the above example(3.6), the transactions
are orderid and list of items are the items.


##### CHAPTER 3. ANALYSIS 30

```
Figure 3.15: Basket Data frame (orderid & products)
```
Displaying the most frequent items in the basket after training the model.

```
Figure 3.16: Frequent Patterns
```
The top 5 most frequent items purchased by customers are Organic Strawberries, Bag of
Organic Bananas, Organic Hass Avocado, Organic Baby Spinach.


##### CHAPTER 3. ANALYSIS 31

#### 3.2.5 Collaborative Filtering

```
Collaborative filtering is used for the process of recommendation systems. Few functions are
created to get customer’s, product’s, feature’s and many other functions.
```
```
The function getuserlist(3.6), creates a list of customer’s with the usercolumn that
comes from the inputted data sets.
1 def get_user_list(df ,user_column):
2 return np.sort(df[user_column ]. unique ())
Listing 3.6: list of users function
```
```
The getproductlist function(3.7) is used to create a list of products, using productnamecolumn
which contains products from the given data then return the products list.
1 def get_product_list(df ,product_name_column):
2 product_list=df[product_name_column ]. unique ()
3 return product_list
Listing 3.7: list of products function
```
Idmapping function(3.8) is used to create or map the products list with userid, itemid
and featuresid. Looping through the user list and assign it to userindexmapping, loop
through the feature lit and assign to featureindexmapping and after performing these steps
return the data that was mapped.
1 def id_mappings(user_list , item_list , feature_list):
2 user_to_index_mapping = {}
3 index_to_user_mapping = {}
4 for user_index , user_id in enumerate(user_list):
5 user_to_index_mapping[user_id] = user_index
6 index_to_user_mapping[user_index] = user_id
7 item_to_index_mapping = {}
8 index_to_item_mapping = {}
9 for item_index , item_id in enumerate(item_list):
10 item_to_index_mapping[item_id] = item_index
11 index_to_item_mapping[item_index] = item_id
12 feature_to_index_mapping = {}
13 index_to_feature_mapping = {}
14 for feature_index , feature_id in enumerate(feature_list):
15 feature_to_index_mapping[feature_id] = feature_index
16 index_to_feature_mapping[feature_index] = feature_id
17 return user_to_index_mapping , index_to_user_mapping ,
18 ↪item_to_index_mapping , index_to_item_mapping ,
19 ↪feature_to_index_mapping , index_to_feature_mapping

```
Listing 3.8: function for ID mappings
```
```
Next function(3.9) is usrprodint (user products interaction), create a usrprod (user
products) data frame by merging products and users data set using evalset as prior for the
```

##### CHAPTER 3. ANALYSIS 32

training data, store the count of products if number of purchases increases or goes up. Again
create a usrprod (user products) data frame by merging products and users data set using
evalset as train for the testing data, then again store the count of products if number of
purchases increases or goes up and also consider the training data products count. Now,
merge the user product train data frame with the user products test data frame and then
return the user product rating or count of train and test data frames.
1 def usr_prod_int(ords_df , OrdProdTr_df , ords_prds_ts , prds_df):
2 usr_prod_tr = ords_df[ords_df["eval_set"] == "prior"]
3 ↪[["user_id", "order_id"]] merge(OrdProdTr_df [["order_id",
4 ↪"product_id"]]).merge(prds_df [["product_id",
5 ↪"product_name"]])[["user_id", "product_name"]]. copy()
6
7 usr_prod_tr["prod_cnt"] = 1
8 usr_prd_rt_tr = usr_prod_tr.groupby (["user_id",
9 ↪"product_name"], as_index = False)["prod_cnt"].sum()
10
11 usr_prod_ts = ords_df[ords_df["eval_set"] == "train"]
12 ↪[["user_id", "order_id"]].\ merge(ords_prds_ts
13 ↪[["order_id","product_id"]]).merge(prds_df [["product_id",
14 ↪"product_name"]])[["user_id", "product_name"]]. copy()
15
16 usr_prod_ts["prod_cnt"] = 1
17 usr_prod_rt_ts = usr_prod_ts.groupby (["user_id",
18 ↪"product_name"], as_index = False)["prod_cnt"].sum()
19
20 usr_prod_rt_ts=usr_prod_rt_ts .\ merge(usr_prd_rt_tr.rename
21 ↪(columns = {"prod_cnt" : "prev_prod_cnt"}), how =
22 ↪"left").fillna (0)
23 usr_prod_rt_ts["prod_cnt"] = usr_prod_rt_ts.apply(lambda
24 ↪x:x["prev_prod_cnt"] +x["prod_cnt"], axis = 1)
25 ↪usr_prod_rt_ts.drop(columns =["prev_prod_cnt"],inplace = True)
26
27 return usr_prd_rt_tr , usr_prod_rt_ts

```
Listing 3.9: function of user product interaction
```
```
After creating these functions, another function(3.10) to return the matrix is created for
the users, products and transactions because the collaborative filtering is totally dependent
on the matrix factorisation.
1 def int_mat(d, d_col_rw , d_col_col , d_col_val , rw_indx_mp ,
2 ↪col_indx_mp):
3 a = d[d_col_rw ].apply(lambda r: rw_indx_mp[r]).values
4 b = d[d_col_col ].apply(lambda r: col_indx_mp[r]).values
5 c = d[d_col_val ]. values
6 return coo_matrix ((c, (a, b)), shape = (len(rw_indx_mp),
7 ↪len(col_indx_mp)))
Listing 3.10: Function for Matrix interaction
```

##### CHAPTER 3. ANALYSIS 33

The last function is products features function(3.11), this function returns the product
features interaction data frame, the departments and aisles are fitted to the product feature
data frame in new columns, then group the data and return the final result grouping for
summing over feature count.
1 def prd_ft_int(prd_df , als_df , dpt_df , als_wt = 1, dpt_wt = 1):
2 prd_ft_df = prd_df.merge(als_df).merge(dpt_df)[["product_name",
3 ↪"aisle", "department"]]
4 prd_ft_df["product_name"] = prd_ft_df["product_name"]
5 prd_ft_df["aisle"] = prd_ft_df["aisle"]
6 prd_ft_df["department"] = prd_ft_df["department"]
7
8 prd_als_df = prd_ft_df [["product_name", "aisle"]]. rename
9 ↪(columns = {"aisle" : "feature"})
10 prd_als_df["feature_cnt"] = als_wt
11 prd_dpt_df = prd_ft_df [["product_name","department"]]. rename
12 ↪(columns = {"department" : "feature"})
13 prd_dpt_df["feature_cnt"] = dpt_wt
14
15 prod_ft_df = pd.concat ([prd_als_df , prd_dpt_df],
16 ↪ignore_index=True)
17
18 prod_ft_df = prod_ft_df.groupby (["product_name", "feature"],
19 ↪as_index = False)["feature_cnt"].sum()
20
21 return prod_ft_df

```
Listing 3.11: funtion for product feature interaction
```
```
Using these functions a LightFM model is trained and AUC score is calculated without
product features this is know as pure collaborative filtering and with product features. Steps
involved in model training and calculating the metrics are:
```
1. Create product feature matrix, this will allow to know how many products were ordered
    and what feature it is.
2. Create user product matrix for both train and test sets, this is the relationship between
    user and product in train and test sets.
3. Create user item matrix for training data, testing data and also create product feature
    interaction matrix.
4. Initialize the model keeping loss as ’warp’.
5. Fit user product matrix train set with number of threads as 2.
6. Then calculate the AUC metric score.

```
After training the model and getting the auc score. The model is retrained again to
recommend the products and the train and test sets are combined together for this purpose.
```

##### CHAPTER 3. ANALYSIS 34

Training set contains previous number of orders with rating by customer, test set contains
most recent number of orders with ratings by the customer.
1 def combined_train_test(tr , ts):
2 tr_dt = {}
3 for tr_r , tr_c , tr_d in zip(tr.row , tr.col , tr.data):
4 tr_dt [(tr_r , tr_c)] = tr_d
5
6 for ts_r , ts_c , ts_d in zip(ts.row , ts.col , ts.data):
7 tr_dt [(ts_r , ts_c)] = max(ts_d , tr_dt.get((ts_r , ts_c), 0))
8
9 r_e = []
10 c_e = []
11 d_e = []
12 for r, c in tr_dt:
13 r_e.append(r)
14 c_e.append(c)
15 d_e.append(tr_dt[(r, c)])
16
17 r_e = np.array(r_e)
18 c_e = np.array(c_e)
19 d_e = np.array(d_e)
20
21 return coo_matrix ((d_e , (r_e , c_e)), shape = (tr.shape[0],
22 $\hookrightarrow$tr.shape [1]))

```
Listing 3.12: Function for combining train, test sets & retraining the model
```
### 3.3 Ethical, Professional and Legal Issues

```
There are no ethical, professional and legal issues involved in this project, because the data
was taken from an open source website and also the data does not contain any human related
information like: address, phone numbers or any other personal information.
```

## Chapter 4

# Results & Discussion

### 4.1 Exploratory Data Analysis Results

#### 4.1.1 How many orders in a week per day?

The week starts from Sunday(0), the customers ordered more during Sundays(0) and Mondays(1)
when compared to other days, which are almost of the same number of orders.

```
Figure 4.1: Orders in a week per day
```
#### 4.1.2 How many orders in a day per hour?

From the figure 4.2 the highest number of orders are during Morning, Afternoon, Evening.

##### 35


##### CHAPTER 4. RESULTS & DISCUSSION 36

```
Figure 4.2: Orders in a day per hour
```
#### 4.1.3 How many orders day vs hour?

Majority of the orders are during Monday morning’s and Sunday afternoon’s.

```
Figure 4.3: Day vs Hour
```
**What is time interval between the orders?**

Customers order once in every week (peak at 7 days) or once in a month (peak at 30 days).
There are also similar peaks at 14, 21 and 28 days (weekly intervals).


##### CHAPTER 4. RESULTS & DISCUSSION 37

```
Figure 4.4: Time Interval of the orders
```
#### 4.1.4 What are the popular products ordered?

Most ordered products in the OrdProdPr data set which is the previous transaction or
order details of customers are Banana, Organic Bananas, Organic Strawberries. Most of the
popular products are from fruits and vegetables aisles.

```
Figure 4.5: Popular Products
```

##### CHAPTER 4. RESULTS & DISCUSSION 38

#### 4.1.5 What are the top aisles that the products from?

The top aisles are fresh vegetables, fresh fruits and this is evident because the most popular
products are ordered from the same aisles.

```
Figure 4.6: Top Aisles
```
#### 4.1.6 What are the popular products that were reordered?

```
Figure 4.7: Popular Products that were reordered
```

##### CHAPTER 4. RESULTS & DISCUSSION 39

#### 4.1.7 What is the reorder ratio of departments?

The **dairy** department has the highest reorder ratio and **personal care** has the lowest
reorder ratio.

```
Figure 4.8: Department reorder ratio
```
#### 4.1.8 What are the popular departments that the products reordered from?

```
Figure 4.9: Popular departments that the products were reordered from
```

##### CHAPTER 4. RESULTS & DISCUSSION 40

#### 4.1.9 Relationship between how adding a product to the cart affects the

#### reorder ratio

Initially added products are more likely to be reordered again when compared to the products
added later. This makes sense, since everyone tend to first order all the products we used to
by frequently and then look out for the new products available.

```
Figure 4.10: Reorder Ration of a product added to the cart
```
#### 4.1.10 Heatmap for Reorder ratio (Day vs Hour)

The reorder ratio is high during morning times in a week when compared to afternoons and
evenings.


##### CHAPTER 4. RESULTS & DISCUSSION 41

```
Figure 4.11: Reorder ratio Day vs Hour
```
### 4.2 Association Rule Mining Results

#### 4.2.1 Apriori Algorithm

1. **Combination Occurrences**

```
Figure 4.12: Combination Occurrences
```
```
From the 1332 transactions there are 41,452 combinations and this is for the small
subset.
```

##### CHAPTER 4. RESULTS & DISCUSSION 42

2. **Deriving the rules on whole data set with minimum support of 0.01**

```
Figure 4.13: Rules with minimum support 0.01
```
```
With minimum support of 0.01, the strongest relationship is between organic raspberries
and organic strawberries, 25% customers who bought organic raspberries also bought
organic strawberries. All other association rules with these criteria involve some produce
and bananas. The highest confidence is 38% which is between fuji apples and banana,
but the lift is not high enough, ranging from 1.4-2.6. It is also noteworthy that, even
though the rules output combinations of the most commonly purchased products, their
support is lower than 0.02. That means all other combinations of two will be present
in less than 2% of all the orders and combinations of three or more will be rare.
```
3. **Deriving the rules on whole data set with minimum support of 0.05 and**
    **maximum length of 4**


##### CHAPTER 4. RESULTS & DISCUSSION 43

```
Figure 4.14: Rules with minimum support 0.05 & maximum length of 4
There are some lifts higher than 5 for cilantro and lime, garlic and onion. The confidence
is higher for fuji apple and banana (38%).
```
4. **Deriving the rules on whole data set with minimum support of 0.002 and**
    **maximum length of 3**

```
Figure 4.15: Rules with minimum support 0.002 & maximum length of 3
With minimum support of 0.002, 218 rules were generated, the top 10 rules were
```

##### CHAPTER 4. RESULTS & DISCUSSION 44

```
displayed. The strongest association with lift 73 is between blueberry and raspberry
non-fat yoghurt, followed by other paired flavours of yoghurt with life ranging from
43-61. The highest confidence of 45% is also for different kinds of yoghurts. Next, there
are paired berries and peppers, then flavoured sparkling water.
```
5. **Deriving the rules on whole data set with minimum support of 0.001 and**
    **maximum length of 2**

```
Figure 4.16: Rules with minimum support 0.001 & maximum length of 2
```
```
With minimum support of 0.001 and maximum length of 2 a total of 400 rules were
returned. From the top 20 rules, the relationship between yoghurt types and some
kinds of sparkling water is reinforced. Lifts are as high as 76, and the confidence is
up to 45%. The customers tend to purchase more than one flavour at once, opting for
diverse tastes. If the retailer’s were willing to promote yoghurt product, they should
sell it with promotions along with other yoghurt products.
```
**Apriori Conclusion**

The model shows a very consistent relationship between different types of yoghurts as shown
by the confidence from the derived rules of apriori algorithm because the customers tend to go
for different flavours that are similar to the ones they buy. This could helps the retailer’s to
use this to their advantage when selling a new type of yoghurt by promoting it with another
flavour similar to it. This also fall into the sparkling water products and it’s flavour’s.

#### 4.2.2 FP-Growth Algorithm

**Deriving the rules on whole data set with Minimum support of 0.01**

1. **Predicting what a customer bought(antecedent) and recommending the**
    **products what they will buy(consequent)**


##### CHAPTER 4. RESULTS & DISCUSSION 45

```
Figure 4.17: Antecedent & Consequent with minimum support of 0.01
```
```
The above result(4.17) has a confidence of 0.29(29%) and above, the model will recommend
the purchase of Bag of Organic Bananas to anyone who have bought Organic Hass
Avocado with confidence of 0.33 & lift value of 2.81, Organic Raspberries with confidence
of 0.32 & lift of 2.72. Confidence says that 38.8% of the customers who bought Organic
Hass Avocado will also buy Bag of Organic Bananas and the lift support this rule with
value of 2.81 which says that there is increase in the expectation that the customers will
buy Bag of Organic Bananas, when we know that they bought Organic Hass Avocado.
```
2. **Actual products vs Predicted products**

```
Figure 4.18: Actual vs Predicted products with minimum support of 0.01
```
**Deriving the rules on whole data set with Minimum support of 0.005**

1. **Predicting what a customer bought(antecedent) and recommending the**
    **products what they will buy(consequent)**


##### CHAPTER 4. RESULTS & DISCUSSION 46

```
Figure 4.19: Antecedent & Consequent with minimum support of 0.005
If the value of minimum support is changed the rules derived will also change, which can
be seen from the result(4.19. As the minimum support is changed from 0.01 to 0.005, the
products in the antecedent has increased to two products. The model will recommend
the purchase of Bag of Organic Bananas to anyone who bought Organic Hass Avocado
& Organic Strawberries with confidence of 0.46 & lift of 3.91 and a new rule has been
discovered in this result for Oragnic Fuji Apple and Banana with confidence of 0.37
and lift value of 2.6. Confidence says that 46.1% of the customers who bought Organic
Hass Avocado & Oragnic Strawberries will also buy Bag of Organic Bananas and the lift
support this rule with a value of 3.91 which says that there is increase in the expectation
that the customers will buy Bag of Organic Bananas, when we know that they bought
Organic Hass Avocado & Organic Strawberries.
```
2. **Actual products vs Predicted products**

```
Figure 4.20: Actual vs Predicted products with minimum support of 0.005
```
**Deriving the rules on whole data set with Minimum support of 0.002**

1. **Predicting what a customer bought(antecedent) and recommending the**
    **products what they will buy(consequent)**


##### CHAPTER 4. RESULTS & DISCUSSION 47

```
Figure 4.21: Antecedent & Consequent with minimum support of 0.002
The minimum support value is changed from 0.005 to 0.002 and derived rules have
increased with more of the two frequent item sets. The model will recommend the
purchase of Bag of Organic Bananas to anyone who bought Organic Hass Avocado &
Organic Raspberries with confidence of 0.52 & lift of 4.41 and a new rule has been
discovered in this result for Strawberries,Organic Avocado and Banana with confidence
of 0.46 and lift value of 3.2. Confidence says that 52.1% of the customers who bought
Organic Hass Avocado & Organic Raspberries will also buy Bag of Bag of Organic
Bananas and the lift support this rule with a value of 4.41 which says that there is
increase in the expectation that the customers will buy Bag of Organic Bananas, when
we know that they bought Organic Hass Avocado & Organic Raspberries.
```
2. **Actual products vs Predicted products**

```
Figure 4.22: Actual vs Predicted products with minimum support of 0.002
```
**Deriving the rules on whole data set with Minimum support of 0.001**

1. **Predicting what a customer bought(antecedent) and recommending the**
    **products what they will buy(consequent)**


##### CHAPTER 4. RESULTS & DISCUSSION 48

```
Figure 4.23: Antecedent & Consequent with minimum support of 0.001
```
```
The minimum support value is changed from 0.002 to 0.001 and the rules for three
frequent item sets are generated. The model will recommend the purchase of Bag of
Organic Bananas to anyone who bought Organic Hass Avocado & Organic Raspberries
& Organic Strawberries with confidence of 0.59 & lift of 5.07 and a new rule has
been discovered in this result for Organic Cucumber, Organic Hass Avocado, Organic
Strawberries and Bag of Organic Bananas with confidence of 0.54 and lift value of
4.63. Confidence says that 59% of the customers who bought Organic Hass Avocado &
Oragnic Raspberries & Organic Strawberries will also buy Bag of Organic Bananas and
the lift support this rule with a value of 5.07 which says that there is increase in the
expectation that the customers will buy Bag of Organic Bananas, when we know that
they bought Organic Hass Avocado & Organic Raspberries & Organic Strawberries.
```
2. **Actual products vs Predicted products**

```
Figure 4.24: Actual vs Predicted products with minimum support of 0.001
```

##### CHAPTER 4. RESULTS & DISCUSSION 49

#### 4.2.3 Collaborative Filtering Results

**Average AUC of the model without features (Pure Collaborative filtering)**

Figure 4.25: Model AUC without features
After modeling the data through LightFM algorithm without features, the average AUC
is 0.94.

**Average AUC of the model with features**

Figure 4.26: Model AUC with features
After adding the features and training the model, the AUC value is reduced to 0.80 when
compared to the model without features.


##### CHAPTER 4. RESULTS & DISCUSSION 50

**Displaying the Recommended products for customer’s 7 & 20**

**Customer 7**

```
Figure 4.27: Result of Customer 7
```

##### CHAPTER 4. RESULTS & DISCUSSION 51

**Customer 20**

```
Figure 4.28: Result of Customer 20
```
From the above two tested predictions for user 7 and 20, we found out that some predicted
products were bought by the customer. For instance, in user 20 we can see that the model


##### CHAPTER 4. RESULTS & DISCUSSION 52

predicted a list of products, out these few products a few have be bought by the customer.
This concludes that atleast 1 out of 10 products are bought by the customers from the
recommended list of products which are predicted by our model. Moreover, our model AUC
is 94%, which is a good accuracy and very accurate but the performance is very slow due to
large data set which is over 8GB.


## Chapter 5

# Conclusion & Future Work

### 5.1 Conclusion

Originally developed in the marketing sector, Market Basket Analysis has been successfully
used in a variety of disciplines, including bioinformatics, nuclear science, immunology, geophysics,
and more recently, geophysics. According to one explanation, MBA is becoming more popular
across scientific disciplines because researchers are better able to assess the presence of
association rules when they use an inductive approach to thinking. Taking everything into
consideration, and putting it all together, we believe that recommendation systems may
have a significant effect on marketing and sales research, which can then be utilized to make
strategic company choices.

### 5.2 Future Work

Implementing new and sophisticated mining techniques, as well as apriori and fp growth for
better performance and faster results for sparse data sets, may help to enhance the overall
quality of the project. As part of the current approach, association rules are only used to
exploit collective information, such as building a model by identifying similarity between
customers’ product associations and recommending another customer purchase an item that
is similar to the one that was previously recommended. Additionally, association rules may be
used to exploit content-based information, such as identifying product similarities and making
recommendations for items that are similar to those that have been previously purchased
by the user. Because the computation of similarity takes performed at the product level, a
content-based recommendation system does not need a large amount of user data to function.
The two methods may be combined into a hybrid strategy that can benefit from the benefits of
both item-based and customer-based approaches in future work, perhaps. This program may
be expanded to include other features such as sales monitoring, product tracking, discounting,
and pricing computation, among others. This technique has the potential to be used in the
future to very big databases where memory space is expensive and has to be increased. It
may be fine-tuned even more to achieve greater efficiency and performance.

##### 53


# Bibliography

```
[1]https://en.wikipedia.org/wiki/Pandas_(software).
```
```
[2]https://en.wikipedia.org/wiki/NumPy.
```
```
[3]https://en.wikipedia.org/wiki/Matplotlib.
```
```
[4] Kaggle instacart data.
```
```
[5]Agrawal, R., and Srikant, R.Fast algorithms for mining association rules. 487–499.
IBM Almaden Research Center 650 Harry Road, San Jose, CA 95120, 1994.
```
```
[6]Cachon, G. P., and K ̈ok, A. G. Category management and coordination in retail
assortment planning in the presence of basket shopping consumers. Management Science
53 (2007), 934–951.
```
```
[7]Cil, I. Consumption universes based supermarket layout through association rule
mining and multidimensional scaling. Expert Systems with Applications 39 (2012),
8611–8625.
```
```
[8]G, S., and Rangaswamy, S. Optimized association rule mining using genetic
algorithm. National Journal of Computer Science and Engineering and Information
Technology Research (JCSEITR) 2 (2012), 1–9.
```
```
[9]Gatzioura, A. & S`anchez-Marr`e, M.A case-based recommendation approach for
market basket data. IEEE Intelligent Systems 30 (2015), 20–27.
```
[10] Julander, C. Basket analysis: A new way of analysing scanner data. _International
Journal of Retail & Distribution Management 20_ (1992).

[11] Kanagawa, Y., M. S.-K. S., and Imamura, T.Association analysis of food allergens.
_Pediatric Allergy and Immunology 20_ (2009), 347–352.

[12] Kaur, M., and Kang, S. Market basket analysis: Identify the changing trends of
market data using association rule mining. _Procedia Computer Science 85_ (2016), 78–85.

[13] Madani, S. _Mining Changes in Customer Purchasing Behavior: A Data Mining
Approach_. 2009.

##### 54


##### BIBLIOGRAPHY 55

[14] Mostafa, M. M. Knowledge discovery of hidden consumer purchase behaviour: A
market basket analysis. _International Journal of Data Analysis Techniques and Strategies
7_ (2015), 384–405.

[15] Paranjape-Voditel, P., and Deshpande, U.An association rule mining based stock
market recommender system. 21–24. Second International Conference on Emerging
Applications of Information Technology, 2011.

[16] Shah, K., S. A.-D. S.. A. K. Recommender systems: An overview of
different approaches to recommendations. _International Conference on Innovations in
Information, Embedded and Communication Systems (ICIIECS)_ (2017), 1–4.

[17] Singh, A., and Sinwar, D.Optimization of association rule mining using fp-growth
algorithm with ga. _International Journal for Research in Applied Science and
Engineering Technology V_ (2017).

[18] Yazgana, P., and Kusakci, A. A literature survey on association rule mining
algorithms. _Southeast Europe Journal of Soft Computing 5_ (2016).


