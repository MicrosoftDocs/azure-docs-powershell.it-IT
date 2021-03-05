---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: dcb4819a3ac13056acd1b51dde2ee67774d51693
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994753"
---
# <span data-ttu-id="4a81e-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4a81e-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="4a81e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a81e-102">SYNOPSIS</span></span>
<span data-ttu-id="4a81e-103">Crea una condivisione file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4a81e-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="4a81e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a81e-104">SYNTAX</span></span>

### <span data-ttu-id="4a81e-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4a81e-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a81e-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="4a81e-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4a81e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4a81e-107">DESCRIPTION</span></span>
<span data-ttu-id="4a81e-108">Il cmdlet **New-AzRmStorageShare** crea una condivisione file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4a81e-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="4a81e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a81e-109">EXAMPLES</span></span>

### <span data-ttu-id="4a81e-110">Esempio 1: Creare una condivisione file di archiviazione con il nome dell'account di archiviazione e il nome della condivisione, con metadati e quota di condivisione come 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="4a81e-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="4a81e-111">Questo comando crea una condivisione file di archiviazione con metadati e quota di condivisione come 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="4a81e-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="4a81e-112">Esempio 2: Creare una condivisione file di archiviazione con un oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="4a81e-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="4a81e-113">Questo comando crea una condivisione file di archiviazione con l'oggetto account di archiviazione e il nome della condivisione.</span><span class="sxs-lookup"><span data-stu-id="4a81e-113">This command creates a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="4a81e-114">Esempio 3: Creare una condivisione file di archiviazione con accesso rapido</span><span class="sxs-lookup"><span data-stu-id="4a81e-114">Example 3: Create a Storage file share with accesstier as Hot</span></span>
```
PS C:\>$share = New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Hot

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Hot
```

<span data-ttu-id="4a81e-115">Questo comando crea una condivisione file di archiviazione con accesso come scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="4a81e-115">This command creates a Storage file share with accesstier as Hot.</span></span>

## <span data-ttu-id="4a81e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a81e-116">PARAMETERS</span></span>

### <span data-ttu-id="4a81e-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="4a81e-117">-AccessTier</span></span>
<span data-ttu-id="4a81e-118">Livello di accesso per una condivisione specifica.</span><span class="sxs-lookup"><span data-stu-id="4a81e-118">Access tier for specific share.</span></span> <span data-ttu-id="4a81e-119">L'account StorageV2 può scegliere tra TransactionOptimized (impostazione predefinita), Hot e Cool.</span><span class="sxs-lookup"><span data-stu-id="4a81e-119">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="4a81e-120">L'account FileStorage può scegliere Premium.</span><span class="sxs-lookup"><span data-stu-id="4a81e-120">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="4a81e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a81e-121">-DefaultProfile</span></span>
<span data-ttu-id="4a81e-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a81e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a81e-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4a81e-123">-Metadata</span></span>
<span data-ttu-id="4a81e-124">Condividere i metadati</span><span class="sxs-lookup"><span data-stu-id="4a81e-124">Share Metadata</span></span>

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

### <span data-ttu-id="4a81e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="4a81e-125">-Name</span></span>
<span data-ttu-id="4a81e-126">Nome condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="4a81e-126">Azure File share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a81e-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="4a81e-127">-QuotaGiB</span></span>
<span data-ttu-id="4a81e-128">Quota di condivisione in Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="4a81e-128">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="4a81e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a81e-129">-ResourceGroupName</span></span>
<span data-ttu-id="4a81e-130">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4a81e-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="4a81e-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4a81e-131">-StorageAccount</span></span>
<span data-ttu-id="4a81e-132">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="4a81e-132">Storage account object</span></span>

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

### <span data-ttu-id="4a81e-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4a81e-133">-StorageAccountName</span></span>
<span data-ttu-id="4a81e-134">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4a81e-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="4a81e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a81e-135">-Confirm</span></span>
<span data-ttu-id="4a81e-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a81e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a81e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a81e-137">-WhatIf</span></span>
<span data-ttu-id="4a81e-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a81e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a81e-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a81e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a81e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a81e-140">CommonParameters</span></span>
<span data-ttu-id="4a81e-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a81e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a81e-142">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a81e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a81e-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="4a81e-143">INPUTS</span></span>

### <span data-ttu-id="4a81e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="4a81e-144">System.String</span></span>

### <span data-ttu-id="4a81e-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4a81e-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="4a81e-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a81e-146">OUTPUTS</span></span>

### <span data-ttu-id="4a81e-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="4a81e-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="4a81e-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="4a81e-148">NOTES</span></span>

## <span data-ttu-id="4a81e-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a81e-149">RELATED LINKS</span></span>
