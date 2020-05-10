Title: Dogtag
Date: 2016-06-28 14:22
Author: amolkahat
Category: Dogtag
Slug: dogtag
Status: published

**Dogtag certificate system** is an open source **Certificate Authority (CA)**. Which is full featured system. It support all aspects of certificate life cycle management. It include Certificate Authority, Key archival, OCSP and smart card management.

Dogtag Certificate System has 5 main components:

-   Certificate Authority (CA)
-   Key Revocation Authority (KRA)
-   Online Certificate Status Protocol (OCSP)
-   Token Key Service (TKS)
-   Token Processing Service (TPS)

**Certificate Authority :**

CA is one who has rights to issue certificates, revoke and renew it. CA is on the top of the certificate system.  CA has the two main components<!--more-->

1.  End User Services
2.  Agent Services

-   **End User Services:**

End User Services include different certificate profiles, which is used to enroll different types of certificates. Users can enroll their certificates using this profiles. Users get these certificate signed by CA.

Certificate Enrollment process creates one certificate request and submit it to the CA. After the approval of certificate request by CA Agents user get signed certificate by CA. This will generate certificate chain to identify the flow of CA to user.

\[caption id="attachment\_509" align="alignnone" width="797"\]![Flow of CA](https://akahat.files.wordpress.com/2016/06/ca-1.png){.alignnone .size-full .wp-image-509 width="797" height="447"} Flow of CA\[/caption\]

Suppose CA is standalone and it issues certificate to user 1 then it generate certificate chain as CA and user. But if CA has sub CA then it generate certificate chain as CA, sub CA and user1.

-   **Agent Services:**

 

Agent Services are support services such as approval, revocation, renewal of certificates. Agents Services include list and approval of request, list of approved certificates, revoke certificate, display certificate revocation list, manage certificate profiles, etc.

When user submits the request using End User Services or from End Entity page these request are approved by Agents. Agent Services can be accessed by only and only admin certificate.

**Key Recovery Authority:**

Key Recovery Authority is an optional subsystem that is configured to archive private keys. KRA subsystem is by default installed after CA subsystem is installed and is dependent on CA for certain operations but can be installed as standalone subsystem too.

**Online Certification Status Protocol:**

Online Certificate Status Manager is an subsystem external to CA. This subsystem acts as an external OCSP which can be publicly accessible. Multiple CA's can publish CRL to a single OCSP. Clients can verify certs using OCSP.

**Token Key Service:**

The token key services manges to the master and transport keys required to generate and distribute keys for smart cards or tokens. A master key is a Triple Digital Encryption Standard (DES) symmetric key stored either in software or hardware token.

**Token Processing System:**

TPS interacts with smart card to help them generate and store keys and certificate for a specific entity.

Smart card operations go through TPS and are forwarded to the appropriate subsystem for action, such as the Certificate Authority to generate certificate or the Key Recovery Authority to archive and recover key.

TPS has some best features that :

-   It uses secure channel to interact with smart cards, based on the keys derived by TKS.
-   TPS uses developer keys sets to initially setup Secure channel.
-   In the case smart card wants to upgrade keys. A new set of keys created by TKS are used to setup Secure Channel.

This Dogtag Certificate system is owned by Red Hat at 2004 by AOL. Red Hat open sourced it in 2008.

**There is also an Enterprise level version of Dogtag known as the Red Hat Certificate System.**

Dogtag has very complex installation and lots of dependency .  I'm working on this project since last 5 months and i have some patches in this project. This is my first open source contribution.

I have also fixed some bugs in the project. Those bugs were CLI bugs. But this project is very complex as per my opinion. <!--more-->
