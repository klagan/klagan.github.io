---
published: true
tags: azure
---
## `System.InvalidOperationException: 'Invalid control character in header: 0x0D'`


I was recently doing some work between an Azure secured web api and Azure secured web application.  When I ran the applications I was presented with the above message.

Just for future reference, this normally means that the client secret is either missing or incorrect.
