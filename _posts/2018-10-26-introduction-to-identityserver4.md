---
published: true
tags: identityserver
---
I have read the documents and I know I am a bit thick, but the documents make me feel even thicker.

They seem neither complete or clear and further diving into the subject provides a lot of misinformation and obfuscation.

And I can tell you now.  Im not going to be able to change this, but I will attempt to bring you up to my level of understanding.

### What is IdentityServer? 
IdentityServer is an OpenConnectID and OAuth 2.0 framework that "enables" developers to build an authority delegation service.

It is indeed capable of a lot more things but we should start here.

### Why does it exist?
It exists to produce a security system that enables *authentication* (the identification of users) and *authorisation* (the permissions of users) using internet standards and best practices that protect user data with out having to understand and implement all the RFC's out there covering these topics.

Identity Providers (*IDP*) like Google, Microsoft and Apple store identification data and "claims" about a user.  Claims can be anything that the IDP *claims* is true about the user such as name, date of birth, subscription level, favourite colour etc.

IdentityServer allows developers to interact with IDP's be them third party or custom built ones.

Using standards and best practices, IdentityServer can orchestrate a means to identify a user and retrieve claims about the user backed by an IDP.  This information is used to access resources in applications.  

There are two types of resources:

* *Identity Resources*
 - Personal Identifiable Information (PII) like Name, DOB, Address
* *API Resources*
 - Read Access to accounts
 - Write Access to Google Drive

Applications can request a user to identify themselves and grant consent to using protected resources on the users behalf without ever handling the authentication request.  This is all done with requests, redirects endpoints and tokens

One thing to note is that this all started with OAuth 2.0 which - unsurprisingly - improved upon OAuth 1.0.  But now there is OpenID Connect which again improves but also extends on OAuth 2.0 and is considered the latest and greatest in internet authentication and authorisation.

### Summary
Of course, this is an over simplification of IdentityServer and what it can do but I hope of the next few posts I can explain how it works and how to implement it.
