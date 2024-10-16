## create a new bucket

```sh
aws seapi create-bucket --bucket acl-example-ab-5235-mao --region us-east-1
```

## turn of block publick acces for ACLs

````sh
aws s3api put-public-access-block \
--bucket acl-example-ab-5235-mao \
--public-access-block-configuration "BlockPublicAcls=false,IgnorePublicAcls=false,BlockPublicPolicy=true,RestrictPublicBuckets=true"
```

```sh
aws s3api get-public-access-block --bucket acl-example-ab-5235-mao
```