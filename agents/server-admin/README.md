# Server Admin

Production-ready Linux server administrator for Raspberry Pi CM5 with enterprise-level security, monitoring, and automation.

## Purpose

Comprehensive Linux server administration for Raspberry Pi CM5 running Raspbian/Debian. Delivers production-ready configurations with enterprise security hardening, professional monitoring, encrypted backups, and complete web stack deployment following industry best practices.

## Core Capabilities

### 🔒 Enterprise Security
Kernel hardening (40+ sysctl parameters), AppArmor MAC enforcement, auditd compliance logging (PCI-DSS, HIPAA, SOC2), file integrity monitoring (AIDE, rkhunter, chkrootkit, ClamAV, Lynis), SSH 2FA with Google Authenticator, PAM password policy, ModSecurity WAF with OWASP CRS, advanced DDoS protection, and fail2ban intrusion prevention.

### 📊 Professional Monitoring
Complete observability stack: Prometheus metrics collection, Grafana visualization dashboards, Alertmanager with email notifications, Node Exporter system metrics, Netdata real-time monitoring, uptime checks with auto-restart, and custom alert rules for CPU, memory, disk, and service availability.

### 💾 Encrypted Backups
GPG-encrypted backups (4096-bit RSA) with rclone offsite storage to cloud providers. Automated MariaDB and PostgreSQL backups, web files archiving, retention policies (7 days local, 30 days remote), monthly restoration testing, and documented recovery procedures.

### ⚡ Performance Optimization
Tuned for Raspberry Pi CM5 (4GB RAM): PHP-FPM dynamic pools with OPcache, MariaDB InnoDB optimization with query cache, PostgreSQL shared buffers and pg_stat_statements, Nginx FastCGI caching and gzip compression, ARM-specific optimizations, log2ram for SD card longevity, and thermal monitoring.

### 🌐 Web Stack
Nginx reverse proxy with OCSP stapling and HTTP/2, PHP-FPM 8.2/8.3 with comprehensive extensions, MariaDB and PostgreSQL with remote access, Let's Encrypt SSL automation with auto-renewal, and SFTP secure file uploads.

### 🛠️ Development Tools
Git with SSH keys, Node.js LTS with npm/yarn/pnpm/PM2, Docker with security hardening, Docker Compose, Podman rootless containers, Composer for PHP, CI/CD pipelines (GitHub Actions, GitLab Runner), and automated deployment scripts.

## Key Features

**Production-Ready Security**: Multi-layer defense with kernel hardening, MAC enforcement, WAF protection, file integrity monitoring, and comprehensive audit logging meeting PCI-DSS, HIPAA, and SOC2 compliance requirements.

**Professional Monitoring**: Complete observability with Prometheus, Grafana, Alertmanager, and automated email alerts for critical events with service auto-restart capabilities.

**Disaster Recovery**: Encrypted backup strategy with offsite cloud storage, automated retention policies, and monthly restoration testing ensuring all backups are encrypted before leaving the server.

**Performance Tuned**: Optimized configurations for PHP-FPM, MariaDB, PostgreSQL, and Nginx with caching strategies, buffer optimization, and resource management for Raspberry Pi hardware.

**Interactive Configuration**: Asks clarifying questions about SSH port, authentication methods, database access, domains, backup destinations, and monitoring preferences with security trade-offs explained.

**Raspberry Pi Optimization**: ARM architecture optimizations, thermal monitoring with alerts, SD card longevity improvements (log2ram), and resource-aware configurations.

## Usage

Load the agent in Augment Code CLI and follow the systematic setup: initial system hardening, SSH 2FA configuration, firewall setup, web stack installation, SSL automation, monitoring deployment, encrypted backups, and development tools.

## Technical Approach

Follows CIS Benchmarks for Debian/Linux, OWASP Top 10 protection with ModSecurity, PCI-DSS compliance requirements, and modern encryption standards. Uses proven tools optimized for Raspberry Pi while maintaining enterprise-level security with defense in depth, least privilege principles, and comprehensive documentation.

