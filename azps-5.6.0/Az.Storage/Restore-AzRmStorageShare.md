---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/restore-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
ms.openlocfilehash: 0ce045df6e19a964cf92d5550cfb94e30c808a3d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007534"
---
# <span data-ttu-id="06d5a-101">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="06d5a-101">Restore-AzRmStorageShare</span></span>

## <span data-ttu-id="06d5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06d5a-102">SYNOPSIS</span></span>
<span data-ttu-id="06d5a-103">Ripristina una condivisione file eliminata.</span><span class="sxs-lookup"><span data-stu-id="06d5a-103">Restores a deleted file share.</span></span>

## <span data-ttu-id="06d5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06d5a-104">SYNTAX</span></span>

### <span data-ttu-id="06d5a-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="06d5a-105">AccountName (Default)</span></span>
```
Restore-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DeletedShareVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06d5a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="06d5a-106">AccountObject</span></span>
```
Restore-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> -DeletedShareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06d5a-107">ShareObject</span><span class="sxs-lookup"><span data-stu-id="06d5a-107">ShareObject</span></span>
```
Restore-AzRmStorageShare -InputObject <PSShare> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06d5a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="06d5a-108">DESCRIPTION</span></span>
<span data-ttu-id="06d5a-109">Il cmdlet **Restore-AzRmStorageShare** ripristina una condivisione file eliminata entro un giorno di conservazione valido se è abilitata l'eliminazione soft della condivisione.</span><span class="sxs-lookup"><span data-stu-id="06d5a-109">The **Restore-AzRmStorageShare** cmdlet restores a deleted file share within a valid retention days if share soft delete is enabled.</span></span>

## <span data-ttu-id="06d5a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06d5a-110">EXAMPLES</span></span>

### <span data-ttu-id="06d5a-111">Esempio 1: Rimuovere e ripristinare una condivisione</span><span class="sxs-lookup"><span data-stu-id="06d5a-111">Example 1: Remove and restore a share</span></span>
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

<span data-ttu-id="06d5a-112">Questo comando elimina prima una condivisione file, quindi elenca le condivisioni e visualizza la versione di condivisione eliminata, infine ripristina una condivisione normale.</span><span class="sxs-lookup"><span data-stu-id="06d5a-112">This command first delete a file share, and then list shares and see the deleted share version, finally restore it back to a normal share.</span></span> <span data-ttu-id="06d5a-113">È necessario abilitato l'eliminazione soft della condivisione con Update-AzStorageFileServiceProperty prima di eliminare la condivisione.</span><span class="sxs-lookup"><span data-stu-id="06d5a-113">Need enabled share soft delete with Update-AzStorageFileServiceProperty, before delete the share.</span></span>

## <span data-ttu-id="06d5a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06d5a-114">PARAMETERS</span></span>

### <span data-ttu-id="06d5a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d5a-115">-DefaultProfile</span></span>
<span data-ttu-id="06d5a-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06d5a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06d5a-117">-DeletedShareVersion</span><span class="sxs-lookup"><span data-stu-id="06d5a-117">-DeletedShareVersion</span></span>
<span data-ttu-id="06d5a-118">Versione di condivisione eliminata, da cui verrà ripristinata.</span><span class="sxs-lookup"><span data-stu-id="06d5a-118">Deleted Share Version, which will be restored from.</span></span>

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

### <span data-ttu-id="06d5a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06d5a-119">-InputObject</span></span>
<span data-ttu-id="06d5a-120">Oggetto Condivisione eliminato</span><span class="sxs-lookup"><span data-stu-id="06d5a-120">Deleted Share object</span></span>

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

### <span data-ttu-id="06d5a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="06d5a-121">-Name</span></span>
<span data-ttu-id="06d5a-122">Nome condivisione eliminato, che verrà ripristinato.</span><span class="sxs-lookup"><span data-stu-id="06d5a-122">Deleted Share Name, which will be restored.</span></span>

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

### <span data-ttu-id="06d5a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06d5a-123">-ResourceGroupName</span></span>
<span data-ttu-id="06d5a-124">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="06d5a-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="06d5a-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="06d5a-125">-StorageAccount</span></span>
<span data-ttu-id="06d5a-126">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="06d5a-126">Storage account object</span></span>

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

### <span data-ttu-id="06d5a-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="06d5a-127">-StorageAccountName</span></span>
<span data-ttu-id="06d5a-128">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="06d5a-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="06d5a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06d5a-129">-Confirm</span></span>
<span data-ttu-id="06d5a-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06d5a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06d5a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06d5a-131">-WhatIf</span></span>
<span data-ttu-id="06d5a-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06d5a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06d5a-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06d5a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06d5a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d5a-134">CommonParameters</span></span>
<span data-ttu-id="06d5a-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06d5a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d5a-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06d5a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d5a-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="06d5a-137">INPUTS</span></span>

### <span data-ttu-id="06d5a-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="06d5a-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="06d5a-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="06d5a-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="06d5a-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06d5a-140">OUTPUTS</span></span>

### <span data-ttu-id="06d5a-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="06d5a-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="06d5a-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="06d5a-142">NOTES</span></span>

## <span data-ttu-id="06d5a-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06d5a-143">RELATED LINKS</span></span>
