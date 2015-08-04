# Upgrading Phoenix

## find out what version you currently have

```
» mix archive
* hex.ez
* phoenix_new-0.13.1.ez
Archives installed at: /Users/alan/.mix/archives
```

## uninstall old version

`» mix archive.uninstall phoenix_new-0.13.1.ez`

## install new version from GitHub

```
» mix archive.install https://github.com/phoenixframework/phoenix/releases/download/v0.15.0/phoenix_new-0.15.0.ez
Are you sure you want to install archive https://github.com/phoenixframework/phoenix/releases/download/v0.15.0/phoenix_new-0.15.0.ez? [Yn] y
* creating /Users/alan/.mix/archives/phoenix_new-0.15.0.ez
```

## check it did the right thing

```
» mix archive
* hex.ez
* phoenix_new-0.15.0.ez
Archives installed at: /Users/alan/.mix/archives
```
