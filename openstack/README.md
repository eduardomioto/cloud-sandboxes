README.md
### OpenStack

### Modules Involved

* Keystone	- Identity Service
* Glance	- Image Service
* Neutron	- Networking
* Nova		- Compute
* Cinder	- Block Storage 
* Swift		- Object Storage
* Horizon

#### Installing - Local Machine [by Git]

* Create a virtual machine
* Run: 

```
sudo useradd -s /bin/bash -d /opt/stack -m stack
echo "stack ALL=(ALL) NOPASSWD: ALL" | sudo tee /etc/sudoers.d/stack
sudo su - stack
git clone https://git.openstack.org/openstack-dev/devstack
cd devstack
```

* Create a local.conf file with 4 passwords preset at the root of the devstack git repo.
```
[[local|localrc]]
ADMIN_PASSWORD=secret
DATABASE_PASSWORD=dbsecret
RABBIT_PASSWORD=rabbitsecret
SERVICE_PASSWORD=servicesecret
```

Run: 
```
FORCE=yes ./stack.sh
```

#### Installing - Local Machine [by Conjure-UP]

conjure-up openstack

#### Reference
- [1] (Installing)[https://docs.openstack.org/developer/devstack/]
- [2] (Udemy OpenStack Course)[https://www.udemy.com/introduction-to-openstack]
- (3) (Conjure Up Openstack)[https://www.ubuntu.com/download/cloud/conjure-up?_ga=1.147230065.750893748.1493665442]