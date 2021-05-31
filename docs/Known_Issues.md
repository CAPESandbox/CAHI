### Pip Dependencies

## Error 1:

On a prestine Ubuntu Focal Vagrant image, the below error may be generated during pip packages installation

```bash
ERROR: Cannot uninstall '<PACKAGE NAME>'. It is a distutils installed project and thus we cannot accurately determine which files belong to it which would lead to only a partial uninstall.
```

The one identified thus far are

```bash
/usr/lib/python3/dist-packages/PyYAML-5.3.1.egg-info
/usr/lib/python3/dist-packages/pyasn1_modules
/usr/lib/python3/dist-packages/pyasn1_modules-0.2.1.egg-info
```

## Solution:

Manually ```rm -rf``` these files should no longer cause Ansible to error out. Handling this automaticaly by Ansible upon converge may be added later.

## Error 2:

When installing ```git+https://github.com/CAPESandbox/peepdf.git```, the below error may be encountered. 

```bash
ERROR: pip's dependency resolver does not currently take into account all the packages that are installed. This behaviour is the source of the following dependency conflicts.
log-symbols 0.0.14 requires colorama>=0.3.9, but you have colorama 0.3.7 which is incompatible.
halo 0.0.31 requires colorama>=0.3.9, but you have colorama 0.3.7 which is incompatible.
```

## Solution:

Currently ```git+https://github.com/CAPESandbox/peepdf.git``` is temporarly not installed by Ansible and should be installed manually.

Error 3:

When installing ```git+https://github.com/andreasvc/pyre2.git```, another dependency conflict occurs

## Solution:

install pyre2 directly via pip. This is currently implemented and installed by Ansible.

## Error 4:

While testing / developing CAHI on CentOS Stream (latest) using the ```cape-pod``` scenario, the below error pops up.

```bash
Error: OCI runtime error: unknown cap: `CAP_PERFMON`
```

## Solution:

This appears to be a known bug on CentOS. The same test runs successfully over RHEL 8.4 (latest). Review the bug report and potential workarounds.

https://bugzilla.redhat.com/show_bug.cgi?id=1946982#c2

## Error 5:

On RHEL 8 / CentOS Stream with Podman, the resulting (rootless) container have wrong permissions on the ```/tmp``` directory.

## Solution:

This is taken care of using Ansible to set the correct permissions on the ```/tmp``` directory upon ```molcule converge```.

https://github.com/containers/buildah/issues/1240
