---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 0f2d86fca85364fa71d50c05d83f278bd997252e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209083"
---
# <span data-ttu-id="36408-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="36408-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="36408-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36408-102">SYNOPSIS</span></span>
<span data-ttu-id="36408-103">Modifica una condivisione file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="36408-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="36408-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36408-104">SYNTAX</span></span>

### <span data-ttu-id="36408-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="36408-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36408-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="36408-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36408-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="36408-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36408-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="36408-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36408-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="36408-109">DESCRIPTION</span></span>
<span data-ttu-id="36408-110">Il cmdlet **New-AzRmStorageShare** modifica una condivisione file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="36408-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="36408-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36408-111">EXAMPLES</span></span>

### <span data-ttu-id="36408-112">Esempio 1: Modifica dei metadati di una condivisione file di archiviazione e quota di condivisione con il nome dell'account di archiviazione e il nome della condivisione</span><span class="sxs-lookup"><span data-stu-id="36408-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 200 -Metadata @{tag0="value0";tag1="value1"}

PS C:\>$share

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  200

PS C:\>$share.Metadata

Key  Value  
---  ----- 
tag0 value0
tag1 value1
```

<span data-ttu-id="36408-113">Questo comando modifica i metadati di una condivisione file di archiviazione e la quota di condivisione con il nome dell'account di archiviazione e il nome della condivisione e mostra il risultato della modifica con l'oggetto di condivisione file restituito.</span><span class="sxs-lookup"><span data-stu-id="36408-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="36408-114">Esempio 2: Modifica dei metadati in una condivisione file di archiviazione con l'oggetto account di archiviazione e il nome della condivisione</span><span class="sxs-lookup"><span data-stu-id="36408-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="36408-115">Questo comando modifica i metadati in una condivisione file di archiviazione con l'oggetto account di archiviazione e il nome della condivisione.</span><span class="sxs-lookup"><span data-stu-id="36408-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="36408-116">Esempio 3: Modifica della quota di condivisione per tutte le condivisioni file di archiviazione in un account di archiviazione con pipeline</span><span class="sxs-lookup"><span data-stu-id="36408-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Update-AzRmStorageShare -QuotaGiB 5000

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   5000
share2   5000
```

<span data-ttu-id="36408-117">Questo comando modifica la quota di condivisione come 5000 GiB per tutte le condivisioni file di archiviazione in un account di archiviazione con pipeline.</span><span class="sxs-lookup"><span data-stu-id="36408-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

### <span data-ttu-id="36408-118">Esempio 4: Modificare una condivisione file di archiviazione con un utente di accesso come Figo</span><span class="sxs-lookup"><span data-stu-id="36408-118">Example 4: Modify a Storage file share with accesstier as Cool</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Cool

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Cool
```

<span data-ttu-id="36408-119">Questo comando modifica una condivisione file di archiviazione con l'accesso come Cool.</span><span class="sxs-lookup"><span data-stu-id="36408-119">This command modifies a Storage file share with accesstier as Cool.</span></span>

## <span data-ttu-id="36408-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36408-120">PARAMETERS</span></span>

### <span data-ttu-id="36408-121">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="36408-121">-AccessTier</span></span>
<span data-ttu-id="36408-122">Livello di accesso per una condivisione specifica.</span><span class="sxs-lookup"><span data-stu-id="36408-122">Access tier for specific share.</span></span> <span data-ttu-id="36408-123">L'account StorageV2 può scegliere tra TransactionOptimized (impostazione predefinita), Hot e Cool.</span><span class="sxs-lookup"><span data-stu-id="36408-123">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="36408-124">L'account FileStorage può scegliere Premium.</span><span class="sxs-lookup"><span data-stu-id="36408-124">FileStorage account can choose Premium.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TransactionOptimized, Premium, Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36408-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36408-125">-DefaultProfile</span></span>
<span data-ttu-id="36408-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36408-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36408-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36408-127">-InputObject</span></span>
<span data-ttu-id="36408-128">Oggetto Condivisione di archiviazione</span><span class="sxs-lookup"><span data-stu-id="36408-128">Storage Share object</span></span>

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

### <span data-ttu-id="36408-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="36408-129">-Metadata</span></span>
<span data-ttu-id="36408-130">Condividere metadati</span><span class="sxs-lookup"><span data-stu-id="36408-130">Share Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36408-131">-Name</span><span class="sxs-lookup"><span data-stu-id="36408-131">-Name</span></span>
<span data-ttu-id="36408-132">Condividi nome</span><span class="sxs-lookup"><span data-stu-id="36408-132">Share Name</span></span>

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

### <span data-ttu-id="36408-133">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="36408-133">-QuotaGiB</span></span>
<span data-ttu-id="36408-134">Quota di condivisione in Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="36408-134">Share Quota in Gibibyte.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Quota

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36408-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36408-135">-ResourceGroupName</span></span>
<span data-ttu-id="36408-136">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="36408-136">Resource Group Name.</span></span>

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

### <span data-ttu-id="36408-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36408-137">-ResourceId</span></span>
<span data-ttu-id="36408-138">Immettere un ID di risorsa condivisione file.</span><span class="sxs-lookup"><span data-stu-id="36408-138">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36408-139">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="36408-139">-StorageAccount</span></span>
<span data-ttu-id="36408-140">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="36408-140">Storage account object</span></span>

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

### <span data-ttu-id="36408-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="36408-141">-StorageAccountName</span></span>
<span data-ttu-id="36408-142">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="36408-142">Storage Account Name.</span></span>

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

### <span data-ttu-id="36408-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36408-143">-Confirm</span></span>
<span data-ttu-id="36408-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36408-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36408-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36408-145">-WhatIf</span></span>
<span data-ttu-id="36408-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36408-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36408-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36408-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36408-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36408-148">CommonParameters</span></span>
<span data-ttu-id="36408-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36408-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36408-150">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36408-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36408-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="36408-151">INPUTS</span></span>

### <span data-ttu-id="36408-152">System.String</span><span class="sxs-lookup"><span data-stu-id="36408-152">System.String</span></span>

### <span data-ttu-id="36408-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36408-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="36408-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="36408-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="36408-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36408-155">OUTPUTS</span></span>

### <span data-ttu-id="36408-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="36408-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="36408-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="36408-157">NOTES</span></span>

## <span data-ttu-id="36408-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36408-158">RELATED LINKS</span></span>
