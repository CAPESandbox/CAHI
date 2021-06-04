# Introduction

CAHI (CAPE Auto-Hardened Installer) is a companion set of dedicated Ansible roles and tasks to build as secured and production-ready CAPE Sandbox local instance as possible. Majority of roles and tasks are ported from [cape2.sh](https://github.com/doomedraven/Tools/blob/master/Sandbox/cape2.sh) and [kvm-qemu.sh](https://github.com/doomedraven/Tools/blob/master/Virtualization/kvm-qemu.sh). In addition, many of the anti-vm baked into the hypervisor is being randomized at run time as opposed to hardcoding values.

**NOTE:** The project is currently in a pre-alpha state and is aimed towards developers at this stage until it is more complete. Content and functionality may be added or removed with no prior notification. DO NOT RUN this against any production systems.

### What is CAPE?

CAPE (Configuration and Payload Extraction) provides a dynamic and automated environment for analyzing (and debugging) malware behavior, extracting payloads (such as raw malware and N-stage binaries), as well as malware configurations (such as CnC IP addresses / domains, mutexes, bot IDs, etc.). All of this is accompanied by a myriad of built-in detection (behavior, host, network, Yara, MITRE, etc.) to depict a holistic view of the analyzed sample. Ultimately, CAPE allows reducing the time and efforts of threat hunting, threat intelligence collection, incident response, and developing proactive detection / prevention strategies. For more information about CAPE, visit the official [CAPE repository](https://github.com/kevoreilly/CAPEv2), or use this project to setup a testing environment and explore hands-on.

### Why use Ansible to deploy CAPE?

The ultimate goal to make CAPE a Configuration-As-Code (or Infrastructure-As-Code) ready. Ansible and associated tooling facilitate this by allowing rapid development, testing and deployment with as minimal efforts as possible while allowing new scenarios and possibilities.

### What does the 'Auto-Hardened' part of the name mean?

It means that the Ansible roles and tasks are built with security in mind. For example, best practices and hardening of the operating system, web server, database, etc. are implemented in an automated fashion to ensure a secured and functional CAPE instance is being deployed. Implementing security and hardening from the get go while ensuring functionality is a considerable challenge, and automating these is a continuous effort.

What 'Auto-Hardened' does NOT mean is that the resulting host will not be unbreakable or unhackable. Risk cannot be eliminated, but we can reduce the attack surface as much as possible, resulting in a better and sustainable security posture (we are infosec folks after all) and in some cases, compliance. Designing a secure architecture that meets your standards is your responsibility and not the roles and tasks within this project.

The project tracks security and hardening configurations that are automated, which will be made available in [Security Automation Tracker](https://github.com/CAPESandbox/CAHI/blob/master/docs/Security_Automation_Tracker.md).

# Deployment for Production

Coming soon.

# Development and Testing Scenarios

The most complete scenarios at this time are ```default```, ```cape-vm``` and to an extent ```cape-cr```, which still requires additional configuration and testing. For additional details on setting up the development environment and the status of each scenario, review the [Development](https://github.com/CAPESandbox/CAHI/blob/master/docs/Development.md) documentation. Make sure to also check the [Known Issues](https://github.com/CAPESandbox/CAHI/blob/master/docs/Known_Issues.md) document under the ```docs``` directory.

| Scenario  | Description                                                         | Status      |
|-----------|---------------------------------------------------------------------|-------------|
| default   | Single custom container to provision CAPE and associated services.  | Ready       |
| cape-vm   | Single VM provisioned with CAPE and services including hypervisor.  | Ready       |
| cape-cr   | Two containers, one for CAPE (and services) and one for hypervisor. | In-Progress |
| cape-ship | Container per service.                                              | One Day     |
| cape-pod  | Same as 'default' but ONLY RHEL8 / CentoOS Stream and Podman.       | Ready       |

A GitHub, Molecule and Ansible CI pipeline will be introduced later as the project stabilizes. For developing on RHEL 8 / CentOS Stream with Podman, see [Podman](https://github.com/CAPESandbox/CAHI/blob/master/docs/Podman.md) documentation.

# Acknowledgements

- [CAPE Sandbox: Malware Configuration And Payload Extraction](https://github.com/kevoreilly/CAPEv2)
