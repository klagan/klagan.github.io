---
published: true
tags: azure
---
I tried to delete an Azure AD directory but found I wasn't allowed due to certain checks failing.

One of those checks was a link to an **enterprise application**.

This is how I did it (assuming Azure AD module is installed in local Powershell by ```install-module azuread```

1. Switch into the Azure AD directory (Azure Active Directory -> Switch Directory)
2. Note the **directory id** in the directory properties
3. Note the **object id** in the enterprise application properties
4. Login ```connect-azuread -tenantid [directory id]```
5. Delete the enterprise application ```Remove-AzureADServicePrincipal -ObjectId [enterprise application object id]```

In summary, all I learnt was that it really shouldn't have been this difficult.
