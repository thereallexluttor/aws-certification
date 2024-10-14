## create a new s3 bucket


````md
aws s3 mb s3://checksums-examples-ab-2342-maop```

## create a file that will we do a checksum on

```
echo "Hello mars"-> myfile.txt
```

## Get a checksum of a file for md5

md5sum myfile.txt

## Upload our file and look at its etag
aws s3 cp myfile.txt s3://checksums-examples-ab-2342-maop
aws s3api head-object --bucket checksums-examples-ab-2342-maop --key myfile.txt


##Lets upload a file with a different kind of checksum

bundle exec ruby crc.rb 


aws s3api put-object \
--bucket="checksums-examples-ab-2342-maop" \
--key="myfilesha1.txt" \
--body="myfile.txt" \
--checksum-algorithm="SHA1" \
--checksum-sha1="YzFlMjllYjk4ZWUwODUyZDkwZjQwYjUwMGVmNzY3MzQzMjRjYjU3Mw=="