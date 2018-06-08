# Xero Connector #

## Configuration ##

To establish connection between Xero Connector and Xero site please configure Xero API application for site by following instructions in *Configuring Xero Application* section. Review *SSL Certificate* section for more details on certificate used by Xero API. Once Xero API configuration is complete, take a note of **Consumer Key** supplied as it will be required to complete configuration in Xero Connector.

During next stage of installation SSL certificate, together with default values would be configured in Xero Connector.

## Configuring Xero Application ##

Open http://developer.xero.com and click on **My Applications** tab. Click on **Add Application** button.

Select **Private** application option, select your Xero company, choose **Upload X509 certificate file (.cer)** and click on **Choose File** button.

Select the certificate (refer to *SSL Certificate* section) and click on **Save** button. Once uploaded, please take a note of the details provided, in particular record the **Consumer Key**.

## Linking Xero Connector to Xero Site ##

In Xero Connector, for each company tab click on **Settings …** button in the bottom left corner and configure the properties required.

In the **General** tab use the **Company** drop down to select particular company. The **Invoice Status** and **Invoice Type** fields are set to **AUTHORISED** and **ACCREC** values by default. Unless instructed otherwise or invoices feature is not used, please leave the default values as they are required by Xero site.

In API tab specify **Consumer Key** obtained earlier in *Configuring Xero Application* section and password supplied for certificate. The default value of **Request Delay in Milliseconds** is **1000**. This is a recommended value which controls the integration between Xero Connector and Xero site. Unless instructed otherwise please leave the default value. Once **Consumer Key** and certificate password are specified you can click on **Test Connection** button to establish connection with Xero site.

## SSL Certificate ##

SSL certificate is required to ensure the connection between Xero Connector and Xero site is secure. Please provide the certificate, password and expiry date to complete Xero Connector configuration. 

If no certificate is explicitly provided, X509 certificate can be generated using OpenSSL application for Xero Connector application.

Following data is used during certificate generation:

1. Company Name
1. Country

*If certificate was generated, all files and password would be provided on completion of installation.*

## SSL/TLS Support ##

Xero Connector supports following security protocols:

* SSL 3.0
* TLS 1.0
* TLS 1.1
* TLS 1.2

*The application automatically negotiates the highest supported protocol with Xero site whilst establishing the initial connection. No additional configuration is required if the protocol is changed or discontinued (as long as new protocol is in the list above) by Xero site.*

## FAQ ##

**When Xero sites updates minimum required SSL/TLS protocol, do we need to install new version of Xero Connector?**

*A: If there are still protocols available that are supported by both Xero site and Xero Connector, no new installation of Xero Connector is required. Restart Xero Connector application to force automatic negotiation of another SSL/TLS protocol.*

**How do I find the expiration date of SSL certificate?**

*A: If the ceritificate was provided, please contact your IT support. If certificate was generated, please contact us for more information. We monitor the expiration dates and can arrange new certificate installation with your IT department.*

**If Xero site discontinued specific SSL/TLS protocol, do we require new SSL certificate?**

*A: No, the same SSL certificate can be used after the change.*

**If Xero site discontinued the support for TLS 1.0, would the users of Xero Connector be affected?**

*A: The users would not be affected, if both Xero site and Xero Connector support other common protocols, like TLS 1.1, TLS 1.2, etc.

## Terms ##

*Terms "**Xero**", "**Xero site**" and "**Xero API**" refer to the property and trademark of www.xero.com*.

*Term "**OpenSSL**" refers to the application licensed under Apache-style license: https://www.openssl.org/*.

