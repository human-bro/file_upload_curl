# file_upload_curl
This repo gives different methods to upload local files using curl and only using terminal incase you dont have gui access or if its slow you can use this when your connected through ssh

# Using 0x0.st
```
curl -F "file=@yourfile.txt" https://0x0.st
```
## Example
```
curl -F "file=@note.txt" https://0x0.st
```

## output will be a link to you file 

```
https://0x0.st/8Gll1.txt
```

## To upload a remote file

```
curl -F "url=https://example.com/file.zip" https://0x0.st
```

## To create hard to guess urls

```
curl -F "file=@yourfile.txt" -F "secret=1" https://0x0.st
```


## To set expiry
```
curl -F "file=@yourfile.txt" -F "expires=86400" https://0x0.st
```

## To delete a file imediately 

> Get the X-Token
```
curl -i -F "file=@yourfile.txt" https://0x0.st
```

> Delete the file
```
curl -F "token=your-token" -F "delete=1" https://0x0.st/yourfile.txt
```

> Note this only works if you give the -i flag in the start of download if its already uploaded you cant get x token we cant extract x token once the file is uploaded so mention the -i flag when you uploading in the start

---
# using litterbox.catbox.moe

## For File upload 

```
curl -F "reqtype=fileupload" -F "time=1h" -F "fileToUpload=@yourfilename.txt" https://litterbox.catbox.moe/re
sources/internals/api.phpinternals/api.php
```


> time = 1h/12h/24h/72h only these values are accepted
## The output put would be like
```
https://litter.catbox.moe/pjb8ct.txt
```
