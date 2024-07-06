# AWS Glue Job

AWS Glue is a fully managed extract, transform, and load (ETL) service that simplifies the process of preparing and transforming data for analytics. One of the key use cases for AWS Glue is data integration and ETL.

### Key Concepts:

- **Extract Data:** AWS Glue can connect to various data sources such as Amazon S3, RDS, DynamoDB, and many others to extract data.
- **Transform Data:** You can transform the extracted data using Python or Scala scripts. AWS Glue provides a dynamic frame, an abstraction over Apache Spark’s DataFrame, making it easier to work with semi-structured data.
- **Load Data:** After transformation, the data can be loaded into a destination such as an S3 bucket, an RDS database, Redshift, or any other data store.

In this article, you will see a method to perform these functions by converting a CSV file to a JSON file using an AWS Glue job.

### Steps:

#### 1. Download a Sample CSV File

Download a sample CSV file from an online source.

![Sample CSV File](https://github.com/AnuV541/AWS-Glue-Job/assets/110184106/84f1198f-f9bf-46c5-95a1-ff89b610a8bb)

#### 2. Sample User File

This is the downloaded sample user file.

![Sample User File](https://github.com/AnuV541/AWS-Glue-Job/assets/110184106/b655b749-ff0c-42d9-87ec-637ac9ca1c93)

#### 3. Create S3 Buckets

Create two buckets in Amazon S3. One will be the source (here `laamour1`), and the other will be the destination (here `laamour2`).

![Create S3 Buckets](https://github.com/AnuV541/AWS-Glue-Job/assets/110184106/5893a83d-c962-46d8-9727-79ba23f98dba)

#### 4. Upload the CSV File to the Source Bucket

Add the CSV file to the source bucket.

![Upload CSV to Source Bucket](https://github.com/AnuV541/AWS-Glue-Job/assets/110184106/c88d1dee-b600-4ff9-ad48-4b86801799b4)

#### 5. Create an AWS Glue Job

Go to the AWS Glue job console and create a test job. Add the following configurations to the job.

![Create AWS Glue Job](https://github.com/AnuV541/AWS-Glue-Job/assets/110184106/319984c4-f933-420a-8dfc-bb5deaef407f)

#### 6. Create Nodes for the S3 Buckets

Create two nodes for the S3 buckets and configure them as shown.

![Create Nodes](https://github.com/AnuV541/AWS-Glue-Job/assets/110184106/1275efeb-7105-4a5d-9358-62154bd33c67)

#### 7. Configure the Source Bucket

Provide the following configuration to the source bucket properties:

![Source Bucket Configuration](https://github.com/AnuV541/AWS-Glue-Job/assets/110184106/eb603c7d-fb91-4421-b948-b6933a788b10)

#### 8. Configure the Target Bucket

Provide the following configuration to the target bucket properties:

![Target Bucket Configuration](https://github.com/AnuV541/AWS-Glue-Job/assets/110184106/1f319d39-16cf-47c9-882e-c7a0aad2c19b)

#### 9. Run the AWS Glue Job

Run the Glue job. After successful deployment, go to the `laamour2` bucket. You will find the CSV file converted to a JSON file.

![Run the Job](https://github.com/AnuV541/AWS-Glue-Job/assets/110184106/1c496e16-49e0-4bf3-8488-b6631d74e05b)

#### 10. JSON Output of the CSV File

This is the JSON output of the CSV file.

![JSON Output](https://github.com/AnuV541/AWS-Glue-Job/assets/110184106/75f7cef8-3088-4e8b-af24-09d60711eb7f)

By using AWS Glue, the ETL process—Extract, Transform, and Load—has been performed efficiently and quickly.

---

This document provides a comprehensive guide to performing a simple ETL operation using AWS Glue, converting a CSV file to a JSON file. AWS Glue’s powerful capabilities and user-friendly interface make it an excellent choice for managing your data transformation needs.
