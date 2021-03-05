---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: deb359905086d68edb4129e023ce6dd8d2ceaf10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013533"
---
# <span data-ttu-id="44012-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="44012-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="44012-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44012-102">SYNOPSIS</span></span>
<span data-ttu-id="44012-103">Crea un destinazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="44012-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="44012-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44012-104">SYNTAX</span></span>

### <span data-ttu-id="44012-105">ClfsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="44012-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44012-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="44012-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44012-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="44012-107">DESCRIPTION</span></span>
<span data-ttu-id="44012-108">Il cmdlet **New-AzHpcCacheStorageTarget aggiunge** una destinazione di archiviazione alla cache di Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="44012-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="44012-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44012-109">EXAMPLES</span></span>

### <span data-ttu-id="44012-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="44012-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="44012-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="44012-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="44012-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44012-112">PARAMETERS</span></span>

### <span data-ttu-id="44012-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44012-113">-AsJob</span></span>
<span data-ttu-id="44012-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="44012-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44012-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="44012-115">-CacheName</span></span>
<span data-ttu-id="44012-116">Nome della cache.</span><span class="sxs-lookup"><span data-stu-id="44012-116">Name of cache.</span></span>

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

### <span data-ttu-id="44012-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="44012-117">-CLFS</span></span>
<span data-ttu-id="44012-118">Aggiornare il tipo di destinazione di archiviazione CLFS.</span><span class="sxs-lookup"><span data-stu-id="44012-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="44012-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44012-119">-DefaultProfile</span></span>
<span data-ttu-id="44012-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44012-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44012-121">-Force</span><span class="sxs-lookup"><span data-stu-id="44012-121">-Force</span></span>
<span data-ttu-id="44012-122">Indica che il cmdlet non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="44012-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="44012-123">Per impostazione predefinita, questo cmdlet chiede di confermare lo svuotamento della cache.</span><span class="sxs-lookup"><span data-stu-id="44012-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="44012-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="44012-124">-HostName</span></span>
<span data-ttu-id="44012-125">Nome host NFS.</span><span class="sxs-lookup"><span data-stu-id="44012-125">NFS host name.</span></span>

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

### <span data-ttu-id="44012-126">-Junction</span><span class="sxs-lookup"><span data-stu-id="44012-126">-Junction</span></span>
<span data-ttu-id="44012-127">Giunzione.</span><span class="sxs-lookup"><span data-stu-id="44012-127">Junction.</span></span>

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

### <span data-ttu-id="44012-128">-Name</span><span class="sxs-lookup"><span data-stu-id="44012-128">-Name</span></span>
<span data-ttu-id="44012-129">Nome della destinazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="44012-129">Name of storage target.</span></span>

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

### <span data-ttu-id="44012-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="44012-130">-NFS</span></span>
<span data-ttu-id="44012-131">Aggiornare il tipo di destinazione di archiviazione NFS.</span><span class="sxs-lookup"><span data-stu-id="44012-131">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="44012-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44012-132">-ResourceGroupName</span></span>
<span data-ttu-id="44012-133">"Nome del gruppo di risorse in cui si vuole creare una destinazione di archiviazione per una determinata cache.</span><span class="sxs-lookup"><span data-stu-id="44012-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

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

### <span data-ttu-id="44012-134">-StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="44012-134">-StorageContainerID</span></span>
<span data-ttu-id="44012-135">StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="44012-135">StorageContainerID</span></span>

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

### <span data-ttu-id="44012-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="44012-136">-UsageModel</span></span>
<span data-ttu-id="44012-137">Modello di utilizzo NFS.</span><span class="sxs-lookup"><span data-stu-id="44012-137">NFS usage model.</span></span>

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

### <span data-ttu-id="44012-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44012-138">-Confirm</span></span>
<span data-ttu-id="44012-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44012-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44012-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44012-140">-WhatIf</span></span>
<span data-ttu-id="44012-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44012-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44012-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44012-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44012-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44012-143">CommonParameters</span></span>
<span data-ttu-id="44012-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44012-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44012-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="44012-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44012-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="44012-146">INPUTS</span></span>

### <span data-ttu-id="44012-147">System.String</span><span class="sxs-lookup"><span data-stu-id="44012-147">System.String</span></span>

## <span data-ttu-id="44012-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44012-148">OUTPUTS</span></span>

### <span data-ttu-id="44012-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="44012-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="44012-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="44012-150">NOTES</span></span>

## <span data-ttu-id="44012-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44012-151">RELATED LINKS</span></span>
