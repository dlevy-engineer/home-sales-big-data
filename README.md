# home-sales-big-data
This project uses SparkSQL to evaluate key metrics about big home sales data, and employs Spark to create temporary views, partition the data, and cache /uncache tables.

## Procedure
- Import the PySpark SQL functions needed for the analysis.
- Read the `home_sales_revised.csv` data into a Spark DataFrame.
- Create a temporary table called `home_sales`.

  #### Observations
  - What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.
  - What is the average price of a home for each year it was built that has three bedrooms and three bathrooms? Round off your answer to two decimal places.
  - What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.
  - What is the "view" rating for homes costing more than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.

- Cache the temporary table `home_sales`.
- Check to ensure the temporary table is cached.
- Using the cached data, run the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
- Partition by the `date_built` field on the formatted parquet home sales data.
- Create a temporary table for the parquet data.
- Run the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
- Uncache the `home_sales` temporary table.
- Verify that the home_sales temporary table is uncached using PySpark.
