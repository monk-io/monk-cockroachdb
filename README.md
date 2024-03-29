# CockroachDB & Monk

This repository contains Monk.io template to deploy CockroachDB either locally or on cloud of your choice (AWS, GCP, Azure, Digital Ocean).

## Prerequisites

- [Install Monk](https://docs.monk.io/docs/get-monk)
- [Register and Login Monk](https://docs.monk.io/docs/acc-and-auth)
- [Add Cloud Provider](https://docs.monk.io/docs/cloud-provider)
- [Add Instance](https://docs.monk.io/docs/multi-cloud)

## Make sure monkd is running

```bash
foo@bar:~$ monk status
daemon: ready
auth: logged in
not connected to cluster
```

## Clone Repository

```bash
git clone https://github.com/monk-io/monk-cockroachdb
```

## Load Template

```bash
cd monk-cockroachdb
monk load MANIFEST
```

## Let's take a look at the themes I have installed

```bash
foo@bar:~$ monk list cockroachdb
✔ Got the list
Type      Template        Repository  Version  Tags
runnable  cockroachdb/db  local       -        -
```

## Deploy Stack

```bash
foo@bar:~$ monk run cockroachdb/db
```

## Variables

| Variable     | Description                      | Default                         |
|--------------|----------------------------------|---------------------------------|
| db_port      | CockroachDB database port        | 26257                           |
| admin_port   | CockroachDB admin interface port | 8080                            |
| image        | Docker image tag                 | v20.1.4                         |

## Stop, remove and clean up workloads and templates

```bash
monk purge -a
```
