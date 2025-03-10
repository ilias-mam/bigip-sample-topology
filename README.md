# BIGIP Network Documentation

## Overview
This document provides an overview of the WAN network configuration, including IP addresses, clusters, and services.

## Network Segments

### WAN Network
- **Subnet**: 192.168.1.0/24

### Cluster Network
- **Subnet**: 172.16.1.0/24

### LAN Network
- **Subnet**: 192.168.2.0/24

### Task Network
- **Subnet**: 192.168.3.0/24

## BigIPS - Virtual IPS
- **Service-Prpd-1**: 192.168.1.20
- **Service-Prpd-2**: 192.168.1.21
- **Service-Test-1**: 192.168.1.22

## Cluster Configuration

### Active Node
- **BIG-IP 1 (ACTIVE)**
  - **WAN IP**: 192.168.1.101
  - **LAN IP**: 192.168.2.101
  - **TEST IP**: 192.168.3.101
  - **Management IP**: 172.16.0.1
  - **Cluster IP**: 172.16.1.1

### Floating IPs between the two bigips
- **Floating WAN**: 192.168.1.10
- **Floating LAN**: 192.168.2.10
- **Floating Test**: 192.168.3.10

### Standby Node
- **BIG-IP 2 (STANDBY)**
  - **WAN IP**: 192.168.1.102
  - **LAN IP**: 192.168.2.102
  - **TEST IP**: 192.168.3.102
  - **Management IP**: 172.16.0.2
  - **Cluster IP**: 172.16.1.2

## Service Pools

### Services-Prpd-1 Pool
- **Service-Prpd-2 Pool**
- **Service-Prpd-3 Pool**
- **Service-Test Pool**

### Members
- **Service-Prot-1 member1**: 192.18.2.11
- **IS Servers prpd-3 member1**: 192.18.2.21
- **IS Servers prpd-2 member2**: 192.18.2.22
- **IS Servers prpd-3 member2**: 192.18.2.23
- **IS Servers prpd-2 member3**: 192.18.2.24
- **IS Servers prpd-3 member3**: 192.18.2.25
- **IS Servers prpd-2 member3**: 192.18.2.26
- **IS Servers prpd-3 member3**: 192.18.2.27

### Service-Test Pool
- **IS Server-Test**: 192.168.33.11

## Summary
This documentation outlines the network configuration, including IP addresses for the active and standby nodes, floating IPs, and service pools. It provides a clear structure for understanding the network setup and the roles of each component.
