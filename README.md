# shopware6-database-dump
Dump a Shopware 6 database for your local environments (and filter GDPR data).

## Disclaimer
We support a standard Shopware 6 database along with the official Klarna, PAYONE and Unzer plugins.

Please understand, that we can not give any guarantees for GDPR compliance of the resulting dump.

## Requirements
You need to have `gzip` and `mysqldump` installed and available via your `PATH`.
MySQL will be accessed via IP, sockets are not supported yet.

## Usage
Run `./shopware6-database-dump.sh` to see available options:

```
Dumps a Shopware 6 database with a bit of cleanup and a GDPR mode ignoring more data.

Usage:
  shopware6-database-dump.sh --database db_name --user username [--host 127.0.0.1] [--port 3306] [--gdpr] [--keep-user-data]
  shopware6-database-dump.sh -d db_name -u username [-H 127.0.0.1] [-p 3306] [--gdpr] [--keep-user-data]
  shopware6-database-dump.sh -h | --help

Options:
  -h --help          Display this help information.
  -d --database      Set database name
  -u --user          Set database user name
  -H --host          Set hostname for database server (default: 127.0.0.1)
  -p --port          Set database server port (default: 3306)
  -pw --password     Set password of database user
  --gdpr             Enable GDPR data filtering
  --keep-user-data   Keeping Shopware user tables when --gdpr option is used
```

Your dump will be written to `dump.sql.gz`.

## License
MIT
