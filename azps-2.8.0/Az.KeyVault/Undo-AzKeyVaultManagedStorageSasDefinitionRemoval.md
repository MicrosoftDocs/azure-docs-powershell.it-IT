---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstoragesasdefinitionremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
ms.openlocfilehash: 7b56e7d251aee8887fe408237d17d275cb87034e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674090"
---
# <span data-ttu-id="df493-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span><span class="sxs-lookup"><span data-stu-id="df493-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span></span>

## <span data-ttu-id="df493-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="df493-102">SYNOPSIS</span></span>
<span data-ttu-id="df493-103">Viene ripristinata una definizione SAS di archiviazione gestita in precedenza eliminata da un Vault.</span><span class="sxs-lookup"><span data-stu-id="df493-103">Recovers a previously deleted KeyVault-managed storage SAS definition.</span></span>

## <span data-ttu-id="df493-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df493-104">SYNTAX</span></span>

### <span data-ttu-id="df493-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="df493-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-VaultName] <String> [-AccountName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df493-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="df493-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-AccountName] <String>
 [-InputObject] <PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df493-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df493-107">DESCRIPTION</span></span>
<span data-ttu-id="df493-108">Il comando **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** recupera una definizione SAS di archiviazione gestita precedentemente eliminata, a condizione che l'eliminazione soft sia abilitata per il Vault e che il tentativo di ripristino si verifichi durante l'intervallo di recupero.</span><span class="sxs-lookup"><span data-stu-id="df493-108">The **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** command recovers a previously deleted managed storage SAS definition, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="df493-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df493-109">EXAMPLES</span></span>

### <span data-ttu-id="df493-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="df493-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName myVault -AccountName myAccount -Name mySasName -InRemovedState
PS C:\> Undo-AzKeyVaultManagedStorageSasDefinitionRemoval -VaultName myVault -AccountName myAccount -Name mySasName

Id          : https://myvault.vault.azure.net:443/storage/myaccount/sas/mysasname
Secret Id   : https://myvault.vault.azure.net/secrets/myaccount-mysasname
Vault Name  : myVault
AccountName : myAccount
Name        : mySasName
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="df493-111">Questa sequenza di comandi determina se la definizione di archiviazione SAS specificata esiste nel Vault in uno stato eliminato; il comando successivo recupera la definizione SAS eliminata e la riporta in uno stato attivo.</span><span class="sxs-lookup"><span data-stu-id="df493-111">This sequence of commands determines whether the specified storage SAS definition exists in the vault in a deleted state; the subsequent command recovers the deleted sas definition, bringing it back into an active state.</span></span>

## <span data-ttu-id="df493-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="df493-112">PARAMETERS</span></span>

### <span data-ttu-id="df493-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="df493-113">-AccountName</span></span>
<span data-ttu-id="df493-114">Nome dell'account di archiviazione gestito con il Vault.</span><span class="sxs-lookup"><span data-stu-id="df493-114">KeyVault-managed storage account name.</span></span>
<span data-ttu-id="df493-115">Cmdlet costruisce il nome di dominio completo di una definizione SAS di archiviazione gestita dal nome della volta, dall'ambiente attualmente selezionato e dall'account di archiviazione gestito.</span><span class="sxs-lookup"><span data-stu-id="df493-115">Cmdlet constructs the FQDN of a managed storage SAS definition from vault name, currently-selected environment and managed storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df493-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df493-116">-DefaultProfile</span></span>
<span data-ttu-id="df493-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="df493-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df493-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df493-118">-InputObject</span></span>
<span data-ttu-id="df493-119">Oggetto definizione SAS di archiviazione gestita eliminata</span><span class="sxs-lookup"><span data-stu-id="df493-119">Deleted managed storage SAS definition object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df493-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="df493-120">-Name</span></span>
<span data-ttu-id="df493-121">Nome della definizione SAS di archiviazione gestita da un Vault.</span><span class="sxs-lookup"><span data-stu-id="df493-121">Name of the KeyVault-managed storage SAS definition.</span></span>
<span data-ttu-id="df493-122">Cmdlet costruisce il nome di dominio completo della destinazione dal nome del Vault, l'ambiente attualmente selezionato, il nome dell'account di archiviazione gestita e quello della definizione SAS.</span><span class="sxs-lookup"><span data-stu-id="df493-122">Cmdlet constructs the FQDN of the target from vault name, currently-selected environment, the name of the managed storage account and the name of the SAS definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df493-123">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="df493-123">-VaultName</span></span>
<span data-ttu-id="df493-124">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="df493-124">Vault name.</span></span>
<span data-ttu-id="df493-125">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="df493-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df493-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="df493-126">-Confirm</span></span>
<span data-ttu-id="df493-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df493-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df493-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df493-128">-WhatIf</span></span>
<span data-ttu-id="df493-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df493-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df493-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df493-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df493-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df493-131">CommonParameters</span></span>
<span data-ttu-id="df493-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df493-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df493-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df493-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df493-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="df493-134">INPUTS</span></span>

### <span data-ttu-id="df493-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="df493-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="df493-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df493-136">OUTPUTS</span></span>

### <span data-ttu-id="df493-137">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="df493-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="df493-138">Note</span><span class="sxs-lookup"><span data-stu-id="df493-138">NOTES</span></span>

## <span data-ttu-id="df493-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df493-139">RELATED LINKS</span></span>
