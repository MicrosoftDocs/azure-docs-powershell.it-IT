---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: 642c5ff36fb0647907cf72218bd626bcdafe19ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835624"
---
# <span data-ttu-id="4585e-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="4585e-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="4585e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4585e-102">SYNOPSIS</span></span>
<span data-ttu-id="4585e-103">Viene ripristinato un account di archiviazione gestito con il Vault in precedenza eliminato.</span><span class="sxs-lookup"><span data-stu-id="4585e-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

## <span data-ttu-id="4585e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4585e-104">SYNTAX</span></span>

### <span data-ttu-id="4585e-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4585e-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4585e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4585e-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4585e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4585e-107">DESCRIPTION</span></span>
<span data-ttu-id="4585e-108">Il comando **Undo-AzKeyVaultManagedStorageAccountRemoval** recupera un account di archiviazione gestita precedentemente eliminato, a condizione che l'eliminazione soft sia abilitata per il Vault e che il tentativo di ripristino si verifichi durante l'intervallo di recupero.</span><span class="sxs-lookup"><span data-stu-id="4585e-108">The **Undo-AzKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="4585e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4585e-109">EXAMPLES</span></span>

### <span data-ttu-id="4585e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4585e-110">Example 1</span></span>
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

<span data-ttu-id="4585e-111">Questa sequenza di comandi determina se l'account di archiviazione specificato esiste nel Vault in uno stato eliminato; il comando successivo recupera l'account di archiviazione eliminato e lo riporta in uno stato attivo.</span><span class="sxs-lookup"><span data-stu-id="4585e-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="4585e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4585e-112">PARAMETERS</span></span>

### <span data-ttu-id="4585e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4585e-113">-DefaultProfile</span></span>
<span data-ttu-id="4585e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4585e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4585e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4585e-115">-InputObject</span></span>
<span data-ttu-id="4585e-116">Oggetto account di archiviazione gestita eliminato</span><span class="sxs-lookup"><span data-stu-id="4585e-116">Deleted Managed Storage Account object</span></span>

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

### <span data-ttu-id="4585e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="4585e-117">-Name</span></span>
<span data-ttu-id="4585e-118">Nome dell'account di archiviazione gestita con il Vault.</span><span class="sxs-lookup"><span data-stu-id="4585e-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="4585e-119">Cmdlet costruisce il nome di dominio completo della destinazione dal nome del Vault, l'ambiente selezionato attualmente e quello dell'account di archiviazione gestita.</span><span class="sxs-lookup"><span data-stu-id="4585e-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

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

### <span data-ttu-id="4585e-120">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="4585e-120">-VaultName</span></span>
<span data-ttu-id="4585e-121">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="4585e-121">Vault name.</span></span>
<span data-ttu-id="4585e-122">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="4585e-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="4585e-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4585e-123">-Confirm</span></span>
<span data-ttu-id="4585e-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4585e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4585e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4585e-125">-WhatIf</span></span>
<span data-ttu-id="4585e-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4585e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4585e-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4585e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4585e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4585e-128">CommonParameters</span></span>
<span data-ttu-id="4585e-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4585e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4585e-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4585e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4585e-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4585e-131">INPUTS</span></span>

### <span data-ttu-id="4585e-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4585e-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="4585e-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4585e-133">OUTPUTS</span></span>

### <span data-ttu-id="4585e-134">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4585e-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="4585e-135">Note</span><span class="sxs-lookup"><span data-stu-id="4585e-135">NOTES</span></span>

## <span data-ttu-id="4585e-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4585e-136">RELATED LINKS</span></span>
