# Development and Production using Podman

## Why Podman?

Before continuing any further, read the below documentation.

1. [Running containers with Podman and shareable systemd services](https://www.redhat.com/sysadmin/podman-shareable-systemd-services)
2. [Improved systemd integration with Podman 2.0](https://www.redhat.com/sysadmin/improved-systemd-podman)
3. [Podman: A more secure way to run containers](https://opensource.com/article/18/10/podman-more-secure-way-run-containers)

Also, see this [bug report](https://bugzilla.redhat.com/show_bug.cgi?id=1946982#c2) and [Known Issues](https://github.com/CAPESandbox/CAHI/blob/master/docs/Known_Issues.md) document under the ```docs``` directory.

**NOTE:** Docker on RHEL 8 / CentOS Stream is not supported by this project.

## Configuring Development Environment

Install dependencies.

```bash
$ sudo dnf install -y python3 python3-pip python3-setuptools-wheel python3-wheel
$ sudo dnf install -y @container-tools
$ pip3 install pip --upgrade --user
$ pip3 install ansible==2.9.22 molecule molecule[podman] podman python-vagrant molecule-vagrant ansible-lint --upgrade --user
```

Start developing!

```bash
$ git clone https://github.com/CAPESandbox/CAHI.git
$ cd CAHI
$ molecule converge --scenario-name cape-pod
```
