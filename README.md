# grafanadata

To play around with grafana we need two things, an grafana account and a data source timescaledb.

You can create a free grafana account here https://grafana.com/signup/starter/connect-account

You can also create a 30 days trial timescaledb database in the could, here https://console.forge.timescale.com/signup

There are guides to how to load data and setup grafana with the database.

https://docs.timescale.com/latest/getting-started/installation-grafana

and other good guides

i would suggest you to install psql for postgres 12 to interact with the database, becaues you need to load data.


To load data from psql create a table with

```
CREATE TABLE modstockdata (
    channel     text                NOT NULL,
    time        bigint              NOT NULL,
    throughput  double precision    NOT NULL
);
```


and then load the data from a csv file

\COPY modstockdata FROM modstockdata.csv CSV