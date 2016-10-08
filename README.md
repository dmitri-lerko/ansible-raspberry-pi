# ansible-raspberry-pi
Repository with ansible playbook for the initial configuration of your Raspberry Pi

You'll need to update IP of your raspberry in hosts.ini.
You also will need to supply values for your WiFi network and password in
group_vars/raspberry.yml

You can than run this playbook by executing the following command:
ansible-playbook main.yml -i hosts.initial

Note: as we perform apt-get update this playbook may take considerable amount
of time. It is recommended to install latest version of raspbarrian before
anything else. Version that comes with NOOBS SD card is usually some-what out
of date.

Alternatively, you can pass SSID and password as extra-vars parameters to Ansible.
ansible-playbook main.yml -i hosts.ini --extra-vars "home_ssid=mega_fiber
home_psk=topsecret"
