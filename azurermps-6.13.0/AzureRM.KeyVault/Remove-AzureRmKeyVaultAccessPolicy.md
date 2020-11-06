---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: 343cea9eb3d708e802d1e06f555fd13ab1cd8c13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515200"
---
# <span data-ttu-id="79a02-101">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="79a02-101">Remove-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="79a02-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79a02-102">SYNOPSIS</span></span>
<span data-ttu-id="79a02-103">Rimuove tutte le autorizzazioni per un utente o un'applicazione da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="79a02-103">Removes all permissions for a user or application from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79a02-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79a02-104">SYNTAX</span></span>

### <span data-ttu-id="79a02-105">ByUserPrincipalName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="79a02-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79a02-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="79a02-106">ByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79a02-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="79a02-107">ByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79a02-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="79a02-108">ByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a02-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="79a02-109">ForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a02-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="79a02-110">InputObjectByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a02-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="79a02-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a02-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="79a02-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a02-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="79a02-113">InputObjectByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a02-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="79a02-114">InputObjectForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a02-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="79a02-115">ResourceIdByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a02-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="79a02-116">ResourceIdByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a02-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="79a02-117">ResourceIdByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a02-118">ResourceIdByEmail</span><span class="sxs-lookup"><span data-stu-id="79a02-118">ResourceIdByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a02-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="79a02-119">ResourceIdForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79a02-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79a02-120">DESCRIPTION</span></span>
<span data-ttu-id="79a02-121">Il cmdlet **Remove-AzureRmKeyVaultAccessPolicy** consente di rimuovere tutte le autorizzazioni per un utente o un'applicazione o per tutti gli utenti e le applicazioni da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="79a02-121">The **Remove-AzureRmKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="79a02-122">Anche se si rimuovono tutte le autorizzazioni, il proprietario dell'abbonamento Azure che contiene il Vault chiave può aggiungere le autorizzazioni per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="79a02-122">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>
<span data-ttu-id="79a02-123">Tieni presente che, anche se specificando il gruppo di risorse è facoltativo per questo cmdlet, devi farlo per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="79a02-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="79a02-124">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79a02-124">EXAMPLES</span></span>

### <span data-ttu-id="79a02-125">Esempio 1: rimuovere le autorizzazioni per un utente</span><span class="sxs-lookup"><span data-stu-id="79a02-125">Example 1: Remove permissions for a user</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PassThru

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

<span data-ttu-id="79a02-126">Questo comando rimuove tutte le autorizzazioni che un utente PattiFuller@contoso.com ha sul Vault chiave denominato Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="79a02-126">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>  <span data-ttu-id="79a02-127">Se viene specificato-PassThru, viene restituito l'oggetto Vault.</span><span class="sxs-lookup"><span data-stu-id="79a02-127">If -PassThru is specified, the KeyVault object is returned.</span></span>

### <span data-ttu-id="79a02-128">Esempio 2: rimuovere le autorizzazioni per un'applicazione</span><span class="sxs-lookup"><span data-stu-id="79a02-128">Example 2: Remove permissions for an application</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="79a02-129">Questo comando consente di rimuovere tutte le autorizzazioni di un'applicazione nel Vault chiave denominato Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="79a02-129">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="79a02-130">Questo esempio identifica l'applicazione usando il nome dell'entità servizio registrata in Azure Active Directory http://payroll.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="79a02-130">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="79a02-131">Esempio 3: rimuovere le autorizzazioni per un'applicazione usando l'ID oggetto</span><span class="sxs-lookup"><span data-stu-id="79a02-131">Example 3: Remove permissions for an application by using its object ID</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="79a02-132">Questo comando consente di rimuovere tutte le autorizzazioni di un'applicazione nel Vault chiave denominato Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="79a02-132">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="79a02-133">Questo esempio identifica l'applicazione dall'ID oggetto dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="79a02-133">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="79a02-134">Esempio 4: rimuovere le autorizzazioni per il provider di risorse Microsoft. Compute</span><span class="sxs-lookup"><span data-stu-id="79a02-134">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="79a02-135">Questo comando rimuove l'autorizzazione per il provider di risorse Microsoft. COMPUTE per ottenere i segreti da Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="79a02-135">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="79a02-136">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79a02-136">PARAMETERS</span></span>

### <span data-ttu-id="79a02-137">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="79a02-137">-ApplicationId</span></span>
<span data-ttu-id="79a02-138">Specifica l'ID dell'applicazione di cui devono essere rimosse le autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="79a02-138">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="79a02-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a02-139">-DefaultProfile</span></span>
<span data-ttu-id="79a02-140">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="79a02-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a02-141">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="79a02-141">-EmailAddress</span></span>
<span data-ttu-id="79a02-142">Specifica l'indirizzo di posta elettronica dell'utente di cui si vuole rimuovere l'accesso.</span><span class="sxs-lookup"><span data-stu-id="79a02-142">Specifies the user email address of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="79a02-143">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="79a02-143">-EnabledForDeployment</span></span>
<span data-ttu-id="79a02-144">Se specificato, disattiva il recupero dei segreti da questo Vault chiave dal provider di risorse Microsoft. COMPUTE quando viene fatto riferimento nella creazione di risorse.</span><span class="sxs-lookup"><span data-stu-id="79a02-144">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="79a02-145">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="79a02-145">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="79a02-146">Se specificato, disattiva il recupero dei segreti da questo Vault chiave tramite la crittografia di Azure disk.</span><span class="sxs-lookup"><span data-stu-id="79a02-146">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="79a02-147">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="79a02-147">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="79a02-148">Se specificato, disattiva il recupero dei segreti da questo Vault chiave da Gestione risorse di Azure quando viene fatto riferimento nei modelli.</span><span class="sxs-lookup"><span data-stu-id="79a02-148">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="79a02-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79a02-149">-InputObject</span></span>
<span data-ttu-id="79a02-150">Oggetto Key Vault.</span><span class="sxs-lookup"><span data-stu-id="79a02-150">Key Vault object.</span></span>

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

### <span data-ttu-id="79a02-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="79a02-151">-ObjectId</span></span>
<span data-ttu-id="79a02-152">Specifica l'ID oggetto dell'entità di servizio o dell'utente in Azure Active Directory per cui rimuovere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="79a02-152">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="79a02-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79a02-153">-PassThru</span></span>
<span data-ttu-id="79a02-154">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="79a02-154">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="79a02-155">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="79a02-155">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="79a02-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79a02-156">-ResourceGroupName</span></span>
<span data-ttu-id="79a02-157">Specifica il nome del gruppo di risorse associato alla volta chiave in cui vengono modificati i criteri di accesso.</span><span class="sxs-lookup"><span data-stu-id="79a02-157">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="79a02-158">Se non viene specificato, questo cmdlet cerca il Vault chiave nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="79a02-158">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

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

### <span data-ttu-id="79a02-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79a02-159">-ResourceId</span></span>
<span data-ttu-id="79a02-160">ID risorsa di un Vault.</span><span class="sxs-lookup"><span data-stu-id="79a02-160">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="79a02-161">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="79a02-161">-ServicePrincipalName</span></span>
<span data-ttu-id="79a02-162">Specifica il nome dell'entità servizio dell'applicazione di cui si vogliono rimuovere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="79a02-162">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="79a02-163">Specificare l'ID applicazione, noto anche come ID client, registrato per l'applicazione in Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="79a02-163">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="79a02-164">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="79a02-164">-UserPrincipalName</span></span>
<span data-ttu-id="79a02-165">Specifica il nome dell'entità utente dell'utente di cui si vuole rimuovere l'accesso.</span><span class="sxs-lookup"><span data-stu-id="79a02-165">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="79a02-166">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="79a02-166">-VaultName</span></span>
<span data-ttu-id="79a02-167">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="79a02-167">Specifies the name of the key vault.</span></span>
<span data-ttu-id="79a02-168">Questo cmdlet consente di rimuovere le autorizzazioni per il Vault chiave specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="79a02-168">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="79a02-169">-Confermare</span><span class="sxs-lookup"><span data-stu-id="79a02-169">-Confirm</span></span>
<span data-ttu-id="79a02-170">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79a02-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79a02-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79a02-171">-WhatIf</span></span>
<span data-ttu-id="79a02-172">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79a02-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79a02-173">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79a02-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79a02-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a02-174">CommonParameters</span></span>
<span data-ttu-id="79a02-175">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79a02-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a02-176">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79a02-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a02-177">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79a02-177">INPUTS</span></span>

### <span data-ttu-id="79a02-178">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="79a02-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="79a02-179">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="79a02-179">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="79a02-180">System. String</span><span class="sxs-lookup"><span data-stu-id="79a02-180">System.String</span></span>

## <span data-ttu-id="79a02-181">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79a02-181">OUTPUTS</span></span>

### <span data-ttu-id="79a02-182">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="79a02-182">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="79a02-183">Note</span><span class="sxs-lookup"><span data-stu-id="79a02-183">NOTES</span></span>

## <span data-ttu-id="79a02-184">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79a02-184">RELATED LINKS</span></span>

[<span data-ttu-id="79a02-185">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="79a02-185">Set-AzureRmKeyVaultAccessPolicy</span></span>](./Set-AzureRmKeyVaultAccessPolicy.md)

