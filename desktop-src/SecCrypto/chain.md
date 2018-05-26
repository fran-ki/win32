---
Description: Represents a certificate trust chain.
ms.assetid: fea72a3e-5a22-47c7-8f6e-0d76fc3339f8
title: Chain object
ms.date: 05/31/2018
ms.topic: interface
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Chain object

\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP. Instead, use the [**X509Chain Class**](T:System.Security.Cryptography.X509Certificates.X509Chain) in the [**System.Security.Cryptography.X509Certificates**](frlrfSystemSecurityCryptographyX509Certificates) namespace.\]

The **Chain** object represents a certificate trust chain.

This object provides properties and methods to build a certificate trust chain to check the validity of certificates. The chain is built using the [**CertificateStatus.CheckFlag**](certificatestatus-checkflag.md) property value and the policy settings of a [**CertificateStatus**](certificatestatus.md) object.

The **Chain** object exposes the following interfaces:

-   **IChain2**: Introduced in CAPICOM 2.0.
-   **IChain**: Introduced in CAPICOM 1.0.

## When to use

The **Chain** object is used to perform the following tasks:

-   Build a certificate trust chain.
-   Obtain the OIDs of all the certificate and application policies valid for the chain.
-   Verify the status of the certificates in the chain.
-   Obtain extended error information.
-   Retrieve the collection of certificates in the chain.

## Members

The **Chain** object has these types of members:

-   [Methods](#methods)
-   [Properties](#properties)

### Methods

The **Chain** object has these methods.



| Method                                                   | Description                                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplicationPolicies**](chain-applicationpolicies.md) | Returns an [**OIDs**](oids.md) collection that represents the application policy OIDs valid for the chain.<br/> (Inherited from **ChainIChain2**)                                                                                                                                                          |
| [**Build**](chain-build.md)                             | Builds a certificate verification chain from an end certificate to the trusted [*root certificate*](security.r_gly#-security-root-certificate-gly), returning a Boolean value that indicates the overall validity of the chain.<br/> (Inherited from **ChainIChain2IChain**) |
| [**CertificatePolicies**](chain-certificatepolicies.md) | Returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs valid for the chain.<br/> (Inherited from **ChainIChain2**)                                                                                                                                                          |
| [**ExtendedErrorInfo**](chain-extendederrorinfo.md)     | Returns a string that contains additional error information about the indexed entry.<br/> (Inherited from **ChainIChain2**)                                                                                                                                                                                 |



 

### Properties

The **Chain** object has these properties.



| Property                                              | Access type          | Description                                                                                                                                                                                 |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificates**](chain-certificates.md)<br/> | Read-only<br/> | Retrieves a [**Certificates**](certificates.md) collection that represents the certificates in the chain. This is the default property.<br/> (Inherited from **ChainIChain2IChain**) |
| [**Status**](chain-status.md)<br/>             | Read-only<br/> | Retrieves the validity status of the chain or a specific certificate in the chain.<br/> (Inherited from **ChainIChain2IChain**)                                                       |



 

## Remarks

The **Chain** object can be created, and it is safe for scripting. The ProgID for the **Chain** object is "CAPICOM.Chain.2".

**CAPICOM 1.*x*:** The ProgID for the **Chain** object is CAPICOM.Chain.1.

## Requirements



|                                  |                                                                                        |
|----------------------------------|----------------------------------------------------------------------------------------|
| End of client support<br/> | Windows Vista<br/>                                                               |
| End of server support<br/> | Windows Server 2008<br/>                                                         |
| Redistributable<br/>       | CAPICOM 2.0 or later on Windows Server 2003 and Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## See also

<dl> <dt>

[**Cryptography Objects**](cryptography-objects.md)
</dt> </dl>

 

 



