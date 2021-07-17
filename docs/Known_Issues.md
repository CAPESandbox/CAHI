
# Known Issues

Issues identified across various stages.

### Table of Contents

- [Python and Pip Issues](#python-and-pip-issues)
- [RHEL 8 or CentOS Stream Development Issues](#rhel-8-or-centos-stream-development-issues)
- [Libvirt Issues](#libvirt-issues)

## Python and pip Issues

### Error 1: ```distutils```

While running the ```cape-vm``` scenario with a prestine Ubuntu Focal Vagrant image, Ansible may error and exit during pip packages installation.

```bash
ERROR: Cannot uninstall '<PACKAGE NAME>'. It is a distutils installed project and thus we cannot accurately 
determine which files belong to it which would lead to only a partial uninstall.
```

The files causing the issue that were identified thus far (but may include others) are the following.

```bash
/usr/lib/python3/dist-packages/PyYAML-5.3.1.egg-info
/usr/lib/python3/dist-packages/pyasn1_modules
/usr/lib/python3/dist-packages/pyasn1_modules-0.2.1.egg-info
```

### Solution:

**NOTE:** This is now automated via ansible in the ```dependencies``` role.

Manually ```rm -rf``` these files should no longer cause Ansible to error out. Handling this automaticaly by Ansible upon converge may be added later.

### Error 2: ```pip dependencies```

Regardless of scenario, when Ansible attempts to install ```git+https://github.com/CAPESandbox/peepdf.git```, the below error may be encountered.

```bash
ERROR: pip's dependency resolver does not currently take into account all the packages that are installed. 
This behaviour is the source of the following dependency conflicts.

log-symbols 0.0.14 requires colorama>=0.3.9, but you have colorama 0.3.7 which is incompatible.
halo 0.0.31 requires colorama>=0.3.9, but you have colorama 0.3.7 which is incompatible.
```

Another dependency error encountered was during the installation of ```git+https://github.com/andreasvc/pyre2.git```.

### Solution:

- For ```peepdf```, it is temporarly not installed by Ansible and should be installed manually later until it can be handled automatically.
- For ```pyre```, it is installed via pip directoy and not from the GitHub repo, which is already handles by CAHI.

[Top](#known-issues)

## RHEL 8 or CentOS Stream Development Issues

### Error 1: ```unknown cap: CAP_PERFMON```

While testing / developing CAHI on CentOS Stream (latest) using the ```cape-pod``` scenario, the below error pops up.

```bash
Error: OCI runtime error: unknown cap: `CAP_PERFMON`
```

### Solution:

This appears to be a known bug on CentOS. The same test runs successfully over RHEL 8.4 (latest). Review the bug report and potential workarounds.

https://bugzilla.redhat.com/show_bug.cgi?id=1946982#c2

### Error 2: ```/tmp wrong permissions```

On RHEL 8 / CentOS Stream with Podman, the resulting (rootless) container have wrong permissions on the ```/tmp``` directory, causing Ansible to fail execution.

### Solution:

This is taken care of using Ansible to set the correct permissions on the ```/tmp``` directory upon ```molcule converge```. Review the bug report.

https://github.com/containers/buildah/issues/1240

[Top](#known-issues)

## Libvirt Issues

### Error 1: ```cannot load AppArmor profile```

Libvirt and apparmor may not run smoothly together with the following error message.

```bash
error: internal error: cannot load AppArmor profile
```

### Solution:

Debugging the issue is best course of action, such as follows.

```bash
$ /usr/libexec/virt-aa-helper

# AND / OR

$ journalctl -u libvirtd | cat
```

### Error 2: ```libvirt.so.0: cannot open shared object file```

Another error that might occur is the one below.

```bash
error while loading shared libraries: libvirt.so.0: cannot open shared object file: No such file or directory
```

### Solution

Solution is another debugging attempt as follows.

```bash
$ strace -Tfe trace=openat /usr/libexec/virt-aa-helper

# AND / OR

$ aa-complain /usr/libexec/virt-aa-helper
```

[Top](#known-issues)
