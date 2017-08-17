# Sprintbox

This is a docker based toolset for running Drupal core sprints.  

Features:

- Drupal 8 HEAD
- `fin init` example

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

    This will initialize local settings and install the site via drush

    ```
    fin init
    ```

3. **On Windows** add `192.168.64.100  drupal8.docksal` to your hosts file

4. Point your browser to the following

    ```
    http://drupal8.docksal
    http://ide.drupal8.docksal
    http://db.drupal8.docksal
    http://irc.drupal8.docksal
    http://mail.drupal8.docksal
    ```

To access db and ide use the following login:
```
userrname: user
password: user
```

When the automated install is complete the command line output will display the admin username and password.

## More automation with 'fin init'

Site provisioning can be automated using `fin init`, which calls the shell script in [.docksal/commands/init](.docksal/commands/init).  
This script is meant to be modified per project. The one in this repo will give you a good example of advanced init script.

Some common tasks that can be handled by the init script:

- initialize local settings files for Docker Compose, Drupal, Behat, etc.
- import DB or perform a site install
- compile Sass
- run DB updates, revert features, clear caches, etc.
- enable/disable modules, update variables values
