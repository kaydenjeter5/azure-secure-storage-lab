# Secure Azure Storage Account Lab

## Project Summary

This lab demonstrates how to create and secure an Azure Storage Account using private blob storage, least-privilege RBAC access, secure configuration settings, and diagnostic logging through Log Analytics.

## Objective

Secure a storage account using:

- Private blob container access
- Least-privilege Azure RBAC
- Secure transfer enforcement
- TLS enforcement
- Anonymous access prevention
- Diagnostic logging
- Basic security recommendation review

## Resources Created

| Resource | Name |
|---|---|
| Resource group | `rg-azure-learning` |
| Storage account | `gluttonystorage01` |
| Blob container | `container-lab-private` |
| Log Analytics workspace | `law-azure-learning` |
| Diagnostic setting | `diag-storage-logs` |

## Storage Account Configuration

The storage account was configured with standard, low-cost lab settings:

- Performance: Standard
- Redundancy: Locally-redundant storage
- Secure transfer required: Enabled
- Minimum TLS version: TLS 1.2 or higher
- Anonymous blob access: Disabled
- Container access level: Private

## Identity And Access Management

Access was assigned using Azure RBAC instead of broad account-level sharing.

| Group | Role | Purpose |
|---|---|---|
| `grp-storage-contributors` | Storage Blob Data Contributor | Upload and manage blobs |
| `grp-azure-readers` | Reader | View storage account metadata without making changes |
| `grp-security-reviewers` | Storage Blob Data Reader or Security Reader | Review storage/security information |

## Access Testing

The lab should verify the following access behavior:

| Test | Expected Result | Actual Result |
|---|---|---|
| Storage contributor uploads a blob | Allowed | TODO |
| Reader attempts to modify blobs | Blocked | TODO |
| Unauthorized user accesses private container | Blocked | TODO |
| Anonymous/public access attempt | Blocked | TODO |
| Storage read/write/delete action appears in logs | Logged | TODO |

## Logging Configuration

A Log Analytics workspace named `law-azure-learning` was created to collect diagnostic logs.

Diagnostic settings were configured from:

```text
Storage account -> Monitoring -> Diagnostic settings
```

The diagnostic setting sends storage activity logs to Log Analytics for review.

Relevant activity includes:

- Storage read events
- Storage write events
- Storage delete events

## Security Review

Microsoft Defender for Cloud was reviewed for storage-related recommendations. Paid plan prompts were not enabled unless required for the lab and understood first.

## Screenshots To Add

Add screenshots to the `screenshots/` folder showing:

- Storage account overview
- Storage account configuration settings
- Private container access level
- RBAC role assignments
- Log Analytics workspace
- Diagnostic setting configuration
- Example access test result
- Example log query result
- Defender for Cloud recommendation, if available

## Lessons Learned

TODO: Add 3-5 bullets in your own words after completing the lab.

Examples:

- Azure Storage security depends on both configuration settings and identity permissions.
- Private containers prevent anonymous blob access.
- RBAC allows more controlled access than sharing storage account keys.
- Diagnostic logs provide evidence for monitoring and investigation.

## Cleanup Notes

To control cost, remove unused test files and review Log Analytics retention. Keep the resource group only if continuing with later Azure labs.

