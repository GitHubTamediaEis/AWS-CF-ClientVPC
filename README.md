
# AWS-CF-VPC

AWS Cloud formation - Stack VPC Nephelai 2.0

  

## Quick user guide

  

### Introduction

  

This repo contains the template for deploying a VPC, Virtual Private Cloud within the AWS TX Group accounts.

  

This page will guide you through the process of deploying said VPC.

  

To deploy a VPC, navigate to the <a  href="./serviceCatalog.md">service catalog</a>, which contains all of the available services you can deploy within AWS.

  

#### Parameters

  

- VpcSize

Select the size of your VPC (S, S2, M, M2, L, L2, XL, XL2).

  

#### Standard size distribution

 ```markdown
|       Size            | S  | M   | L   | XL   |
|                       |----|-----|-----|------|
| **Private subnet**    | 64 | 256 |1024 | 4096 |
|  **Public subnet**    | 16 |  64 | 256 | 1024 |
| **IntraVPC subnet**   | 0  |  16 |  64 |  256 |
 ```
  

#### Optional size distribution
  ```markdown
|       Size            | S2 | M2  | L2  | XL2  |
|                       |----|-----|-----|------|
| **Private subnet**    | 32 | 128 | 512 | 2048 |
|  **Public subnet**    | 32 | 128 | 512 | 2048 |
| **IntraVPC subnet**   | 0  | 16  | 64  | 256  |
```

- Token for M, M2, L, L2, XL and XL2 sized VPC

  

If you select a VPC size other than S, you need to request a token from Network Services first (network@tamedia.ch) providing the following details: Requirement for bigger VPCs (the number of needed IP addresses), the region to deploy in, your account ID and the desired VPC size.

  

-  Connect to central router (Transit Gateway)

`Yes/No`

  

Allow (or not) connections to other accounts in EIS infrastructure, for VPN access, on premise access, or other internal applications.


  

- Tag (Custom implementations)

This is for specific use cases discussed and implemented by Network Services.

  
### Why choose a service catalog's VPC rather than a simple AWS VPC

By choosing the VPC proposed in the catalog service you have the possibility to choose VPC solution that, in addition to having the size you want, allows you to have no overlapping. In fact, the range of IP addresses that are assigned to its networks is unique which allows you to reach external services and to be reached by external services. Moreover, we offer you the possibility to enable communication between several VPC companies but also to communicate with shared services such as VPN, all thanks to our transit gateway.  

#### Glossary

- AWS - Amazon Web Services

- VPC - Virtual Private Cloud - Virtual Data Center