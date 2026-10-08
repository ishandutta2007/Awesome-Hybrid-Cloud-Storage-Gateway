# Awesome-Hybrid-Cloud-Storage-Gateway

## Top Hybrid Cloud Storage Gateway Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Cloud Tiering, Global File Systems & Self-Hosted Storage Gateways*  

**Last updated: October 2026**



This repository tracks notable **commercial hybrid cloud storage gateway platforms** and **open-source projects** that bridge on-premises storage with cloud object storage — providing local caching, global file access, and seamless data tiering for distributed organizations.



**Examples** include AWS Storage Gateway, Azure Stack Edge, NetApp Cloud Volumes ONTAP, Pure Storage Cloud Block Store, Panzura CloudFS, Nasuni File Data Platform, CTERA Enterprise File Services, Cohesity SmartFiles, Qumulo Core, and Lucidity (the category leaders).



**Open-source emphasis**: Hybrid cloud storage gateways are an emerging open-source domain. **Vaultaire** provides a universal storage orchestration engine that turns any storage backend into a unified S3-compatible API with intelligent tiering . **NooBaa** delivers a high-performance S3 application gateway to any backend — file, S3-compatible, multi-cloud, with caching and replication . **gfeh** brings a multi-protocol VFS layer for object storage with read-through caching and two-way mirroring . **FreeNAS** (now TrueNAS) provides an open-source NAS OS with ZFS, CIFS/NFS/iSCSI, and container integration . **MooseFS** offers a European distributed NAS alternative with POSIX compliance and up to 16 exabytes of capacity . **Lustre** and **OpenZFS** are available as managed services on AWS and GCP . This section is heavily expanded.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



| Platform | Description & Best For | Pricing | Free Tier / Trial Limit |
| :--- | :--- | :--- | :--- |
| **[AWS Storage Gateway](https://aws.amazon.com/storagegateway/)** | **AWS hybrid cloud storage service** providing S3 File (NFS/SMB), Volume (iSCSI), and Tape gateways with local LRU caching. Best for AWS-native hybrid storage. | **$0.01 / GB written** (capped at $125/gateway/mo) + standard S3 storage fees ($0.023/GB/mo) | **100 GB written** to AWS per account free forever (Always Free) |
| **[Azure Stack Edge](https://azure.microsoft.com/en-us/products/azure-stack/edge/)** | **Managed edge computing & storage gateway** device with AI acceleration and Azure Blob/File integration. Best for Azure-native hybrid edge storage. | Starts at **~$399 / month** hardware subscription fee + standard Azure Blob storage charges | **No hardware trial** (Azure cloud account provides 30-day / $200 credit for cloud services only) |
| **[NetApp Cloud Volumes ONTAP](https://www.netapp.com/cloud/)** | **Enterprise NAS & block storage** combining ONTAP data management (NFS, SMB, iSCSI) with cloud elasticity. Best for enterprise workloads needing NetApp features. | Starts at **$0.64 / hour** (Explore tier, up to 2TB) or ~$0.10 / GB-month payload capacity | **Freemium plan free forever** up to 500 GiB provisioned capacity (or 30-day trial with unmetered capacity) |
| **[Panzura CloudFS](https://panzura.com/)** | **Global cloud file system** with 60s snapshot RPO, global deduplication, and ransomware protection. Best for multi-site file collaboration. | Starts at **~$276.12 / TB / year** (CloudFS Archive) or **$840 / TB / year** (NAS tier) on AWS Marketplace | **No free tier** (Custom interactive demo & TCO assessment provided upon request) |
| **[Nasuni File Data Platform](https://www.nasuni.com/)** | **Cloud-native file service platform** replacing legacy NAS and backup with cloud-scale global file locking. Best for multi-site file consolidation. | Starts at **~$850 – $1,050 / TB / year** subscription license fee | **14-day free trial** with up to **5 TB** licensed data limit |
| **[CTERA Enterprise File Services](https://www.ctera.com/)** | **Global file system & gateway** with WAN optimization, endpoint backup, and edge filers. Best for distributed enterprise file services. | Starts at **~$1,200 / node / year** (or custom AWS/Azure private marketplace offer) | **30-day free trial** with full platform evaluation license |
| **[Cohesity SmartFiles](https://www.cohesity.com/)** | **Software-defined scale-out file & object platform** for enterprise data consolidation. Best for file data management and backup consolidation. | Starts at **~$150 – $400+ / TB / year** backend capacity (or ~$731 / TB / year list unit) | **30-day free trial** for cloud platform services (no perpetual free tier) |
| **[Qumulo Core](https://qumulo.com/)** | **Scale-out file storage system** with real-time data analytics, NFS, SMB, and S3 access. Best for media, HPC, and life sciences workloads. | **$0.009 to $0.026 / GB-month** (~$9.22 to $26.62 / TB-month) for cloud software + AWS/GCP infra | **30-day cloud trial** (with 1TB / 12TB trial editions on AWS Marketplace) |
| **[Pure Storage Cloud Block Store](https://www.purestorage.com/)** | **Cloud block storage platform** enabling workload portability across AWS and Azure with thin provisioning. Best for Pure Storage ecosystem users. | Starts at **~$80 – $90 / TB / month** based on Effective Used Capacity (EuC) + cloud infra | **30-day free trial** available via AWS / Azure Marketplace listings |
| **[Lucidity](https://www.lucidity.cloud/)** | **Autonomous cloud storage auto-scaler** providing automatic block storage expansion/shrinking for EBS disks. Best for cloud storage cost optimization. | Percentage of storage savings (~15-30% of reclaimed EBS costs) / customized software subscription | **Free storage audit tool** & no-commitment storage assessment + 14-day demo trial |



## Open-Source GitHub Projects



### Universal Storage Gateways



- **[Vaultaire](https://github.com/fairforge/vaultaire)**  

  **Universal storage orchestration engine that turns any storage backend into intelligent, unified infrastructure**, Apache-2.0 licensed . **Provides a single S3-compatible API across multiple storage backends** — "universal translator for storage"  . **Multi-backend support**: local filesystem, S3/S3-compatible, Seagate Lyve Cloud, Wasabi, Cloudflare R2, Backblaze B2, MinIO . **Intelligent tiering for automatic hot/cold data management**, erasure coding for built-in redundancy, and event streaming for full audit trail . **Three deployment options**: stored.ge managed service ($3.99/TB/month), stored.cloud enterprise platform ($19.99/TB/month), and Vaultaire Core self-hosted (open source) . **Best for multi-cloud storage orchestration** .



- **[NooBaa](https://github.com/noobaa/noobaa-core)**  

  **High-performance S3 application gateway to any backend**, Apache-2.0 licensed . **Connects to file systems, S3-compatible storage, and multi-clouds** with caching and replication  . **Abstracts data from any storage resource** — "the first dynamic data gateway" . **Best for hybrid and multi-cloud object storage** .



- **[gfeh](https://github.com/town-os/gfeh)**  

  **Multi-protocol VFS layer for object storage**, open-source . **Four federation modes**: Subtree mount (upstream reads/writes with short cache), Read-through cache (local with fetch-on-miss), Transparent proxy (synchronous upstream), and Two-way mirror (full local copy with conflict policy)  . **Mutations are journalled** — survive crashes, retry with backoff, land in audit log . **Console with 48 locales** for user self-service and public file sharing via tokens . **Best for unified object storage access** .



### Distributed File Systems & NAS



- **[MooseFS](https://github.com/moosefs/moosefs)**  

  **Open-source distributed NAS alternative to Qumulo and Dell PowerScale**, GPL-2.0 licensed . **Pure software solution** — runs on any x86 or ARM machine including Raspberry Pi  . **Supports up to 16 exabytes of capacity and 2 billion files per cluster** . **POSIX-compliant volume** with chunkservers for direct client access via Ethernet or InfiniBand — avoids the bottleneck of NFS/SMB share servers . **Free open-source version** plus Pro version with support billed per disk . **European alternative** to US-based storage vendors . **Best for media production and research environments** .



- **[FreeNAS / TrueNAS](https://github.com/truenas/scale)**  

  **Open-source storage OS based on FreeBSD**, BSD license . **ZFS storage with CIFS, NFS, and iSCSI support**  . **Intuitive management interface** with dynamic disk management and container integration . **Data protection during drive failures** . **Note**: FreeNAS has been renamed TrueNAS CORE (FreeBSD) / TrueNAS SCALE (Linux) . **Best for self-hosted NAS with ZFS** .



### Cloud Storage Services (Open-Source on Hyperscalers)



- **[Lustre](https://github.com/lustre/lustre)** — Available as managed service on AWS and GCP  . **High-performance parallel file system for HPC workloads** .



- **[OpenZFS](https://github.com/openzfs/zfs)** — Available on AWS and GCP  . **Enterprise-grade file system with data integrity and snapshots** .



- **[NetApp Trident](https://github.com/NetApp/trident)** — Open-source storage orchestrator for Kubernetes, fully supported by NetApp  . **Works with ONTAP and Element storage systems** with NFS and iSCSI connections . **Best for Kubernetes persistent storage** .



### Additional Strong Open-Source Options



- **MinIO** — S3-compatible object storage for cloud-native workloads . **Best for S3-compatible storage** .

- **Ceph** — Unified distributed storage with object, block, and file . **Best for unified storage infrastructure** .

- **SeaweedFS** — Fast distributed storage for billions of files with S3 API . **Best for large-scale file storage** .

- **GlusterFS** — Distributed file system with no-metadata server architecture . **Best for scale-out NAS** .

- **Rclone** — Universal cloud sync tool with 70+ storage providers . **Best for cloud data movement** .

- **restic** — Encrypted, deduplicated backups to cloud storage . **Best for secure backup to cloud** .



**Frameworks for building custom hybrid cloud storage gateway solutions**: Combine **Vaultaire** for universal S3 API across multiple backends with intelligent tiering . Use **NooBaa** for high-performance S3 gateway with caching and replication . Deploy **gfeh** for multi-protocol VFS access with read-through caching and two-way mirroring . Choose **MooseFS** for distributed NAS with POSIX compliance and exabyte scale . Use **FreeNAS/TrueNAS** for self-hosted ZFS storage . Integrate **NetApp Trident** for Kubernetes persistent storage with ONTAP backends . Note that true enterprise hybrid cloud storage gateways with global file systems, WAN optimization, and vendor-supported SLAs (AWS Storage Gateway, Azure Stack Edge, Panzura, Nasuni) remain primarily commercial territory; open-source stacks provide strong S3 gateways, distributed file systems, and NAS foundations that require integration for complete hybrid cloud storage.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Hybrid cloud storage gateways handle sensitive business data. Self-hosted solutions require proper security hardening, encryption at rest and in transit, access controls, and compliance with data privacy regulations.

- **Cache sizing is critical** for S3 File Gateway — start with 150 GiB and increase based on CloudWatch metrics. Cache can be increased but not reduced  .

- **AWS FSx File Gateway is no longer available to new customers**  . S3 File Gateway remains available.

- **Open-source storage gateways vary in maturity** — Vaultaire is in MVP development (Step 47 of 500)  ; NooBaa and MooseFS are production-ready .

- **License considerations**: Vaultaire uses Apache-2.0  , NooBaa uses Apache-2.0  , MooseFS uses GPL-2.0  , and FreeNAS/TrueNAS uses BSD . Verify licensing against your use case before committing.

- The open-source ecosystem provides strong S3 gateways, distributed file systems, and NAS foundations, but **global file systems, WAN optimization, and vendor-supported SLAs** remain primarily commercial offerings.



---



**Made for storage engineers, infrastructure architects, and organizations seeking hybrid cloud storage sovereignty.**

Let's make hybrid cloud storage gateways more open, transparent, and interoperable.
