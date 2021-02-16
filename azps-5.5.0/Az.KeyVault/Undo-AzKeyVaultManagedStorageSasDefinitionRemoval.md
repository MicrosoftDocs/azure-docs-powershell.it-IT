---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstoragesasdefinitionremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
ms.openlocfilehash: bb44bc8f5e4537691d1e5d5493a29111ceaf42a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185446"
---
# <span data-ttu-id="eabce-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span><span class="sxs-lookup"><span data-stu-id="eabce-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span></span>

## <span data-ttu-id="eabce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eabce-102">SYNOPSIS</span></span>
<span data-ttu-id="eabce-103">Recupera una definizione di firma di accesso condiviso per l'archiviazione gestita da KeyVault eliminata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="eabce-103">Recovers a previously deleted KeyVault-managed storage SAS definition.</span></span>

## <span data-ttu-id="eabce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eabce-104">SYNTAX</span></span>

### <span data-ttu-id="eabce-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eabce-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-VaultName] <String> [-AccountName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eabce-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="eabce-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-AccountName] <String>
 [-InputObject] <PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eabce-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eabce-107">DESCRIPTION</span></span>
<span data-ttu-id="eabce-108">Il comando **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** recupera una definizione di firma di accesso condiviso per l'archiviazione gestita eliminata in precedenza, a condizione che l'eliminazione reversibile sia abilitata per il vault e che il tentativo di recupero sia eseguito durante l'intervallo di recupero.</span><span class="sxs-lookup"><span data-stu-id="eabce-108">The **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** command recovers a previously deleted managed storage SAS definition, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="eabce-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eabce-109">EXAMPLES</span></span>

### <span data-ttu-id="eabce-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eabce-110">Example 1</span></span>
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

<span data-ttu-id="eabce-111">Questa sequenza di comandi determina se la definizione della firma di accesso condiviso di archiviazione specificata esiste nell'insieme di credenziali in stato di eliminazione; Il comando successivo recupera la definizione di sas eliminata e la riporta allo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="eabce-111">This sequence of commands determines whether the specified storage SAS definition exists in the vault in a deleted state; the subsequent command recovers the deleted sas definition, bringing it back into an active state.</span></span>

## <span data-ttu-id="eabce-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eabce-112">PARAMETERS</span></span>

### <span data-ttu-id="eabce-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eabce-113">-AccountName</span></span>
<span data-ttu-id="eabce-114">Nome dell'account di archiviazione gestito da KeyVault.</span><span class="sxs-lookup"><span data-stu-id="eabce-114">KeyVault-managed storage account name.</span></span>
<span data-ttu-id="eabce-115">Il cmdlet crea l'FQDN di una definizione della firma di accesso condiviso per l'archiviazione gestita dal nome del vault, dall'ambiente attualmente selezionato e dal nome dell'account di archiviazione gestito.</span><span class="sxs-lookup"><span data-stu-id="eabce-115">Cmdlet constructs the FQDN of a managed storage SAS definition from vault name, currently-selected environment and managed storage account name.</span></span>

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

### <span data-ttu-id="eabce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eabce-116">-DefaultProfile</span></span>
<span data-ttu-id="eabce-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eabce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eabce-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eabce-118">-InputObject</span></span>
<span data-ttu-id="eabce-119">Oggetto definizione della firma di accesso condiviso per l'archiviazione gestita eliminata</span><span class="sxs-lookup"><span data-stu-id="eabce-119">Deleted managed storage SAS definition object</span></span>

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

### <span data-ttu-id="eabce-120">-Name</span><span class="sxs-lookup"><span data-stu-id="eabce-120">-Name</span></span>
<span data-ttu-id="eabce-121">Nome della definizione della firma di accesso condiviso per l'archiviazione gestita da KeyVault.</span><span class="sxs-lookup"><span data-stu-id="eabce-121">Name of the KeyVault-managed storage SAS definition.</span></span>
<span data-ttu-id="eabce-122">Il cmdlet crea l'FQDN della destinazione dal nome dell'insieme di credenziali, l'ambiente attualmente selezionato, il nome dell'account di archiviazione gestito e il nome della definizione di firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="eabce-122">Cmdlet constructs the FQDN of the target from vault name, currently-selected environment, the name of the managed storage account and the name of the SAS definition.</span></span>

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

### <span data-ttu-id="eabce-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="eabce-123">-VaultName</span></span>
<span data-ttu-id="eabce-124">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="eabce-124">Vault name.</span></span>
<span data-ttu-id="eabce-125">Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="eabce-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="eabce-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eabce-126">-Confirm</span></span>
<span data-ttu-id="eabce-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eabce-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eabce-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eabce-128">-WhatIf</span></span>
<span data-ttu-id="eabce-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eabce-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eabce-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eabce-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eabce-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eabce-131">CommonParameters</span></span>
<span data-ttu-id="eabce-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eabce-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eabce-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eabce-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eabce-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="eabce-134">INPUTS</span></span>

### <span data-ttu-id="eabce-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="eabce-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="eabce-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eabce-136">OUTPUTS</span></span>

### <span data-ttu-id="eabce-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="eabce-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="eabce-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="eabce-138">NOTES</span></span>

## <span data-ttu-id="eabce-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eabce-139">RELATED LINKS</span></span>
