# AWS-S3bucket
This repo highlights how to create an AWS S3 bucket, using the CLI.
Naming Nomenclature can be found [here](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html)

- Install the AWS CLI on your machine
```bash
$ sudo apt udpate
$ sudo apt install awscli
```

- Configure your AWS Access keys and Secret Access Key on your machine
```bash
$ aws configure
```

- Create a buket with a unique name
```bash
$ aws mb s3://bucketname --region your-region
```

- To enforce an owner on the bucket, add the following code to the above command
```bash
--object-ownership BucketOwnerEnforced
```

- To list items in the bucket, run the following:
```bash
$ aws s3 ls <bucket-url>
```

### Example
```bash
$ aws s3 mb s3://may4u --region us-east-1
```

**Output**
```bash
$ make_bucket: may4u
```

<img width="899" alt="image" src="https://user-images.githubusercontent.com/49791498/160407207-2a60bc25-f1ad-4ca2-8f4f-cbf9ba6b8476.png">

- To delete the bucket,
```bash
$ aws s3 rb s3://bucket-name --force  
```
