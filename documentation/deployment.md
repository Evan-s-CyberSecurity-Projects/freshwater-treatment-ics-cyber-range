
---

## `documentation/deployment.md`

```markdown
# Deployment Guide

This document describes the deployment lifecycle for the Freshwater Treatment
ICS Cyber Range.

The environment is designed to be created automatically rather than assembled
manually inside GNS3.

---

## Deployment Workflow

```text
Developer Change
      ↓
GitHub
      ↓
Jenkins
      ↓
Docker Image Build
      ↓
Container Registry
      ↓
GNS3 API
      ↓
Topology Creation
      ↓
Network Configuration
      ↓
Node Startup
      ↓
Connectivity Validation
