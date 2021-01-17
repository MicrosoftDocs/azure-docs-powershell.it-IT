---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
ms.openlocfilehash: fa799a05b76f9f6941b19bf171beb77318b77d39
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476227"
---
# <span data-ttu-id="3e411-101">Set-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="3e411-101">Set-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="3e411-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e411-102">SYNOPSIS</span></span>
<span data-ttu-id="3e411-103">Aggiorna una destinazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3e411-103">Updates a Storage Target.</span></span>

## <span data-ttu-id="3e411-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e411-104">SYNTAX</span></span>

### <span data-ttu-id="3e411-105">ClfsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3e411-105">ClfsParameterSet (Default)</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e411-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e411-106">NfsParameterSet</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e411-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e411-107">DESCRIPTION</span></span>
<span data-ttu-id="3e411-108">Il cmdlet **set-AzHpcCacheStorageTarget** aggiorna una destinazione di archiviazione associata alla cache di Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="3e411-108">The **Set-AzHpcCacheStorageTarget** cmdlet updates a Storage Target attached to Azure HPC cache.</span></span>

## <span data-ttu-id="3e411-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e411-109">EXAMPLES</span></span>

### <span data-ttu-id="3e411-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3e411-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="3e411-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3e411-111">Example 2</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/export"})
```

## <span data-ttu-id="3e411-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e411-112">PARAMETERS</span></span>

### <span data-ttu-id="3e411-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e411-113">-AsJob</span></span>
<span data-ttu-id="3e411-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3e411-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e411-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="3e411-115">-CacheName</span></span>
<span data-ttu-id="3e411-116">Nome della cache.</span><span class="sxs-lookup"><span data-stu-id="3e411-116">Name of cache.</span></span>

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

### <span data-ttu-id="3e411-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="3e411-117">-CLFS</span></span>
<span data-ttu-id="3e411-118">Aggiornare il tipo di destinazione di archiviazione CLFS.</span><span class="sxs-lookup"><span data-stu-id="3e411-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="3e411-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e411-119">-DefaultProfile</span></span>
<span data-ttu-id="3e411-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e411-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e411-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3e411-121">-Force</span></span>
<span data-ttu-id="3e411-122">Indica che il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="3e411-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="3e411-123">Per impostazione predefinita, questo cmdlet richiede di confermare che si vuole svuotare la cache.</span><span class="sxs-lookup"><span data-stu-id="3e411-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="3e411-124">-Junction</span><span class="sxs-lookup"><span data-stu-id="3e411-124">-Junction</span></span>
<span data-ttu-id="3e411-125">Giunzione.</span><span class="sxs-lookup"><span data-stu-id="3e411-125">Junction.</span></span>

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

### <span data-ttu-id="3e411-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e411-126">-Name</span></span>
<span data-ttu-id="3e411-127">Nome della destinazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3e411-127">Name of storage target.</span></span>

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

### <span data-ttu-id="3e411-128">-NFS</span><span class="sxs-lookup"><span data-stu-id="3e411-128">-NFS</span></span>
<span data-ttu-id="3e411-129">Aggiornare il tipo di destinazione di archiviazione NFS.</span><span class="sxs-lookup"><span data-stu-id="3e411-129">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="3e411-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e411-130">-ResourceGroupName</span></span>
<span data-ttu-id="3e411-131">Nome del gruppo di risorse in cui si vuole aggiornare la destinazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3e411-131">Name of resource group under which you want to update storage target.</span></span>

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

### <span data-ttu-id="3e411-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3e411-132">-Confirm</span></span>
<span data-ttu-id="3e411-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e411-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e411-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e411-134">-WhatIf</span></span>
<span data-ttu-id="3e411-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e411-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e411-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e411-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e411-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e411-137">CommonParameters</span></span>
<span data-ttu-id="3e411-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e411-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e411-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e411-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e411-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e411-140">INPUTS</span></span>

### <span data-ttu-id="3e411-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3e411-141">System.String</span></span>

## <span data-ttu-id="3e411-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e411-142">OUTPUTS</span></span>

### <span data-ttu-id="3e411-143">Microsoft. Azure. PowerShell. Cmdlets. HPCCache. Models. PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="3e411-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="3e411-144">Note</span><span class="sxs-lookup"><span data-stu-id="3e411-144">NOTES</span></span>

## <span data-ttu-id="3e411-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e411-145">RELATED LINKS</span></span>
