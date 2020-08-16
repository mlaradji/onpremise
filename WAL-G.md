To configure WAL-G for AWS, insert credentials in `postgres-walg.env`. An example is provided below.

```bash
PGDATA=/var/lib/postgresql/data
PGWAL=/var/lib/postgresql/data/pg_xlog

# AWS S3 (`AWS_REGION` must be set if any of the other env vars are set. Otherwise, `wal-g` will fail to start.)
AWS_SECRET_ACCESS_KEY=
AWS_ACCESS_KEY_ID=
AWS_REGION=
WALG_S3_PREFIX=
```