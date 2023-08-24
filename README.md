# Dolibarr hosting playground

This repository contains a environment that allows to test [Dolibarr](https://github.com/Dolibarr/dolibarr/) deployment.

```sh
$ docker compose pull
$ docker compose up -d dolibarr --wait
❯ docker compose up -d dolibarr --wait

[+] Running 4/4
 ✔ Network dolibarr-hosting-playground_default       Created    0.2s
 ✔ Container dolibarr-hosting-playground-postgres-1  Healthy   10.8s
 ✔ Container dolibarr-hosting-playground-mail-1      Healthy   10.8s
 ✔ Container dolibarr-hosting-playground-dolibarr-1  Healthy    1.2s
```

Follow this step:

- Go to <http://0.0.0.0/install/fileconf.php?selectlang=en_US>
- Fill `password` in "Password" field
- Click on "Next step->"
- Click on "Next step->"
- Click on "Next step->"
- Define Admin login / password, for instance `admin`, `password` and click on "Next step->"
- Click on "Go to Dolibarr (setup area)"
- Configure "Company/Organization" and "Modules/Applications" sections

Execute:

```sh
$ touch volumes/documents/install.lock
$ sudo chmod u-w volumes/conf/conf.php
```
