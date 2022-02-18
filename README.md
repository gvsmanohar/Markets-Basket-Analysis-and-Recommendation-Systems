# Markets-Basket-Analysis-and-Recommendation-Systems

### Abstract

In recent times, data, especially data mining has played a crucial role in transforming various
industries. Market Basket Analysis is known as an old data mining area, which can be used
as the best example for association rules. Market Basket Analysis(MBA), also known as
association rule mining or affinity analysis, is a technique that may be used in a variety of
areas such as marketing, bio-informatics, education industry, nuclear research and several
other areas. In the past, there have been many mining rules or algorithms which have been
developed by the researchers and currently, there are a lot of researchers working on these
rules to develop new ones in order to make it easy for the retailers to reach their target.
The primary goal of Market Basket Analysis in marketing is to give information to retailers
in order for them to better understand the purchasing behaviour of their customers. This
information can then be used to assist the retailer in making more efficient decisions. The
current methods are designed to operate with static data and do not account for changes
in data over time. Rather than mining static data, the suggested association rules offer a
novel approach to taking into account changes occurring in the data. The ability to make
decisions and comprehend the behaviour of customers has become an increasingly important
and difficult issue for businesses seeking to maintain their position in highly competitive
marketplaces. Technological advancements have opened the way for breakthroughs in query
processing speed and response time in the sub-second range. For evaluating large amounts of
data and making accurate choices, data mining technologies have emerged as the most reliable
technology available in the market. In order to demonstrate the superiority of Market Basket
Analysis over traditional methods, an experimental study was conducted utilizing association
rules. This project covers the data mining method known as association rule mining, as well as
the algorithms: Apriori and FP-Growth that may be useful in examining customer behaviour
and assisting the retailers to increase the sales and customer experience.

### Aims and Objectives

The primary goal of the project is to enable Instacart merchants to understand their existing
customers’ buying behaviour better and to anticipate the purchase behaviour of their prospective
customers. The use of customer transaction data can assist businesses in understanding their
customers’ purchasing behaviour, offering the appropriate bundles and promotions, assortment
planning, and inventory management, thereby helping them to retain customers, increase
sales, and extend their customer relationship.
**The Goals of the project are as follows:**

1. To get an understanding of the buying patterns of the items that are included in the
    customer’s basket.
2. To do research on a wide range of goods that are often bought by customers.
3. To research the most probable goods that consumers will buy, as well as the most likely
    product categories that customers will acquire.
4. To provide product recommendations and suggestions to the customers.



###Overview of the Report

The technological age in which we live has made it possible for commercial organizations to
amass vast amounts of data on their customers and suppliers. Currently, database technology
innovation has developed enough to maintain these information stacks stable; nevertheless, it
is important not only to retain that information but also to evaluate the information in order
to enhance the value of the organization. Businesses must develop appropriate and low-cost
advertising methods that can respond to changes in customer perceptions and requests for
goods in today’s customer-centred marketplaces. Moreover, it may aid businesses in the
identification of a whole new market approach that may be targeted successfully. All together,
reliable, as much as possible, and protected proof-based data is required in order to make
important decisions about market strategy. Data Mining has received probably the greatest
answer to this need as a result of technological advancement. It is the process of identifying
and refining significant data from massive databases, and it covers a wide range of statistical
and computational techniques, such as neural network analysis and clustering, classification,
and summarization of information. This project includes the development of association rules,
which is one of the Data Mining methods used by Market Basket Research and is one of the
techniques used by Market Basket Research. The analysis is carried out on the transaction
data collected from the grocery shops, with the use of Apriori and FP-Growth algorithms, the
main aim is to examine the category of products that are most likely to be promoted in
combination with one another and also to recommend the products to the customers.


# Analysis

The data set for this project is obtained from an open-source website[4], Kaggle. The
data consists of six separate data sets, **orders.csv, products.csv, departments.csv,
aisles.csv, orderproductsprior.csv, orderproductstrain.csv**. From these data sets
there are a total of 206,200 customers or users, over 3 million orders (3.2M), so that is
approximately 16 orders per customer. The total number of products available in the store are
around 49,700 and the number of total ordered products are 3.4 million, so 652 orders for a single
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
- addtocartorder: Order in which each product was added to the cart
- reordered: if a product is reordered or not (Boolean), 1 if a product is reordered
otherwise 0.

So, the aisles data set and departments data set are merged with the products data set,
because the aisles and products data sets have aisleid as a common column. Merging
along this column, we can identify the products according to their respective aisles and for
departments and products data sets we have departmentid as a common column, merging
along this column will result in the department names of all the products.

### Future Work

Implementing new and sophisticated mining techniques, as well as apriori and fp growth for
better performance and faster results for sparse data sets, may help to enhance the overall
quality of the project. As part of the current approach, association rules are only used to
exploit collective information, such as building a model by identifying similarities between
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
future is very big databases where memory space is expensive and has to be increased. It
may be fine-tuned even more to achieve greater efficiency and performance.
