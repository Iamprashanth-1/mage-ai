# Database

By default, Mage uses sqlite to store orchestration data (trigger, pipeline run, and block run). To use a different database, you can set the `MAGE_DATABASE_CONNECTION_URL` environment variable.

In production, you can set the environment variable in the corresponding Terraform script.

### Postgres
`export MAGE_DATABASE_CONNECTION_URL=postgresql+psycopg2://user:password@host:port/dbname`
