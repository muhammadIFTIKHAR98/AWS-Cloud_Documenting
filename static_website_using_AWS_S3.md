#we can create the new static website using the AWS S3 bucket only.
#steps required
  1) create a S3 bucket (name should be keep in mind as it will show the same name on the website) (keep the availability zone in mind) keep the Block public access - OFF, bucket versioning - Enabled / Disabled, static website hosting - Enabled.
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

  3) now upload the files required for static web hosting. there are several files and folders to be uploaded such as -
         css , fonts, images, js folders for website design and theme.
         index.html for website (saved in the same repository with the same name).
         error.html for website in case some error occured while calling index.html (saved in the same repository with the same name).

     

  5) now open the S3 bucket then into static web hosting and click the link.
