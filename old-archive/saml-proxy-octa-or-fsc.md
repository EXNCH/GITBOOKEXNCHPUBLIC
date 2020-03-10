# SAML Proxy Octa \| FSC

## Prisma SaaS

Log in to Prisma SaaS.

Select --&gt; Settings --&gt; SAML Proxy, then toggle to enable Unmanaged Device Access Control Configuration.

![](../.gitbook/assets/screenshot-2020-03-09-at-11.21.32.png)

Select Identity Provider Settings Add Identity Provider.



**Now we first have to configure an Octa SAML.**

## Octa SAML

Login to Okta.

Select --&gt; Applications Add --&gt; Applications --&gt; Create New App.

Create the new app with a Web platform and SAML 2.0 sign-on method, then Create.

![](../.gitbook/assets/screenshot-2020-03-09-at-13.28.10.png)

![](../.gitbook/assets/screenshot-2020-03-09-at-13.29.12.png)

![](../.gitbook/assets/screenshot-2020-03-09-at-13.29.33.png)

Open Prisma SaaS in a Secondary Tab

Settings --&gt;  Unmanaged Device Access Control --&gt; SAML Proxy --&gt; Identity Provider Settings

![](../.gitbook/assets/screenshot-2020-03-09-at-13.33.58.png)

![](../.gitbook/assets/screenshot-2020-03-09-at-13.33.58%20%281%29.png)

press next

![](../.gitbook/assets/screenshot-2020-03-09-at-13.35.57.png)

Finish

![](../.gitbook/assets/screenshot-2020-03-09-at-13.37.46.png)

Record values for the following Okta IdP settings in your [planning worksheet](https://docs.paloaltonetworks.com/prisma/prisma-saas/prisma-saas-admin/secure-cloud-apps/add-unsanctioned-device-access-control-to-prisma-saas/configure-unsanctioned-device-access-control.html#id183K9A00O8P_idd5f41c16-2da9-4246-b141-b78af175e7a1), then Download the Okta certificate.

* Identity Provider Single Sign-On URL
* Identity Provider Issuer

![](../.gitbook/assets/screenshot-2020-03-09-at-13.40.45.png)

Rename the Okta X.509 certificate from CERT extension to either CER or CRT file extension.



![](../.gitbook/assets/screenshot-2020-03-09-at-13.41.15.png)

From the Prisma SaaS SAML app, select Assign Assign to to add and manage people or groups.

![](../.gitbook/assets/screenshot-2020-03-09-at-13.43.58.png)

1. Log in to Prisma SaaS, and selectSettingsSAML ProxyIdentity Provider SettingsAdd Identity Provider.
2. Enter your IdP’s name inIDP Name.
3. ClickChoose File and upload the Okta certificate that you downloaded earlier.
4. Specify values for the following Okta IdP settings, using your [planning worksheet](https://docs.paloaltonetworks.com/prisma/prisma-saas/prisma-saas-admin/secure-cloud-apps/add-unsanctioned-device-access-control-to-prisma-saas/configure-unsanctioned-device-access-control.html#id183K9A00O8P_idd5f41c16-2da9-4246-b141-b78af175e7a1), thenSave.
   * IDP Entity ID
   * SSO URL

![](../.gitbook/assets/screenshot-2020-03-09-at-13.47.08.png)

## Office 365 in Octa

Add Application

![](../.gitbook/assets/screenshot-2020-03-09-at-13.53.21.png)

