---
description: >-
  Prisma SaaS is your SAML IdP, not Okta. When you add the SAML IdP on the
  firewall, you need to use the Prisma SaaS SAML Proxy values.
---

# SAML Proxy PAN Firewall \| FSC

## Import and export the cert

Login to Prisma SaaS --&gt; Settings --&gt; Unmanaged Device Access Control --&gt; SAML Proxy --&gt; Identity Provider Configuration

Download the Idenity Provider Certificate.

![](../.gitbook/assets/screenshot-2020-03-09-at-14.14.25.png)

Log in to NGFW.

Import the Prisma SaaS certificate prisma\_saas.cer .

![](../.gitbook/assets/image.png)

## Config SAML Idenitity Provider

Create the SAML **Identity Provider Server Profile** .

* Link to the Prisma SaaS certificate you imported.
* Settings according to the Screenshot

![](../.gitbook/assets/screenshot-2020-03-09-at-14.19.16.png)

## Create the Authentication Profile

Specify the SAML Identity Provider Server Profile that you created

![](../.gitbook/assets/screenshot-2020-03-09-at-14.24.50.png)

Locate the SAML Identity Provider Server Profile that you created.

Click on the Metadata link to download and open the file.

Locate and record the Entity ID one the line that begins entityID= .

![](../.gitbook/assets/screenshot-2020-03-09-at-14.25.40.png)

![](../.gitbook/assets/screenshot-2020-03-09-at-14.27.29.png)

Create the Client Authentication , specifying the SAML Identity Provider Server Profile

![](../.gitbook/assets/screenshot-2020-03-09-at-14.29.25.png)

![](../.gitbook/assets/screenshot-2020-03-09-at-14.29.35.png)

## Configure Gateway Settings on Prisma SaaS

Log in to Prisma SaaS.

Select Settings SAML Proxy Gateway Settings Edit.

![](../.gitbook/assets/screenshot-2020-03-09-at-14.32.13.png)



