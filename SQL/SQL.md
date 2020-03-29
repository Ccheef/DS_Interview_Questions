**1.Given the following datasets(shown as pictures below), can you write a SQL query that returns the top 3 performing ad groups each day?
Here we'll define performance as the ratio between revenue and spend (e.g. revenue / spend). In other words, the higher the ratio the better the peformance. There are multile ad groups in the datasets. The output of the query will be the date and an array of the ad groups.**
![table_1](Q1_table1.png) 
![table_2](Q1_table2.png)
* First we need to merge the tables by date and ad groups. Next, we need to rank the the ads daily by the rev_spend_ratio. Finally, we need to limit the ads daily by the rank, where rank <= 3. Then, we need to aggregate the ad into array. The solution:
![Q1_Solution](Q1_Solution.png)
