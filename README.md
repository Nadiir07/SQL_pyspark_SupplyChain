Supply Chain Analytics in Databricks
This project implements a Kimball-style Star Schema and semantic layer (v_supply_chain_performance) on Databricks to evaluate fulfillment risk and regional profitability. 
Using Spark SQL window functions, the analytical layer measures lead time variance (VAR_SAMP) and on-time delivery rates across routes and product categories. 
During implementation, column naming inconsistencies with single and double underscores (e.g., Days_for_shipping__real_) caused AnalysisException errors during schema registration. 
This issue was resolved by inspecting table metadata via DESCRIBE TABLE and explicitly aliasing normalized column names within the semantic view. The pipeline connects operational lead time delays directly to financial metrics like net profit margin. 
The resulting architecture replaces raw transactional data with a scalable, structured platform for supply chain risk analysis.
