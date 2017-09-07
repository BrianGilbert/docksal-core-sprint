# Sprintbox

This is a docker based toolset for running Drupal core sprints.  

Features:

- Drupal 8 HEAD
- `fin init` command - launches the stack, then triggers `fin site-install`
- `fin site-install` command - installs Drupal

## Setup instructions

### Step #1: Docksal environment setup

**This is a one time setup - skip this if you already have a working Docksal environment.**  

Follow [Docksal environment setup instructions](http://docksal.readthedocs.io/en/master/getting-started/env-setup)

### Step #2: Project setup

1. Clone this repo into your Projects directory

    ```
    git clone https://github.com/briangilbert/docksal-core-sprint.git drupal8-sprint
    cd drupal8-sprint
    ```

2. Initialize the site

    ```
    fin init
    ```

3. Point your browser to the following

    ```
    http://drupal8.docksal
    http://ide.drupal8.docksal
    http://db.drupal8.docksal
    http://irc.drupal8.docksal
    http://mail.drupal8.docksal
    ```

## Credentials

### Drupal

http://drupal8.docksal

```
username: admin
password: password
```

## Cloud9 IDE

http://ide.drupal8.docksal

```
username: user
password: user
```

## Database (Adminer)

http://db.drupal8.docksal

```
username: user
password: user
database: default
```
