# Azure Static Website Portfolio

This project is my personal portfolio website hosted on Microsoft Azure. I created it as a hands-on project to practice working with Azure Storage, static website hosting, security settings, and basic cost optimization.

The website was built using HTML and CSS and is hosted using the Static Website feature in Azure Storage.

## Architecture

```text
GitHub Repository
       |
       | index.html
       v
Azure Resource Group
       |
       v
Azure Storage Account
(StorageV2 / Standard)
       |
       v
Static Website Hosting
       |
       v
$web Container
       |
       v
Public HTTPS Endpoint
       |
       v
Portfolio Website
```

## Azure Services Used

- Azure Resource Group
- Azure Storage Account
- Azure Blob Storage
- Azure Static Website Hosting

## Configuration

| Setting | Configuration |
|---|---|
| Account kind | StorageV2 (General-purpose v2) |
| Performance | Standard |
| Redundancy | Locally Redundant Storage (LRS) |
| Access tier | Hot |
| Static website | Enabled |
| Index document | `index.html` |
| Secure transfer | Enabled |
| Minimum TLS version | TLS 1.2 |

## Cost Optimization

Since this is a small portfolio website, I wanted to keep the Azure costs as low as possible.

I used Azure Storage Static Website hosting instead of running a virtual machine or web server. I also selected Standard storage with LRS redundancy and avoided additional services such as Azure Front Door and Microsoft Defender for Storage.

## Security

For the storage account:

- Secure transfer is enabled.
- Minimum TLS version is TLS 1.2.
- Anonymous blob access is disabled.
- Microsoft-managed encryption keys are used.
- SFTP and NFS are disabled because they are not needed.
- Public network access is enabled so the portfolio can be accessed from the internet.

## Resource Tags

I added tags to make the Azure resources easier to identify and organize.

| Tag | Value |
|---|---|
| Project | CloudPortfolio |
| Environment | Portfolio |
| Purpose | StaticWebsite |

## Deployment

1. Created the GitHub repository.
2. Created the portfolio website using HTML and CSS.
3. Created a resource group in Azure.
4. Created a StorageV2 storage account using Standard performance and LRS.
5. Configured the storage account networking and security settings.
6. Added resource tags.
7. Enabled Static Website hosting.
8. Set `index.html` as the index document.
9. Uploaded `index.html` to the `$web` container.
10. Tested the Azure HTTPS endpoint to confirm that the website was working.

## What I Learned

This project gave me practical experience with:

- Azure Storage Accounts and Blob Storage
- Static website hosting in Azure
- Storage account security and networking settings
- Storage redundancy and access tiers
- Azure resource groups and tags
- Basic Azure cost optimization
- Deploying and testing a website in Azure

## Live Website

**Live Website:** https://myportfoliowebpage.z1.web.core.windows.net/

## Screenshots

### Storage Account Overview

<img width="1905" height="914" alt="storage-account-overview" src="https://github.com/user-attachments/assets/06524fd6-e43f-4576-b50e-a5dd382baca4" />

The storage account uses StorageV2, Standard performance, and locally redundant storage (LRS). The overview also shows the configured security, networking, and resource tags.

### Static Website Configuration

<img width="1909" height="889" alt="static-website-config" src="https://github.com/user-attachments/assets/9e9c57d6-a57f-4df1-8358-dc8d3d88b469" />

Static website hosting is enabled with `index.html` configured as the index document. Azure automatically created the `$web` container and provided a public HTTPS endpoint.

### Live Portfolio Website

<img width="1894" height="983" alt="live-portfolio" src="https://github.com/user-attachments/assets/5ff78438-dc80-4d0f-8fab-4611ffa7dec6" />

The portfolio website running successfully from the Azure Storage static website endpoint.

## Author

**Russell Jazdan (Rasool Yazdanshenas)**  
Cloud Student

- GitHub: https://github.com/Russjaz
- LinkedIn: https://www.linkedin.com/in/russell-jazdan-7ab346143/
