---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 5f47237088808fe8966d239f9a0de7c892301db0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410719"
---
# <span data-ttu-id="d39a7-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d39a7-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="d39a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d39a7-102">SYNOPSIS</span></span>
<span data-ttu-id="d39a7-103">Concede o modifica le autorizzazioni esistenti per un utente, un'applicazione o un gruppo di sicurezza per eseguire operazioni con un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="d39a7-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="d39a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d39a7-104">SYNTAX</span></span>

### <span data-ttu-id="d39a7-105">ByUserPrincipalName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d39a7-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d39a7-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="d39a7-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d39a7-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d39a7-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d39a7-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d39a7-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d39a7-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="d39a7-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d39a7-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="d39a7-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d39a7-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d39a7-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d39a7-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d39a7-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d39a7-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d39a7-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d39a7-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="d39a7-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d39a7-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="d39a7-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d39a7-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d39a7-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d39a7-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d39a7-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d39a7-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d39a7-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d39a7-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="d39a7-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d39a7-120">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d39a7-120">DESCRIPTION</span></span>
<span data-ttu-id="d39a7-121">Il cmdlet **Set-AzKeyVaultAccessPolicy** concede o modifica le autorizzazioni esistenti per un utente, un'applicazione o un gruppo di sicurezza per eseguire le operazioni specificate con un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="d39a7-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="d39a7-122">Non modifica le autorizzazioni di altri utenti, applicazioni o gruppi di sicurezza nel vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="d39a7-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="d39a7-123">Se si impostano le autorizzazioni per un gruppo di sicurezza, questa operazione interessa solo gli utenti di tale gruppo.</span><span class="sxs-lookup"><span data-stu-id="d39a7-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="d39a7-124">Le directory seguenti devono essere tutte della stessa directory di Azure:</span><span class="sxs-lookup"><span data-stu-id="d39a7-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="d39a7-125">Directory predefinita della sottoscrizione di Azure in cui si trova il vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="d39a7-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="d39a7-126">La directory di Azure che contiene l'utente o il gruppo di applicazioni a cui si concedono le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="d39a7-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="d39a7-127">Esempi di scenari in cui queste condizioni non sono soddisfatte e questo cmdlet non funziona sono:</span><span class="sxs-lookup"><span data-stu-id="d39a7-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="d39a7-128">Autorizzazione di un utente di un'altra organizzazione per la gestione del vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="d39a7-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="d39a7-129">Ogni organizzazione ha una propria directory.</span><span class="sxs-lookup"><span data-stu-id="d39a7-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="d39a7-130">L'account azure ha più directory.</span><span class="sxs-lookup"><span data-stu-id="d39a7-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="d39a7-131">Se si registra un'applicazione in una directory diversa da quella predefinita, non è possibile autorizzare l'applicazione all'uso del vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="d39a7-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="d39a7-132">L'applicazione deve essere nella directory predefinita.</span><span class="sxs-lookup"><span data-stu-id="d39a7-132">The application must be in the default directory.</span></span>
<span data-ttu-id="d39a7-133">Anche se è facoltativo specificare il gruppo di risorse per questo cmdlet, è consigliabile farlo per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="d39a7-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

> [!NOTE]
> <span data-ttu-id="d39a7-134">Quando si usa un'entità servizio per concedere le autorizzazioni per i criteri di accesso, è necessario usare il `-BypassObjectIdValidation` parametro.</span><span class="sxs-lookup"><span data-stu-id="d39a7-134">When using a service principal to grant access policy permissions, you must use the `-BypassObjectIdValidation` parameter.</span></span>

## <span data-ttu-id="d39a7-135">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d39a7-135">EXAMPLES</span></span>

### <span data-ttu-id="d39a7-136">Esempio 1: Concedere a un utente le autorizzazioni per un vault chiave e modificare le autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="d39a7-136">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :
```

<span data-ttu-id="d39a7-137">Il primo comando concede a un utente di Azure Active Directory le autorizzazioni per eseguire operazioni su chiavi e segreti con un vault delle chiavi denominato PattiFuller@contoso.com Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="d39a7-137">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="d39a7-138">Il *parametro PassThru* restituisce l'oggetto aggiornato restituito dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d39a7-138">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="d39a7-139">Il secondo comando modifica le autorizzazioni concesse nel primo comando per consentire ora di ottenere informazioni segrete oltre a impostarle PattiFuller@contoso.com ed eliminarle.</span><span class="sxs-lookup"><span data-stu-id="d39a7-139">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="d39a7-140">Le autorizzazioni per le operazioni chiave rimangono invariate dopo questo comando.</span><span class="sxs-lookup"><span data-stu-id="d39a7-140">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="d39a7-141">Il comando finale modifica ulteriormente le autorizzazioni esistenti per PattiFuller@contoso.com rimuovere tutte le autorizzazioni per le operazioni chiave.</span><span class="sxs-lookup"><span data-stu-id="d39a7-141">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="d39a7-142">Le autorizzazioni per le operazioni segrete rimangono invariate dopo questo comando.</span><span class="sxs-lookup"><span data-stu-id="d39a7-142">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="d39a7-143">Esempio 2: Concedere a un'entità servizio applicazioni le autorizzazioni per leggere e scrivere segreti</span><span class="sxs-lookup"><span data-stu-id="d39a7-143">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="d39a7-144">Questo comando concede le autorizzazioni per un'applicazione per una chiave vault denominata Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="d39a7-144">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="d39a7-145">Il *parametro ServicePrincipalName* specifica l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d39a7-145">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="d39a7-146">L'applicazione deve essere registrata in Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d39a7-146">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="d39a7-147">Il valore del parametro *ServicePrincipalName* deve essere il nome dell'entità servizio dell'applicazione o il GUID dell'ID applicazione.</span><span class="sxs-lookup"><span data-stu-id="d39a7-147">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="d39a7-148">Questo esempio specifica il nome dell'entità servizio e il comando concede all'applicazione le autorizzazioni `http://payroll.contoso.com` per leggere e scrivere segreti.</span><span class="sxs-lookup"><span data-stu-id="d39a7-148">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="d39a7-149">Esempio 3: Concedere le autorizzazioni per un'applicazione usando l'ID oggetto</span><span class="sxs-lookup"><span data-stu-id="d39a7-149">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="d39a7-150">Questo comando concede all'applicazione le autorizzazioni per leggere e scrivere segreti.</span><span class="sxs-lookup"><span data-stu-id="d39a7-150">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="d39a7-151">Questo esempio specifica l'applicazione usando l'ID oggetto dell'entità servizio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d39a7-151">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="d39a7-152">Esempio 4: Concedere le autorizzazioni per un nome dell'entità utente</span><span class="sxs-lookup"><span data-stu-id="d39a7-152">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="d39a7-153">Questo comando consente di ottenere, elencare e impostare le autorizzazioni per il nome dell'entità utente specificata per l'accesso ai segreti.</span><span class="sxs-lookup"><span data-stu-id="d39a7-153">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="d39a7-154">Esempio 5: Consentire il recupero di informazioni segrete da un vault delle chiavi da parte del provider di risorse Microsoft.Compute</span><span class="sxs-lookup"><span data-stu-id="d39a7-154">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="d39a7-155">Questo comando concede le autorizzazioni per il recupero di informazioni segrete dal vault della chiave Contoso03Vault da parte del provider di risorse Microsoft.Compute.</span><span class="sxs-lookup"><span data-stu-id="d39a7-155">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="d39a7-156">Esempio 6: Concedere autorizzazioni a un gruppo di sicurezza</span><span class="sxs-lookup"><span data-stu-id="d39a7-156">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="d39a7-157">Il primo comando usa il cmdlet Get-AzADGroup per ottenere tutti i gruppi di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d39a7-157">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="d39a7-158">Dall'output vengono restituiti 3 gruppi denominati **gruppo1,** **gruppo2** e **gruppo3.**</span><span class="sxs-lookup"><span data-stu-id="d39a7-158">From the output, you see 3 groups returned, named **group1**, **group2**, and **group3**.</span></span> <span data-ttu-id="d39a7-159">Più gruppi possono avere lo stesso nome, ma hanno sempre un Id Oggetto univoco.</span><span class="sxs-lookup"><span data-stu-id="d39a7-159">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="d39a7-160">Quando vengono restituiti più gruppi con lo stesso nome, usare ObjectId nell'output per identificare quello che si vuole usare.</span><span class="sxs-lookup"><span data-stu-id="d39a7-160">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="d39a7-161">Usare quindi l'output di questo comando con Set-AzKeyVaultAccessPolicy per concedere le autorizzazioni a gruppo2 per il vault della chiave, **denominato myownvault.**</span><span class="sxs-lookup"><span data-stu-id="d39a7-161">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="d39a7-162">Questo esempio enumera i gruppi denominati "gruppo2" in linea nella stessa riga di comando.</span><span class="sxs-lookup"><span data-stu-id="d39a7-162">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="d39a7-163">Nell'elenco restituito potrebbero essere presenti più gruppi denominati "gruppo2".</span><span class="sxs-lookup"><span data-stu-id="d39a7-163">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="d39a7-164">Questo esempio seleziona il primo, indicato dall'indice \[ 0 \] nell'elenco restituito.</span><span class="sxs-lookup"><span data-stu-id="d39a7-164">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="d39a7-165">Esempio 7: Concedere ad Azure Information Protection l'accesso alla chiave del tenant gestita dal cliente (BYOK)</span><span class="sxs-lookup"><span data-stu-id="d39a7-165">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="d39a7-166">Questo comando autorizza Azure Information Protection a usare una chiave gestita dal cliente (lo scenario bring your own key, o "BYOK") come chiave tenant di Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="d39a7-166">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="d39a7-167">Quando si esegue questo comando, specificare il nome del vault della chiave, ma è necessario specificare il parametro *ServicePrincipalName* con il GUID **00000012-0000-0000-c000-000000000000 e** specificare le autorizzazioni nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="d39a7-167">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="d39a7-168">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d39a7-168">PARAMETERS</span></span>

### <span data-ttu-id="d39a7-169">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d39a7-169">-ApplicationId</span></span>
<span data-ttu-id="d39a7-170">Per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="d39a7-170">For future use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39a7-171">-BypassObjectIdValid</span><span class="sxs-lookup"><span data-stu-id="d39a7-171">-BypassObjectIdValidation</span></span>
<span data-ttu-id="d39a7-172">Consente di specificare un ID oggetto senza convalidare l'esistenza dell'oggetto in Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d39a7-172">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="d39a7-173">Usare questo parametro solo se si vuole concedere l'accesso al vault della chiave a un ID oggetto che fa riferimento a un gruppo di sicurezza delegato di un altro tenant di Azure.</span><span class="sxs-lookup"><span data-stu-id="d39a7-173">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39a7-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d39a7-174">-DefaultProfile</span></span>
<span data-ttu-id="d39a7-175">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="d39a7-175">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39a7-176">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="d39a7-176">-EmailAddress</span></span>
<span data-ttu-id="d39a7-177">Specifica l'indirizzo di posta elettronica dell'utente a cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="d39a7-177">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="d39a7-178">Questo indirizzo e-mail deve essere presente nella directory associata all'abbonamento corrente ed essere univoco.</span><span class="sxs-lookup"><span data-stu-id="d39a7-178">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress, ResourceIdByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39a7-179">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="d39a7-179">-EnabledForDeployment</span></span>
<span data-ttu-id="d39a7-180">Consente al provider di risorse Microsoft.Compute di recuperare i dati nascosti da questo vault della chiave quando si fa riferimento a questo vault chiave nella creazione di risorse, ad esempio durante la creazione di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d39a7-180">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39a7-181">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="d39a7-181">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="d39a7-182">Consente al servizio di crittografia del disco di Azure di ottenere informazioni segrete e chiavi di annullamento della sincronizzazione da questo vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="d39a7-182">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39a7-183">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="d39a7-183">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="d39a7-184">Consente a Gestione risorse di Azure di ottenere informazioni segrete da questo vault chiave quando si fa riferimento a questo vault chiave in una distribuzione di modelli.</span><span class="sxs-lookup"><span data-stu-id="d39a7-184">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39a7-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d39a7-185">-InputObject</span></span>
<span data-ttu-id="d39a7-186">Oggetto Vault chiave</span><span class="sxs-lookup"><span data-stu-id="d39a7-186">Key Vault Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d39a7-187">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d39a7-187">-ObjectId</span></span>
<span data-ttu-id="d39a7-188">Specifica l'ID oggetto dell'utente o dell'entità servizio in Azure Active Directory per cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="d39a7-188">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39a7-189">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d39a7-189">-PassThru</span></span>
<span data-ttu-id="d39a7-190">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="d39a7-190">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d39a7-191">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="d39a7-191">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39a7-192">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="d39a7-192">-PermissionsToCertificates</span></span>
<span data-ttu-id="d39a7-193">Specifica una matrice di autorizzazioni per i certificati da concedere a un utente o a un'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="d39a7-193">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="d39a7-194">Valori accettabili per questo parametro:</span><span class="sxs-lookup"><span data-stu-id="d39a7-194">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="d39a7-195">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d39a7-195">Get</span></span>
- <span data-ttu-id="d39a7-196">Elenco</span><span class="sxs-lookup"><span data-stu-id="d39a7-196">List</span></span>
- <span data-ttu-id="d39a7-197">Elimina</span><span class="sxs-lookup"><span data-stu-id="d39a7-197">Delete</span></span>
- <span data-ttu-id="d39a7-198">Crea</span><span class="sxs-lookup"><span data-stu-id="d39a7-198">Create</span></span>
- <span data-ttu-id="d39a7-199">Importare</span><span class="sxs-lookup"><span data-stu-id="d39a7-199">Import</span></span>
- <span data-ttu-id="d39a7-200">Aggiorna</span><span class="sxs-lookup"><span data-stu-id="d39a7-200">Update</span></span>
- <span data-ttu-id="d39a7-201">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="d39a7-201">Managecontacts</span></span>
- <span data-ttu-id="d39a7-202">Getissuers</span><span class="sxs-lookup"><span data-stu-id="d39a7-202">Getissuers</span></span>
- <span data-ttu-id="d39a7-203">Listissuers</span><span class="sxs-lookup"><span data-stu-id="d39a7-203">Listissuers</span></span>
- <span data-ttu-id="d39a7-204">Setissuers</span><span class="sxs-lookup"><span data-stu-id="d39a7-204">Setissuers</span></span>
- <span data-ttu-id="d39a7-205">Eliminaissuers</span><span class="sxs-lookup"><span data-stu-id="d39a7-205">Deleteissuers</span></span>
- <span data-ttu-id="d39a7-206">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="d39a7-206">Manageissuers</span></span>
- <span data-ttu-id="d39a7-207">Recupera</span><span class="sxs-lookup"><span data-stu-id="d39a7-207">Recover</span></span>
- <span data-ttu-id="d39a7-208">Backup</span><span class="sxs-lookup"><span data-stu-id="d39a7-208">Backup</span></span>
- <span data-ttu-id="d39a7-209">Ripristina</span><span class="sxs-lookup"><span data-stu-id="d39a7-209">Restore</span></span>
- <span data-ttu-id="d39a7-210">Ripulire</span><span class="sxs-lookup"><span data-stu-id="d39a7-210">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39a7-211">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="d39a7-211">-PermissionsToKeys</span></span>
<span data-ttu-id="d39a7-212">Specifica una matrice di autorizzazioni per le operazioni chiave da concedere a un utente o a un'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="d39a7-212">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="d39a7-213">Valori accettabili per questo parametro:</span><span class="sxs-lookup"><span data-stu-id="d39a7-213">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="d39a7-214">Decrittografa</span><span class="sxs-lookup"><span data-stu-id="d39a7-214">Decrypt</span></span>
- <span data-ttu-id="d39a7-215">Crittografa</span><span class="sxs-lookup"><span data-stu-id="d39a7-215">Encrypt</span></span>
- <span data-ttu-id="d39a7-216">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="d39a7-216">UnwrapKey</span></span>
- <span data-ttu-id="d39a7-217">WrapKey</span><span class="sxs-lookup"><span data-stu-id="d39a7-217">WrapKey</span></span>
- <span data-ttu-id="d39a7-218">Verifica</span><span class="sxs-lookup"><span data-stu-id="d39a7-218">Verify</span></span>
- <span data-ttu-id="d39a7-219">Firma</span><span class="sxs-lookup"><span data-stu-id="d39a7-219">Sign</span></span>
- <span data-ttu-id="d39a7-220">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d39a7-220">Get</span></span>
- <span data-ttu-id="d39a7-221">Elenco</span><span class="sxs-lookup"><span data-stu-id="d39a7-221">List</span></span>
- <span data-ttu-id="d39a7-222">Aggiorna</span><span class="sxs-lookup"><span data-stu-id="d39a7-222">Update</span></span>
- <span data-ttu-id="d39a7-223">Crea</span><span class="sxs-lookup"><span data-stu-id="d39a7-223">Create</span></span>
- <span data-ttu-id="d39a7-224">Importare</span><span class="sxs-lookup"><span data-stu-id="d39a7-224">Import</span></span>
- <span data-ttu-id="d39a7-225">Elimina</span><span class="sxs-lookup"><span data-stu-id="d39a7-225">Delete</span></span>
- <span data-ttu-id="d39a7-226">Backup</span><span class="sxs-lookup"><span data-stu-id="d39a7-226">Backup</span></span>
- <span data-ttu-id="d39a7-227">Ripristina</span><span class="sxs-lookup"><span data-stu-id="d39a7-227">Restore</span></span>
- <span data-ttu-id="d39a7-228">Recupera</span><span class="sxs-lookup"><span data-stu-id="d39a7-228">Recover</span></span>
- <span data-ttu-id="d39a7-229">Ripulire</span><span class="sxs-lookup"><span data-stu-id="d39a7-229">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39a7-230">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="d39a7-230">-PermissionsToSecrets</span></span>
<span data-ttu-id="d39a7-231">Specifica una matrice di autorizzazioni per le operazioni segrete da concedere a un utente o a un'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="d39a7-231">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="d39a7-232">Valori accettabili per questo parametro:</span><span class="sxs-lookup"><span data-stu-id="d39a7-232">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="d39a7-233">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d39a7-233">Get</span></span>
- <span data-ttu-id="d39a7-234">Elenco</span><span class="sxs-lookup"><span data-stu-id="d39a7-234">List</span></span>
- <span data-ttu-id="d39a7-235">Imposta</span><span class="sxs-lookup"><span data-stu-id="d39a7-235">Set</span></span>
- <span data-ttu-id="d39a7-236">Elimina</span><span class="sxs-lookup"><span data-stu-id="d39a7-236">Delete</span></span>
- <span data-ttu-id="d39a7-237">Backup</span><span class="sxs-lookup"><span data-stu-id="d39a7-237">Backup</span></span>
- <span data-ttu-id="d39a7-238">Ripristina</span><span class="sxs-lookup"><span data-stu-id="d39a7-238">Restore</span></span>
- <span data-ttu-id="d39a7-239">Recupera</span><span class="sxs-lookup"><span data-stu-id="d39a7-239">Recover</span></span>
- <span data-ttu-id="d39a7-240">Ripulire</span><span class="sxs-lookup"><span data-stu-id="d39a7-240">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39a7-241">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="d39a7-241">-PermissionsToStorage</span></span>
<span data-ttu-id="d39a7-242">Specifica le autorizzazioni per l'operazione di definizione saS e l'account di archiviazione gestito da concedere a un utente o a un'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="d39a7-242">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39a7-243">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d39a7-243">-ResourceGroupName</span></span>
<span data-ttu-id="d39a7-244">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d39a7-244">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39a7-245">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d39a7-245">-ResourceId</span></span>
<span data-ttu-id="d39a7-246">ID risorsa Vault chiave</span><span class="sxs-lookup"><span data-stu-id="d39a7-246">Key Vault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d39a7-247">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d39a7-247">-ServicePrincipalName</span></span>
<span data-ttu-id="d39a7-248">Specifica il nome dell'entità servizio dell'applicazione a cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="d39a7-248">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="d39a7-249">Specificare l'ID applicazione, noto anche come ID client, registrato per l'applicazione in AzureActive Directory.</span><span class="sxs-lookup"><span data-stu-id="d39a7-249">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="d39a7-250">L'applicazione con il nome dell'entità servizio specificata da questo parametro deve essere registrata nella directory di Azure che contiene la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="d39a7-250">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName, ResourceIdByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39a7-251">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d39a7-251">-UserPrincipalName</span></span>
<span data-ttu-id="d39a7-252">Specifica il nome dell'entità utente dell'utente a cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="d39a7-252">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="d39a7-253">Il nome dell'entità utente deve essere presente nella directory associata alla sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="d39a7-253">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName, ResourceIdByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39a7-254">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d39a7-254">-VaultName</span></span>
<span data-ttu-id="d39a7-255">Specifica il nome di un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="d39a7-255">Specifies the name of a key vault.</span></span>
<span data-ttu-id="d39a7-256">Questo cmdlet modifica i criteri di accesso per il vault delle chiavi specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d39a7-256">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39a7-257">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d39a7-257">-Confirm</span></span>
<span data-ttu-id="d39a7-258">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d39a7-258">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39a7-259">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d39a7-259">-WhatIf</span></span>
<span data-ttu-id="d39a7-260">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d39a7-260">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d39a7-261">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d39a7-261">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39a7-262">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d39a7-262">CommonParameters</span></span>
<span data-ttu-id="d39a7-263">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d39a7-263">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d39a7-264">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d39a7-264">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d39a7-265">INPUT</span><span class="sxs-lookup"><span data-stu-id="d39a7-265">INPUTS</span></span>

### <span data-ttu-id="d39a7-266">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d39a7-266">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="d39a7-267">System.String</span><span class="sxs-lookup"><span data-stu-id="d39a7-267">System.String</span></span>

## <span data-ttu-id="d39a7-268">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d39a7-268">OUTPUTS</span></span>

### <span data-ttu-id="d39a7-269">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d39a7-269">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="d39a7-270">NOTE</span><span class="sxs-lookup"><span data-stu-id="d39a7-270">NOTES</span></span>

## <span data-ttu-id="d39a7-271">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d39a7-271">RELATED LINKS</span></span>

[<span data-ttu-id="d39a7-272">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d39a7-272">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="d39a7-273">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d39a7-273">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

