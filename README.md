# s3-sync

[![MIT License](http://img.shields.io/badge/license-MIT-blue.svg?style=flat)](LICENSE)

## About

Upload the log file to Amazon S3.

## Requirement

 * AWS Command Line Interface

## Configuration

 * `AWS_DEFAULT_REGION` : Region of S3 bucket.
 * `AWS_S3_BUCKET_PATH` : Local path and S3 path.

e.g.

```
$ cat s3-sync.conf
AWS_DEFAULT_REGION="ap-northeast-1"
AWS_S3_BUCKET_PATH=("/var/log/%s3://path/to/bucket/" "/var/log/%s3://path/to/bucket/")
```

## License

MIT License
