# AWS-CF-VPC
AWS Cloud formation - Stack VPC Nephelai 2.0

## Quick user guide

### Introduction

This repo contains the template for deploying a VPC, Virtual Private Cloud within the AWS TX Group accounts.

This page will guide you through the process of deploying said VPC.

To deploy a VPC, navigate to the [service catalog](#service), which contains all of the available services you can deploy within AWS.

### Parameters

#### VpcSize
Select the size of your VPC (S, S2, M, L, XL).

##### Standard size distribution

Size | S | M | L | XL
:---: | ---: | ---: | ---: | ---:
**Private subnet** | 64 | 256 | 1024 | 4096
**Public subnet** | 16 | 64 | 256 | 1024
**IntraVPC subnet** | 0 | 16 | 64 | 256

##### Optional size distribution

Size | S2 | M2 | L2 | XL2
:---: | ---: | ---: | ---: | ---:
**Private subnet** | 32 | 128 | 512 | 2048
**Public subnet** | 32 | 128 | 512 | 2048
**IntraVPC subnet** | 0 | 16 | 64 | 256

Sizes are subject to possible changes.

#### Token for M, L and XL sized VPC
If you select a VPC size other than S, you need to request a token from Network Services first (network@tamedia.ch) providing the following details: Requirement for bigger VPCs (the number of needed IP addresses), the region to deploy in, your account ID and the desired VPC size.

#### Connect to central router (Transit Gateway)
`Yes/No`

Allow (or not) connections to other accounts in EIS infrastructure, for VPN access, on premise access, or other internal applications.

#### Access to MediaIT services
`Yes/No`

Allow (or not) your VPC to join the mediait domain.

#### Tag (Custom implementations)
This is for specific use cases discussed and implemented by Network Services, e.g specific VPN access or inter-application connections.

<a name="service"/>

### Service Catalog (How To Use)

This is a frontend provided by Network Services to allow the client to set up their own VPC for AWS based applications.

You need to make sure you can access the services in the catalog:
- By navigating to your AWS Service Catalog: https://eu-west-1.console.aws.amazon.com/console/home?region=eu-west-1
- Type `service catalog` in the search bar

![type in search bar](/images/2020-02-11_135058.png)
- Click on portfolios

![](/images/svcc2.png)

- Click on imported

![](/images/2020-02-11_135855.png)

- Click on infrastructure

![](/images/2020-02-11_140118.png)

- Click on `Groups, roles, and users`

![](/images/2020-02-11_140214.png)

- Add groups, roles, users

![](/images/2020-02-11_140351.png)

- Click on the roles tab, and check your role

![](/images/2020-02-11_140647.png)

## Glossary
- AWS - Amazon Web Services
- VPC - Virtual Private Cloud - Virtual Data Center