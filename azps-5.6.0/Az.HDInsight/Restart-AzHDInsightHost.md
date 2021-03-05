---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/restart-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
ms.openlocfilehash: bdedaee92a187d1086cdcd71948981e93fed508a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986816"
---
# <span data-ttu-id="7a3f8-101">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="7a3f8-101">Restart-AzHDInsightHost</span></span>

## <span data-ttu-id="7a3f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a3f8-102">SYNOPSIS</span></span>
<span data-ttu-id="7a3f8-103">Riavvia gli host specifici del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7a3f8-103">Restarts the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="7a3f8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a3f8-104">SYNTAX</span></span>

### <span data-ttu-id="7a3f8-105">SetByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7a3f8-105">SetByNameParameterSet (Default)</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String> [-Name] <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a3f8-106">SetByAzureHDInsightHostInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a3f8-106">SetByAzureHDInsightHostInfoParameterSet</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AzureHDInsightHostInfo] <AzureHDInsightHostInfo[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a3f8-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7a3f8-107">DESCRIPTION</span></span>
<span data-ttu-id="7a3f8-108">Questo cmdlet **Restart-AzHDInsightHost** riavvia gli host specifici del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7a3f8-108">This **Restart-AzHDInsightHost** cmdlet restart the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="7a3f8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a3f8-109">EXAMPLES</span></span>

### <span data-ttu-id="7a3f8-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7a3f8-110">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Restart-AzHDInsightHost -ClusterName $clusterName -Name wn0, wn1
```

<span data-ttu-id="7a3f8-111">Questo comando riavvia due host del cluster: worknode1, worknode2.</span><span class="sxs-lookup"><span data-stu-id="7a3f8-111">This command restarts two hosts of the cluster: worknode1, worknode2.</span></span>

### <span data-ttu-id="7a3f8-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7a3f8-112">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $worknode1= Get-AzHDInsightHost -ClusterName $clusterName | Where-Object {$_.Name -like "wn1*"}
PS C:\> $worknode1 | Restart-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="7a3f8-113">Questo comando illustra come collaborare con il cmdlet "Get-AzHDInsightHost".</span><span class="sxs-lookup"><span data-stu-id="7a3f8-113">This command shows how to cooperate with the cmdlet 'Get-AzHDInsightHost'.</span></span>

## <span data-ttu-id="7a3f8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a3f8-114">PARAMETERS</span></span>

### <span data-ttu-id="7a3f8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a3f8-115">-AsJob</span></span>
<span data-ttu-id="7a3f8-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7a3f8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a3f8-117">-AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="7a3f8-117">-AzureHDInsightHostInfo</span></span>
<span data-ttu-id="7a3f8-118">Ottiene o imposta il nome dell'host.</span><span class="sxs-lookup"><span data-stu-id="7a3f8-118">Gets or sets the name of the host.</span></span>

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

### <span data-ttu-id="7a3f8-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7a3f8-119">-ClusterName</span></span>
<span data-ttu-id="7a3f8-120">Ottiene o imposta il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="7a3f8-120">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="7a3f8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a3f8-121">-DefaultProfile</span></span>
<span data-ttu-id="7a3f8-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a3f8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a3f8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7a3f8-123">-Name</span></span>
<span data-ttu-id="7a3f8-124">Ottiene o imposta il nome dell'host.</span><span class="sxs-lookup"><span data-stu-id="7a3f8-124">Gets or sets the name of the host.</span></span>

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

### <span data-ttu-id="7a3f8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a3f8-125">-PassThru</span></span>
<span data-ttu-id="7a3f8-126">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="7a3f8-126">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="7a3f8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a3f8-127">-ResourceGroupName</span></span>
<span data-ttu-id="7a3f8-128">Ottiene o imposta il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7a3f8-128">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="7a3f8-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a3f8-129">-Confirm</span></span>
<span data-ttu-id="7a3f8-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a3f8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a3f8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a3f8-131">-WhatIf</span></span>
<span data-ttu-id="7a3f8-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a3f8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a3f8-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a3f8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a3f8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a3f8-134">CommonParameters</span></span>
<span data-ttu-id="7a3f8-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a3f8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a3f8-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7a3f8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a3f8-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="7a3f8-137">INPUTS</span></span>

### <span data-ttu-id="7a3f8-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7a3f8-138">System.String[]</span></span>

### <span data-ttu-id="7a3f8-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]</span><span class="sxs-lookup"><span data-stu-id="7a3f8-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]</span></span>

## <span data-ttu-id="7a3f8-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a3f8-140">OUTPUTS</span></span>

### <span data-ttu-id="7a3f8-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a3f8-141">System.Boolean</span></span>

## <span data-ttu-id="7a3f8-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="7a3f8-142">NOTES</span></span>

## <span data-ttu-id="7a3f8-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a3f8-143">RELATED LINKS</span></span>
