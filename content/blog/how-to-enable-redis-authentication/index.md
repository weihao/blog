---
title: Enable Redis Authentication
date: "2020-01-22T00:00:00.000Z"
description: "Enable redis password authentication system"
---

## Enable Redis Authentication

Enable redis authentication password.

```sh
redis-cli
CONFIG SET requirepass your_secret_password
```

Test authentication password.

```sh
redis-cli
AUTH your_secret_password
```

If it returns `OK`, then it is working.
