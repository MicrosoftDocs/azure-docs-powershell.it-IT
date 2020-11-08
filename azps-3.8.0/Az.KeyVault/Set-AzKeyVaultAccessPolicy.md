---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 15ee05260a4714831808b68b1bc8b1784d9ffdd2
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030836"
---
# <span data-ttu-id="19950-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="19950-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="19950-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19950-102">SYNOPSIS</span></span>
<span data-ttu-id="19950-103">Concede o modifica le autorizzazioni esistenti per un utente, un'applicazione o un gruppo di sicurezza per eseguire operazioni con un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="19950-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="19950-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19950-104">SYNTAX</span></span>

### <span data-ttu-id="19950-105">ByUserPrincipalName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="19950-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19950-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="19950-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19950-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="19950-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19950-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="19950-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19950-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="19950-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19950-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="19950-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19950-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="19950-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19950-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="19950-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19950-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="19950-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19950-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="19950-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19950-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="19950-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19950-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="19950-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19950-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="19950-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19950-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="19950-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19950-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="19950-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19950-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19950-120">DESCRIPTION</span></span>
<span data-ttu-id="19950-121">Il cmdlet **set-AzKeyVaultAccessPolicy** concede o modifica le autorizzazioni esistenti per un utente, un'applicazione o un gruppo di sicurezza per eseguire le operazioni specificate con un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="19950-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="19950-122">Non modifica le autorizzazioni di altri utenti, applicazioni o gruppi di sicurezza nel Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="19950-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="19950-123">Se si stanno impostando le autorizzazioni per un gruppo di sicurezza, questa operazione interessa solo gli utenti del gruppo di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="19950-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="19950-124">Le directory seguenti devono essere tutte della stessa directory di Azure:</span><span class="sxs-lookup"><span data-stu-id="19950-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="19950-125">Directory predefinita dell'abbonamento a Azure in cui si trova il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="19950-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="19950-126">Directory di Azure che contiene l'utente o il gruppo di applicazioni a cui si stanno concedendo le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="19950-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="19950-127">Esempi di scenari in cui queste condizioni non vengono soddisfatte e questo cmdlet non funziona:</span><span class="sxs-lookup"><span data-stu-id="19950-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="19950-128">Autorizzazione di un utente di un'organizzazione diversa per gestire il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="19950-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="19950-129">Ogni organizzazione ha una propria directory.</span><span class="sxs-lookup"><span data-stu-id="19950-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="19950-130">L'account di Azure include più directory.</span><span class="sxs-lookup"><span data-stu-id="19950-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="19950-131">Se si registra un'applicazione in una directory diversa da quella predefinita, non è possibile autorizzare l'applicazione a usare il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="19950-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="19950-132">L'applicazione deve essere nella directory predefinita.</span><span class="sxs-lookup"><span data-stu-id="19950-132">The application must be in the default directory.</span></span>
<span data-ttu-id="19950-133">Tieni presente che, anche se specificando il gruppo di risorse è facoltativo per questo cmdlet, devi farlo per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="19950-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="19950-134">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19950-134">EXAMPLES</span></span>

### <span data-ttu-id="19950-135">Esempio 1: concedere le autorizzazioni a un utente per un Vault chiave e modificare le autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="19950-135">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
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

<span data-ttu-id="19950-136">Il primo comando concede le autorizzazioni per un utente in Azure Active Directory, PattiFuller@contoso.com per eseguire operazioni su chiavi e segreti con un Vault chiave denominato Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="19950-136">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="19950-137">Il parametro *PassThru* genera l'oggetto updated restituito dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19950-137">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="19950-138">Il secondo comando modifica le autorizzazioni concesse al PattiFuller@contoso.com primo comando per consentire l'ottenimento di segreti oltre a impostarli ed eliminarli.</span><span class="sxs-lookup"><span data-stu-id="19950-138">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="19950-139">Le autorizzazioni per le operazioni chiave restano invariate dopo questo comando.</span><span class="sxs-lookup"><span data-stu-id="19950-139">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="19950-140">Il comando finale modifica ulteriormente le autorizzazioni esistenti per PattiFuller@contoso.com rimuovere tutte le autorizzazioni per le operazioni principali.</span><span class="sxs-lookup"><span data-stu-id="19950-140">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="19950-141">Le autorizzazioni per le operazioni segrete restano invariate dopo questo comando.</span><span class="sxs-lookup"><span data-stu-id="19950-141">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="19950-142">Esempio 2: concedere le autorizzazioni per un'entità del servizio applicazione per la lettura e la scrittura di segreti</span><span class="sxs-lookup"><span data-stu-id="19950-142">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="19950-143">Questo comando consente di concedere le autorizzazioni per un'applicazione per un Vault chiave denominato Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="19950-143">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="19950-144">Il parametro *servicePrincipalName* specifica l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="19950-144">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="19950-145">L'applicazione deve essere registrata in Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="19950-145">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="19950-146">Il valore del parametro *servicePrincipalName* deve essere il nome dell'entità servizio dell'applicazione o il GUID dell'ID applicazione.</span><span class="sxs-lookup"><span data-stu-id="19950-146">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="19950-147">Questo esempio specifica il nome dell'entità servizio `http://payroll.contoso.com` e il comando concede alle autorizzazioni dell'applicazione la lettura e la scrittura dei segreti.</span><span class="sxs-lookup"><span data-stu-id="19950-147">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="19950-148">Esempio 3: concedere le autorizzazioni per un'applicazione usando il relativo ID oggetto</span><span class="sxs-lookup"><span data-stu-id="19950-148">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="19950-149">Questo comando concede alle autorizzazioni dell'applicazione la lettura e la scrittura di segreti.</span><span class="sxs-lookup"><span data-stu-id="19950-149">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="19950-150">Questo esempio specifica l'applicazione che usa l'ID oggetto dell'entità servizio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="19950-150">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="19950-151">Esempio 4: concedere le autorizzazioni per un nome dell'entità utente</span><span class="sxs-lookup"><span data-stu-id="19950-151">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="19950-152">Questo comando consente di concedere le autorizzazioni Get, List e set per il nome dell'entità utente specificato per l'accesso ai segreti.</span><span class="sxs-lookup"><span data-stu-id="19950-152">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="19950-153">Esempio 5: abilitare i segreti da recuperare da un Vault chiave dal provider di risorse Microsoft. Compute</span><span class="sxs-lookup"><span data-stu-id="19950-153">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="19950-154">Questo comando concede le autorizzazioni per i segreti da recuperare dall'archivio della chiave Contoso03Vault dal provider di risorse Microsoft. Compute.</span><span class="sxs-lookup"><span data-stu-id="19950-154">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="19950-155">Esempio 6: concedere le autorizzazioni a un gruppo di sicurezza</span><span class="sxs-lookup"><span data-stu-id="19950-155">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="19950-156">Il primo comando usa il cmdlet Get-AzADGroup per ottenere tutti i gruppi di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="19950-156">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="19950-157">Nell'output vengono visualizzati 3 gruppi restituiti, denominati **Group1** , **group2** e **Group3**.</span><span class="sxs-lookup"><span data-stu-id="19950-157">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="19950-158">Più gruppi possono avere lo stesso nome, ma hanno sempre un ObjectId univoco.</span><span class="sxs-lookup"><span data-stu-id="19950-158">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="19950-159">Quando viene restituito più di un gruppo con lo stesso nome, usare il parametro ObjectId nell'output per identificare quello che si vuole usare.</span><span class="sxs-lookup"><span data-stu-id="19950-159">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="19950-160">Si usa quindi l'output di questo comando con Set-AzKeyVaultAccessPolicy per concedere le autorizzazioni a group2 per il Vault chiave, denominato **myownvault**.</span><span class="sxs-lookup"><span data-stu-id="19950-160">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="19950-161">Questo esempio enumera i gruppi denominati "group2" inline nella stessa riga di comando.</span><span class="sxs-lookup"><span data-stu-id="19950-161">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="19950-162">Nell'elenco restituito possono essere presenti più gruppi denominati "group2".</span><span class="sxs-lookup"><span data-stu-id="19950-162">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="19950-163">Questo esempio seleziona il primo, indicato dall'indice \[ 0 \] nell'elenco restituito.</span><span class="sxs-lookup"><span data-stu-id="19950-163">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="19950-164">Esempio 7: concedere ad Azure Information Protection Access alla chiave tenant gestita dal cliente (BYOK)</span><span class="sxs-lookup"><span data-stu-id="19950-164">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="19950-165">Questo comando autorizza Azure Information Protection a usare una chiave gestita dal cliente (la chiave Bring your own o "BYOK") come chiave del tenant di Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="19950-165">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="19950-166">Quando si esegue questo comando, specificare il proprio nome per il Vault chiave, ma è necessario specificare il parametro *servicePrincipalName* con il GUID **00000012-0000-0000-C000-000000000000** e specificare le autorizzazioni nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="19950-166">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="19950-167">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19950-167">PARAMETERS</span></span>

### <span data-ttu-id="19950-168">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="19950-168">-ApplicationId</span></span>
<span data-ttu-id="19950-169">Per un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="19950-169">For future use.</span></span>

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

### <span data-ttu-id="19950-170">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="19950-170">-BypassObjectIdValidation</span></span>
<span data-ttu-id="19950-171">Consente di specificare un ID oggetto senza convalidare che l'oggetto esiste in Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="19950-171">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="19950-172">Usare questo parametro solo se si vuole concedere l'accesso al Vault della chiave a un ID oggetto che fa riferimento a un gruppo di sicurezza delegata di un altro tenant Azure.</span><span class="sxs-lookup"><span data-stu-id="19950-172">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

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

### <span data-ttu-id="19950-173">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19950-173">-DefaultProfile</span></span>
<span data-ttu-id="19950-174">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="19950-174">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19950-175">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="19950-175">-EmailAddress</span></span>
<span data-ttu-id="19950-176">Specifica l'indirizzo di posta elettronica dell'utente a cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="19950-176">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="19950-177">Questo indirizzo di posta elettronica deve esistere nella directory associata alla sottoscrizione corrente ed essere univoco.</span><span class="sxs-lookup"><span data-stu-id="19950-177">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

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

### <span data-ttu-id="19950-178">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="19950-178">-EnabledForDeployment</span></span>
<span data-ttu-id="19950-179">Consente al provider di risorse Microsoft. Compute di recuperare i segreti da questo Vault chiave quando si fa riferimento a questo Vault chiave nella creazione di risorse, ad esempio quando si crea una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="19950-179">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="19950-180">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="19950-180">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="19950-181">Abilita il servizio di crittografia di Azure disk per ottenere segreti e scartare le chiavi da questo caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="19950-181">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="19950-182">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="19950-182">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="19950-183">Consente a Azure Resource Manager di ottenere segreti da questo Vault chiave quando si fa riferimento a questo Vault chiave in una distribuzione di modelli.</span><span class="sxs-lookup"><span data-stu-id="19950-183">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="19950-184">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19950-184">-InputObject</span></span>
<span data-ttu-id="19950-185">Oggetto Key Vault</span><span class="sxs-lookup"><span data-stu-id="19950-185">Key Vault Object</span></span>

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

### <span data-ttu-id="19950-186">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="19950-186">-ObjectId</span></span>
<span data-ttu-id="19950-187">Specifica l'ID oggetto dell'entità di servizio o dell'utente in Azure Active Directory per cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="19950-187">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="19950-188">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19950-188">-PassThru</span></span>
<span data-ttu-id="19950-189">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="19950-189">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="19950-190">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="19950-190">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="19950-191">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="19950-191">-PermissionsToCertificates</span></span>
<span data-ttu-id="19950-192">Specifica una matrice di autorizzazioni di certificato da concedere a un utente o a un'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="19950-192">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="19950-193">Valori accettabili per questo parametro:</span><span class="sxs-lookup"><span data-stu-id="19950-193">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="19950-194">Ottieni</span><span class="sxs-lookup"><span data-stu-id="19950-194">Get</span></span>
- <span data-ttu-id="19950-195">Elenco</span><span class="sxs-lookup"><span data-stu-id="19950-195">List</span></span>
- <span data-ttu-id="19950-196">Eliminare</span><span class="sxs-lookup"><span data-stu-id="19950-196">Delete</span></span>
- <span data-ttu-id="19950-197">Creare</span><span class="sxs-lookup"><span data-stu-id="19950-197">Create</span></span>
- <span data-ttu-id="19950-198">Importazione</span><span class="sxs-lookup"><span data-stu-id="19950-198">Import</span></span>
- <span data-ttu-id="19950-199">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="19950-199">Update</span></span>
- <span data-ttu-id="19950-200">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="19950-200">Managecontacts</span></span>
- <span data-ttu-id="19950-201">Getissuers</span><span class="sxs-lookup"><span data-stu-id="19950-201">Getissuers</span></span>
- <span data-ttu-id="19950-202">Listissuers</span><span class="sxs-lookup"><span data-stu-id="19950-202">Listissuers</span></span>
- <span data-ttu-id="19950-203">Emittenti</span><span class="sxs-lookup"><span data-stu-id="19950-203">Setissuers</span></span>
- <span data-ttu-id="19950-204">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="19950-204">Deleteissuers</span></span>
- <span data-ttu-id="19950-205">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="19950-205">Manageissuers</span></span>
- <span data-ttu-id="19950-206">Recuperare</span><span class="sxs-lookup"><span data-stu-id="19950-206">Recover</span></span>
- <span data-ttu-id="19950-207">Backup</span><span class="sxs-lookup"><span data-stu-id="19950-207">Backup</span></span>
- <span data-ttu-id="19950-208">Ripristinare</span><span class="sxs-lookup"><span data-stu-id="19950-208">Restore</span></span>
- <span data-ttu-id="19950-209">Eliminazione</span><span class="sxs-lookup"><span data-stu-id="19950-209">Purge</span></span>

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

### <span data-ttu-id="19950-210">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="19950-210">-PermissionsToKeys</span></span>
<span data-ttu-id="19950-211">Specifica una matrice di autorizzazioni per le operazioni chiave da concedere a un utente o a un'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="19950-211">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="19950-212">Valori accettabili per questo parametro:</span><span class="sxs-lookup"><span data-stu-id="19950-212">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="19950-213">Decrittografare</span><span class="sxs-lookup"><span data-stu-id="19950-213">Decrypt</span></span>
- <span data-ttu-id="19950-214">Crittografare</span><span class="sxs-lookup"><span data-stu-id="19950-214">Encrypt</span></span>
- <span data-ttu-id="19950-215">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="19950-215">UnwrapKey</span></span>
- <span data-ttu-id="19950-216">WrapKey</span><span class="sxs-lookup"><span data-stu-id="19950-216">WrapKey</span></span>
- <span data-ttu-id="19950-217">Verificare</span><span class="sxs-lookup"><span data-stu-id="19950-217">Verify</span></span>
- <span data-ttu-id="19950-218">Segno</span><span class="sxs-lookup"><span data-stu-id="19950-218">Sign</span></span>
- <span data-ttu-id="19950-219">Ottieni</span><span class="sxs-lookup"><span data-stu-id="19950-219">Get</span></span>
- <span data-ttu-id="19950-220">Elenco</span><span class="sxs-lookup"><span data-stu-id="19950-220">List</span></span>
- <span data-ttu-id="19950-221">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="19950-221">Update</span></span>
- <span data-ttu-id="19950-222">Creare</span><span class="sxs-lookup"><span data-stu-id="19950-222">Create</span></span>
- <span data-ttu-id="19950-223">Importazione</span><span class="sxs-lookup"><span data-stu-id="19950-223">Import</span></span>
- <span data-ttu-id="19950-224">Eliminare</span><span class="sxs-lookup"><span data-stu-id="19950-224">Delete</span></span>
- <span data-ttu-id="19950-225">Backup</span><span class="sxs-lookup"><span data-stu-id="19950-225">Backup</span></span>
- <span data-ttu-id="19950-226">Ripristinare</span><span class="sxs-lookup"><span data-stu-id="19950-226">Restore</span></span>
- <span data-ttu-id="19950-227">Recuperare</span><span class="sxs-lookup"><span data-stu-id="19950-227">Recover</span></span>
- <span data-ttu-id="19950-228">Eliminazione</span><span class="sxs-lookup"><span data-stu-id="19950-228">Purge</span></span>

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

### <span data-ttu-id="19950-229">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="19950-229">-PermissionsToSecrets</span></span>
<span data-ttu-id="19950-230">Specifica una matrice di autorizzazioni per le operazioni segrete da concedere a un utente o a un'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="19950-230">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="19950-231">Valori accettabili per questo parametro:</span><span class="sxs-lookup"><span data-stu-id="19950-231">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="19950-232">Ottieni</span><span class="sxs-lookup"><span data-stu-id="19950-232">Get</span></span>
- <span data-ttu-id="19950-233">Elenco</span><span class="sxs-lookup"><span data-stu-id="19950-233">List</span></span>
- <span data-ttu-id="19950-234">Impostare</span><span class="sxs-lookup"><span data-stu-id="19950-234">Set</span></span>
- <span data-ttu-id="19950-235">Eliminare</span><span class="sxs-lookup"><span data-stu-id="19950-235">Delete</span></span>
- <span data-ttu-id="19950-236">Backup</span><span class="sxs-lookup"><span data-stu-id="19950-236">Backup</span></span>
- <span data-ttu-id="19950-237">Ripristinare</span><span class="sxs-lookup"><span data-stu-id="19950-237">Restore</span></span>
- <span data-ttu-id="19950-238">Recuperare</span><span class="sxs-lookup"><span data-stu-id="19950-238">Recover</span></span>
- <span data-ttu-id="19950-239">Eliminazione</span><span class="sxs-lookup"><span data-stu-id="19950-239">Purge</span></span>

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

### <span data-ttu-id="19950-240">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="19950-240">-PermissionsToStorage</span></span>
<span data-ttu-id="19950-241">Specifica le autorizzazioni dell'account di archiviazione gestita e delle operazioni di definizione SaS per concedere a un utente o a un servizio Principal.</span><span class="sxs-lookup"><span data-stu-id="19950-241">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

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

### <span data-ttu-id="19950-242">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19950-242">-ResourceGroupName</span></span>
<span data-ttu-id="19950-243">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="19950-243">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="19950-244">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19950-244">-ResourceId</span></span>
<span data-ttu-id="19950-245">ID risorsa chiave Vault</span><span class="sxs-lookup"><span data-stu-id="19950-245">Key Vault Resource Id</span></span>

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

### <span data-ttu-id="19950-246">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="19950-246">-ServicePrincipalName</span></span>
<span data-ttu-id="19950-247">Specifica il nome dell'entità servizio dell'applicazione a cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="19950-247">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="19950-248">Specifica l'ID applicazione, noto anche come ID client, registrato per l'applicazione nella directory AzureActive.</span><span class="sxs-lookup"><span data-stu-id="19950-248">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="19950-249">L'applicazione con il nome dell'entità servizio specificata da questo parametro deve essere registrata nella directory Azure che contiene l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="19950-249">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

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

### <span data-ttu-id="19950-250">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="19950-250">-UserPrincipalName</span></span>
<span data-ttu-id="19950-251">Specifica il nome dell'entità utente dell'utente a cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="19950-251">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="19950-252">Il nome dell'entità utente deve esistere nella directory associata alla sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="19950-252">This user principal name must exist in the directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="19950-253">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="19950-253">-VaultName</span></span>
<span data-ttu-id="19950-254">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="19950-254">Specifies the name of a key vault.</span></span>
<span data-ttu-id="19950-255">Questo cmdlet modifica i criteri di accesso per il Vault chiave specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="19950-255">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="19950-256">-Confermare</span><span class="sxs-lookup"><span data-stu-id="19950-256">-Confirm</span></span>
<span data-ttu-id="19950-257">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19950-257">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19950-258">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19950-258">-WhatIf</span></span>
<span data-ttu-id="19950-259">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19950-259">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19950-260">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19950-260">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19950-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19950-261">CommonParameters</span></span>
<span data-ttu-id="19950-262">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19950-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19950-263">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19950-263">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19950-264">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19950-264">INPUTS</span></span>

### <span data-ttu-id="19950-265">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="19950-265">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="19950-266">System. String</span><span class="sxs-lookup"><span data-stu-id="19950-266">System.String</span></span>

## <span data-ttu-id="19950-267">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19950-267">OUTPUTS</span></span>

### <span data-ttu-id="19950-268">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="19950-268">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="19950-269">Note</span><span class="sxs-lookup"><span data-stu-id="19950-269">NOTES</span></span>

## <span data-ttu-id="19950-270">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19950-270">RELATED LINKS</span></span>

[<span data-ttu-id="19950-271">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="19950-271">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="19950-272">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="19950-272">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

