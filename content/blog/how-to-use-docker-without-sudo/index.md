---
title: Use Docker Without Sudo
date: "2020-01-22T00:00:00.000Z"
description: "Execute docker commands without blocked by asking to use sudo"
---

## Use Docker Without Sudo

This command adds you into docker group, so you could run docker command without sudo.
```sh
sudo usermod -aG docker $USER
```
The user you added has to **log out and log back in** for it to work.
