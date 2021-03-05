---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: 289adecd07837134fed9279758cf1142d30183a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010462"
---
# <span data-ttu-id="ade7a-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="ade7a-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="ade7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ade7a-102">SYNOPSIS</span></span>
<span data-ttu-id="ade7a-103">Recupera un account di archiviazione gestito da KeyVault eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="ade7a-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

## <span data-ttu-id="ade7a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ade7a-104">SYNTAX</span></span>

### <span data-ttu-id="ade7a-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ade7a-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ade7a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ade7a-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ade7a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ade7a-107">DESCRIPTION</span></span>
<span data-ttu-id="ade7a-108">Il comando **Undo-AzKeyVaultManagedStorageAccountRemoval** recupera un account di archiviazione gestito eliminato in precedenza, a condizione che l'eliminazione reversibile sia abilitata per il vault e che il tentativo di recupero sia eseguito durante l'intervallo di recupero.</span><span class="sxs-lookup"><span data-stu-id="ade7a-108">The **Undo-AzKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="ade7a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ade7a-109">EXAMPLES</span></span>

### <span data-ttu-id="ade7a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ade7a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName myVault -Name myAccount -InRemovedState
PS C:\> Undo-AzKeyVaultManagedStorageAccountRemoval -VaultName myVault -Name myAccount

Id                  : https://myvault.vault.azure.net:443/storage/myaccount
Vault Name          : myVault
AccountName         : myAccount
Account Resource Id : /subscriptions/8bc48661-1801-4b7a-8ca1-6a3cadfb4870/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/myaccount
Active Key Name     : key2
Auto Regenerate Key : False
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="ade7a-111">Questa sequenza di comandi determina se l'account di archiviazione specificato esiste nel vault in stato di eliminazione; Il comando successivo recupera l'account di archiviazione eliminato e lo riporta allo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="ade7a-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="ade7a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ade7a-112">PARAMETERS</span></span>

### <span data-ttu-id="ade7a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade7a-113">-DefaultProfile</span></span>
<span data-ttu-id="ade7a-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ade7a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ade7a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ade7a-115">-InputObject</span></span>
<span data-ttu-id="ade7a-116">Oggetto Account di archiviazione gestito eliminato</span><span class="sxs-lookup"><span data-stu-id="ade7a-116">Deleted Managed Storage Account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ade7a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ade7a-117">-Name</span></span>
<span data-ttu-id="ade7a-118">Nome dell'account di archiviazione gestito da KeyVault.</span><span class="sxs-lookup"><span data-stu-id="ade7a-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="ade7a-119">Il cmdlet crea il nome FQDN della destinazione dal nome del vault, l'ambiente attualmente selezionato e il nome dell'account di archiviazione gestito.</span><span class="sxs-lookup"><span data-stu-id="ade7a-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade7a-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ade7a-120">-VaultName</span></span>
<span data-ttu-id="ade7a-121">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="ade7a-121">Vault name.</span></span>
<span data-ttu-id="ade7a-122">Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="ade7a-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ade7a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ade7a-123">-Confirm</span></span>
<span data-ttu-id="ade7a-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ade7a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ade7a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ade7a-125">-WhatIf</span></span>
<span data-ttu-id="ade7a-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ade7a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ade7a-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ade7a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ade7a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade7a-128">CommonParameters</span></span>
<span data-ttu-id="ade7a-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ade7a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade7a-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ade7a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade7a-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="ade7a-131">INPUTS</span></span>

### <span data-ttu-id="ade7a-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ade7a-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="ade7a-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ade7a-133">OUTPUTS</span></span>

### <span data-ttu-id="ade7a-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ade7a-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="ade7a-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="ade7a-135">NOTES</span></span>

## <span data-ttu-id="ade7a-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ade7a-136">RELATED LINKS</span></span>
