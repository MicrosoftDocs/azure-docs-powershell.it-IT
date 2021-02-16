---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: e19565aa8ae249acf61fce67f0a2b54e20143758
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209290"
---
# <span data-ttu-id="f8a47-101">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f8a47-101">Remove-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="f8a47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8a47-102">SYNOPSIS</span></span>
<span data-ttu-id="f8a47-103">Rimuove tutte le autorizzazioni per un utente o un'applicazione da un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="f8a47-103">Removes all permissions for a user or application from a key vault.</span></span>

## <span data-ttu-id="f8a47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8a47-104">SYNTAX</span></span>

### <span data-ttu-id="f8a47-105">ByUserPrincipalName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f8a47-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8a47-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="f8a47-106">ByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8a47-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f8a47-107">ByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8a47-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="f8a47-108">ByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8a47-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="f8a47-109">ForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8a47-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="f8a47-110">InputObjectByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8a47-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f8a47-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8a47-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f8a47-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8a47-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="f8a47-113">InputObjectByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8a47-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="f8a47-114">InputObjectForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8a47-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="f8a47-115">ResourceIdByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8a47-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f8a47-116">ResourceIdByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8a47-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f8a47-117">ResourceIdByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8a47-118">ResourceIdByEmail</span><span class="sxs-lookup"><span data-stu-id="f8a47-118">ResourceIdByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8a47-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="f8a47-119">ResourceIdForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8a47-120">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f8a47-120">DESCRIPTION</span></span>
<span data-ttu-id="f8a47-121">Il cmdlet **Remove-AzKeyVaultAccessPolicy** rimuove tutte le autorizzazioni per un utente o un'applicazione o per tutti gli utenti e le applicazioni da un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="f8a47-121">The **Remove-AzKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="f8a47-122">Anche se si rimuovono tutte le autorizzazioni, il proprietario della sottoscrizione di Azure che contiene il vault della chiave può aggiungere autorizzazioni al vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="f8a47-122">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>
<span data-ttu-id="f8a47-123">Anche se è facoltativo specificare il gruppo di risorse per questo cmdlet, è consigliabile farlo per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="f8a47-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="f8a47-124">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8a47-124">EXAMPLES</span></span>

### <span data-ttu-id="f8a47-125">Esempio 1: Rimuovere le autorizzazioni per un utente</span><span class="sxs-lookup"><span data-stu-id="f8a47-125">Example 1: Remove permissions for a user</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     :
                                   Permissions to Certificates                : get, create
                                   Permissions to (Key Vault Managed) Storage :


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   :
                                   Virtual Network Rules                      :

Tags                             :
```

<span data-ttu-id="f8a47-126">Questo comando rimuove tutte le autorizzazioni di un utente nella chiave PattiFuller@contoso.com vault denominata Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="f8a47-126">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>  <span data-ttu-id="f8a47-127">Se si imposta -PassThru, viene restituito l'oggetto KeyVault.</span><span class="sxs-lookup"><span data-stu-id="f8a47-127">If -PassThru is specified, the KeyVault object is returned.</span></span>

### <span data-ttu-id="f8a47-128">Esempio 2: Rimuovere le autorizzazioni per un'applicazione</span><span class="sxs-lookup"><span data-stu-id="f8a47-128">Example 2: Remove permissions for an application</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="f8a47-129">Questo comando rimuove tutte le autorizzazioni di un'applicazione sulla chiave vault denominata Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="f8a47-129">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="f8a47-130">Questo esempio identifica l'applicazione usando il nome dell'entità servizio registrato in Azure Active `http://payroll.contoso.com` Directory.</span><span class="sxs-lookup"><span data-stu-id="f8a47-130">This example identifies the application by using the service principal name registered in Azure Active Directory, `http://payroll.contoso.com`.</span></span>

### <span data-ttu-id="f8a47-131">Esempio 3: Rimuovere le autorizzazioni per un'applicazione usando l'ID oggetto</span><span class="sxs-lookup"><span data-stu-id="f8a47-131">Example 3: Remove permissions for an application by using its object ID</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="f8a47-132">Questo comando rimuove tutte le autorizzazioni di un'applicazione sulla chiave vault denominata Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="f8a47-132">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="f8a47-133">Questo esempio identifica l'applicazione in base all'ID oggetto dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="f8a47-133">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="f8a47-134">Esempio 4: Rimuovere le autorizzazioni per il provider di risorse Microsoft.Compute</span><span class="sxs-lookup"><span data-stu-id="f8a47-134">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="f8a47-135">Questo comando rimuove l'autorizzazione per il provider di risorse Microsoft.Compute per ottenere informazioni segrete da Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="f8a47-135">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="f8a47-136">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8a47-136">PARAMETERS</span></span>

### <span data-ttu-id="f8a47-137">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f8a47-137">-ApplicationId</span></span>
<span data-ttu-id="f8a47-138">Specifica l'ID dell'applicazione di cui rimuovere le autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="f8a47-138">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="f8a47-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8a47-139">-DefaultProfile</span></span>
<span data-ttu-id="f8a47-140">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="f8a47-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8a47-141">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="f8a47-141">-EmailAddress</span></span>
<span data-ttu-id="f8a47-142">Specifica l'indirizzo di posta elettronica dell'utente di cui si vuole rimuovere l'accesso.</span><span class="sxs-lookup"><span data-stu-id="f8a47-142">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmail, InputObjectByEmail, ResourceIdByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8a47-143">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="f8a47-143">-EnabledForDeployment</span></span>
<span data-ttu-id="f8a47-144">Se specificato, disabilita il recupero dei dati nascosti da questo vault della chiave da parte del provider di risorse Microsoft.Compute quando si fa riferimento nella creazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="f8a47-144">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="f8a47-145">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="f8a47-145">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="f8a47-146">Se specificato, disabilita il recupero dei dati nascosti da questo vault della chiave tramite Crittografia disco di Azure.</span><span class="sxs-lookup"><span data-stu-id="f8a47-146">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="f8a47-147">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="f8a47-147">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="f8a47-148">Se specificato, disabilita il recupero di informazioni segrete da questo vault della chiave da parte di Gestione risorse di Azure quando viene fatto riferimento nei modelli.</span><span class="sxs-lookup"><span data-stu-id="f8a47-148">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="f8a47-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8a47-149">-InputObject</span></span>
<span data-ttu-id="f8a47-150">Oggetto Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f8a47-150">Key Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmail, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8a47-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f8a47-151">-ObjectId</span></span>
<span data-ttu-id="f8a47-152">Specifica l'ID oggetto dell'utente o dell'entità servizio in Azure Active Directory per cui rimuovere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="f8a47-152">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="f8a47-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8a47-153">-PassThru</span></span>
<span data-ttu-id="f8a47-154">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="f8a47-154">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f8a47-155">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="f8a47-155">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f8a47-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8a47-156">-ResourceGroupName</span></span>
<span data-ttu-id="f8a47-157">Specifica il nome del gruppo di risorse associato alla chiave vault di cui si stanno modificando i criteri di accesso.</span><span class="sxs-lookup"><span data-stu-id="f8a47-157">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="f8a47-158">Se non è specificato, questo cmdlet cerca il vault delle chiavi nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="f8a47-158">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8a47-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8a47-159">-ResourceId</span></span>
<span data-ttu-id="f8a47-160">ID risorsa KeyVault.</span><span class="sxs-lookup"><span data-stu-id="f8a47-160">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmail, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8a47-161">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f8a47-161">-ServicePrincipalName</span></span>
<span data-ttu-id="f8a47-162">Specifica il nome dell'entità servizio dell'applicazione di cui si vogliono rimuovere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="f8a47-162">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="f8a47-163">Specificare l'ID applicazione, noto anche come ID client, registrato per l'applicazione in Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f8a47-163">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="f8a47-164">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f8a47-164">-UserPrincipalName</span></span>
<span data-ttu-id="f8a47-165">Specifica il nome dell'entità utente dell'utente di cui si vuole rimuovere l'accesso.</span><span class="sxs-lookup"><span data-stu-id="f8a47-165">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="f8a47-166">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f8a47-166">-VaultName</span></span>
<span data-ttu-id="f8a47-167">Specifica il nome del vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="f8a47-167">Specifies the name of the key vault.</span></span>
<span data-ttu-id="f8a47-168">Questo cmdlet rimuove le autorizzazioni per il vault delle chiavi specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f8a47-168">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8a47-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8a47-169">-Confirm</span></span>
<span data-ttu-id="f8a47-170">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8a47-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8a47-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8a47-171">-WhatIf</span></span>
<span data-ttu-id="f8a47-172">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8a47-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8a47-173">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8a47-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8a47-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8a47-174">CommonParameters</span></span>
<span data-ttu-id="f8a47-175">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8a47-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8a47-176">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f8a47-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8a47-177">INPUT</span><span class="sxs-lookup"><span data-stu-id="f8a47-177">INPUTS</span></span>

### <span data-ttu-id="f8a47-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f8a47-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="f8a47-179">System.String</span><span class="sxs-lookup"><span data-stu-id="f8a47-179">System.String</span></span>

## <span data-ttu-id="f8a47-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8a47-180">OUTPUTS</span></span>

### <span data-ttu-id="f8a47-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f8a47-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="f8a47-182">NOTE</span><span class="sxs-lookup"><span data-stu-id="f8a47-182">NOTES</span></span>

## <span data-ttu-id="f8a47-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8a47-183">RELATED LINKS</span></span>

[<span data-ttu-id="f8a47-184">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f8a47-184">Set-AzKeyVaultAccessPolicy</span></span>](./Set-AzKeyVaultAccessPolicy.md)

