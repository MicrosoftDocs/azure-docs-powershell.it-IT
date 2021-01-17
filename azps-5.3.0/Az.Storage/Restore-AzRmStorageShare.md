---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
ms.openlocfilehash: 70d3c8c435a88b4f0f968d1519efd9af6d9907e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479375"
---
# <span data-ttu-id="748a9-101">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="748a9-101">Restore-AzRmStorageShare</span></span>

## <span data-ttu-id="748a9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="748a9-102">SYNOPSIS</span></span>
<span data-ttu-id="748a9-103">Ripristina una condivisione file eliminata.</span><span class="sxs-lookup"><span data-stu-id="748a9-103">Restores a deleted file share.</span></span>

## <span data-ttu-id="748a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="748a9-104">SYNTAX</span></span>

### <span data-ttu-id="748a9-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="748a9-105">AccountName (Default)</span></span>
```
Restore-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DeletedShareVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="748a9-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="748a9-106">AccountObject</span></span>
```
Restore-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> -DeletedShareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="748a9-107">ShareObject</span><span class="sxs-lookup"><span data-stu-id="748a9-107">ShareObject</span></span>
```
Restore-AzRmStorageShare -InputObject <PSShare> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="748a9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="748a9-108">DESCRIPTION</span></span>
<span data-ttu-id="748a9-109">Il cmdlet **Restore-AzRmStorageShare** consente di ripristinare una condivisione di file eliminata entro un periodo di conservazione valido se è abilitata l'eliminazione di condivisione soft.</span><span class="sxs-lookup"><span data-stu-id="748a9-109">The **Restore-AzRmStorageShare** cmdlet restores a deleted file share within a valid retention days if share soft delete is enabled.</span></span>

## <span data-ttu-id="748a9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="748a9-110">EXAMPLES</span></span>

### <span data-ttu-id="748a9-111">Esempio 1: rimuovere e ripristinare una condivisione</span><span class="sxs-lookup"><span data-stu-id="748a9-111">Example 1: Remove and restore a share</span></span>
```powershell
PS C:\> Remove-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Name $shareName -Force

PS C:\> Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6                

PS C:\> Restore-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Name $shareName -DeletedShareVersion 01D61FD1FC5498B6

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   100
```

<span data-ttu-id="748a9-112">Questo comando Elimina prima di tutto una condivisione file e quindi elenca le condivisioni e Vedi la versione di condivisione eliminata, infine Ripristinala in una normale condivisione.</span><span class="sxs-lookup"><span data-stu-id="748a9-112">This command first delete a file share, and then list shares and see the deleted share version, finally restore it back to a normal share.</span></span> <span data-ttu-id="748a9-113">È necessario abilitare Condividi Elimina soft con Update-AzStorageFileServiceProperty, prima di eliminare la condivisione.</span><span class="sxs-lookup"><span data-stu-id="748a9-113">Need enabled share soft delete with Update-AzStorageFileServiceProperty, before delete the share.</span></span>

## <span data-ttu-id="748a9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="748a9-114">PARAMETERS</span></span>

### <span data-ttu-id="748a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="748a9-115">-DefaultProfile</span></span>
<span data-ttu-id="748a9-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="748a9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="748a9-117">-DeletedShareVersion</span><span class="sxs-lookup"><span data-stu-id="748a9-117">-DeletedShareVersion</span></span>
<span data-ttu-id="748a9-118">Versione di condivisione eliminata, da cui verranno ripristinati.</span><span class="sxs-lookup"><span data-stu-id="748a9-118">Deleted Share Version, which will be restored from.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="748a9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="748a9-119">-InputObject</span></span>
<span data-ttu-id="748a9-120">Oggetto condivisione eliminata</span><span class="sxs-lookup"><span data-stu-id="748a9-120">Deleted Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="748a9-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="748a9-121">-Name</span></span>
<span data-ttu-id="748a9-122">Nome della condivisione eliminato, che verrà ripristinato.</span><span class="sxs-lookup"><span data-stu-id="748a9-122">Deleted Share Name, which will be restored.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="748a9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="748a9-123">-ResourceGroupName</span></span>
<span data-ttu-id="748a9-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="748a9-124">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="748a9-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="748a9-125">-StorageAccount</span></span>
<span data-ttu-id="748a9-126">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="748a9-126">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="748a9-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="748a9-127">-StorageAccountName</span></span>
<span data-ttu-id="748a9-128">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="748a9-128">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="748a9-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="748a9-129">-Confirm</span></span>
<span data-ttu-id="748a9-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="748a9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="748a9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="748a9-131">-WhatIf</span></span>
<span data-ttu-id="748a9-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="748a9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="748a9-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="748a9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="748a9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="748a9-134">CommonParameters</span></span>
<span data-ttu-id="748a9-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="748a9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="748a9-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="748a9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="748a9-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="748a9-137">INPUTS</span></span>

### <span data-ttu-id="748a9-138">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="748a9-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="748a9-139">Microsoft. Azure. Commands. Management. storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="748a9-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="748a9-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="748a9-140">OUTPUTS</span></span>

### <span data-ttu-id="748a9-141">Microsoft. Azure. Commands. Management. storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="748a9-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="748a9-142">Note</span><span class="sxs-lookup"><span data-stu-id="748a9-142">NOTES</span></span>

## <span data-ttu-id="748a9-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="748a9-143">RELATED LINKS</span></span>
