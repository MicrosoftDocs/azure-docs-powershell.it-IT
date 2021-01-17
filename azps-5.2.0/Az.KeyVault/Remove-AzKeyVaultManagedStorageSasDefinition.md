---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 392c8aa5259419851d3cb85967ddf85afa3c94de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328126"
---
# <span data-ttu-id="e930a-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="e930a-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="e930a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e930a-102">SYNOPSIS</span></span>
<span data-ttu-id="e930a-103">Consente di rimuovere una chiave di archiviazione delle definizioni SAS storage di Azure.</span><span class="sxs-lookup"><span data-stu-id="e930a-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="e930a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e930a-104">SYNTAX</span></span>

### <span data-ttu-id="e930a-105">ByDefinitionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e930a-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e930a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e930a-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e930a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e930a-107">DESCRIPTION</span></span>
<span data-ttu-id="e930a-108">Consente di rimuovere una chiave di archiviazione delle definizioni SAS storage di Azure.</span><span class="sxs-lookup"><span data-stu-id="e930a-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="e930a-109">Viene inoltre rimosso il segreto usato per ottenere il token SAS per la definizione SAS.</span><span class="sxs-lookup"><span data-stu-id="e930a-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="e930a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e930a-110">EXAMPLES</span></span>

### <span data-ttu-id="e930a-111">Esempio 1: rimuovere una definizione della chiave di archiviazione di Azure gestita da Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e930a-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
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

<span data-ttu-id="e930a-112">Consente di rimuovere una definizione SAS di archiviazione gestita Key Vault mysasdef associata all'account "mystorageaccount" nel Vault "Vault".</span><span class="sxs-lookup"><span data-stu-id="e930a-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="e930a-113">Esempio 2: rimuovere una definizione della chiave archiviata di Azure storage SAS senza la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e930a-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
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

<span data-ttu-id="e930a-114">Consente di rimuovere una definizione SAS di archiviazione gestita Key Vault mysasdef associata all'account "mystorageaccount" nel Vault "Vault".</span><span class="sxs-lookup"><span data-stu-id="e930a-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="e930a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e930a-115">PARAMETERS</span></span>

### <span data-ttu-id="e930a-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e930a-116">-AccountName</span></span>
<span data-ttu-id="e930a-117">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e930a-117">Storage account name.</span></span>
<span data-ttu-id="e930a-118">Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, l'ambiente selezionato e il nome dell'account di archiviazione corrente.</span><span class="sxs-lookup"><span data-stu-id="e930a-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

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

### <span data-ttu-id="e930a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e930a-119">-DefaultProfile</span></span>
<span data-ttu-id="e930a-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e930a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e930a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e930a-121">-Force</span></span>
<span data-ttu-id="e930a-122">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="e930a-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e930a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e930a-123">-InputObject</span></span>
<span data-ttu-id="e930a-124">Oggetto ManagedStorageSasDefinition.</span><span class="sxs-lookup"><span data-stu-id="e930a-124">ManagedStorageSasDefinition object.</span></span>

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

### <span data-ttu-id="e930a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="e930a-125">-Name</span></span>
<span data-ttu-id="e930a-126">Nome della definizione di archiviazione SAS.</span><span class="sxs-lookup"><span data-stu-id="e930a-126">Storage sas definition name.</span></span>
<span data-ttu-id="e930a-127">Cmdlet costruisce il nome di dominio completo di una definizione SAS di archiviazione dal nome della volta, dall'ambiente attualmente selezionato, dal nome dell'account di archiviazione e dalla definizione SAS.</span><span class="sxs-lookup"><span data-stu-id="e930a-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="e930a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e930a-128">-PassThru</span></span>
<span data-ttu-id="e930a-129">Cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e930a-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e930a-130">Se questa opzione è specificata, cmdlet restituisce l'account di archiviazione gestita che è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="e930a-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="e930a-131">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="e930a-131">-VaultName</span></span>
<span data-ttu-id="e930a-132">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="e930a-132">Vault name.</span></span>
<span data-ttu-id="e930a-133">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="e930a-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e930a-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e930a-134">-Confirm</span></span>
<span data-ttu-id="e930a-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e930a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e930a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e930a-136">-WhatIf</span></span>
<span data-ttu-id="e930a-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e930a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e930a-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e930a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e930a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e930a-139">CommonParameters</span></span>
<span data-ttu-id="e930a-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e930a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e930a-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e930a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e930a-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e930a-142">INPUTS</span></span>

### <span data-ttu-id="e930a-143">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e930a-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="e930a-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e930a-144">OUTPUTS</span></span>

### <span data-ttu-id="e930a-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="e930a-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="e930a-146">Note</span><span class="sxs-lookup"><span data-stu-id="e930a-146">NOTES</span></span>

## <span data-ttu-id="e930a-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e930a-147">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

