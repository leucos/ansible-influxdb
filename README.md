ansible-influxdb role
===============

Installs [influxdb](https://github.com/influxdata/influxdb) on ubuntu
14.04 and up.

See `defaults/main.yml` for variables.

Run `vagrant up && vagrant ssh -c specs` tu run specs (and play with influxdb).

Port 3000 is forwarded so you can install grafana too (see [ansible-grafana](https://github.com/leucos/ansible-grafana))

Michel Blanc <mb@mbnet.fr>
