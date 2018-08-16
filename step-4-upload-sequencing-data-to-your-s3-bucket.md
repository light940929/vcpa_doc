# Step 4: Upload sequencing data to your S3 bucket

#### **The AWS command line interface \(CLI\) installed in step 1.4 facilitate users to copy and upload sequencing data to your S3 bucket in batch mode.**

To copy files to/from the S3 bucket in AWS CLI, users can use the following command:

```text
 aws s3 cp <source> <destination>
```



#### **1\) copy one sequencing file \(sequencing\_data.bam or equencing\_data.cram\) to the "data" directory located in my-s3-bucket**

```text
aws s3 cp sequencing_data.bam  s3://my-s3-bucket/data/aws s3 cp sequencing_data.cram s3://my-s3-bucket/data/
```

#### 2\) copy all files in my-data-dir into the "data" directory located in my-s3-bucket

```text
aws s3 cp my-data-dir/ s3://my-s3-bucket/data/ --recursive
```

