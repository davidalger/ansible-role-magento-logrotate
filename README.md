# Ansible Role: Magento Logrotate

[![Build Status](https://travis-ci.org/davidalger/ansible-role-magento-logrotate.svg?branch=master)](https://travis-ci.org/davidalger/ansible-role-magento-logrotate)

Installs a logrotate script for Magento in /etc/logrotate.d

## Requirements

None.

## Role Variables

See `defaults/main.yml` for details.

## Dependencies

None.

## Example Playbook

    - hosts: web-servers
      magento_logrotate_sets:
        - path: /var/www/html/current/var/log/*.log
          owner: www-data
          group: www-data
    
      roles:
        - { role: davidalger.magento_logrotate, tags: magento }

## License

This work is licensed under the MIT license. See LICENSE file for details.

## Author Information

This role was created in 2017 by [David Alger](http://davidalger.com/).
