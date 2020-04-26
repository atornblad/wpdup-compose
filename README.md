# wpdup-compose

Lightweight docker-compose-based Wordpress development environment for use with exports from
the Duplicator WordPress Migration Plugin *(found [here](https://wordpress.org/plugins/duplicator/) and [here](https://snapcreek.com/duplicator/))*.

## How to use

1. Install and run Wordpress Duplicator on the website you want to export.
2. Copy the export files (`installer.php` and the `*_archive.zip`) to the dupinstall directory.
3. Run `docker-compose up`
4. Open [localhost:8080](http://localhost:8080/) in your browser *(or if you're using docker-machine, go to the machine's IP address)*.
5. Follow the instructions. In step **2** of 4 *(Install Database)*, give the following values:

| Field    | Value        |
| -------- | ------------ |
| Host     | `mysql`      |
| Database | `wordpress`  |
| User     | `wpuser`     |
| Password | `wppassword` |

6. In step **3** of 4 *(Update Data)*, expand the **Options** section to add a new Admin account, if necessary.
