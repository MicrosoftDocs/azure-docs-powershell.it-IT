---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/restart-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
ms.openlocfilehash: 4e0b5fda29696fb45515c3b478b9dc29ff67263e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322935"
---
# <span data-ttu-id="f629c-101">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="f629c-101">Restart-AzHDInsightHost</span></span>

## <span data-ttu-id="f629c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f629c-102">SYNOPSIS</span></span>
<span data-ttu-id="f629c-103">Riavvia gli host specifici del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f629c-103">Restarts the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="f629c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f629c-104">SYNTAX</span></span>

### <span data-ttu-id="f629c-105">SetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f629c-105">SetByNameParameterSet (Default)</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String> [-Name] <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f629c-106">SetByAzureHDInsightHostInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="f629c-106">SetByAzureHDInsightHostInfoParameterSet</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AzureHDInsightHostInfo] <AzureHDInsightHostInfo[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f629c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f629c-107">DESCRIPTION</span></span>
<span data-ttu-id="f629c-108">Questo cmdlet **Restart-AzHDInsightHost** riavvia gli host specifici del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f629c-108">This **Restart-AzHDInsightHost** cmdlet restart the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="f629c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f629c-109">EXAMPLES</span></span>

### <span data-ttu-id="f629c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f629c-110">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Restart-AzHDInsightHost -ClusterName $clusterName -Name wn0, wn1
```

<span data-ttu-id="f629c-111">Questo comando Riavvia due host del cluster: worknode1, worknode2.</span><span class="sxs-lookup"><span data-stu-id="f629c-111">This command restarts two hosts of the cluster: worknode1, worknode2.</span></span>

### <span data-ttu-id="f629c-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f629c-112">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $worknode1= Get-AzHDInsightHost -ClusterName $clusterName | Where-Object {$_.Name -like "wn1*"}
PS C:\> $worknode1 | Restart-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="f629c-113">Questo comando Mostra come collaborare con il cmdlet "Get-AzHDInsightHost".</span><span class="sxs-lookup"><span data-stu-id="f629c-113">This command shows how to cooperate with the cmdlet 'Get-AzHDInsightHost'.</span></span>

## <span data-ttu-id="f629c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f629c-114">PARAMETERS</span></span>

### <span data-ttu-id="f629c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f629c-115">-AsJob</span></span>
<span data-ttu-id="f629c-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f629c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f629c-117">-AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="f629c-117">-AzureHDInsightHostInfo</span></span>
<span data-ttu-id="f629c-118">Ottiene o imposta il nome dell'host.</span><span class="sxs-lookup"><span data-stu-id="f629c-118">Gets or sets the name of the host.</span></span>

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

### <span data-ttu-id="f629c-119">-Clustername</span><span class="sxs-lookup"><span data-stu-id="f629c-119">-ClusterName</span></span>
<span data-ttu-id="f629c-120">Ottiene o imposta il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="f629c-120">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="f629c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f629c-121">-DefaultProfile</span></span>
<span data-ttu-id="f629c-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f629c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f629c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="f629c-123">-Name</span></span>
<span data-ttu-id="f629c-124">Ottiene o imposta il nome dell'host.</span><span class="sxs-lookup"><span data-stu-id="f629c-124">Gets or sets the name of the host.</span></span>

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

### <span data-ttu-id="f629c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f629c-125">-PassThru</span></span>
<span data-ttu-id="f629c-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f629c-126">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="f629c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f629c-127">-ResourceGroupName</span></span>
<span data-ttu-id="f629c-128">Ottiene o imposta il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f629c-128">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="f629c-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f629c-129">-Confirm</span></span>
<span data-ttu-id="f629c-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f629c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f629c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f629c-131">-WhatIf</span></span>
<span data-ttu-id="f629c-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f629c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f629c-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f629c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f629c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f629c-134">CommonParameters</span></span>
<span data-ttu-id="f629c-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f629c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f629c-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f629c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f629c-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f629c-137">INPUTS</span></span>

### <span data-ttu-id="f629c-138">System. String []</span><span class="sxs-lookup"><span data-stu-id="f629c-138">System.String[]</span></span>

### <span data-ttu-id="f629c-139">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightHostInfo []</span><span class="sxs-lookup"><span data-stu-id="f629c-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]</span></span>

## <span data-ttu-id="f629c-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f629c-140">OUTPUTS</span></span>

### <span data-ttu-id="f629c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f629c-141">System.Boolean</span></span>

## <span data-ttu-id="f629c-142">Note</span><span class="sxs-lookup"><span data-stu-id="f629c-142">NOTES</span></span>

## <span data-ttu-id="f629c-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f629c-143">RELATED LINKS</span></span>
