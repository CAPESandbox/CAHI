***********************
CAPE-SHIP Scenario
***********************

This scenario implements a multi-container deployment (Microservices architecture) for CAPE Sandbox using official Docker images where possible to minimize footprint.

* **cape-postgres**: Official `postgres:17-alpine`.
* **cape-mongo**: Official `mongo:7.0`.
* **cape-nginx**: Official `nginx:alpine`.
* **cape-core-server**: Custom Ubuntu 24.04 container running the CAPE engine.

Requirements
============

* Docker Engine
* Ansible
* Molecule
