# Jenkins Build Server

* Dependencies
  * Ansible 2.4.3

# VM provision

* Dependencies
  * Vagrant 2.0.4
  * VirtualBox 5.2.10

```sh
vagrant up
```

> Append this `192.168.50.4  build.server.com` in `/etc/hosts`
> and put `http://build.server.com` in browser
> or
> simply use ip address `192.168.50.4`

After that copy `Jenkins Initial Admin Password` from terminal and paste it in Jenkins first form for unlocking Jenkins.

# Running provision on aws

* Dependencies

  * AWS account

  * Running `Ubuntu Trusty 64bit` instance 

    ​

* Ping

```sh
ansible aws -i hosts/all -m ping
```

* Run provisioning

```sh
ansible-playbook provision/install.yml -i hosts/all
```
