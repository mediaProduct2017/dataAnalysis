# dataAnalysis
dataWarehouse.ipynb focuses on data cleaning and data warehouse construction.

Data science和data analysis关注的核心是建模过程，data engineering关注的核心是数据的准备和清洗、数据的存储、结论的展示等，可以认为，data engineering是data science的一部分。

Data analysis中有一类很常见的问题是，根据当前的一些数据预测未来的情况。比如，在训练狗的网站中，根据网站采集的当前用户的数据，预测该用户付费完成所有训练项目的概率有多大，从而预测未来的销售额；在udacity中，根据学员当前登录网站的数据以及学习情况，预测他完成该nano degree的概率，从而预测未来的销售额。

Data analysis最常用的ETL框架是pandas, numpy和matplotlib.

Data analysis process:

1. question (新的技术产生新的数据，然后根据新的数据提出问题；或者，先提出关心的问题，然后根据问题准备数据)
2. data wrangling: data acquisiton, data cleaning（missing data, outlier, unreasonable data）
3. explore: build intutions about data and find patterns about data
4. draw conclusions or make predictions（建模过程，核心; statistics and machine learning）
5. communicate (blog post, email, paper, power point, conversation; data visulization)

Data wrangling and data exploring are very intertwined because you can't really clean any problems with the data before you take a look at what problems there are.
