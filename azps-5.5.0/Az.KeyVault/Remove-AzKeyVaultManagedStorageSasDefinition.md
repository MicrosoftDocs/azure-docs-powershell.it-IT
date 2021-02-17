---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 392c8aa5259419851d3cb85967ddf85afa3c94de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192350"
---
# <span data-ttu-id="7956a-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="7956a-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="7956a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7956a-102">SYNOPSIS</span></span>
<span data-ttu-id="7956a-103">Rimuove le definizioni della firma di accesso condiviso di Archiviazione di Azure gestite da Vault.</span><span class="sxs-lookup"><span data-stu-id="7956a-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="7956a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7956a-104">SYNTAX</span></span>

### <span data-ttu-id="7956a-105">ByDefinitionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7956a-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7956a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7956a-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7956a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7956a-107">DESCRIPTION</span></span>
<span data-ttu-id="7956a-108">Rimuove le definizioni della firma di accesso condiviso di Archiviazione di Azure gestite da Vault.</span><span class="sxs-lookup"><span data-stu-id="7956a-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="7956a-109">In questo modo viene rimosso anche il segreto usato per ottenere il token di firma di accesso condiviso in base a questa definizione di firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="7956a-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="7956a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7956a-110">EXAMPLES</span></span>

### <span data-ttu-id="7956a-111">Esempio 1: Rimuovere una definizione di firma di accesso condiviso di Archiviazione di Azure gestita da Vault.</span><span class="sxs-lookup"><span data-stu-id="7956a-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="7956a-112">Rimuove una definizione di firma di accesso condiviso gestita dal Vault delle chiavi 'mysasdef' associata all'account 'mystorageaccount' nel vault 'myvault'.</span><span class="sxs-lookup"><span data-stu-id="7956a-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="7956a-113">Esempio 2: Rimuovere una definizione di firma di accesso condiviso di Archiviazione di Azure gestita dal Vault senza conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7956a-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru -Force

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="7956a-114">Rimuove una definizione di firma di accesso condiviso gestita dal Vault delle chiavi 'mysasdef' associata all'account 'mystorageaccount' nel vault 'myvault'.</span><span class="sxs-lookup"><span data-stu-id="7956a-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="7956a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7956a-115">PARAMETERS</span></span>

### <span data-ttu-id="7956a-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7956a-116">-AccountName</span></span>
<span data-ttu-id="7956a-117">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7956a-117">Storage account name.</span></span>
<span data-ttu-id="7956a-118">Il cmdlet crea l'FQDN di un account di archiviazione gestito dal nome del vault, l'ambiente e il nome dell'account di archiviazione attualmente selezionati.</span><span class="sxs-lookup"><span data-stu-id="7956a-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7956a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7956a-119">-DefaultProfile</span></span>
<span data-ttu-id="7956a-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="7956a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7956a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7956a-121">-Force</span></span>
<span data-ttu-id="7956a-122">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="7956a-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7956a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7956a-123">-InputObject</span></span>
<span data-ttu-id="7956a-124">Oggetto ManagedStorageSasDefinition.</span><span class="sxs-lookup"><span data-stu-id="7956a-124">ManagedStorageSasDefinition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7956a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7956a-125">-Name</span></span>
<span data-ttu-id="7956a-126">Nome della definizione della firma di accesso condiviso per l'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7956a-126">Storage sas definition name.</span></span>
<span data-ttu-id="7956a-127">Il cmdlet crea l'FQDN di una definizione di firma di accesso condiviso per l'archiviazione dal nome del vault, dall'ambiente attualmente selezionato, dal nome dell'account di archiviazione e dal nome della definizione della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="7956a-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7956a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7956a-128">-PassThru</span></span>
<span data-ttu-id="7956a-129">Il cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7956a-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7956a-130">Se si specifica questa opzione, il cmdlet restituisce l'account di archiviazione gestito eliminato.</span><span class="sxs-lookup"><span data-stu-id="7956a-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="7956a-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7956a-131">-VaultName</span></span>
<span data-ttu-id="7956a-132">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="7956a-132">Vault name.</span></span>
<span data-ttu-id="7956a-133">Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="7956a-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7956a-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7956a-134">-Confirm</span></span>
<span data-ttu-id="7956a-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7956a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7956a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7956a-136">-WhatIf</span></span>
<span data-ttu-id="7956a-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7956a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7956a-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7956a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7956a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7956a-139">CommonParameters</span></span>
<span data-ttu-id="7956a-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7956a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7956a-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7956a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7956a-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="7956a-142">INPUTS</span></span>

### <span data-ttu-id="7956a-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7956a-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="7956a-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7956a-144">OUTPUTS</span></span>

### <span data-ttu-id="7956a-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="7956a-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="7956a-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="7956a-146">NOTES</span></span>

## <span data-ttu-id="7956a-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7956a-147">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

