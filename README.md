# Enterprise Data Center & ABIS Infrastructure Deployment (Production + DR)

**Role:** Technical lead and infrastructure owner
**Scope:** 65 physical servers across multiple racks, Production and Disaster-Recovery sites, open-source stack only
**Stack:** Ubuntu Server 22.04/24.04, Kubernetes (multi-master), Crunchy PostgreSQL Operator, PgBouncer, Rook-Ceph, Keycloak, HAProxy + Keepalived, VPN, VLANs

## Summary

I led the end-to-end design, deployment, hardening, and operational readiness of Production and Disaster-Recovery data centers for an enterprise Automated Biometric Identification System (ABIS). The platform was built entirely on open-source technology, with no dependency on commercial or licensed infrastructure software, and went from bare-metal server installation to production-ready application hosting.

## The Challenge

The environment needed a full enterprise data center stood up across two sites with equivalent capacity: high-throughput biometric processing, highly available application and identity services, resilient storage, segmented and firewalled networking, and a tested disaster-recovery path, all documented to a standard that would support future compliance audits.

## What I Did

- **Architecture and planning.** Mapped application requirements to server roles, storage needs, network zones, firewall rules, HA dependencies, and DR requirements; produced IP schema, network diagrams, server role mapping, and DR procedures.
- **Bare-metal to baseline.** Installed and standardized Ubuntu across 65 servers with hostname and network planning, OS-level hardening, package standardization, access control, and baseline security controls.
- **Kubernetes platform.** Deployed multi-master, multi-worker Kubernetes clusters across both sites with container networking, ingress routing, namespace separation, autoscaling, PodDisruptionBudgets, and anti-affinity rules; ran high-throughput biometric extraction and matching on dedicated external servers in a hybrid design.
- **Database high availability.** Deployed PostgreSQL HA using the Crunchy PostgreSQL Operator with primary and replica nodes, PgBouncer connection pooling, backup integration, and DR replication readiness.
- **Storage.** Integrated Rook-Ceph for block storage (databases), shared filesystem storage (application data), and S3-compatible object storage (backup repositories).
- **Network and security.** Segmented the environment into isolated VLANs for application, database, storage, management, biometric processing, and DR traffic; isolated it from direct internet access with firewall whitelisting, Kubernetes network policies, audit logging, and centralized access management.
- **High availability and disaster recovery.** Layered HA across Kubernetes self-healing, application and database replicas, PgBouncer pooling, HAProxy load balancing, VIP failover, and replicated storage; ran DR planning, failover procedures, dependency mapping, recovery validation, and DR drills.
- **Compliance documentation.** Produced architecture, security, and DR documentation aligned to ISO/IEC 22237 for data center infrastructure and ISO/IEC 27001:2022 for information security.

## Results

- Delivered complete Production and DR infrastructure for an enterprise ABIS platform, built on open-source technology only.
- High availability implemented across application, database, load-balancing, storage, and biometric service layers.
- Tested disaster recovery with validated failover procedures and DR drills.
- Full architecture, security, and DR documentation for long-term support and compliance readiness.

## Skills Demonstrated

Solution architecture, vendor coordination, Linux systems, Kubernetes, high availability, disaster recovery, database infrastructure, software-defined storage, network segmentation, security hardening, and compliance-focused documentation.
