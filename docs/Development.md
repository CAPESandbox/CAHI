## Configuring Development Environment

A development environment can be setup using one of the methods below, depending on development needs and resources available.

1. Docker as Development Platform

   Advantages:
     - Simple and rapid.
     - Ideal for web / UI prototyping.
  
   Disadvantages:
     - No virtualization support (for example, KVM).
     - Does not provide a fully funcational CAPE Sandbox deployment.

2. Vagrant as Development Platform (not implemented yet)

   Advantages:
     - More production-like deployment, though nested.
  
   Disadvantages:
     - May take time to fully setup a development platform.
     - Potentially slower performance due to nested virtualization.

**NOTE:** Do not use the development platform as your production deployment.

## Automating the Development Environment Build

Coming soon! Follow the per-platform manual steps below to setup the development environment.

## Docker as Development Platform

The following dependencies are required
  - Ansible 2.9.X
  - Molecule
  - Docker (podman should work but not tested yet)

 ```bash
 $ pip3 install ansible==2.9.20 molecule[docker] ansible-lint --user
 ```

Afterwards, clone CAHI repoistory and enter the newly created directory

```bash
 $ git clone https://github.com/kevoreilly/CAHI.git
 $ cd CAHI
```

Finally, fire up a development instance

```bash
 $ molecule converge
```

Once all roles and tasks finished, you can login to the container instance

```bash
$ molecule login
```

Issuing the above command, molecule will automatically build the docker image based of the existing Dockerfile (which implements systemd), then run ansible roles and tasks against the created docker image.

## Vagrant as Development Platform

**NOTE:** The vagrant molecule scenario is not implemented at this point.

The following dependencies are required
  - Ansible 2.9.X
  - Molecule
  - Vagrant
  - VirtualBox
  - python-vagrant
  - molecule-vagrant

VirtualBox is used by Vagrant to setup a development host and not as CAPE's virtualization backend. VirtualBox can be installed as follows.

```bash
wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add -
wget -q https://www.virtualbox.org/download/oracle_vbox.asc -O- | sudo apt-key add -
echo "deb [arch=amd64] http://download.virtualbox.org/virtualbox/debian $(lsb_release -cs) contrib" | sudo tee -a /etc/apt/sources.list.d/virtualbox.list
sudo apt update
sudo apt install virtualbox
```

Installing Vagrant

```bash
$ curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -
$ sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"
$ sudo apt-get update && sudo apt-get install vagrant
```

Installing remaining requirements

```bash
$ wget 
$ pip3 install ansible==2.9.20 molecule python-vagrant molecule-vagrant ansible-lint --user
```

Afterwards, clone CAHI repoistory and enter the newly created directory

```bash
 $ git clone https://github.com/kevoreilly/CAHI.git
 $ cd CAHI
```

Finally, fire up a development VM by explicitly specifiying the vagrant scenario

```bash
$ molecule converge --scenario-name vagrant
```

Once all roles and tasks finished, you can login to the container instance

```bash
$ molecule login -s vagrant
```

## Development Cheatsheets

1. To login to the created docker image for testing and debugging

    ```bash
    $ molecule login
    ```

2. For continuous development, the following scenario can be followed:

    ```bash
    $ molecule converge
    ```

    implement roles / tasks changes, then run

    ```bash
    $ molecule converge
    ```

    implement roles / tasks changes again, then run

    ```bash
    $ molecule converge
    ```

    and so on.

3. To destroy the development instance

    ```bash
    $ molecule destroy
    ```
