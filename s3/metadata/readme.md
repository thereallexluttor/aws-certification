##create bucket

aws s3 mb s3://metadata-fun-ab-5235-mao

##create a new file

echo "Hello mars!" > hello.txt

##upload file with metadada

aws s3api put-object --bucket metadata-fun-ab-5235-mao --key hello.txt --body hello.txt --metadata Planet=Mars

##get metada through head object
aws s3api head-object --bucket metadata-fun-ab-5235-mao --key hello.txt