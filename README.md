# Awesome-Cloud-Backup-Posture-Management

# Top Cloud Backup Posture Management Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Backup Coverage Discovery, Policy Enforcement & Ransomware Resilience*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Cloud Backup Posture Management (CBPM)**. These tools autonomously scan cloud resources, map backup coverage, enforce retention policies, and ensure recovery readiness—turning backup from a manual checklist into a continuously verified system.

**Examples** include Eon, Clumio, Veeam, HYCU, Rubrik, Cohesity, Druva, Commvault Cloud, Metallic, and Keepit (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, independent backup verification, and open monitoring infrastructure—ideal for platform engineers, SREs, and developers seeking transparent, vendor-independent backup posture management.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Eon](https://www.eon.io/)**  
  The first **Cloud Backup Posture Management (CBPM)** platform, autonomously scanning, mapping, and classifying cloud resources continuously . Provides backup recommendations based on business and compliance needs, ensuring appropriate backup policy is in use. Backup storage is fully managed, portable, and globally searchable—enabling customers to find and restore individual files and run SQL queries on backed-up database snapshots without full resource provisioning . Transforms static backup archives into queryable data lakes, with Google Cloud integration for BigQuery, Vertex AI, and Gemini . Reports **90% improvement in data recovery time** and **30-50% reduction in backup storage costs** .

- **[Clumio (Commvault)](https://www.clumio.com/)**  
  AWS-native backup and recovery platform acquired by Commvault in 2024. Provides managed, cloud-native data protection at scale with consumption-based pricing starting around $0.01 per GiB-month for S3 storage . **AWS-first**—does not support Azure, with Google Cloud Storage support in early access as of April 2026 . Now ships as **Clumio by Commvault** while remaining a distinct AWS-native SaaS product .

- **[Veeam](https://www.veeam.com/)**  
  Broadest workload coverage across cloud, virtual, physical, and SaaS. Offers **Veeam Backup for Microsoft 365** and **Veeam Backup for Salesforce** with granular restore and metadata protection.

- **[HYCU](https://www.hycu.com/)**  
  Multi-cloud backup and recovery for Nutanix, VMware, and SaaS applications including Microsoft 365 and Salesforce. Features R-Cloud for SaaS data protection.

- **[Rubrik](https://www.rubrik.com/)**  
  Zero Trust data security platform with immutable backups, ransomware detection, and automated recovery. Offers **Rubrik Security Cloud** for posture management across enterprise, cloud, and SaaS data.

- **[Cohesity](https://www.cohesity.com/)**  
  Data security and management platform with backup, recovery, and threat intelligence. **Helios** provides SaaS-based management and posture visibility across data sources.

- **[Druva](https://www.druva.com/)**  
  Cloud-native SaaS data protection with endpoint backup, Microsoft 365 protection, and ransomware resilience. **Druva Cloud Platform** provides unified posture management.

- **[Commvault Cloud](https://www.commvault.com/)**  
  Enterprise data protection platform with **Cloud Cleanroom Recovery** for ransomware recovery testing and **ThreatWise** for proactive threat detection. Metallic is the SaaS-delivered offering for mid-market.

- **[Metallic (Commvault)](https://www.metallic.io/)**  
  SaaS-delivered backup and recovery from Commvault. Provides enterprise-grade data protection with simple subscription pricing for Microsoft 365, Salesforce, and endpoint data.

- **[Keepit](https://www.keepit.com/)**  
  Independent cloud backup for Microsoft 365, Google Workspace, and Salesforce with immutable data storage and 10-year retention guarantee. Vendor-neutral with German data residency options.

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
