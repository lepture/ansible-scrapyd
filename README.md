# lepture.scrapyd

Ansible role which manage Scrapyd.

Requirements
------------

- Stouts.supervisor
- Stouts.nginx

Suggested requirments:

- Stouts.python

Role Variables
--------------

```
scrapyd_enabled: true
scrapyd_user: scrapy
scrapyd_home: /var/www/scrapyd
scrapyd_python: python2.7
scrapyd_version: 1.1.0
scrapyd_extensions: []
scrapyd_port: 6800
scrapyd_host: scrapyd.example.com
scrapyd_logfile_dir:
```


Example Playbook
----------------

```
- hosts: servers

  roles:
  - Stouts.supervisor
  - Stouts.nginx
  - lepture.scrapyd

  vars:
    scrapyd_port: 6800
    scrapyd_host: scrapyd.example.com
    scrapyd_extensions:
      - scrapy-sentry
```

License
-------

BSD. Created by Hsiaoming Yang <http://lepture.com/>.
