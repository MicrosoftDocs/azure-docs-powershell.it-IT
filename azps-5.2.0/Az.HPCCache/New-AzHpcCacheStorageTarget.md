---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: eee07c01b0c9e0e2b072787d0d37a6a868fbf150
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363072"
---
# <span data-ttu-id="634b1-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="634b1-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="634b1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="634b1-102">SYNOPSIS</span></span>
<span data-ttu-id="634b1-103">Crea una destinazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="634b1-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="634b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="634b1-104">SYNTAX</span></span>

### <span data-ttu-id="634b1-105">ClfsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="634b1-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="634b1-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="634b1-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="634b1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="634b1-107">DESCRIPTION</span></span>
<span data-ttu-id="634b1-108">Il cmdlet **New-AzHpcCacheStorageTarget** aggiunge una destinazione di archiviazione alla cache di Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="634b1-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="634b1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="634b1-109">EXAMPLES</span></span>

### <span data-ttu-id="634b1-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="634b1-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="634b1-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="634b1-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="634b1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="634b1-112">PARAMETERS</span></span>

### <span data-ttu-id="634b1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="634b1-113">-AsJob</span></span>
<span data-ttu-id="634b1-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="634b1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="634b1-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="634b1-115">-CacheName</span></span>
<span data-ttu-id="634b1-116">Nome della cache.</span><span class="sxs-lookup"><span data-stu-id="634b1-116">Name of cache.</span></span>

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

### <span data-ttu-id="634b1-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="634b1-117">-CLFS</span></span>
<span data-ttu-id="634b1-118">Aggiornare il tipo di destinazione di archiviazione CLFS.</span><span class="sxs-lookup"><span data-stu-id="634b1-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="634b1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="634b1-119">-DefaultProfile</span></span>
<span data-ttu-id="634b1-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="634b1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="634b1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="634b1-121">-Force</span></span>
<span data-ttu-id="634b1-122">Indica che il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="634b1-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="634b1-123">Per impostazione predefinita, questo cmdlet richiede di confermare che si vuole svuotare la cache.</span><span class="sxs-lookup"><span data-stu-id="634b1-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="634b1-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="634b1-124">-HostName</span></span>
<span data-ttu-id="634b1-125">Nome host NFS.</span><span class="sxs-lookup"><span data-stu-id="634b1-125">NFS host name.</span></span>

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

### <span data-ttu-id="634b1-126">-Junction</span><span class="sxs-lookup"><span data-stu-id="634b1-126">-Junction</span></span>
<span data-ttu-id="634b1-127">Giunzione.</span><span class="sxs-lookup"><span data-stu-id="634b1-127">Junction.</span></span>

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

### <span data-ttu-id="634b1-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="634b1-128">-Name</span></span>
<span data-ttu-id="634b1-129">Nome della destinazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="634b1-129">Name of storage target.</span></span>

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

### <span data-ttu-id="634b1-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="634b1-130">-NFS</span></span>
<span data-ttu-id="634b1-131">Aggiornare il tipo di destinazione di archiviazione NFS.</span><span class="sxs-lookup"><span data-stu-id="634b1-131">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="634b1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="634b1-132">-ResourceGroupName</span></span>
<span data-ttu-id="634b1-133">"Nome del gruppo di risorse in cui si vuole creare la destinazione di archiviazione per la cache specificata.</span><span class="sxs-lookup"><span data-stu-id="634b1-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

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

### <span data-ttu-id="634b1-134">-StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="634b1-134">-StorageContainerID</span></span>
<span data-ttu-id="634b1-135">StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="634b1-135">StorageContainerID</span></span>

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

### <span data-ttu-id="634b1-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="634b1-136">-UsageModel</span></span>
<span data-ttu-id="634b1-137">Modello di utilizzo di NFS.</span><span class="sxs-lookup"><span data-stu-id="634b1-137">NFS usage model.</span></span>

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

### <span data-ttu-id="634b1-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="634b1-138">-Confirm</span></span>
<span data-ttu-id="634b1-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="634b1-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="634b1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="634b1-140">-WhatIf</span></span>
<span data-ttu-id="634b1-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="634b1-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="634b1-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="634b1-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="634b1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="634b1-143">CommonParameters</span></span>
<span data-ttu-id="634b1-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="634b1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="634b1-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="634b1-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="634b1-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="634b1-146">INPUTS</span></span>

### <span data-ttu-id="634b1-147">System. String</span><span class="sxs-lookup"><span data-stu-id="634b1-147">System.String</span></span>

## <span data-ttu-id="634b1-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="634b1-148">OUTPUTS</span></span>

### <span data-ttu-id="634b1-149">Microsoft. Azure. PowerShell. Cmdlets. HPCCache. Models. PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="634b1-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="634b1-150">Note</span><span class="sxs-lookup"><span data-stu-id="634b1-150">NOTES</span></span>

## <span data-ttu-id="634b1-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="634b1-151">RELATED LINKS</span></span>
