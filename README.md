# ansible-php

Default use ppa:ondrej/php repository and version 8.1

### Default variable:
```
__php_repo_name: "ondrej-php"
__php_repo_uris: ["https://ppa.launchpadcontent.net/ondrej/php/ubuntu/"]
__php_packages_state: present
__php_repo_signed: "https://keyserver.ubuntu.com/pks/lookup?op=get&search=0x71DAEAAB4AD4CAB6"
__php_version: "8.1"
__php_fpm_daemon: "php8.1-fpm"
__php_fpm_enable: false

__php_packages:
  - php{{ __php_version }}-bcmath
  - php{{ __php_version }}-cli
  - php{{ __php_version }}-common
  - php{{ __php_version }}-curl
  - php{{ __php_version }}-dev
  - php{{ __php_version }}-fpm
  - php{{ __php_version }}-gd
  - php{{ __php_version }}-igbinary
  - php{{ __php_version }}-imagick
  - php{{ __php_version }}-mbstring
  - php{{ __php_version }}-opcache
  - php{{ __php_version }}-pgsql
  - php{{ __php_version }}-raphf
  - php{{ __php_version }}-readline
  - php{{ __php_version }}-redis
  - php{{ __php_version }}-xdebug
  - php{{ __php_version }}-xml
  - php{{ __php_version }}-zip
  - php{{ __php_version }}
```

### Playbook:

```
- name: PHP install
  hosts: dev-api
  roles:
    - pastir.php
```