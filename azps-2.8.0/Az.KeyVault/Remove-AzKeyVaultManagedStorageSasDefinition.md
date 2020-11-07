---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 0fe20196f805f292ecc6b351fbb9138c6617bb4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674123"
---
# <span data-ttu-id="8729e-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="8729e-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="8729e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8729e-102">SYNOPSIS</span></span>
<span data-ttu-id="8729e-103">Consente di rimuovere una chiave di archiviazione delle definizioni SAS storage di Azure.</span><span class="sxs-lookup"><span data-stu-id="8729e-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="8729e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8729e-104">SYNTAX</span></span>

### <span data-ttu-id="8729e-105">ByDefinitionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8729e-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8729e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8729e-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8729e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8729e-107">DESCRIPTION</span></span>
<span data-ttu-id="8729e-108">Consente di rimuovere una chiave di archiviazione delle definizioni SAS storage di Azure.</span><span class="sxs-lookup"><span data-stu-id="8729e-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="8729e-109">Viene inoltre rimosso il segreto usato per ottenere il token SAS per la definizione SAS.</span><span class="sxs-lookup"><span data-stu-id="8729e-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="8729e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8729e-110">EXAMPLES</span></span>

### <span data-ttu-id="8729e-111">Esempio 1: rimuovere una definizione della chiave di archiviazione di Azure gestita da Key Vault.</span><span class="sxs-lookup"><span data-stu-id="8729e-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="8729e-112">Consente di rimuovere una definizione SAS di archiviazione gestita Key Vault mysasdef associata all'account "mystorageaccount" nel Vault "Vault".</span><span class="sxs-lookup"><span data-stu-id="8729e-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="8729e-113">Esempio 2: rimuovere una definizione della chiave archiviata di Azure storage SAS senza la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8729e-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru -Force

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="8729e-114">Consente di rimuovere una definizione SAS di archiviazione gestita Key Vault mysasdef associata all'account "mystorageaccount" nel Vault "Vault".</span><span class="sxs-lookup"><span data-stu-id="8729e-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="8729e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8729e-115">PARAMETERS</span></span>

### <span data-ttu-id="8729e-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8729e-116">-AccountName</span></span>
<span data-ttu-id="8729e-117">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8729e-117">Storage account name.</span></span>
<span data-ttu-id="8729e-118">Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, l'ambiente selezionato e il nome dell'account di archiviazione corrente.</span><span class="sxs-lookup"><span data-stu-id="8729e-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

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

### <span data-ttu-id="8729e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8729e-119">-DefaultProfile</span></span>
<span data-ttu-id="8729e-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8729e-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8729e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8729e-121">-Force</span></span>
<span data-ttu-id="8729e-122">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="8729e-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8729e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8729e-123">-InputObject</span></span>
<span data-ttu-id="8729e-124">Oggetto ManagedStorageSasDefinition.</span><span class="sxs-lookup"><span data-stu-id="8729e-124">ManagedStorageSasDefinition object.</span></span>

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

### <span data-ttu-id="8729e-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="8729e-125">-Name</span></span>
<span data-ttu-id="8729e-126">Nome della definizione di archiviazione SAS.</span><span class="sxs-lookup"><span data-stu-id="8729e-126">Storage sas definition name.</span></span>
<span data-ttu-id="8729e-127">Cmdlet costruisce il nome di dominio completo di una definizione SAS di archiviazione dal nome della volta, dall'ambiente attualmente selezionato, dal nome dell'account di archiviazione e dalla definizione SAS.</span><span class="sxs-lookup"><span data-stu-id="8729e-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="8729e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8729e-128">-PassThru</span></span>
<span data-ttu-id="8729e-129">Cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="8729e-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="8729e-130">Se questa opzione è specificata, cmdlet restituisce l'account di archiviazione gestita che è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="8729e-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="8729e-131">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="8729e-131">-VaultName</span></span>
<span data-ttu-id="8729e-132">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="8729e-132">Vault name.</span></span>
<span data-ttu-id="8729e-133">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="8729e-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8729e-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8729e-134">-Confirm</span></span>
<span data-ttu-id="8729e-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8729e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8729e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8729e-136">-WhatIf</span></span>
<span data-ttu-id="8729e-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8729e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8729e-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8729e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8729e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8729e-139">CommonParameters</span></span>
<span data-ttu-id="8729e-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8729e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8729e-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8729e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8729e-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8729e-142">INPUTS</span></span>

### <span data-ttu-id="8729e-143">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8729e-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="8729e-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8729e-144">OUTPUTS</span></span>

### <span data-ttu-id="8729e-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="8729e-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="8729e-146">Note</span><span class="sxs-lookup"><span data-stu-id="8729e-146">NOTES</span></span>

## <span data-ttu-id="8729e-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8729e-147">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

