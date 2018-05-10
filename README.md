# Docksal Quickstart

An example [Docksal](https://docksal.readthedocs.io/en/master/) setup for Drupal projects.

## Setup

1. Make sure you have Docksal installed. If not, you can follow the instructions on the [offical Docksal website](https://docs.docksal.io/en/master/getting-started/env-setup/).

2. Copy the contents of the repo to your Drupal project. From your project's root directory, you can run the following:

   ```bash
    curl -OLs https://github.com/millerrs/docksal-quickstart/archive/master.zip && unzip -qn master.zip && rm master.zip && cp -r docksal-quickstart-master/composer-drupal-8/.docksal . && rm -rf docksal-quickstart-master
    ```

3. Copy *docksal-local.example.env* and rename to *docksal-local.env*.

   ```bash
   cp .docksal/docksal-local.example.env .docksal/docksal-local.env 
   ```

4. Make changes to the *docksal-local.env* file. Options include:
    
    * Changing the virtual host (default: `drupal8.docksal`)
    * Changing the project's document root (default: `docroot/web`)
    * Changing the static port for MariaDB (default: `33061`)
    * Enabling xdebug (default: `0`)
    * Adding a Pantheon site name (default: `none`)

5. Run `fin init`

   If you have a Pantheon site, the latest DB will be downloaded and imported during the site installation.  By default, a database will be setup and you can import a copy of your DB using the included DB import command (`fin db-import [path to db]`).

   Check and see that your site runs.  Now you can start coding!