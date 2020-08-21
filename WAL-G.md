To configure WAL-G for AWS, insert credentials in `postgres-walg.env`. An example is provided below.

```bash
PGDATA=/var/lib/postgresql/data
PGWAL=/var/lib/postgresql/data/pg_xlog

# AWS S3 (`AWS_REGION` must be set if any of the other env vars are set. Otherwise, `wal-g` will fail to start.)
# Note that `WALG_S3_PREFIX` should not contain the `AWS_REGION`. For example, the following config is wrong
# AWS_REGION=ca-central-1
# WALG_S3_PREFIX=s3://ca-central-1/postgres-backup/backup1
# and the following is the correct form
# AWS_REGION=ca-central-1
# WALG_S3_PREFIX=s3://postgres-backup/backup1
# since `wal-g` will try to look for the `ca-central-1/postgres-backup/backup1` bucket in `ca-central-1` in the former case.
AWS_SECRET_ACCESS_KEY=
AWS_ACCESS_KEY_ID=
AWS_REGION=
WALG_S3_PREFIX=
```