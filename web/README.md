Web
=====

## nginx

This playbook installs the nginx package.

### Vars

* **delete_defaul_vhost**: Delete or not default vhost
    * Type: Boolean
    * Default: false
* **user**:
    * Type: String
    * Default: www-data
* **worker_processes**:
    * Type: Integer
    * Default: $ansible_processor_count
* **pid**:
    * Type: String
    * Default: /var/run/nginx.pid
* **worker_connections**:
    * Type: Integer
    * Default: 768

### Usage

``` bash
$ ansible-playbook nginx.yml -uroot
```

## vhost

This playbook set up all static webs with the [Middleman](http://www.middlemanapp.com)

### Vars

* **name**: The vhost name and main URL
    * Type: String
    * Example: example.org
* **listen**: Port on which server will listen for this URL
    * Type: String
    * Example: ```*:80```
* **aliases**: Other server URLs
    * Type: Array of strings
    * Example: www.example.org
* **repo**: Repository from which source code is pulled
    * Type: String
    * Example: git@github.com:LastStar/laststar.eu
