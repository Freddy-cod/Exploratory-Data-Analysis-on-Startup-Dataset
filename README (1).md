
# Exploratory Data Anaylsis on the Startup Dataset.

The purpose of this project is to perform an Exploratory
Data anaylis on the startup data so as to unravel insights and 
trends within the startup world in USA .

### What data is being analysed ?
The data contains data about Startups in the USA . It reveals
data about startup investments , industry trends , startup individual information and its status . It contains numerical and 
categorical data .

### How the data is being analysed ?
Before the actual analysis , the data is cleaned .

### Data Cleaning

Firstly there were some duplicates within the dataset. Two columns had different names but contained the same information. To solve this problem, I created a function that accepts two columns as inputs and compares them to determine how many and whether the contained information within those columns are similar.

Secondly, I realized that the column providing dates was of datatype object. We solved this and turned all the columns containing dates to date time datatype for effective analysis. These dates outlines the dates upon which the company was started, when it was closed, when it first raised money and when last it raised money.

Thirdly, there are some columns which do not contribute much to our analysis, so we dropped them, e.g. id, latitude, label, longitude.

Fourthly, the dataset contained columns which were unmanned. This does not contribute much to our data analysis since we do not know what the information within the column entails.

### Missing Data

Firstly the data has missing values, I used the missingno library to easily visualize the missing values. Furthermore I computed the percentage of the missing data, this helps us to know how to handle the missing data.

The column closed_at has over 63% of missing data. The null values may mean to a greater extent that the company has not closed but is still operating hence the null value. We dropped this column since we are not going to be using it for our analysis.

Unnamed column: 6 and Unnamed: 0 was dropped since it has no value whatsoever. We do not know what the entries of these column mean.

age_first_milestone_year column has only 16 percent of the missing value . We only used this column in analyzing the data distribution thus we did not tamper with this data. We could have filled this data set with mean values, however I think the few data will not affect our findings, and we only use this column once.


### Data analysis
### Main Findings

With regards to data visualization and analysis.  Using a boxplot, I firstly understood the data distribution of the features that I want to analyze. The features that I analyzed included the following features: age_first_funding_year, age_last_funding_year, age_first_milestone_year, age_last_milestone_year, relationships, funding_rounds, milestones and funding_total_usd .

The first thing we seek to consider is whether the total money that the startup has raised affect its status.  Startup in this case, means either the startup has been acquired or has been closed. A bar graph helped us understand that, most companies that raised a significant amount of money has a higher chance of being acquired. Companies who raised little money seem to close at the end of the day.

Secondly, we seek to understand which category raised a lot of money and which one did not. A bar graph easily revealed that startups in the mobile space raised a lot of money. Startups in the clean tech space also raised a lot of money. However during this period startups in the real estate space raised small funds .This can help us understand why startups in a certain industry did not raise funds in that period and help us understand the current  startup trends.

Thirdly, the other goal is to understand the number of startups that go through the rounds of raising money till the end. Interestingly over 300 did not have a backing of a venture capitalist. 

Most startups that go through series A round and raise money, however from this point going on to series D, the number of startups that successful raise money till series D continues to dwindle. At this stage most of the startup have closed. However this seem not affect the total number of startup in the top 500. Most startups in this dataset are in the top 500.

Fourthly using a count plot we try to find out the status of the startup in relation to the number of rounds it went through. Most companies that were acquired had done 2 series rounds .And most startups that closed had raised series A. Thus this suggest that the fact that the startup raised series A does not guarantee its success.

Another interesting finding is that most startups that were acquired have 5 relationships. Most companies that have 2 relationships closed at the end of the day. The moderate number of relationships that seemed to propel a startup to success is 4 and 5. This help us understand the importance of relationships in a startup.

One of the most important things we need to understand as well is, which city seem to lead the race in terms of where most of the money was raised. We found out that Kirkland takes the lead in this dataset and surprisingly overtook San Francisco which is known to be a startup hub.

Let’s look at the correlations in the dataset. There is a strong relationship between age last funding year and the age first funding year. This is the same with age last milestones and age last milestone year.
Another interesting relationship we care about is, startups with 2 and 3 milestones will get more funding rounds (up to 8). On the other hand there seem to be a weak relationship between the milestones which the company has achieved with the total amount of money it raised.



## Acknowledgements

 - [Towards Data Science](https://towardsdatascience.com/exploratory-data-analysis-8fc1cb20fd15)
 
  
## Authors

- [@Freddy-cod](https://github.com/Freddy-cod)

  