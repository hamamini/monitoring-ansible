# Install Monitoring via Ansible

### Prometheus, Grafana, and Node-exporter

put your host in inventory file and run the following command:

~~~~
ansible-playbook -i inventory.ini monitoring/monitoring.yml
~~~~

This script available for both Debian-based and RedHat-based distros.

#### Python issues

Note: In case of failure check the destination for `/usr/lib/python` if there is NOT install `python2` or `python-minimal`.

#### Handlers issue

Note: The handlers only applied when the `notify` task has been changed, or else if you want to run them on each try put them in `tasks`.