# Gathering AWS Glue Troubleshooting Information<a name="troubleshooting-contact-support"></a>

If you encounter errors or unexpected behavior in AWS Glue and need to contact AWS Support, you should first gather information about names, IDs, and logs that are associated with the failed action\. Having this information available enables AWS Support to help you resolve the problems you're experiencing\. 

Along with your *account ID*, gather the following information for each of these types of failures:

**When a crawler fails, gather the following information:**  

+ Crawler name

+ Crawler ID

  Logs from crawler runs are located in CloudWatch Logs under `/aws-glue/crawlers`\. The URL link to the crawler logs in the AWS Glue console contains both the crawler name and the crawler ID\. Also, the first record of the crawler log in CloudWatch Logs contains the crawler ID for that run\.

**When a test connection fails, gather the following information:**  

+ Connection name

+ Connection ID

+ JDBC connection string in the form `jdbc:protocol://host:port/database-name`\.

  Logs from test connections are located in CloudWatch Logs under ` /aws-glue/testconnection`\. 

**When a job fails, gather the following information:**  

+ Job name 

+ Job run ID in the form `jr_xxxxx`\.

  Logs from job runs are located in CloudWatch Logs under ` /aws-glue/jobs`\. 

**When a local Zeppelin Notebook server fails to start:**  
If you are running on Microsoft Windows, make sure that the `JAVA_HOME` environment variable points to the right Java directory\. It's possible to update Java without updating this variable, and if it points to a folder that no longer exists, Zeppelin fails to start\.