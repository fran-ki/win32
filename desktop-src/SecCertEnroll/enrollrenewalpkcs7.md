---
Description: Creates a PKCS \#7 request object to renew an existing certificate. The request object uses a new key pair but retains the cryptographic provider associated with the certificate being renewed.
ms.assetid: 12a3f1b4-b31e-470e-8ce6-87f497841240
title: enrollRenewalPKCS7
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# enrollRenewalPKCS7

The enrollRenewalPKCS7 sample creates a PKCS \#7 request object to renew an existing certificate. The request object uses a new key pair but retains the cryptographic provider associated with the certificate being renewed.

## Location

When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollRenewalPKCS7 folder.

## Discussion

The enrollRenewalPKCS7 sample:

1.  Processes the command line arguments. The command line should contain the name of the template used to create the certificate request.
2.  Retrieves an existing certificate by using the name of the template specified on the command line or, if a certificate cannot be found, attempts to enroll one by using the template. The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.
3.  Verifies the certificate chain and converts the certificate to a **BSTR**.
4.  Creates an [**IX509CertificateRequestPkcs7**](/windows/win32/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7?branch=master) object and initializes it by using the existing certificate. Because the *inheritOptions* parameter is set to InheritDefault, a new key pair is created for the request but the cryptographic provider in the existing certificate is used. For more information, see the [**InitializeFromCertificate**](/windows/win32/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate?branch=master) method.
5.  Creates an [**IX509Enrollment**](/windows/win32/CertEnroll/nn-certenroll-ix509enrollment?branch=master) object, initializes it by using the PKCS \#7 request object, attempts to enroll it with the CA and monitors the status of the enrollment process. The checkEnrollStatus function is defined in enrollCommon.cpp.

## Related topics

<dl> <dt>

[CMC Request](cmc-request.md)
</dt> <dt>

[PKCS \#7 Renewal Request](pkcs--7--renewal-request.md)
</dt> <dt>

[Using the Included Samples](using-the-included-samples.md)
</dt> </dl>

 

 


