
# AWS Terraform Backend With S3 Bucket

### This Repository Provides a Terraform Configuration to Set Up an AWS Backend Using an S3 Bucket for Storing Terraform State Files. By Using an S3 bucket, We Can Ensure that Terraform State is Stored in a Reliable and Scalable Way, While Also Enabling State Locking Via DynamoDB to Prevent Concurrent Modification.

## Create and Setup S3 Bucket for Storing Terraform State File

## Create and Setup DynamoDB Table for Terraform State File Locking

## Configure S3 Bucket and DynamoDB Table Details in terraform.tf File
```sh
backend "s3" {

    bucket = "S3 Bucket Name"
    region = "AWS Region in Which S3 Bucket is Provisioned"
    key    = "Path to Terraform State File in the S3 Bucket"

    dynamodb_table = "DynamoDB Table"

}
```

## Conclusion**<br>
## This Configuration Sets Up a Remote Backend With S3 and Optional State Locking Via DynamoDB, Providing a Robust, Team Friendly Way to Manage Terraform State File.