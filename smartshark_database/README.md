# SmartSHARK Database

Rename and complete the .env file:

```bash
cp .env.example .env
```

Start the database container:

```bash
docker compose up mongo
```

## Option A: Using the provided database dump

The database dump should be downloaded from Zenodo and placed in the `db` folder, which is mounted to the MongoDB container.

```bash
wget -O db/smartshark_db.gz https://zenodo.org/records/15363704/files/smartshark_db.gz
```

The database dump is a gzipped archive. To restore the database, run the following commands:

```bash
docker compose exec mongo bash
mongorestore --gzip --archive=/db/smartshark_db.gz --db smartshark --password smartshark --username smartshark --authenticationDatabase admin
```

## Option B: Run SmartSHARK to collect data

Download and unzip the project repositories to the repos folder:

```bash
wget -O /repos/elasticsearch.zip https://zenodo.org/record/15363704/files/elasticsearch.zip
wget -O /repos/nova.zip https://zenodo.org/record/15363704/files/nova.zip
unzip /repos/elasticsearch.zip -d /repos/
unzip /repos/nova.zip -d /repos/
```

Start the SmartSHARK containers **one by one** in order. **Never all at the same time!**
Example:

```bash
docker compose up -d ...
```
