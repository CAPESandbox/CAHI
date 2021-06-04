## Security Hardening and Best Practices Automation

Currently, the following secure configurations are either under active automation development or being considered for the future iterations.

| Security Feature Automation                                | Status                       |
|------------------------------------------------------------|------------------------------|
| Multi-Facotr Authentication (google-authenticator) for SSH | Completed, Test/Rev Required |
| ModSecurity WAF for NGINX                                  | Completed                    |
| Fail2ban                                                   | Completed, Under Review      |
| CIS (Center of Information Security) Benchmarks for NGINX  | Completed, Under Review      |
| CIS (Center of Information Security) Benchmarks for Ubuntu | Brainstorming                |

## CIS (Center of Information Security) Benchmarks Automation Tracker

### Ubuntu

| Item    | Control                                                                       | Scored     | Automated          |
|---------|-------------------------------------------------------------------------------|------------|--------------------|
| 4.3     | Ensure logrotate is configured                                                | Scored     | :heavy_check_mark: |
| 4.4     | Ensure logrotate assigns appropriate permissions                              | Scored     | :heavy_check_mark: |

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
