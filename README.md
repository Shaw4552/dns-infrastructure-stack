# DNS Infrastructure Stack (Pi-hole + Unbound)

## Overview

This project documents the design and implementation of a centralized DNS infrastructure stack using Pi-hole and Unbound, built to simulate production-grade DNS filtering and resolution services.

---

## Objectives

- Provide secure and reliable DNS resolution
- Implement domain-level filtering policies
- Support internal service discovery
- Enable DNS resolution over VPN
- Prepare for multi-node redundancy

---

## Architecture

### Components

- Pi-hole
  - DNS filtering
  - Policy enforcement
  - Client grouping

- Unbound
  - Recursive DNS resolver
  - Privacy-focused resolution (no upstream tracking)

- Caddy (planned/optional)
  - Internal TLS for service endpoints

---

## Design Principles

- Least-privilege DNS access
- Centralized resolution
- Separation between infrastructure and client networks
- Future-ready for high availability

---

## Features

- Domain blocking and allowlisting
- Group-based DNS policies
- Internal DNS records for services
- VPN-compatible DNS routing
- Reduced dependency on external DNS providers

---

## High Availability (Planned)

- Primary DNS node
- Secondary DNS node
- Policy synchronization
- Failover validation

---

## Lessons Learned

- DNS must be treated as critical infrastructure
- Client grouping is essential for avoiding service breakage
- DNS behavior differs significantly across device types
- Proper firewall rules are required for cross-VLAN DNS

---

## Future Improvements

- Automated policy sync (CI/CD)
- Health checks and failover automation
- Observability and logging improvements

---

## Sanitization Notice

All IP addresses, domains, and identifiers are generalized to protect infrastructure security.