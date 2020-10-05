# Product Reviews Big Data
Review analysis with Big Data

## Project overview
The goal of the project is to investigate the bias of Amazon Vine opinions on of video games. PySpark and Hadoop are utilized to process Big Data of amazon product reviews that are loaded from AWS server. After loading cleaning and transforming the data, the data are loaded into PostgreSQP data base that is located on AWS server. The Python algorithm used for data ETL is written and it is executed from Google Colab.

## Objectives
* Utilize Big Data to determine if Amazon Vine opinions of video games are biased.
* Load the data into PostgeSQL data base located on AWS server.

## Results and analysis

### AWS operation
* Data successfully retrieved from aws, processed and loaded to postgresql database at aws location

### Vine opinions
* Average rating of opinions with Vine that have higher score that without Vine independently if product was purchased or not
* Most of the Vine opinions were done without purchasing product
* Strong suggestion that Amazon Vine data are biased  

Table of average product ratings:
<p align="center">
<img src="https://github.com/tolewicz/Product_Reviews_Big_Data/blob/main/Images/VIne_table.JPG" width="700" height= "450" title= "2D log">
</p>

### Explanation 
In the first glance bias of Vine on the product review seem to be negligible: rating with vine is 4.07 Rating w/o vine is 4.05
However, once the data is filtered by purchased product and compared vine vs no vine the difference is larger: with vine 4.45, without vine 4.19. The reason for such filtering is that, the opinion about purchased product comes from the user, not from a bot. To verify if the vine ratings is biased I looked at the review of product purchased and not purchased with vine. It turned out that the number of purchased products with vine is only 22, which means that most of the vine opinions (4268) was done without purchasing the product, which strongly suggests that the vine opinion is biased.

## Resources 
* Technologies used: Python, Google Colab, PySpark, Hadoop, PostgreSQL, Amazon Web Services (AWS)
* Programs: Analysis_BIg_Data_challenge.ipynb, BIg_Data_challenge.ipynb




