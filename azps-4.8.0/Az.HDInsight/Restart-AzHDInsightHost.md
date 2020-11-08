---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/restart-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
ms.openlocfilehash: d4b184dfbf834822110369e40fbbfb4eb168e424
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033093"
---
# <span data-ttu-id="4c9f5-101">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="4c9f5-101">Restart-AzHDInsightHost</span></span>

## <span data-ttu-id="4c9f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c9f5-102">SYNOPSIS</span></span>
<span data-ttu-id="4c9f5-103">Riavvia gli host specifici del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4c9f5-103">Restarts the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="4c9f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c9f5-104">SYNTAX</span></span>

### <span data-ttu-id="4c9f5-105">SetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4c9f5-105">SetByNameParameterSet (Default)</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String> [-Name] <String[]> [-AsJob]
 [[-DefaultProfile] <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c9f5-106">SetByAzureHDInsightHostInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c9f5-106">SetByAzureHDInsightHostInfoParameterSet</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AzureHDInsightHostInfo] <AzureHDInsightHostInfo[]> [-AsJob] [[-DefaultProfile] <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c9f5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c9f5-107">DESCRIPTION</span></span>
<span data-ttu-id="4c9f5-108">Questo cmdlet **Restart-AzHDInsightHost** riavvia gli host specifici del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4c9f5-108">This **Restart-AzHDInsightHost** cmdlet restart the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="4c9f5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c9f5-109">EXAMPLES</span></span>

### <span data-ttu-id="4c9f5-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4c9f5-110">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Restart-AzHDInsightHost -ClusterName $clusterName -Name wn0, wn1
```

<span data-ttu-id="4c9f5-111">Questo comando Riavvia due host del cluster: worknode1, worknode2.</span><span class="sxs-lookup"><span data-stu-id="4c9f5-111">This command restarts two hosts of the cluster: worknode1, worknode2.</span></span>

### <span data-ttu-id="4c9f5-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4c9f5-112">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $worknode1= Get-AzHDInsightHost -ClusterName $clusterName | Where-Object {$_.Name -like "wn1*"}
PS C:\> $worknode1 | Restart-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="4c9f5-113">Questo comando Mostra come collaborare con il cmdlet "Get-AzHDInsightHost".</span><span class="sxs-lookup"><span data-stu-id="4c9f5-113">This command shows how to cooperate with the cmdlet 'Get-AzHDInsightHost'.</span></span>

## <span data-ttu-id="4c9f5-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c9f5-114">PARAMETERS</span></span>

### <span data-ttu-id="4c9f5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c9f5-115">-AsJob</span></span>
<span data-ttu-id="4c9f5-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4c9f5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c9f5-117">-AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="4c9f5-117">-AzureHDInsightHostInfo</span></span>
<span data-ttu-id="4c9f5-118">Ottiene o imposta il nome dell'host.</span><span class="sxs-lookup"><span data-stu-id="4c9f5-118">Gets or sets the name of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]
Parameter Sets: SetByAzureHDInsightHostInfoParameterSet
Aliases: Host

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c9f5-119">-Clustername</span><span class="sxs-lookup"><span data-stu-id="4c9f5-119">-ClusterName</span></span>
<span data-ttu-id="4c9f5-120">Ottiene o imposta il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="4c9f5-120">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c9f5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c9f5-121">-DefaultProfile</span></span>
<span data-ttu-id="4c9f5-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c9f5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c9f5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c9f5-123">-Name</span></span>
<span data-ttu-id="4c9f5-124">Ottiene o imposta il nome dell'host.</span><span class="sxs-lookup"><span data-stu-id="4c9f5-124">Gets or sets the name of the host.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByNameParameterSet
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c9f5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c9f5-125">-PassThru</span></span>
<span data-ttu-id="4c9f5-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4c9f5-126">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="4c9f5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c9f5-127">-ResourceGroupName</span></span>
<span data-ttu-id="4c9f5-128">Ottiene o imposta il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4c9f5-128">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c9f5-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4c9f5-129">-Confirm</span></span>
<span data-ttu-id="4c9f5-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c9f5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c9f5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c9f5-131">-WhatIf</span></span>
<span data-ttu-id="4c9f5-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c9f5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c9f5-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c9f5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c9f5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c9f5-134">CommonParameters</span></span>
<span data-ttu-id="4c9f5-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c9f5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c9f5-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c9f5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c9f5-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c9f5-137">INPUTS</span></span>

### <span data-ttu-id="4c9f5-138">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightHostInfo, Microsoft. Azure. PowerShell. cmdlet. HDInsight, Version = 3.2.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4c9f5-138">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo, Microsoft.Azure.PowerShell.Cmdlets.HDInsight, Version=3.2.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4c9f5-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c9f5-139">OUTPUTS</span></span>

### <span data-ttu-id="4c9f5-140">Microsoft. Azure. Management. HDInsight. Models. cluster</span><span class="sxs-lookup"><span data-stu-id="4c9f5-140">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="4c9f5-141">Note</span><span class="sxs-lookup"><span data-stu-id="4c9f5-141">NOTES</span></span>

## <span data-ttu-id="4c9f5-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c9f5-142">RELATED LINKS</span></span>
