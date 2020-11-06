---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: ca175d0873b74d8b13d1755f3d0986580c5853ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518092"
---
# <span data-ttu-id="924d4-101">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="924d4-101">Remove-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="924d4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="924d4-102">SYNOPSIS</span></span>
<span data-ttu-id="924d4-103">Rimuove tutte le autorizzazioni per un utente o un'applicazione da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="924d4-103">Removes all permissions for a user or application from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="924d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="924d4-104">SYNTAX</span></span>

### <span data-ttu-id="924d4-105">ByUserPrincipalName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="924d4-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="924d4-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="924d4-106">ByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="924d4-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="924d4-107">ByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="924d4-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="924d4-108">ByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="924d4-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="924d4-109">ForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="924d4-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="924d4-110">InputObjectByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="924d4-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="924d4-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="924d4-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="924d4-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="924d4-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="924d4-113">InputObjectByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="924d4-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="924d4-114">InputObjectForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="924d4-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="924d4-115">DESCRIPTION</span></span>
<span data-ttu-id="924d4-116">Il cmdlet **Remove-AzureRmKeyVaultAccessPolicy** consente di rimuovere tutte le autorizzazioni per un utente o un'applicazione o per tutti gli utenti e le applicazioni da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="924d4-116">The **Remove-AzureRmKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="924d4-117">Anche se si rimuovono tutte le autorizzazioni, il proprietario dell'abbonamento Azure che contiene il Vault chiave può aggiungere le autorizzazioni per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="924d4-117">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>

<span data-ttu-id="924d4-118">Tieni presente che, anche se specificando il gruppo di risorse è facoltativo per questo cmdlet, devi farlo per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="924d4-118">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="924d4-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="924d4-119">EXAMPLES</span></span>

### <span data-ttu-id="924d4-120">Esempio 1: rimuovere le autorizzazioni per un utente</span><span class="sxs-lookup"><span data-stu-id="924d4-120">Example 1: Remove permissions for a user</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

<span data-ttu-id="924d4-121">Questo comando rimuove tutte le autorizzazioni che un utente PattiFuller@contoso.com ha sul Vault chiave denominato Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="924d4-121">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>

### <span data-ttu-id="924d4-122">Esempio 2: rimuovere le autorizzazioni per un'applicazione</span><span class="sxs-lookup"><span data-stu-id="924d4-122">Example 2: Remove permissions for an application</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="924d4-123">Questo comando consente di rimuovere tutte le autorizzazioni di un'applicazione nel Vault chiave denominato Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="924d4-123">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="924d4-124">Questo esempio identifica l'applicazione usando il nome dell'entità servizio registrata in Azure Active Directory http://payroll.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="924d4-124">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="924d4-125">Esempio 3: rimuovere le autorizzazioni per un'applicazione usando l'ID oggetto</span><span class="sxs-lookup"><span data-stu-id="924d4-125">Example 3: Remove permissions for an application by using its object ID</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="924d4-126">Questo comando consente di rimuovere tutte le autorizzazioni di un'applicazione nel Vault chiave denominato Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="924d4-126">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="924d4-127">Questo esempio identifica l'applicazione dall'ID oggetto dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="924d4-127">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="924d4-128">Esempio 4: rimuovere le autorizzazioni per il provider di risorse Microsoft. Compute</span><span class="sxs-lookup"><span data-stu-id="924d4-128">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="924d4-129">Questo comando rimuove l'autorizzazione per il provider di risorse Microsoft. COMPUTE per ottenere i segreti da Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="924d4-129">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="924d4-130">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="924d4-130">PARAMETERS</span></span>

### <span data-ttu-id="924d4-131">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="924d4-131">-ApplicationId</span></span>
<span data-ttu-id="924d4-132">Specifica l'ID dell'applicazione di cui devono essere rimosse le autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="924d4-132">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="924d4-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="924d4-133">-DefaultProfile</span></span>
<span data-ttu-id="924d4-134">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="924d4-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="924d4-135">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="924d4-135">-EmailAddress</span></span>
<span data-ttu-id="924d4-136">Specifica l'indirizzo di posta elettronica dell'utente di cui si vuole rimuovere l'accesso.</span><span class="sxs-lookup"><span data-stu-id="924d4-136">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByEmail, InputObjectByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="924d4-137">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="924d4-137">-EnabledForDeployment</span></span>
<span data-ttu-id="924d4-138">Se specificato, disattiva il recupero dei segreti da questo Vault chiave dal provider di risorse Microsoft. COMPUTE quando viene fatto riferimento nella creazione di risorse.</span><span class="sxs-lookup"><span data-stu-id="924d4-138">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="924d4-139">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="924d4-139">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="924d4-140">Se specificato, disattiva il recupero dei segreti da questo Vault chiave tramite la crittografia di Azure disk.</span><span class="sxs-lookup"><span data-stu-id="924d4-140">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="924d4-141">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="924d4-141">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="924d4-142">Se specificato, disattiva il recupero dei segreti da questo Vault chiave da Gestione risorse di Azure quando viene fatto riferimento nei modelli.</span><span class="sxs-lookup"><span data-stu-id="924d4-142">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="924d4-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="924d4-143">-InputObject</span></span>
<span data-ttu-id="924d4-144">Oggetto Key Vault.</span><span class="sxs-lookup"><span data-stu-id="924d4-144">Key Vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmail, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="924d4-145">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="924d4-145">-ObjectId</span></span>
<span data-ttu-id="924d4-146">Specifica l'ID oggetto dell'entità di servizio o dell'utente in Azure Active Directory per cui rimuovere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="924d4-146">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="924d4-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="924d4-147">-PassThru</span></span>
<span data-ttu-id="924d4-148">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="924d4-148">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="924d4-149">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="924d4-149">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="924d4-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="924d4-150">-ResourceGroupName</span></span>
<span data-ttu-id="924d4-151">Specifica il nome del gruppo di risorse associato alla volta chiave in cui vengono modificati i criteri di accesso.</span><span class="sxs-lookup"><span data-stu-id="924d4-151">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="924d4-152">Se non viene specificato, questo cmdlet cerca il Vault chiave nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="924d4-152">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="924d4-153">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="924d4-153">-ServicePrincipalName</span></span>
<span data-ttu-id="924d4-154">Specifica il nome dell'entità servizio dell'applicazione di cui si vogliono rimuovere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="924d4-154">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="924d4-155">Specificare l'ID applicazione, noto anche come ID client, registrato per l'applicazione in Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="924d4-155">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="924d4-156">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="924d4-156">-UserPrincipalName</span></span>
<span data-ttu-id="924d4-157">Specifica il nome dell'entità utente dell'utente di cui si vuole rimuovere l'accesso.</span><span class="sxs-lookup"><span data-stu-id="924d4-157">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="924d4-158">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="924d4-158">-VaultName</span></span>
<span data-ttu-id="924d4-159">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="924d4-159">Specifies the name of the key vault.</span></span>
<span data-ttu-id="924d4-160">Questo cmdlet consente di rimuovere le autorizzazioni per il Vault chiave specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="924d4-160">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="924d4-161">-Confermare</span><span class="sxs-lookup"><span data-stu-id="924d4-161">-Confirm</span></span>
<span data-ttu-id="924d4-162">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="924d4-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="924d4-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="924d4-163">-WhatIf</span></span>
<span data-ttu-id="924d4-164">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="924d4-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="924d4-165">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="924d4-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="924d4-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="924d4-166">CommonParameters</span></span>
<span data-ttu-id="924d4-167">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="924d4-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="924d4-168">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="924d4-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="924d4-169">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="924d4-169">INPUTS</span></span>

### <span data-ttu-id="924d4-170">Nessuno</span><span class="sxs-lookup"><span data-stu-id="924d4-170">None</span></span>
<span data-ttu-id="924d4-171">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="924d4-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="924d4-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="924d4-172">OUTPUTS</span></span>

### <span data-ttu-id="924d4-173">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="924d4-173">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="924d4-174">Note</span><span class="sxs-lookup"><span data-stu-id="924d4-174">NOTES</span></span>

## <span data-ttu-id="924d4-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="924d4-175">RELATED LINKS</span></span>

[<span data-ttu-id="924d4-176">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="924d4-176">Set-AzureRmKeyVaultAccessPolicy</span></span>](./Set-AzureRmKeyVaultAccessPolicy.md)

