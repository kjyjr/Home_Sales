# Home_Sales

In this challenge, Spark was used to make temporary views, partition data, cache and uncache a temporary table, verify that the table was uncached, and determine run times for queries.

In particular, knowledge of SparkSQL was applied to determine key metrics about home sales data. The key metrics answered the following questions:

What is the average price for a four-bedroom house sold for each year?

What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms?

What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet?

What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000?

The runtime for the query to answer that last question was determined and then compared with the runtime for the query based on cached data. The cached runtime was significantly faster - one-third the time, in fact, of the noncached query. Then the cached time was further compared with a partitioned/parquet dataframe query. The partitioned/parquet runtime was better than the noncached runtime, but still not as fast the cached one - a little more than double the rate, in fact, of the cached runtime.