# Awesome-Cloud-Backup-Posture-Management

## Top Cloud Backup Posture Management Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Backup Coverage Discovery, Policy Enforcement & Ransomware Resilience*  

**Last updated: March 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Cloud Backup Posture Management (CBPM)**. These tools autonomously scan cloud resources, map backup coverage, enforce retention policies, and ensure recovery readiness—turning backup from a manual checklist into a continuously verified system.



**Examples** include Eon, Clumio, Veeam, HYCU, Rubrik, Cohesity, Druva, Commvault Cloud, Metallic, and Keepit (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, independent backup verification, and open monitoring infrastructure—ideal for platform engineers, SREs, and developers seeking transparent, vendor-independent backup posture management.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## Sector Overview & Market Dynamics

The global cloud backup and data protection market is estimated at **$7.13B–$8.73B in 2026** (projected to exceed **$25B–$30B by 2032** at a 16–22% CAGR), with the emerging Cloud Backup Posture Management (CBPM) segment gaining rapid momentum within the broader $9B+ Cloud Security Posture Management (CSPM) landscape. The sector is **moderately fragmented and rapidly consolidating**, characterized by established enterprise giants (Veeam, Rubrik, Cohesity, Commvault) executing major M&A alongside venture-backed challengers (Eon, Keepit) disrupting legacy snapshots with autonomous, query-driven posture governance.

## SaaS/Hosted Platforms

| Platform | Company Scale (Valuation / Revenue) | Starting Pricing Tier | Free Tier / Trial Limits | Key Capabilities & Highlights |
| :--- | :--- | :--- | :--- | :--- |
| **[Rubrik](https://www.rubrik.com/)** | **~$22B–$23B** Market Cap / **$1.09B+** ARR (FY2025) | Starts at **~$130–$228/FETB/mo** (or ~$50,000/yr baseline contract; Enterprise quotes via Private Offer) | **Proof of Concept (PoC) / Guided Sandbox**: 30-day dedicated evaluation sandbox in enterprise environment (no unassisted free tier) | Zero Trust data security platform with immutable backups, ransomware anomaly detection, and automated recovery via Rubrik Security Cloud across enterprise, cloud, and SaaS. |
| **[Veeam](https://www.veeam.com/)** | **~$15B** Valuation (2024 secondary) / **$1.75B+** ARR | Starts at **$1.08/user/mo** (Entra ID), **$3.33/user/mo** (M365 Backup), or **~$155–$250/workload/yr** (VUL Foundation) | **Free Forever**: Veeam Community Edition protects up to **10 workloads** indefinitely. **Free Trial**: 30-day enterprise trial (falls back to Community Edition) / 14-day SaaS trial. | Broadest workload coverage across virtual (VMware/Proxmox), cloud (AWS/Azure/GCP), and SaaS with granular restore and metadata protection. |
| **[Cohesity](https://www.cohesity.com/)** | **~$7B** Valuation / **$1.6B+** Combined Revenue (with Veritas) | Starts at **~$29,100/yr** (10 BETB DataProtect as a Service on AWS Marketplace baseline, ~$242.50/BETB/mo) | **Free Trial**: 30-day free trial of Cohesity Cloud Services (DataProtect as a Service) with full sandbox testing (no permanent free tier). | Data security and management platform with backup, disaster recovery, threat intelligence, and Helios posture visibility. |
| **[Commvault Cloud](https://www.commvault.com/)** | **~$5.5B–$6.5B** Market Cap / **$1.03B+** ARR (FY2025) | Starts at **$1.70/user/mo** (Standard M365) to **$3.60/user/mo** (Enterprise M365); FETB consumption available | **Free Trial**: 30-day full-feature trial (no credit card required) or 30,000 AWS/Azure Marketplace trial credits over 30 days. | Enterprise data protection platform featuring Cloud Cleanroom Recovery for cyber recovery testing and ThreatWise proactive cyber deception. |
| **[Eon](https://www.eon.io/)** | **$4B** Valuation (Series D) / **$500M** Raised | Starts at **~$0.01–$0.025/GB/mo** (consumption-based via AWS/GCP Marketplace contracts; custom capacity commitments) | **Free Tier**: "Free for builders" developer access tier. **Free Trial**: 14-to-30 day cloud marketplace evaluation (infrastructure costs excluded). | Autonomous Cloud Backup Posture Management (CBPM) platform scanning and classifying cloud resources continuously, queryable backup data lakes, and automated recovery without full VM provisioning. |
| **[Druva](https://www.druva.com/)** | **~$2B+** Valuation / **$250M+** ARR | Starts at **$4.00–$8.00/user/mo** (inSync SaaS/Endpoints) or ~$200–$250/TB/mo consumption for cloud workloads | **Free Trial**: 30-day full-feature trial for Microsoft 365, endpoints, and cloud workloads with live chat support and AI guidance (no credit card required). | 100% SaaS-based data protection and posture management with global deduplication, endpoint protection, and automated ransomware resilience. |
| **[Metallic (Commvault)](https://www.metallic.io/)** | Part of **Commvault ($5.5B–$6.5B)** | Starts at **$1.70/user/mo** (M365 Backup standard) up to **$4.50/user/mo** (M365 Compliance tier) | **Free Trial**: 30-day free trial across M365, endpoints, and VM backup workloads (no credit card required). | SaaS-delivered backup and recovery under the Commvault Cloud portfolio, providing subscription data protection for M365, Salesforce, and endpoints. |
| **[Clumio (Commvault)](https://www.clumio.com/)** | Acquired by **Commvault** (2024) | Starts at **$0.010/GiB/mo** (Archive tier) & **$0.025/GiB/mo** (Standard tier) + $1.50/M managed objects | **Free Trial**: 14-day free trial on AWS and GCP Marketplaces (includes instant access snapshot restores and DynamoDB/S3 protection). | AWS-native serverless data protection and posture management with instant access search and granular recovery for S3, EBS, and DynamoDB. |
| **[Keepit](https://www.keepit.com/)** | **~$172M+** Raised / Private | Starts at **$2.60–$4.95/user/mo** (or £4.00/user/mo on UK G-Cloud; includes unlimited storage & retention) | **Free Trial**: 30-day enterprise evaluation trial for Microsoft 365, Google Workspace, and Salesforce (no permanent free tier). | Dedicated vendor-independent cloud-to-cloud backup with tamper-proof immutable data storage and 10-year retention guarantee. |
| **[HYCU](https://www.hycu.com/)** | **~$140M+** Raised / Private | Starts at **$1.20/user/mo** (Identity/Okta), **$2.25/user/mo** (M365), or **$5,000/yr** (Starter Bundle: 50 VMs, 10 TB, 100 SaaS users) | **Free Trial**: 14-day free trial for HYCU R-Cloud and cloud-native Azure/AWS data protection. | Multi-cloud backup for Nutanix, VMware, and R-Cloud integration covering 70+ SaaS applications and identity suites. |



## Open-Source GitHub Projects



- **[Restic Explorer](https://github.com/tmseidel/restic-explorer)**  

  Lightweight monitoring interface for **restic backup repositories** (license varies). Built to feed status and health data into observability solutions such as Grafana, Prometheus, or Uptime Kuma. Features **observability-first health signals** (`/actuator/health` exposes per-repository scan, integrity-check, and retention status), **multi-repository dashboard** with status badges and lock warnings, **automated scanning and integrity checks** (`restic snapshots` and `restic check --read-data`), **retention policies** with amber violation warnings, and **encrypted credentials** (AES-256-GCM at rest). Supports S3/S3-compatible, Azure Blob, SFTP, REST Server, and Rclone backends . **The most purpose-built open-source backup posture monitoring tool for restic deployments.**



- **[Backmon](https://github.com/dreitier/backmon)**  

  Monitoring tool for **backup files in filesystems and object storages** (MIT). Monitors presence, size, and timestamps of recurring backup files stored in local filesystem or S3-compatible object storage (AWS S3, MinIO) . Integrates with **Prometheus and Grafana** for analyzing backup duration and alerting on constraint failures. Helm chart available for Kubernetes deployment. **Go-based with Docker containers available.**



- **[Bacula-Web](https://github.com/bacula-web/bacula-web)**  

  Open-source reporting and monitoring tool for **Bacula backup infrastructure** (GPLv2). Provides main dashboard with overall backup job status, used volumes, weekly statistics; jobs report and logs; pools and volumes reports; multiple Bacula director statistics from single web UI; and browse backup jobs files and folders . Requires only read-only access to Bacula catalog database. Translated in 15+ languages. **The most mature open-source backup reporting tool for Bacula environments.**



- **[BackupBeacon](https://wordpress.org/plugins/backupbeacon/)**  

  Independent watchdog for **WordPress backup verification** (open-source). Most backup failures are silent—BackupBeacon is the alarm that doesn't grade itself. Add backup destinations with freshness limits in hours; point backup jobs at token-authenticated ping endpoint; every successful backup pings . Evaluates every destination hourly (WP-Cron): **fresh**, **stale** (past limit), or **silent** (never recorded). Email and persistent admin notice on stale/silent. **No external account, no per-site fees**—pings arrive at your own WordPress site. Backup-plugin-agnostic—works with any tool that can run curl after finishing .



- **[jobwatch](https://www.npmjs.com/package/jobwatch)**  

  Check-in system for **cron jobs and backups** (open-source). A job that runs fine emits nothing on its own; the only way to know it stopped is that it stops checking in. Jobs call `jobwatch checkin <name>` when they finish; separate scheduled `jobwatch status` reports anything quiet . Statuses: **OK**, **OVERDUE**, **NEVER**. Exit codes compose directly as cron job or monitoring command check. Configurable per-job `every` and `grace` periods. **Lightweight Node.js-based watchdog for any scheduled backup script.**



- **[Velero Backup Verification (OneUptime)](https://github.com/OneUptime)**  

  Open-source **backup verification tests using Velero restore jobs** (license varies). Kubernetes Job that performs end-to-end verification: checks backup status is Completed, creates test namespace, performs restore with namespace mappings, verifies restored resources (pods, services, PVCs), tests application connectivity, generates verification report, and cleans up test resources . CronJob runs daily at 3 AM with concurrency policy Forbid. **The most comprehensive open-source backup verification pattern for Kubernetes environments.**



- **[Ceph Backup Verification Runbook](https://github.com/OneUptime)**  

  Open-source runbook for **Rook-Ceph backup verification** (license varies). Systematic verification steps for all Ceph data paths: **RBD snapshots** (list, check size not zero, clone and mount), **Velero backups** (check status, restore to staging namespace), **CephFS backup** (Restic snapshots, integrity check, subdirectory restore), **RGW bucket replication** (sync status, object count parity), and **checksum verification** (md5sum before/after restore) . **Monthly restore testing minimum** to confirm disaster recovery procedures work.



- **[Nakivo Prometheus Exporter](https://pypi.org/project/nakivo-prometheus-exporter/)**  

  Open-source Prometheus exporter for **Nakivo Backup & Replication** (license varies). Connects to Nakivo API endpoint and fetches licensing and backup state information as Prometheus metrics . Configurable multi-host monitoring with `cert_verify` options. **Proof of concept**—currently fetches VM backup state and licensing state, with quiescing, backup sizes, and durations listed as future additions. Recommended scrape interval: 1 hour.



- **[Prometheus Borg Exporter](https://github.com/mad-ady/prometheus-borg-exporter)**  

  Bash script to **monitor Borg backup with Prometheus** (license varies). 17 GitHub stars . Complementary to Restic Explorer for environments using BorgBackup instead of restic.



### Additional Strong Open-Source Options



- **[Pulse](https://github.com/rcourtman/pulse)** — Real-time monitoring dashboard for **Proxmox VE, Proxmox Mail Gateway, PBS, and Docker infrastructure** with alerts and webhooks (open-source). Features unified view of PBS backups, PVE backups, and snapshots; interactive Backup Explorer with cross-highlighted bar chart and grid; quick time-range pivots; and smart alerts via email, Discord, Slack, Telegram . **The most feature-rich open-source backup posture dashboard for Proxmox environments.**

- **[DBackup](https://github.com/Skyfay/DBackup)** — Open-source backup solution with **backup file integrity verification** (v2.7.0). Storage Explorer shows SHA-256/MD5 checksums and last verification result per file, with Verify Now button running tracked async execution . Native checksum verification for S3/R2/Hetzner (SHA-256 via object metadata), Google Drive (MD5 via API), OneDrive (SHA-256 via Graph API), and local filesystem—**no download required**. Post-upload verification opt-in for all storage destinations.

- **[OpenObserve](https://github.com/openobserve/openobserve)** — Open-source observability platform for metrics, logs, and traces—can ingest backup health signals from multiple sources.

- **[Grafana](https://github.com/grafana/grafana)** — Open-source analytics and monitoring platform for building unified backup posture dashboards.

- **[Zabbix](https://www.zabbix.com/)** — Open-source enterprise monitoring with **native AWS Backup template** providing vault discovery, recovery point tracking, lock status, retention period monitoring, and job state filtering . Template macros configure backup job filtering by state, resource type, and resource name.

- Community **n8n** workflows for backup alert routing and posture reporting automation.



**Frameworks for building custom systems**: Combine **Restic Explorer** or **Backmon** for backup health monitoring with **Velero Backup Verification** for end-to-end restore testing, **Bacula-Web** for Bacula reporting, **Pulse** for Proxmox dashboards, and **Prometheus + Grafana** for unified alerting—creating a fully self-hosted, enterprise-grade backup posture management platform.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Cloud backup posture management systems handling backup data must comply with data protection regulations (GDPR, CCPA, etc.) and industry-specific retention requirements.

- **A backup that has never been tested is not a backup.** Most verification stops at the backup's Completed status—go one step further and confirm volume bytes actually moved and restores produce the expected data . Velero's data mover can confirm byte counts; DBackup provides SHA-256/MD5 checksums .

- **Backup tools restore into clusters that already exist.** They do not create the cluster, nodes, network, load balancers, or DNS. A DR plan that starts with "restore the backup" must state what the backup gets restored into .

- **Declared state is not stored state.** A GitOps controller can rebuild application definitions from Git while the recovery cluster has never run the application—the store holds the data, the declarations hold the structure, and restoring one without the other fails .

- **Metric edge cases exist.** Velero's `velero_backup_last_status` metric reflects the latest backup of a schedule, not a specific backup—it can report 1 even when recent backups are PartiallyFailed . Always cross-check with `velero backup describe`.

- **Open-source coverage is tool-specific.** Restic Explorer, Backmon, and Bacula-Web are mature for their respective backup tools. There is no generic open-source CBPM that discovers unprotected cloud resources across AWS, Azure, and GCP—that remains a commercial capability .

- Self-hosted open-source solutions require proper security hardening, credential encryption (AES-256-GCM recommended), and ongoing maintenance. Backup posture is not compliance—it is evidence that recovery is possible.



---



**Made for platform engineers, SREs, backup administrators, and developers building transparent backup posture solutions.**  

Let's make Cloud Backup Posture Management more open, data-driven, and verifiable.
