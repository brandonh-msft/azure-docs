---
title: Identity data storage for European customers - Azure Active Directory | Microsoft Docs
description: Learn about where Azure Active Directory stores identity-related data for its European customers.
services: active-directory
author: msaburnley
manager: daveba
ms.author: ajburnle

ms.service: active-directory
ms.subservice: fundamentals
ms.workload: identity
ms.topic: conceptual
ms.date: 03/04/2019
ms.custom: "it-pro, seodec18"
ms.collection: M365-identity-device-management
---

# Identity data storage for European customers in Azure Active Directory
Identity data is stored by Azure AD in a geographical location  based on the address provided by your organization when subscribing for a Microsoft Online service such as  Office 365 and Azure. For information on where your identity data is stored, you can use the [Where is your data located?](https://www.microsoft.com/trustcenter/privacy/where-your-data-is-located) section of the Microsoft Trust Center.

For customers who provided an address in Europe, Azure AD keeps most of the identity data within European datacenters. This document provides information on any data that is stored outside of Europe by Azure AD services.

## Microsoft Azure multi-factor authentication (MFA)
    
- All two-factor authentication using phone calls or SMS originate from US datacenters and are also routed by global providers.
- Push notifications using the Microsoft Authenticator app originate from US datacenters. In addition, device vendor specific services may also come into play and these services maybe outside Europe.
- OATH codes are always validated in the U.S. 

## Microsoft Azure Active Directory B2C (Azure AD B2C)

Azure AD B2C policy configuration data and Key Containers are stored in U.S. datacenters. These do not contain any user personal data. For more info about policy configurations, see the [Azure Active Directory B2C: Built-in policies](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-reference-policies) article.

## Microsoft Azure Active Directory B2B (Azure AD B2B) 
    
Azure AD B2B stores invitations with redeem link and redirect URL information in US datacenters. In addition, email address of users that unsubscribe from receiving B2B invitations are  also stored in U.S. datacenters.

## Microsoft Azure Active Directory Domain Services (Azure AD DS)

Azure AD DS stores user data in the same location as the customer-selected Azure Virtual Network. So, if the network is outside Europe, the data is replicated and stored outside Europe.

## Other considerations

Services and applications that integrate with Azure AD have access to identity data. Evaluate each service and application you use to determine how identity data is processed by that specific service and application, and whether they meet your company's data storage requirements.

For more information about Microsoft services' data residency, see the [Where is your data located?](https://www.microsoft.com/trustcenter/privacy/where-your-data-is-located) section of the Microsoft Trust Center.

## Next steps
For more information about any of the features and functionality described above, see these articles:
- [What is Multi-Factor Authentication?](https://docs.microsoft.com/azure/active-directory/authentication/multi-factor-authentication)

- [Azure AD self-service password reset](https://docs.microsoft.com/azure/active-directory/authentication/active-directory-passwords-overview)

- [What is Azure Active Directory B2C?](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview)

- [What is Azure AD B2B collaboration?](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b)

- [Azure Active Directory (AD) Domain Services](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-overview)
