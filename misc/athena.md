# Access cloudfront logs in athena

 - Reference - https://docs.aws.amazon.com/athena/latest/ug/cloudfront-logs.html

## Step 1 - Create TABLE in Athena over cloudfront logs 
    * cr_access -> cloudresume Access

```sql

CREATE EXTERNAL TABLE IF NOT EXISTS default.cr_access_cloudfront_logs (
  `date` DATE,
  time STRING,
  x_edge_location STRING,
  sc_bytes BIGINT,
  c_ip STRING,
  cs_method STRING,
  cs_host STRING,
  cs_uri_stem STRING,
  sc_status INT,
  cs_referrer STRING,
  cs_user_agent STRING,
  cs_uri_query STRING,
  cs_cookie STRING,
  x_edge_result_type STRING,
  x_edge_request_id STRING,
  x_host_header STRING,
  cs_protocol STRING,
  cs_bytes BIGINT,
  time_taken FLOAT,
  x_forwarded_for STRING,
  ssl_protocol STRING,
  ssl_cipher STRING,
  x_edge_response_result_type STRING,
  cs_protocol_version STRING,
  fle_status STRING,
  fle_encrypted_fields INT,
  c_port INT,
  time_to_first_byte FLOAT,
  x_edge_detailed_result_type STRING,
  sc_content_type STRING,
  sc_content_len BIGINT,
  sc_range_start BIGINT,
  sc_range_end BIGINT
)
ROW FORMAT DELIMITED 
FIELDS TERMINATED BY '\t'
LOCATION 's3://hk-log-bucket-00/cloudresume/'
TBLPROPERTIES ( 'skip.header.line.count'='2' )

```



## Step 2 - Query logs for insights 

1. All logs for a date 

     ```sql
     SELECT * 
     FROM default.cr_access_cloudfront_logs 
     WHERE "date" = DATE '2023-12-01' ;
     ```

2. Distinct Edge locations

    ```sql
    SELECT distinct x_edge_location 
    FROM default.cr_access_cloudfront_logs 
    order by x_edge_location desc;
    ```