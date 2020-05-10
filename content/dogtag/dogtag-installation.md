Title: Dogtag - Installation (Interactive)
Date: 2016-07-01 18:00
Author: amolkahat
Category: Dogtag
Slug: dogtag-installation
Status: published

In previous blog i explained about **Dogtag certificate system** as an overview. Now lets install it your system. Dogtag certificate system is fully featured system which support multiple options of certificate enrollment and smart card enrollment. This certificate system require large no of dependency.

Now we look how to install it and how to build it.

For fedora 23 or later versions :

`$ sudo dnf install 389-ds-base dogtag-pki`{style="display:inline-block;background-color:lightgray;width:100%;"}

-   **389-ds-base:**
    -   389-ds-base is directory server which is used by directory server as a back end for Dogtag Certificate System. The certificate system is uses to store certificate request and certificate in the database.
    -   This is also known as Light Weight Directory Access Protocol (LDAP).
-   **dogtag-pki:**
    -   dogtag-pki is certificate system rpm files which installs the certificate system environment and dependency.
    -   This is include stable downstream version of dogtag-pki.
    -   This project maintained by Red Hat.

**Subsystem Installation:**

-   CA is Certificate Authority which is top of the system. The CA can be installed by two ways
    -   Using Interactive Installation
    -   Using Config File Installation.
-   Using Interactive installation:
    -   Using pkispawn you can install CA and other subsystem. Using pkispawn you can install config file installation too.
    -   pkispawn command will ask for some parameters.
        -   **Subsystem:** Specify subsystem which you want to install like CA, KRA, OCSP, TKS, TPS.
    -   Now specify Tomcat Parameters:
        1.  **Instance Name:** Specify Instance name of the subsystem.
        2.  **Instance Secure and Unsecure port:** Every subsystem will ask for two ports. One port is secure port and another is unsecure port. The secure port is used for administrator and unsecure port will be used by the users.
        3.  **AJP and Management port: **AJP and Management ports are used by tomcat instance.
    -   Administrator Section will prompt for this:
        1.  **Instance User Name: **Instance user name is require when we login to console for edit subsystem profile.
        2.  **Instance Password and Confirm Password: **Instance password which is used to login console to edit subsystem profiles.
        3.  **Certificate Import:** This option is ask for the certificate to import certificate of CA. If we installing standalone CA then we did not require this option, but for another subsystem this option is optional.
        4.  **Export Certificate: **It will store subsystem certificate either in **Client Directory** (If specified) or in **/root/.dogtag/Instance/** directory.
    -   Specify Directory server information:
        -   **Hostname: **Your machine name. By default it is localhost.localdomain. You can change it to server.example.org.
        -   **LDAPS Connection: **This option will ask for TLS enabled LDAP connection. If you choose secure connection then you have to specify CA certificate which used to crate TLS enabled LDAP.
        -   **LDAP and LDAPS port: **This option will ask for LDAP port. If you choose LDAPS connection then you have to specify LDAPS port too.
        -   **Password: **Password of Directory Server. It was specified at the installation time.
        -   **Base DN: **This is the directory server branch in which data of certificates is stored.
    -   Security Domain:
        -   **Name of Security Domain: **Security Domain name is a name of your website. For Ex: example.org Security Domain, google.com Security Domain, etc.
    -   Now Begin installation.
-   After successful installation it will show Admin details like Name, pkcs12 file, certificate database. Instance management commands, subsystem URL.

To install CA, KRA, OCSP, TKS, TPS all the procedure is same. If you are installing on same tomcat then it will not prompt for tomcat section.

There is little difference in the installation of TPS subsystem. In TPS you have to specify KRA, and TKS url with base dn i.e. dc=example,dc=org.
