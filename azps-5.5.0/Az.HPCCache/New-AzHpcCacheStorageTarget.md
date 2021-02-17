---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: eee07c01b0c9e0e2b072787d0d37a6a868fbf150
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209378"
---
# <span data-ttu-id="8da53-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="8da53-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="8da53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8da53-102">SYNOPSIS</span></span>
<span data-ttu-id="8da53-103">Crea un destinazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8da53-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="8da53-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8da53-104">SYNTAX</span></span>

### <span data-ttu-id="8da53-105">ClfsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8da53-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8da53-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="8da53-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8da53-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8da53-107">DESCRIPTION</span></span>
<span data-ttu-id="8da53-108">Il cmdlet **New-AzHpcCacheStorageTarget aggiunge** una destinazione di archiviazione alla cache di Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="8da53-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="8da53-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8da53-109">EXAMPLES</span></span>

### <span data-ttu-id="8da53-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8da53-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="8da53-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8da53-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="8da53-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8da53-112">PARAMETERS</span></span>

### <span data-ttu-id="8da53-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8da53-113">-AsJob</span></span>
<span data-ttu-id="8da53-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8da53-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8da53-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="8da53-115">-CacheName</span></span>
<span data-ttu-id="8da53-116">Nome della cache.</span><span class="sxs-lookup"><span data-stu-id="8da53-116">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da53-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="8da53-117">-CLFS</span></span>
<span data-ttu-id="8da53-118">Aggiornare il tipo di destinazione di archiviazione CLFS.</span><span class="sxs-lookup"><span data-stu-id="8da53-118">Update CLFS Storage Target type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ClfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da53-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da53-119">-DefaultProfile</span></span>
<span data-ttu-id="8da53-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8da53-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8da53-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8da53-121">-Force</span></span>
<span data-ttu-id="8da53-122">Indica che il cmdlet non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="8da53-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="8da53-123">Per impostazione predefinita, questo cmdlet chiede di confermare lo svuotamento della cache.</span><span class="sxs-lookup"><span data-stu-id="8da53-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="8da53-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="8da53-124">-HostName</span></span>
<span data-ttu-id="8da53-125">Nome host NFS.</span><span class="sxs-lookup"><span data-stu-id="8da53-125">NFS host name.</span></span>

```yaml
Type: System.String
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da53-126">-Junction</span><span class="sxs-lookup"><span data-stu-id="8da53-126">-Junction</span></span>
<span data-ttu-id="8da53-127">Giunzione.</span><span class="sxs-lookup"><span data-stu-id="8da53-127">Junction.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da53-128">-Name</span><span class="sxs-lookup"><span data-stu-id="8da53-128">-Name</span></span>
<span data-ttu-id="8da53-129">Nome della destinazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8da53-129">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageTargetName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da53-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="8da53-130">-NFS</span></span>
<span data-ttu-id="8da53-131">Aggiornare il tipo di destinazione di archiviazione NFS.</span><span class="sxs-lookup"><span data-stu-id="8da53-131">Update NFS Storage Target type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da53-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8da53-132">-ResourceGroupName</span></span>
<span data-ttu-id="8da53-133">"Nome del gruppo di risorse in cui si vuole creare una destinazione di archiviazione per una determinata cache.</span><span class="sxs-lookup"><span data-stu-id="8da53-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da53-134">-StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="8da53-134">-StorageContainerID</span></span>
<span data-ttu-id="8da53-135">StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="8da53-135">StorageContainerID</span></span>

```yaml
Type: System.String
Parameter Sets: ClfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da53-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="8da53-136">-UsageModel</span></span>
<span data-ttu-id="8da53-137">Modello di utilizzo NFS.</span><span class="sxs-lookup"><span data-stu-id="8da53-137">NFS usage model.</span></span>

```yaml
Type: System.String
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da53-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8da53-138">-Confirm</span></span>
<span data-ttu-id="8da53-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8da53-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8da53-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8da53-140">-WhatIf</span></span>
<span data-ttu-id="8da53-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8da53-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8da53-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8da53-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8da53-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da53-143">CommonParameters</span></span>
<span data-ttu-id="8da53-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8da53-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da53-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8da53-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da53-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="8da53-146">INPUTS</span></span>

### <span data-ttu-id="8da53-147">System.String</span><span class="sxs-lookup"><span data-stu-id="8da53-147">System.String</span></span>

## <span data-ttu-id="8da53-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8da53-148">OUTPUTS</span></span>

### <span data-ttu-id="8da53-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="8da53-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="8da53-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="8da53-150">NOTES</span></span>

## <span data-ttu-id="8da53-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8da53-151">RELATED LINKS</span></span>
