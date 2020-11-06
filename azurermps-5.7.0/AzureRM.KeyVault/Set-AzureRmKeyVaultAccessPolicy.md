---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: 20a36e35c509ecca889d4059bd7e74ccafa22dc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512548"
---
# <span data-ttu-id="f318a-101">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f318a-101">Set-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="f318a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f318a-102">SYNOPSIS</span></span>
<span data-ttu-id="f318a-103">Concede o modifica le autorizzazioni esistenti per un utente, un'applicazione o un gruppo di sicurezza per eseguire operazioni con un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f318a-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f318a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f318a-104">SYNTAX</span></span>

### <span data-ttu-id="f318a-105">ByUserPrincipalName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f318a-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f318a-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="f318a-106">ByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f318a-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f318a-107">ByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f318a-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f318a-108">ByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f318a-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="f318a-109">ForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f318a-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="f318a-110">InputObjectByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f318a-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f318a-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f318a-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f318a-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f318a-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f318a-113">InputObjectByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f318a-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="f318a-114">InputObjectForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f318a-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f318a-115">DESCRIPTION</span></span>
<span data-ttu-id="f318a-116">Il cmdlet **set-AzureRmKeyVaultAccessPolicy** concede o modifica le autorizzazioni esistenti per un utente, un'applicazione o un gruppo di sicurezza per eseguire le operazioni specificate con un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f318a-116">The **Set-AzureRmKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="f318a-117">Non modifica le autorizzazioni di altri utenti, applicazioni o gruppi di sicurezza nel Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f318a-117">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>

<span data-ttu-id="f318a-118">Se si stanno impostando le autorizzazioni per un gruppo di sicurezza, questa operazione interessa solo gli utenti del gruppo di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="f318a-118">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>

<span data-ttu-id="f318a-119">Le directory seguenti devono essere tutte della stessa directory di Azure:</span><span class="sxs-lookup"><span data-stu-id="f318a-119">The following directories must all be the same Azure directory:</span></span> 
- <span data-ttu-id="f318a-120">Directory predefinita dell'abbonamento a Azure in cui si trova il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f318a-120">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="f318a-121">Directory di Azure che contiene l'utente o il gruppo di applicazioni a cui si stanno concedendo le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="f318a-121">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>

<span data-ttu-id="f318a-122">Esempi di scenari in cui queste condizioni non vengono soddisfatte e questo cmdlet non funziona:</span><span class="sxs-lookup"><span data-stu-id="f318a-122">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span> 

- <span data-ttu-id="f318a-123">Autorizzazione di un utente di un'organizzazione diversa per gestire il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f318a-123">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="f318a-124">Ogni organizzazione ha una propria directory.</span><span class="sxs-lookup"><span data-stu-id="f318a-124">Each organization has its own directory.</span></span> 
- <span data-ttu-id="f318a-125">L'account di Azure include più directory.</span><span class="sxs-lookup"><span data-stu-id="f318a-125">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="f318a-126">Se si registra un'applicazione in una directory diversa da quella predefinita, non è possibile autorizzare l'applicazione a usare il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f318a-126">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="f318a-127">L'applicazione deve essere nella directory predefinita.</span><span class="sxs-lookup"><span data-stu-id="f318a-127">The application must be in the default directory.</span></span>

<span data-ttu-id="f318a-128">Tieni presente che, anche se specificando il gruppo di risorse è facoltativo per questo cmdlet, devi farlo per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="f318a-128">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="f318a-129">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f318a-129">EXAMPLES</span></span>

### <span data-ttu-id="f318a-130">Esempio 1: concedere le autorizzazioni a un utente per un Vault chiave e modificare le autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="f318a-130">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru
```

<span data-ttu-id="f318a-131">Il primo comando concede le autorizzazioni per un utente in Azure Active Directory, PattiFuller@contoso.com per eseguire operazioni su chiavi e segreti con un Vault chiave denominato Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="f318a-131">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="f318a-132">Il secondo comando modifica le autorizzazioni concesse al PattiFuller@contoso.com primo comando per consentire l'ottenimento di segreti oltre a impostarli ed eliminarli.</span><span class="sxs-lookup"><span data-stu-id="f318a-132">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="f318a-133">Le autorizzazioni per le operazioni chiave restano invariate dopo questo comando.</span><span class="sxs-lookup"><span data-stu-id="f318a-133">The permissions to key operations remain unchanged after this command.</span></span> <span data-ttu-id="f318a-134">Il parametro *PassThru* genera l'oggetto updated restituito dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f318a-134">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

<span data-ttu-id="f318a-135">Il comando finale modifica ulteriormente le autorizzazioni esistenti per PattiFuller@contoso.com rimuovere tutte le autorizzazioni per le operazioni principali.</span><span class="sxs-lookup"><span data-stu-id="f318a-135">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="f318a-136">Le autorizzazioni per le operazioni segrete restano invariate dopo questo comando.</span><span class="sxs-lookup"><span data-stu-id="f318a-136">The permissions to secret operations remain unchanged after this command.</span></span> <span data-ttu-id="f318a-137">Il parametro *PassThru* genera l'oggetto updated restituito dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f318a-137">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

### <span data-ttu-id="f318a-138">Esempio 2: concedere le autorizzazioni per un'entità del servizio applicazione per la lettura e la scrittura di segreti</span><span class="sxs-lookup"><span data-stu-id="f318a-138">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="f318a-139">Questo comando consente di concedere le autorizzazioni per un'applicazione per un Vault chiave denominato Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="f318a-139">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span> 

<span data-ttu-id="f318a-140">Il parametro *servicePrincipalName* specifica l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f318a-140">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="f318a-141">L'applicazione deve essere registrata in Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f318a-141">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="f318a-142">Il valore del parametro *servicePrincipalName* deve essere il nome dell'entità servizio dell'applicazione o il GUID dell'ID applicazione.</span><span class="sxs-lookup"><span data-stu-id="f318a-142">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>

<span data-ttu-id="f318a-143">Questo esempio specifica il nome dell'entità servizio http://payroll.contoso.com e il comando concede alle autorizzazioni dell'applicazione la lettura e la scrittura dei segreti.</span><span class="sxs-lookup"><span data-stu-id="f318a-143">This example specifies the service principal name http://payroll.contoso.com, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="f318a-144">Esempio 3: concedere le autorizzazioni per un'applicazione usando il relativo ID oggetto</span><span class="sxs-lookup"><span data-stu-id="f318a-144">Example 3: Grant permissions for an application using its object ID</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="f318a-145">Questo comando concede alle autorizzazioni dell'applicazione la lettura e la scrittura di segreti.</span><span class="sxs-lookup"><span data-stu-id="f318a-145">This command grants the application permissions to read and write secrets.</span></span>

<span data-ttu-id="f318a-146">Questo esempio specifica l'applicazione che usa l'ID oggetto dell'entità servizio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f318a-146">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="f318a-147">Esempio 4: concedere le autorizzazioni per un nome dell'entità utente</span><span class="sxs-lookup"><span data-stu-id="f318a-147">Example 4: Grant permissions for a user principal name</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="f318a-148">Questo comando consente di concedere le autorizzazioni Get, List e set per il nome dell'entità utente specificato per l'accesso ai segreti.</span><span class="sxs-lookup"><span data-stu-id="f318a-148">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="f318a-149">Esempio 5: abilitare i segreti da recuperare da un Vault chiave dal provider di risorse Microsoft. Compute</span><span class="sxs-lookup"><span data-stu-id="f318a-149">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="f318a-150">Questo comando concede le autorizzazioni per i segreti da recuperare dall'archivio della chiave Contoso03Vault dal provider di risorse Microsoft. Compute.</span><span class="sxs-lookup"><span data-stu-id="f318a-150">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="f318a-151">Esempio 6: concedere le autorizzazioni a un gruppo di sicurezza</span><span class="sxs-lookup"><span data-stu-id="f318a-151">Example 6: Grant permissions to a security group</span></span>
```
PS C:\>Get-AzureRmADGroup
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzureRmADGroup -SearchString 'group2')[0].Id -PermissionsToKeys All -PermissionsToSecrets All
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
group1                                                        96a0daa6-9841-4a9c-bdeb-e7062276c688
group2                                                        b8a401eb-63ad-4a30-b0e1-a7461969fe54
group3                                                        da07a6be-2c1e-4e42-934d-ceb57cf652b4
```

<span data-ttu-id="f318a-152">Il primo comando usa il cmdlet Get-AzureRmADGroup per ottenere tutti i gruppi di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f318a-152">The first command uses the Get-AzureRmADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="f318a-153">Nell'output vengono visualizzati 3 gruppi restituiti, denominati **Group1** , **group2** e **Group3**.</span><span class="sxs-lookup"><span data-stu-id="f318a-153">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="f318a-154">Più gruppi possono avere lo stesso nome, ma hanno sempre un ObjectId univoco.</span><span class="sxs-lookup"><span data-stu-id="f318a-154">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="f318a-155">Quando viene restituito più di un gruppo con lo stesso nome, usare il parametro ObjectId nell'output per identificare quello che si vuole usare.</span><span class="sxs-lookup"><span data-stu-id="f318a-155">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>

<span data-ttu-id="f318a-156">Si usa quindi l'output di questo comando con Set-AzureRmKeyVaultAccessPolicy per concedere le autorizzazioni a group2 per il Vault chiave, denominato **myownvault**.</span><span class="sxs-lookup"><span data-stu-id="f318a-156">You then use the output of this command with Set-AzureRmKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="f318a-157">Questo esempio enumera i gruppi denominati "group2" inline nella stessa riga di comando.</span><span class="sxs-lookup"><span data-stu-id="f318a-157">This example enumerates the groups named 'group2' inline in the same command line.</span></span>

<span data-ttu-id="f318a-158">Nell'elenco restituito possono essere presenti più gruppi denominati "group2".</span><span class="sxs-lookup"><span data-stu-id="f318a-158">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="f318a-159">Questo esempio seleziona il primo, indicato dall'indice \[ 0 \] nell'elenco restituito.</span><span class="sxs-lookup"><span data-stu-id="f318a-159">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="f318a-160">Esempio 7: concedere ad Azure Information Protection Access alla chiave tenant gestita dal cliente (BYOK)</span><span class="sxs-lookup"><span data-stu-id="f318a-160">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="f318a-161">Questo comando autorizza Azure Information Protection a usare una chiave gestita dal cliente (la chiave Bring your own o "BYOK") come chiave del tenant di Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="f318a-161">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>

<span data-ttu-id="f318a-162">Quando si esegue questo comando, specificare il proprio nome per il Vault chiave, ma è necessario specificare il parametro *servicePrincipalName* con il GUID **00000012-0000-0000-C000-000000000000** e specificare le autorizzazioni nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="f318a-162">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="f318a-163">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f318a-163">PARAMETERS</span></span>

### <span data-ttu-id="f318a-164">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f318a-164">-ApplicationId</span></span>
<span data-ttu-id="f318a-165">Per un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="f318a-165">For future use.</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f318a-166">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="f318a-166">-BypassObjectIdValidation</span></span>
<span data-ttu-id="f318a-167">Consente di specificare un ID oggetto senza convalidare che l'oggetto esiste in Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f318a-167">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>

<span data-ttu-id="f318a-168">Usare questo parametro solo se si vuole concedere l'accesso al Vault della chiave a un ID oggetto che fa riferimento a un gruppo di sicurezza delegata di un altro tenant Azure.</span><span class="sxs-lookup"><span data-stu-id="f318a-168">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f318a-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f318a-169">-DefaultProfile</span></span>
<span data-ttu-id="f318a-170">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f318a-170">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f318a-171">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="f318a-171">-EmailAddress</span></span>
<span data-ttu-id="f318a-172">Specifica l'indirizzo di posta elettronica dell'utente a cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="f318a-172">Specifies the user email address of the user to whom to grant permissions.</span></span>

<span data-ttu-id="f318a-173">Questo indirizzo di posta elettronica deve esistere nella directory associata alla sottoscrizione corrente ed essere univoco.</span><span class="sxs-lookup"><span data-stu-id="f318a-173">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f318a-174">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="f318a-174">-EnabledForDeployment</span></span>
<span data-ttu-id="f318a-175">Consente al provider di risorse Microsoft. Compute di recuperare i segreti da questo Vault chiave quando si fa riferimento a questo Vault chiave nella creazione di risorse, ad esempio quando si crea una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f318a-175">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f318a-176">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="f318a-176">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="f318a-177">Abilita il servizio di crittografia di Azure disk per ottenere segreti e scartare le chiavi da questo caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="f318a-177">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f318a-178">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="f318a-178">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="f318a-179">Consente a Azure Resource Manager di ottenere segreti da questo Vault chiave quando si fa riferimento a questo Vault chiave in una distribuzione di modelli.</span><span class="sxs-lookup"><span data-stu-id="f318a-179">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f318a-180">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f318a-180">-InputObject</span></span>
<span data-ttu-id="f318a-181">Oggetto Key Vault</span><span class="sxs-lookup"><span data-stu-id="f318a-181">Key Vault Object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f318a-182">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f318a-182">-ObjectId</span></span>
<span data-ttu-id="f318a-183">Specifica l'ID oggetto dell'entità di servizio o dell'utente in Azure Active Directory per cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="f318a-183">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f318a-184">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f318a-184">-PassThru</span></span>
<span data-ttu-id="f318a-185">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="f318a-185">Returns an object representing the item with which you are working.</span></span>

<span data-ttu-id="f318a-186">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="f318a-186">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f318a-187">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="f318a-187">-PermissionsToCertificates</span></span>
<span data-ttu-id="f318a-188">Specifica una matrice di autorizzazioni di certificato da concedere a un utente o a un'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="f318a-188">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="f318a-189">Valori accettabili per questo parametro:</span><span class="sxs-lookup"><span data-stu-id="f318a-189">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="f318a-190">Ottieni</span><span class="sxs-lookup"><span data-stu-id="f318a-190">Get</span></span>
- <span data-ttu-id="f318a-191">Elenco</span><span class="sxs-lookup"><span data-stu-id="f318a-191">List</span></span>
- <span data-ttu-id="f318a-192">Eliminare</span><span class="sxs-lookup"><span data-stu-id="f318a-192">Delete</span></span>
- <span data-ttu-id="f318a-193">Creare</span><span class="sxs-lookup"><span data-stu-id="f318a-193">Create</span></span>
- <span data-ttu-id="f318a-194">Importazione</span><span class="sxs-lookup"><span data-stu-id="f318a-194">Import</span></span>
- <span data-ttu-id="f318a-195">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f318a-195">Update</span></span>
- <span data-ttu-id="f318a-196">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="f318a-196">Managecontacts</span></span>
- <span data-ttu-id="f318a-197">Getissuers</span><span class="sxs-lookup"><span data-stu-id="f318a-197">Getissuers</span></span>
- <span data-ttu-id="f318a-198">Listissuers</span><span class="sxs-lookup"><span data-stu-id="f318a-198">Listissuers</span></span>
- <span data-ttu-id="f318a-199">Emittenti</span><span class="sxs-lookup"><span data-stu-id="f318a-199">Setissuers</span></span>
- <span data-ttu-id="f318a-200">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="f318a-200">Deleteissuers</span></span>
- <span data-ttu-id="f318a-201">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="f318a-201">Manageissuers</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f318a-202">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="f318a-202">-PermissionsToKeys</span></span>
<span data-ttu-id="f318a-203">Specifica una matrice di autorizzazioni per le operazioni chiave da concedere a un utente o a un'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="f318a-203">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="f318a-204">Valori accettabili per questo parametro:</span><span class="sxs-lookup"><span data-stu-id="f318a-204">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="f318a-205">Decrittografare</span><span class="sxs-lookup"><span data-stu-id="f318a-205">Decrypt</span></span>
- <span data-ttu-id="f318a-206">Crittografare</span><span class="sxs-lookup"><span data-stu-id="f318a-206">Encrypt</span></span>
- <span data-ttu-id="f318a-207">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="f318a-207">UnwrapKey</span></span>
- <span data-ttu-id="f318a-208">WrapKey</span><span class="sxs-lookup"><span data-stu-id="f318a-208">WrapKey</span></span>
- <span data-ttu-id="f318a-209">Verificare</span><span class="sxs-lookup"><span data-stu-id="f318a-209">Verify</span></span>
- <span data-ttu-id="f318a-210">Segno</span><span class="sxs-lookup"><span data-stu-id="f318a-210">Sign</span></span>
- <span data-ttu-id="f318a-211">Ottieni</span><span class="sxs-lookup"><span data-stu-id="f318a-211">Get</span></span>
- <span data-ttu-id="f318a-212">Elenco</span><span class="sxs-lookup"><span data-stu-id="f318a-212">List</span></span>
- <span data-ttu-id="f318a-213">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f318a-213">Update</span></span>
- <span data-ttu-id="f318a-214">Creare</span><span class="sxs-lookup"><span data-stu-id="f318a-214">Create</span></span>
- <span data-ttu-id="f318a-215">Importazione</span><span class="sxs-lookup"><span data-stu-id="f318a-215">Import</span></span>
- <span data-ttu-id="f318a-216">Eliminare</span><span class="sxs-lookup"><span data-stu-id="f318a-216">Delete</span></span>
- <span data-ttu-id="f318a-217">Backup</span><span class="sxs-lookup"><span data-stu-id="f318a-217">Backup</span></span>
- <span data-ttu-id="f318a-218">Ripristinare</span><span class="sxs-lookup"><span data-stu-id="f318a-218">Restore</span></span>
- <span data-ttu-id="f318a-219">Recuperare</span><span class="sxs-lookup"><span data-stu-id="f318a-219">Recover</span></span>
- <span data-ttu-id="f318a-220">Eliminazione</span><span class="sxs-lookup"><span data-stu-id="f318a-220">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f318a-221">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="f318a-221">-PermissionsToSecrets</span></span>
<span data-ttu-id="f318a-222">Specifica una matrice di autorizzazioni per le operazioni segrete da concedere a un utente o a un'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="f318a-222">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="f318a-223">Valori accettabili per questo parametro:</span><span class="sxs-lookup"><span data-stu-id="f318a-223">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="f318a-224">Ottieni</span><span class="sxs-lookup"><span data-stu-id="f318a-224">Get</span></span>
- <span data-ttu-id="f318a-225">Elenco</span><span class="sxs-lookup"><span data-stu-id="f318a-225">List</span></span>
- <span data-ttu-id="f318a-226">Impostare</span><span class="sxs-lookup"><span data-stu-id="f318a-226">Set</span></span>
- <span data-ttu-id="f318a-227">Eliminare</span><span class="sxs-lookup"><span data-stu-id="f318a-227">Delete</span></span>
- <span data-ttu-id="f318a-228">Backup</span><span class="sxs-lookup"><span data-stu-id="f318a-228">Backup</span></span>
- <span data-ttu-id="f318a-229">Ripristinare</span><span class="sxs-lookup"><span data-stu-id="f318a-229">Restore</span></span>
- <span data-ttu-id="f318a-230">Recuperare</span><span class="sxs-lookup"><span data-stu-id="f318a-230">Recover</span></span>
- <span data-ttu-id="f318a-231">Eliminazione</span><span class="sxs-lookup"><span data-stu-id="f318a-231">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f318a-232">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="f318a-232">-PermissionsToStorage</span></span>
<span data-ttu-id="f318a-233">Specifica le autorizzazioni dell'account di archiviazione gestita e delle operazioni di definizione SaS per concedere a un utente o a un servizio Principal.</span><span class="sxs-lookup"><span data-stu-id="f318a-233">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f318a-234">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f318a-234">-ResourceGroupName</span></span>
<span data-ttu-id="f318a-235">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f318a-235">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f318a-236">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f318a-236">-ServicePrincipalName</span></span>
<span data-ttu-id="f318a-237">Specifica il nome dell'entità servizio dell'applicazione a cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="f318a-237">Specifies the service principal name of the application to which to grant permissions.</span></span>

<span data-ttu-id="f318a-238">Specifica l'ID applicazione, noto anche come ID client, registrato per l'applicazione nella directory AzureActive.</span><span class="sxs-lookup"><span data-stu-id="f318a-238">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="f318a-239">L'applicazione con il nome dell'entità servizio specificata da questo parametro deve essere registrata nella directory Azure che contiene l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="f318a-239">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f318a-240">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f318a-240">-UserPrincipalName</span></span>
<span data-ttu-id="f318a-241">Specifica il nome dell'entità utente dell'utente a cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="f318a-241">Specifies the user principal name of the user to whom to grant permissions.</span></span>

<span data-ttu-id="f318a-242">Il nome dell'entità utente deve esistere nella directory associata alla sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="f318a-242">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f318a-243">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="f318a-243">-VaultName</span></span>
<span data-ttu-id="f318a-244">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f318a-244">Specifies the name of a key vault.</span></span>

<span data-ttu-id="f318a-245">Questo cmdlet modifica i criteri di accesso per il Vault chiave specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f318a-245">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f318a-246">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f318a-246">-Confirm</span></span>
<span data-ttu-id="f318a-247">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f318a-247">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f318a-248">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f318a-248">-WhatIf</span></span>
<span data-ttu-id="f318a-249">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f318a-249">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f318a-250">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f318a-250">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f318a-251">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f318a-251">CommonParameters</span></span>
<span data-ttu-id="f318a-252">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f318a-252">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f318a-253">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f318a-253">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f318a-254">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f318a-254">INPUTS</span></span>

### <span data-ttu-id="f318a-255">String, Guid, String [], switch</span><span class="sxs-lookup"><span data-stu-id="f318a-255">String, Guid, String[], Switch</span></span>

## <span data-ttu-id="f318a-256">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f318a-256">OUTPUTS</span></span>

### <span data-ttu-id="f318a-257">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f318a-257">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="f318a-258">Note</span><span class="sxs-lookup"><span data-stu-id="f318a-258">NOTES</span></span>

## <span data-ttu-id="f318a-259">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f318a-259">RELATED LINKS</span></span>

[<span data-ttu-id="f318a-260">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="f318a-260">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="f318a-261">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f318a-261">Remove-AzureRmKeyVaultAccessPolicy</span></span>](./Remove-AzureRmKeyVaultAccessPolicy.md)

