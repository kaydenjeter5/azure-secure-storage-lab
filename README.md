# Azure Secure Storage Account Lab

This project documents a hands-on Azure security lab focused on securing an Azure Storage Account with least-privilege access, private blob storage, diagnostic logging, and basic security review.

## Objective

Build and secure an Azure Storage Account using identity-based access control, secure configuration settings, private containers, logging, and access testing.

## Skills Demonstrated

- Azure Storage Account deployment
- Microsoft Entra ID and Azure RBAC
- Least-privilege access control
- Private blob container configuration
- Secure transfer and TLS enforcement
- Anonymous access prevention
- Diagnostic settings and Log Analytics
- Basic cloud security documentation

## Lab Environment

| Component | Value |
|---|---|
| Cloud provider | Microsoft Azure |
| Resource group | `rg-azure-learning` |
| Storage account | `gluttonystorage01` |
| Container | `container-lab-private` |
| Log Analytics workspace | `law-azure-learning` |
| Redundancy | Locally-redundant storage |

## Security Controls Implemented

- Disabled anonymous blob access
- Required secure transfer
- Enforced modern TLS
- Used private container access
- Applied least-privilege RBAC assignments
- Sent diagnostic logs to Log Analytics
- Reviewed storage-related security recommendations

## Repository Structure

```text
.
├── README.md
├── docs/
│   └── secure-storage-account-lab.md
└── screenshots/
    └── .gitkeep
```

## Status

Lab documentation is in progress. Screenshots should be added to the `screenshots/` folder as evidence of configuration, RBAC assignments, logging, and access testing.

