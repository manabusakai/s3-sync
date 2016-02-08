# s3-sync

[![MIT License](http://img.shields.io/badge/license-MIT-blue.svg?style=flat)](LICENSE)

## About

Upload the log file to Amazon S3.

## Requirement

 * AWS Command Line Interface

## Usage

Setup.

```
$ sudo mv s3-sync.conf /etc/sysconfig/s3-sync.conf
$ sudo mv s3-sync /etc/init.d/s3-sync
$ sudo chown root:root /etc/init.d/s3-sync
$ sudo chmod +x /etc/init.d/s3-sync
```

Synchronize.

```
$ sudo service s3-sync sync
```

Use the `cron` for automatic synchronization.

```
$ cat /etc/cron.d/s3-sync
5 * * * * root service s3-sync sync
```

## Configuration

### `AWS_DEFAULT_REGION`

Region of S3 bucket.

### `AWS_S3_BUCKET_PATH`

Local path and S3 path (Split with `%`).

e.g.

```
$ cat /etc/sysconfig/s3-sync.conf
AWS_DEFAULT_REGION="ap-northeast-1"
AWS_S3_BUCKET_PATH=("/var/log/%s3://path/to/bucket/" "/var/log/%s3://path/to/bucket/")
```

## License

MIT License
