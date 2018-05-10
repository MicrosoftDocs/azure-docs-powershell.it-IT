---
title: Creare un'entità servizio di Azure con Azure PowerShell
description: Informazioni su come creare un'entità servizio per un'app o un servizio con Azure PowerShell.
keywords: Azure PowerShell, Azure Active Directory, Azure AD, AD, Controllo degli accessi in base al ruolo
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 6eda2d2a729331b212938aa2681d0188a25b734a
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/08/2018
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Creare un'entità servizio di Azure con Azure PowerShell

Se si prevede di gestire un'app o un servizio con Azure PowerShell, è consigliabile eseguire tale app o servizio in un'entità servizio di Azure Active Directory (AAD), anziché con le proprie credenziali. Questo argomento illustra come creare un'entità di sicurezza con Azure PowerShell.

> [!NOTE]
> È inoltre possibile creare un'entità servizio tramite il portale di Azure. Per informazioni dettagliate, vedere [Usare il portale per creare un'applicazione Active Directory e un'entità servizio che accedono alle risorse](/azure/azure-resource-manager/resource-group-create-service-principal-portal).

## <a name="what-is-a-service-principal"></a>Che cos'è un'"entità servizio"?

Un'entità servizio di Azure è un'identità di sicurezza usata da app, servizi e strumenti di automazione creati dall'utente per accedere a risorse di Azure specifiche. Può essere considerata come una "identità utente" (nome utente e password o certificato) con un ruolo specifico e autorizzazioni attentamente controllate. A differenza di un'identità utente generica, essa deve essere in grado di eseguire soltanto operazioni specifiche. Se le viene concesso solo il livello minimo di autorizzazioni necessarie per eseguire le attività di gestione, un'entità servizio migliora la sicurezza.

## <a name="verify-your-own-permission-level"></a>Verificare il proprio livello di autorizzazione

Innanzitutto, è necessario avere autorizzazioni sufficienti sia nell'istanza di Azure Active Directory che nella sottoscrizione di Azure. In particolare, è necessario poter creare un'app in Active Directory e assegnare un ruolo all'entità servizio.

Il modo più semplice per verificare se l'account dispone delle autorizzazioni appropriate è tramite il portale. Vedere l'articolo su come [controllare le autorizzazioni necessarie nel portale](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).

## <a name="create-a-service-principal-for-your-app"></a>Creare un'entità servizio per l'app

Dopo avere eseguito l'accesso all'account Azure, è possibile creare l'entità servizio. È necessario disporre di uno dei modi seguenti per identificare l'app distribuita:

* Nome univoco dell'app distribuita, ad esempio "MyDemoWebApp" negli esempi seguenti, oppure
* ID dell'applicazione, GUID univoco associato all'app, al servizio o all'oggetto distribuito

### <a name="get-information-about-your-application"></a>Ottenere informazioni sull'applicazione

Per individuare le informazioni sull'applicazione si può usare il cmdlet `Get-AzureRmADApplication`.

```powershell
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a>Creare un'entità servizio per l'applicazione

Per creare l'entità servizio si usa il cmdlet `New-AzureRmADServicePrincipal`.

```powershell
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $password
```

```
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a>Ottenere informazioni sull'entità servizio

```powershell
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a>Accedere con l'entità servizio

È ora possibile effettuare l'accesso come nuova entità servizio per l'app usando l'*appId* e la *password* specificati. È necessario fornire l'Id tenant per l'account. L'Id tenant viene visualizzato quando si accede ad Azure con le credenziali personali.

```powershell
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Login-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

Eseguire questo comando da una nuova sessione di PowerShell. Dopo aver eseguito correttamente l'accesso, verrà visualizzato un output simile al seguente:

```
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

Congratulazioni! È possibile usare queste credenziali per eseguire l'app. Sarà poi necessario modificare le autorizzazioni dell'entità servizio.

## <a name="managing-roles"></a>Gestione dei ruoli

> [!NOTE]
> Il controllo di accesso in base al ruolo di Azure (Role-Based Access Control - RBAC) è un modello per la definizione e gestione dei ruoli per le entità utente e servizio. I ruoli dispongono di set di autorizzazioni associate a essi, che determinano le risorse che un'entità può leggere scrivere o gestire e a cui può accedere. Per altre informazioni sui ruoli e sul controllo degli accessi in base al ruolo, vedere [Controllo degli accessi in base al ruoli: ruoli predefiniti](/azure/active-directory/role-based-access-built-in-roles).

Azure PowerShell fornisce i cmdlet seguenti per gestire le assegnazioni dei ruoli:

* [Get-AzureRmRoleAssignment](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [New-AzureRmRoleAssignment](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [Remove-AzureRmRoleAssignment](/powershell/module/azurerm.resources/remove-azurermroleassignment)

Il ruolo predefinito per un'entità servizio è quello **Collaboratore**. Potrebbe non essere la scelta migliore in base allo scope delle interazioni dell'app con i servizi di Azure, date le ampie autorizzazioni.
Il ruolo **Lettore** è più restrittivo e può essere una buona scelta per le app di sola lettura. È possibile visualizzare i dettagli delle autorizzazioni specifiche del ruolo o creare autorizzazioni personalizzate tramite il portale di Azure.

In questo esempio si aggiunge il ruolo**Lettore** all'esempio precedente e si elimina quello **Collaboratore**:

```powershell
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```powershell
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

Per visualizzare i ruoli correnti assegnati:

```powershell
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

Altri cmdlet di Azure PowerShell per la gestione dei ruoli:

* [Get-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleDefinition](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a>Modificare le credenziali dell'entità di sicurezza

È buona norma verificare le autorizzazioni e aggiornare le password a intervalli regolari. È anche consigliabile gestire e modificare le credenziali di sicurezza quando si modifica un'app. Ad esempio, si può modificare la password dell'entità servizio creando una nuova password ed eliminando la precedente.

### <a name="add-a-new-password-for-the-service-principal"></a>Aggiungere una nuova password per l'entità servizio

```powershell
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a>Ottenere un elenco di credenziali per l'entità servizio

```powershell
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a>Rimuovere la vecchia password dall'entità servizio

```powershell
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a>Verificare l'elenco di credenziali per l'entità servizio

```powershell
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```
