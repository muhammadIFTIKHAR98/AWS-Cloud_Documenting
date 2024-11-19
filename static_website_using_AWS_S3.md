#we can create the new static website using the AWS S# bucket only.
#steps required
  1) create a S3 bucket (keep the availability zone in mind) keep the Block public access - OFF, bucket versioning - Enabled / Disabled, static website hosting - Enabled.
  2) create Bucket policy - it can be created by using the given policy generator option
      {
    "Version": "2012-10-17",
    "Id": "Policy1732011086328",
    "Statement":
    [
        {
            "Sid": "Stmt1732011083685",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::vegan-product-launch02/*"
        }
    ]
    }

  3) now upload the files required for static web hosting.
