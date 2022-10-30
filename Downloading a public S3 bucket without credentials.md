So, you've found an amazon S3 bucket with a bunch of col stuff in it and want to download all of it?

We begin by installing the aws cli utility.

```bash
$ pip install awscli
```

Next, we have to configure it. Set the access key and secret key to anything you like. It won't matter because the bucket you want to download is public and we won't be signing our requests. Depending on the region set in the URL of the S3 bucket, set the region. If there's no region in the URL, enter a random word. Then go to ~/.aws/config to remove the line `Region=` and save it. 

```bash
$ aws configure
```

Create a directory to dump everything in and enter it.

```bash
$ mkdir bucket-dl
$ cd ./bucket-dl
```

And, begin the copy

```bash
$ aws s3 cp s3://calm-assets . --recursive --no-sign-request
```

The command starts an s3 bucket copy from the bucket calm-assets to the working directory `.`  with the added flags asking for recursive copying and not signing the requests with the dummy access and secret keys.

That's it. This is the fastest way to dump a public Amazon S3 bucket to your computer.