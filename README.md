# sharelatex-texlive2018-docker

The docker-compose.yml file is from [overleaf/overleaf](https://github.com/overleaf/overleaf) and our version is upgraded to **texlive2018**.

Thanks to [dennis1f/sharelatex-texlive2018](https://github.com/dennis1f/sharelatex-texlive2018) who built the sharelatex-texlive2018 docker image.

## Usage

```bash
# 1. start up the server
docker-compose up -d
# 2. create the admin account
docker exec sharelatex /bin/bash -c "cd /var/www/sharelatex; grunt user:create-admin --email admin@example.com"
```

You will be given a URL to visit where you can set the password for this user and log in for the first time.

Then open the sharelatex on the default port: http://127.0.0.1:30000

## Setting

```bash
vim docker-compose.yml
```

sharelatex, mongodb, redis data are stored `/opt/sharelatex` by default.

The default language is `cn`, if you use English, just remove this line: `SHARELATEX_SITE_LANGUAGE: cn`
