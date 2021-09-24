## Security Hardening and Best Practices Automation

Currently, the following secure configurations are either under active automation development or being considered for the future iterations.

| Security Feature Automation                                    | Status                       |
|----------------------------------------------------------------|------------------------------|
| Multi-Facotr Authentication (google-authenticator) for SSH     | Completed, Test/Rev Required |
| Multi-Facotr Authentication (google-authenticator) for Cockpit | Brainstorming, Under Review  |
| ModSecurity WAF for NGINX                                      | Completed                    |
| Fail2ban                                                       | Completed, Under Review      |
| CIS (Center of Information Security) Benchmarks for NGINX      | Completed, Under Review      |
| CIS (Center of Information Security) Benchmarks for Ubuntu     | In Progress                  |

## CIS (Center of Information Security) Benchmarks Automation Tracker

### Ubuntu

| Item    | Control                                                                          | Scored     | Automated          |
|---------|----------------------------------------------------------------------------------|------------|--------------------|
| 1.1.1.1 | Ensure mounting of cramfs filesystem is disabled                                 | Scored     | :heavy_check_mark: |
| 1.1.1.2 | Ensure mounting of freevxfs filesystem is disabled                               | Scored     | :heavy_check_mark: |
| 1.1.1.3 | Ensure mounting of jffs2 filesystem is disabled                                  | Scored     | :heavy_check_mark: |
| 1.1.1.4 | Ensure mounting of hfs filesystem is disabled                                    | Scored     | :heavy_check_mark: |
| 1.1.1.5 | Ensure mounting of hfsplus filesystem is disabled                                | Scored     | :heavy_check_mark: |
| 1.1.1.6 | Ensure mounting of udf filesystem is disabled                                    | Scored     | :heavy_check_mark: |
| 1.1.1.7 | Ensure mounting of vfat filesystem is disabled                                   | Scored     | :heavy_check_mark: |
| 1.1.23  | Disable Automounting                                                             | Scored     | :heavy_check_mark: |
| 1.1.24  | Disable USB Storage                                                              | Scored     | :heavy_check_mark: |
| 1.3.1   | Ensure sudo is installed                                                         | Scored     | :heavy_check_mark: |
| 1.3.2   | Ensure sudo commands use pty                                                     | Scored     | :heavy_check_mark: |
| 1.3.3   | Ensure sudo log file exists                                                      | Scored     | :heavy_check_mark: |
| 1.6.2   | Ensure address space layout randomization (ASLR) is enabled                      | Scored     | :heavy_check_mark: |
| 1.6.4   | Ensure core dumps are restricted                                                 | Scored     | :heavy_check_mark: |
| 1.8.1.1 | Ensure message of the day is configured properly                                 | Scored     | :heavy_check_mark: |
| 1.8.1.2 | Ensure local login warning banner is configured properly                         | Scored     | :heavy_check_mark: |
| 1.8.1.3 | Ensure remote login warning banner is configured properly                        | Scored     | :heavy_check_mark: |
| 1.8.1.4 | Ensure permissions on /etc/motd are configured                                   | Scored     | :heavy_check_mark: |
| 1.8.1.5 | Ensure permissions on /etc/issue are configured                                  | Scored     | :heavy_check_mark: |
| 1.8.1.6 | Ensure permissions on /etc/issue.net are configured                              | Scored     | :heavy_check_mark: |
| 1.9     | Ensure updates, patches, and additional security software are installed          | Scored     | :heavy_check_mark: |
| 2.1.1   | Ensure xinetd is not installed                                                   | Scored     | :heavy_check_mark: |
| 2.1.2   | Ensure openbsd-inetd is not installed                                            | Scored     | :heavy_check_mark: |
| 2.2.1.1 | Ensure time synchronization is in use                                            | Scored     | :heavy_check_mark: |
| 2.2.1.2 | Ensure systemd-timesyncd is configured                                           | Scored     | :heavy_check_mark: |
| 2.2.1.4 | Ensure ntp is configured                                                         | Scored     | :heavy_check_mark: |
| 2.2.2   | Ensure X Window System is not installed                                          | Scored     | :heavy_check_mark: |
| 2.2.3   | Ensure Avahi Server is not installed                                             | Scored     | :heavy_check_mark: |
| 2.2.4   | Ensure CUPS is not installed                                                     | Scored     | :heavy_check_mark: |
| 2.2.5   | Ensure DHCP Server is not installed                                              | Scored     | :heavy_check_mark: |
| 2.2.6   | Ensure LDAP server is not installed                                              | Scored     | :heavy_check_mark: |
| 2.2.7   | Ensure NFS is not installed                                                      | Scored     | :heavy_check_mark: |
| 2.2.8   | Ensure DNS Server is not installed                                               | Scored     | :heavy_check_mark: |
| 2.2.9   | Ensure FTP Server is not installed                                               | Scored     | :heavy_check_mark: |
| 2.2.10  | Ensure HTTP server is not installed                                              | Scored     | :heavy_check_mark: |
| 2.2.11  | Ensure IMAP and POP3 server are not installed                                    | Scored     | :heavy_check_mark: |
| 2.2.12  | Ensure Samba is not installed                                                    | Scored     | :heavy_check_mark: |
| 2.2.13  | Ensure HTTP Proxy Server is not installed                                        | Scored     | :heavy_check_mark: |
| 2.2.14  | Ensure SNMP Server is not installed                                              | Scored     | :heavy_check_mark: |
| 2.2.16  | Ensure rsync service is not installed                                            | Scored     | :heavy_check_mark: |
| 2.2.17  | Ensure NIS Server is not installed                                               | Scored     | :heavy_check_mark: |
| 2.3.1   | Ensure NIS Client is not installed                                               | Scored     | :heavy_check_mark: |
| 2.3.2   | Ensure rsh client is not installed                                               | Scored     | :heavy_check_mark: |
| 2.3.3   | Ensure talk client is not installed                                              | Scored     | :heavy_check_mark: |
| 2.3.4   | Ensure telnet client is not installed                                            | Scored     | :heavy_check_mark: |
| 2.3.5   | Ensure LDAP client is not installed                                              | Scored     | :heavy_check_mark: |
| 2.3.6   | Ensure RPC is not installed                                                      | Scored     | :heavy_check_mark: |
| 3.3.1   | Ensure source routed packets are not accepted                                    | Scored     | :heavy_check_mark: |
| 3.3.2   | Ensure ICMP redirects are not accepted                                           | Scored     | :heavy_check_mark: |
| 3.3.3   | Ensure secure ICMP redirects are not accepted                                    | Scored     | :heavy_check_mark: |
| 3.3.4   | Ensure suspicious packets are logged                                             | Scored     | :heavy_check_mark: |
| 3.3.5   | Ensure broadcast ICMP requests are ignored                                       | Scored     | :heavy_check_mark: |
| 3.3.6   | Ensure bogus ICMP responses are ignored                                          | Scored     | :heavy_check_mark: |
| 3.3.7   | Ensure Reverse Path Filtering is enabled                                         | Scored     | :heavy_check_mark: |
| 3.3.8   | Ensure TCP SYN Cookies is enabled                                                | Scored     | :heavy_check_mark: |
| 3.3.9   | Ensure IPv6 router advertisements are not accepted                               | Scored     | :heavy_check_mark: |
| 3.4.1   | Ensure DCCP is disabled                                                          | Scored     | :heavy_check_mark: |
| 3.4.2   | Ensure SCTP is disabled                                                          | Scored     | :heavy_check_mark: |
| 3.4.3   | Ensure RDS is disabled                                                           | Scored     | :heavy_check_mark: |
| 3.4.4   | Ensure TIPC is disabled                                                          | Scored     | :heavy_check_mark: |
| 4.3     | Ensure logrotate is configured                                                   | Scored     | :heavy_check_mark: |
| 4.3     | Ensure logrotate is configured                                                   | Scored     | :heavy_check_mark: |
| 4.3     | Ensure logrotate is configured                                                   | Scored     | :heavy_check_mark: |
| 4.4     | Ensure logrotate assigns appropriate permissions                                 | Scored     | :heavy_check_mark: |
| 4.1.1.1 | Ensure auditd is installed                                                       | Scored     | :heavy_check_mark: |
| 4.1.1.2 | Ensure auditd service is enabled                                                 | Scored     | :heavy_check_mark: |
| 4.1.1.3 | Ensure auditing for processes that start prior to auditd is enabled              | Scored     | :heavy_check_mark: |
| 4.1.1.4 | Ensure audit_backlog_limit is sufficient                                         | Scored     | :heavy_check_mark: |
| 4.1.2.1 | Ensure audit log storage size is configured                                      | Scored     | :heavy_check_mark: |
| 4.1.2.2 | Ensure audit logs are not automatically deleted                                  | Scored     | :heavy_check_mark: |
| 4.1.2.3 | Ensure system is disabled when audit logs are full                               | Scored     | :heavy_check_mark: |
| 4.1.3   | Ensure events that modify date and time information are collected                | Scored     | :heavy_check_mark: |
| 4.1.4   | Ensure events that modify user/group information are collected                   | Scored     | :heavy_check_mark: |
| 4.1.5   | Ensure events that modify the system's network environment are collected         | Scored     | :heavy_check_mark: |
| 4.1.6   | Ensure events that modify the system's Mandatory Access Controls are collected   | Scored     | :heavy_check_mark: |
| 4.1.7   | Ensure login and logout events are collected                                     | Scored     | :heavy_check_mark: |
| 4.1.8   | Ensure session initiation information is collected                               | Scored     | :heavy_check_mark: |
| 4.1.9   | Ensure discretionary access control permission modification events are collected | Scored     | :heavy_check_mark: |
| 4.1.10  | Ensure unsuccessful unauthorized file access attempts are collected              | Scored     | :heavy_check_mark: |
| 4.1.12  | Ensure successful file system mounts are collected                               | Scored     | :heavy_check_mark: |
| 4.1.13  | Ensure file deletion events by users are collected                               | Scored     | :heavy_check_mark: |
| 4.1.14  | Ensure changes to system administration scope (sudoers) is collected             | Scored     | :heavy_check_mark: |
| 4.1.15  | Ensure system administrator command executions (sudo) are collected              | Scored     | :heavy_check_mark: |
| 4.1.16  | Ensure kernel module loading and unloading is collected                          | Scored     | :heavy_check_mark: |
| 4.1.17  | Ensure the audit configuration is immutable                                      | Scored     | :heavy_check_mark: |
| 4.2.1.1 | Ensure rsyslog is installed                                                      | Scored     | :heavy_check_mark: |
| 4.2.1.2 | Ensure rsyslog Service is enabled                                                | Scored     | :heavy_check_mark: |
| 5.1.1   | Ensure cron daemon is enabled and running                                        | Scored     | :heavy_check_mark: |
| 5.1.2   | Ensure permissions on /etc/crontab are configured                                | Scored     | :heavy_check_mark: |
| 5.1.3   | Ensure permissions on /etc/cron.hourly are configured                            | Scored     | :heavy_check_mark: |
| 5.1.4   | Ensure permissions on /etc/cron.daily are configured                             | Scored     | :heavy_check_mark: |
| 5.1.5   | Ensure permissions on /etc/cron.weekly are configured                            | Scored     | :heavy_check_mark: |
| 5.1.6   | Ensure permissions on /etc/cron.monthly are configured                           | Scored     | :heavy_check_mark: |
| 5.1.7   | Ensure permissions on /etc/cron.d are configured                                 | Scored     | :heavy_check_mark: |
| 5.1.8   | Ensure cron is restricted to authorized users                                    | Scored     | :heavy_check_mark: |
| 5.1.9   | Ensure at is restricted to authorized users                                      | Scored     | :heavy_check_mark: |
| 5.2.1   | Ensure permissions on /etc/ssh/sshd_config are configured                        | Scored     | :heavy_check_mark: |
| 5.2.2   | Ensure permissions on SSH private host key files are configured                  | Scored     | :heavy_check_mark: |
| 5.2.3   | Ensure permissions on SSH public host key files are configured                   | Scored     | :heavy_check_mark: |
| 5.2.4   | Ensure SSH LogLevel is appropriate                                               | Scored     | :heavy_check_mark: |
| 5.2.5   | Ensure SSH X11 forwarding is disabled                                            | Scored     | :heavy_check_mark: |
| 5.2.6   | Ensure SSH MaxAuthTries is set to 4 or less                                      | Scored     | :heavy_check_mark: |
| 5.2.7   | Ensure SSH IgnoreRhosts is enabled                                               | Scored     | :heavy_check_mark: |
| 5.2.8   | Ensure SSH HostbasedAuthentication is disabled                                   | Scored     | :heavy_check_mark: |
| 5.2.9   | Ensure SSH root login is disabled                                                | Scored     | :heavy_check_mark: |
| 5.2.10  | Ensure SSH PermitEmptyPasswords is disabled                                      | Scored     | :heavy_check_mark: |
| 5.2.11  | Ensure SSH PermitUserEnvironment is disabled                                     | Scored     | :heavy_check_mark: |
| 5.2.12  | Ensure only strong Ciphers are used                                              | Scored     | :heavy_check_mark: |
| 5.2.13  | Ensure only strong MAC algorithms are used                                       | Scored     | :heavy_check_mark: |
| 5.2.14  | Ensure only strong Key Exchange algorithms are used                              | Scored     | :heavy_check_mark: |
| 5.2.15  | Ensure SSH Idle Timeout Interval is configured                                   | Scored     | :heavy_check_mark: |
| 5.2.16  | Ensure SSH LoginGraceTime is set to one minute or less                           | Scored     | :heavy_check_mark: |
| 5.2.17  | Ensure SSH access is limited                                                     | Scored     | :heavy_check_mark: |
| 5.2.18  | Ensure SSH warning banner is configured                                          | Scored     | :heavy_check_mark: |
| 5.2.19  | Ensure SSH PAM is enabled                                                        | Scored     | :heavy_check_mark: |
| 5.2.20  | Ensure SSH AllowTcpForwarding is disabled                                        | Scored     | :heavy_check_mark: |
| 5.2.21  | Ensure SSH MaxStartups is configured                                             | Scored     | :heavy_check_mark: |
| 5.2.22  | Ensure SSH MaxSessions is limited                                                | Scored     | :heavy_check_mark: |
| 5.4.1.1 | Ensure password expiration is 365 days or less                                   | Scored     | :heavy_check_mark: |
| 5.4.1.2 | Ensure minimum days between password changes is configured                       | Scored     | :heavy_check_mark: |
| 5.4.1.3 | Ensure password expiration warning days is 7 or more                             | Scored     | :heavy_check_mark: |
| 5.4.3   | Ensure default group for the root account is GID 0                               | Scored     | :heavy_check_mark: |
| 5.4.4   | Ensure default user umask is 027 or more restrictive                             | Scored     | :heavy_check_mark: |
| 5.4.5   | Ensure default user shell timeout is 900 seconds or less                         | Scored     | :heavy_check_mark: |
| 6.1.2   | Ensure permissions on /etc/passwd are configured                                 | Scored     | :heavy_check_mark: |
| 6.1.3   | Ensure permissions on /etc/gshadow- are configured                               | Scored     | :heavy_check_mark: |
| 6.1.4   | Ensure permissions on /etc/shadow are configured                                 | Scored     | :heavy_check_mark: |
| 6.1.5   | Ensure permissions on /etc/group are configured                                  | Scored     | :heavy_check_mark: |
| 6.1.6   | Ensure permissions on /etc/passwd- are configured                                | Scored     | :heavy_check_mark: |
| 6.1.7   | Ensure permissions on /etc/shadow- are configured                                | Scored     | :heavy_check_mark: |
| 6.1.8   | Ensure permissions on /etc/group- are configured                                 | Scored     | :heavy_check_mark: |
| 6.1.9   | Ensure permissions on /etc/gshadow are configured                                | Scored     | :heavy_check_mark: |

### NGINX

| Item    | Control                                                                       | Scored     | Automated          |
|---------|-------------------------------------------------------------------------------|------------|--------------------|
| 2.1.2   | Ensure HTTP WebDAV module is not installed                                    | Scored     | :heavy_check_mark: |
| 2.1.2   | Ensure modules with gzip functionality are disabled                           | Scored     | :heavy_check_mark: |
| 2.3.1   | Ensure NGINX directories and files are owned by root                          | Scored     | :heavy_check_mark: |
| 2.3.2   | Ensure access to NGINX directories and files is restricted                    | Scored     | :heavy_check_mark: |
| 2.4.3   | Ensure keepalive_timeout is 10 seconds or less, but not 0                     | Scored     | :heavy_check_mark: |
| 2.4.4   | Ensure send_timeout is set to 10 seconds or less, but not 0                   | Scored     | :heavy_check_mark: |
| 2.5.1   | Ensure server_tokens directive is set to 'off'                                | Scored     | :heavy_check_mark: |
| 2.5.2   | Ensure default error and index.html pages do not reference NGINX              | Scored     | :heavy_check_mark: |
| 2.5.3   | Ensure hidden file serving is disabled                                        | Not Scored | :heavy_check_mark: |
| 2.5.4   | Ensure the NGINX reverse proxy does not enable information disclosure         | Scored     | :heavy_check_mark: |
| 4.1.1   | Ensure HTTP is redirected to HTTPS                                            | Scored     | :heavy_check_mark: |
| 4.1.4   | Ensure only modern TLS protocols are used                                     | Scored     | :heavy_check_mark: |
| 4.1.5   | Disable weak ciphers                                                          | Scored     | :heavy_check_mark: |
| 4.1.6   | Ensure custom Diffie-Hellman parameters are used                              | Scored     | :heavy_check_mark: |
| 4.1.7   | Ensure Online Certificate Status Protocol (OCSP) stapling is enabled          | Scored     | :heavy_check_mark: |
| 4.1.8   | Ensure HTTP Strict Transport Security (HSTS) is enabled                       | Scored     | :heavy_check_mark: |
| 4.1.13  | Ensure session resumption is disabled to enable perfect forward security      | Scored     | :heavy_check_mark: |
| 4.1.14  | Ensure HTTP/2.0 is used                                                       | Not Scored | :heavy_check_mark: |
| 5.1.2   | Ensure only whitelisted HTTP methods are allowed                              | Not Scored | :heavy_check_mark: |
| 5.2.2   | Ensure the maximum request body size is set correctly                         | Scored     | :heavy_check_mark: |
| 5.2.3   | Ensure the maximum buffer size for URIs is defined                            | Scored     | :heavy_check_mark: |
| 5.3.1   | Ensure X-Frame-Options header is configured and enabled                       | Scored     | :heavy_check_mark: |
| 5.3.2   | Ensure X-Content-Type-Options header is configured and enabled                | Scored     | :heavy_check_mark: |
| 5.3.3   | Ensure the X-XSS-Protection Header is enabled and configured properly         | Scored     | :heavy_check_mark: |
| 5.3.4   | Ensure that Content Security Policy (CSP) is enabled and configured properly  | Not Scored | :heavy_check_mark: |
