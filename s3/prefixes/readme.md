##create our bucket
```sh
aws s3 mb s3://prefixes-fun-ab-5235-mao
```
##create our folder
```sh
aws s3api put-object --bucket="prefixes-fun-ab-5235-mao" --key="hello/"
```

##create many folders
```sh
aws s3api put-object --bucket="prefixes-fun-ab-5235-mao" --key="mauricio/perucho/sequeda/hedinyer/me/gusta/la/torta/de/vino"
```

