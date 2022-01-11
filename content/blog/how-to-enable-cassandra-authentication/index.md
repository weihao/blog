---
title: Enable Cassandra Authentication
date: "2020-01-22T00:00:00.000Z"
description: "Enable cassandra user and password authentication system"
---

## Enable Cassandra Database Authentication

Edit `cassandra.yaml`

```sh
nano /etc/cassandra/cassandra.yaml
```

Set `authenticator` to `PasswordAuthenticator`

```
authenticator: PasswordAuthenticator
```

**Restart the service**

Use default super user to log into `cqlsh`

```sh
cqlsh -u cassandra -p cassandra
```

Create a new super user

```sh
CREATE ROLE prod WITH SUPERUSER = true AND LOGIN = true AND PASSWORD = 'prod';
```

Disable default super user

```sh
ALTER ROLE cassandra WITH SUPERUSER = false AND LOGIN = false;
```
