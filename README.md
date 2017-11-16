# Remote MySQL Dump

Bash utility for executing a `mysqldump` on a remote host with options for using a `.env` file and connecting via `ssh`

## Usage
>mysqldump-remote [OPTIONS] -u=user --mysql-database=database_name --env="./.env"

## Options
  - **-u|--mysql-user**
    - Database user name
  - **-h|--mysql-host** (Default: "localhost")
    - Database host
  - **-p|--mysql-password**
    - Database password
  - **-d|--mysql-database**
    - Database name
  - **--ssh-user**
    - SSH User
  - **--ssh-host**
    - SSH Host
  - **--ssh-key**
    - SSH Key
  - **-c|--compress** (Default: no)
    - Compress output file with gunzip
  - **-o|--output** (Default: current directory)
    - Directory to output saved file
  - **-e|--env**
    - Environment variables file location ([.env format](https://github.com/vlucas/phpdotenv#usage))
  - **-f|--file-name**
    - Output file name (disregards prefix and suffix)
  - **--prefix**
    - Output file prefix
  - **--suffix**
    - Output file suffix
  - **-h|--help**
    - Display help and exit
  - **-v|-vv|--verbose**
    - Verbose output
    - *-v|--verbose* will output verbose details of the MySQL dump
    - *-vv* (very verbose) will output verbose SSH connection details

## ENV File Variables
  - **MYSQL_HOST**
    - MySQL host or IP address
  - **MYSQL_USER**
    - MySQL database user
  - **MYSQL_PWD**
    - MySQL user password
  - **MYSQL_DB**
    - MySQL database name
  - **SSH_USER**
    - SSH user
  - **SSH_HOST**
    - SSH host name or IP address
  - **SSH_KEY**
    - Path to SSH public key
  - **SSH_PORT**
    - Port to use to connect to remote server via SSH
