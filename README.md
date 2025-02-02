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
5. communicate (blog post, email, paper, power point, conversation; data visualization)

Data wrangling and data exploring are very intertwined because you can't really clean any problems with the data before you take a look at what problems there are.

从互联网上获取数据(data acquisiton)的途径有：直接下载数据文件，通过网站API从网站数据库中获取，通过爬虫从网站页面获取。

数据存储有可能是在data wrangling之后，也有可能是在data exploring之后。有可能存储在单机系统中，也有可能存储在分布式系统中。存好之后，在需要建模的时候，再从数据库中把需要的数据取出来。

## 数学建模

如上所说，用logistic regression或者neural network来建模的话，是可以用来预测销售量的。

比如，某个网站的用户可能付费或者不付费，有两种办法可以预测销售额。一是，算出每个用户付费的概率，分别乘以付费额，算出总的销售额的期望。二是，先算出每个用户付费的概率，如果概率大于0.5的话，就预测该用户会付费，然后用付费用户数*付费额，就是预测的总的销售额，这种方法在计算销售额时不够科学，但是，好处是，可以预测哪些潜在用户很可能付费，然后跟踪这些用户，把资源投入到这些用户身上，可以有的放矢的把潜在客户转化为付费客户。

在explore和make prediction的过程中，可以得到自变量和因变量之间的相关关系，如果需要进一步确定因果关系，就要用到A/B testing.
