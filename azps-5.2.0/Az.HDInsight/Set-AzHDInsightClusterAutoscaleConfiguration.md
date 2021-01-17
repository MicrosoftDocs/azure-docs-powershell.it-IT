---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 1C3B7A57-D645-498C-98F4-DAE9B782123E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: bb22bda0f22ae128942e6e1d5a7aed9b0b646875
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328325"
---
# <span data-ttu-id="1ae5d-101">Set-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ae5d-101">Set-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="1ae5d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1ae5d-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae5d-103">Imposta la configurazione di scala automatica di un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1ae5d-103">Sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1ae5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ae5d-104">SYNTAX</span></span>

### <span data-ttu-id="1ae5d-105">LoadAutoscaleByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1ae5d-105">LoadAutoscaleByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae5d-106">ScheduleAutoscaleByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ae5d-106">ScheduleAutoscaleByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae5d-107">AutoscaleConfigurationByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ae5d-107">AutoscaleConfigurationByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae5d-108">LoadAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ae5d-108">LoadAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-MinWorkerNodeCount <Int32>]
 [-MaxWorkerNodeCount <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ae5d-109">ScheduleAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ae5d-109">ScheduleAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae5d-110">AutoscaleConfigurationByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ae5d-110">AutoscaleConfigurationByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae5d-111">LoadAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ae5d-111">LoadAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae5d-112">ScheduleAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ae5d-112">ScheduleAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae5d-113">AutoscaleConfigurationByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ae5d-113">AutoscaleConfigurationByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ae5d-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ae5d-114">DESCRIPTION</span></span>
<span data-ttu-id="1ae5d-115">Questo cmdlet **set-AzHDInsightClusterAutoscaleConfiguration** imposta la configurazione di scala automatica di un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1ae5d-115">This cmdlet **Set-AzHDInsightClusterAutoscaleConfiguration** sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1ae5d-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ae5d-116">EXAMPLES</span></span>

### <span data-ttu-id="1ae5d-117">Esempio 1: impostare la configurazione della scala automatica basata sul caricamento del cluster HDInsight</span><span class="sxs-lookup"><span data-stu-id="1ae5d-117">Example 1: Set the Load-based autoscale configuration of the HDInsight cluster</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup `
            -ClusterName $clusterName -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="1ae5d-118">Questo comando imposta la configurazione della scala automatica basata sul caricamento di un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1ae5d-118">This command sets the Load-based autoscale configuration of an Azure HDInsight cluster.</span></span>

### <span data-ttu-id="1ae5d-119">Esempio 2: impostare la scala automatica basata su pianificazione del cluster HDInsight</span><span class="sxs-lookup"><span data-stu-id="1ae5d-119">Example 2: Set the Schedule-based autoscale of the HDInsight cluster</span></span>
```powershell
# Create autoscale conditions
PS C:\> $condition1=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
PS C:\> $condition2=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 4 -Day Friday

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition1,$condition2
```

<span data-ttu-id="1ae5d-120">Questo comando imposta la configurazione della scala automatica basata su pianificazione del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1ae5d-120">This command sets the Schedule-based autoscale configuration of the HDInsight cluster.</span></span>

### <span data-ttu-id="1ae5d-121">Esempio 3: impostare la configurazione di scala automatica del cluster HDInsight basato su un altro cluster che ha impostato la configurazione di scala automatica</span><span class="sxs-lookup"><span data-stu-id="1ae5d-121">Example 3: Set the autoscale configuration of the HDInsight cluster based another cluster which has set autoscale configuration</span></span>
```powershell
# Get the autoscale configuration of another cluster.
PS C:\> $clusterResourceGroup="group"
PS C:\> $anotherClusterName="anotherClusterName"
PS C:\> $autoscaleConfig=Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $anotherClusterName

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName `
            -Autoscale $autoscaleConfig
```

<span data-ttu-id="1ae5d-122">Questo comando imposta la configurazione di scala automatica del cluster HDInsight basato su un altro cluster.</span><span class="sxs-lookup"><span data-stu-id="1ae5d-122">This command sets the autoscale configuration of the HDInsight cluster based another cluster.</span></span>

## <span data-ttu-id="1ae5d-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1ae5d-123">PARAMETERS</span></span>

### <span data-ttu-id="1ae5d-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ae5d-124">-AsJob</span></span>
<span data-ttu-id="1ae5d-125">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1ae5d-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ae5d-126">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ae5d-126">-AutoscaleConfiguration</span></span>
<span data-ttu-id="1ae5d-127">Ottiene o imposta la configurazione di scala automatica</span><span class="sxs-lookup"><span data-stu-id="1ae5d-127">Gets or sets the autoscale configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: AutoscaleConfigurationByNameParameterSet, AutoscaleConfigurationByResourceIdParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae5d-128">-Clustername</span><span class="sxs-lookup"><span data-stu-id="1ae5d-128">-ClusterName</span></span>
<span data-ttu-id="1ae5d-129">Ottiene o imposta il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="1ae5d-129">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae5d-130">-Condition</span><span class="sxs-lookup"><span data-stu-id="1ae5d-130">-Condition</span></span>
<span data-ttu-id="1ae5d-131">Ottiene o imposta la condizione di scala automatica basata su pianificazione.</span><span class="sxs-lookup"><span data-stu-id="1ae5d-131">Gets or sets the condition of schedule-based autoscale.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae5d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae5d-132">-DefaultProfile</span></span>
<span data-ttu-id="1ae5d-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ae5d-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ae5d-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ae5d-134">-InputObject</span></span>
<span data-ttu-id="1ae5d-135">Ottiene o imposta l'oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="1ae5d-135">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: LoadAutoscaleByInputObjectParameterSet, ScheduleAutoscaleByInputObjectParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae5d-136">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="1ae5d-136">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="1ae5d-137">Ottiene o imposta il numero massimo di workernode di scala di ridimensionamento basato su carico.</span><span class="sxs-lookup"><span data-stu-id="1ae5d-137">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae5d-138">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="1ae5d-138">-MinWorkerNodeCount</span></span>
<span data-ttu-id="1ae5d-139">Ottiene o imposta il numero minimo di workernode di scala di ridimensionamento basato su carico.</span><span class="sxs-lookup"><span data-stu-id="1ae5d-139">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae5d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae5d-140">-ResourceGroupName</span></span>
<span data-ttu-id="1ae5d-141">Ottiene o imposta il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1ae5d-141">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae5d-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ae5d-142">-ResourceId</span></span>
<span data-ttu-id="1ae5d-143">Ottiene o imposta l'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="1ae5d-143">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByResourceIdParameterSet, AutoscaleConfigurationByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae5d-144">-Programmazione</span><span class="sxs-lookup"><span data-stu-id="1ae5d-144">-Schedule</span></span>
<span data-ttu-id="1ae5d-145">Impostare i parametri basati sulla pianificazione</span><span class="sxs-lookup"><span data-stu-id="1ae5d-145">Set schedule-based parameters</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae5d-146">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="1ae5d-146">-TimeZone</span></span>
<span data-ttu-id="1ae5d-147">Ottiene o imposta il fuso orario di scala automatica basata su pianificazione.</span><span class="sxs-lookup"><span data-stu-id="1ae5d-147">Gets or sets the time zone of schedule-based autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae5d-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1ae5d-148">-Confirm</span></span>
<span data-ttu-id="1ae5d-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ae5d-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ae5d-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ae5d-150">-WhatIf</span></span>
<span data-ttu-id="1ae5d-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ae5d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ae5d-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ae5d-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ae5d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae5d-153">CommonParameters</span></span>
<span data-ttu-id="1ae5d-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae5d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae5d-155">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ae5d-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae5d-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1ae5d-156">INPUTS</span></span>

### <span data-ttu-id="1ae5d-157">System. String</span><span class="sxs-lookup"><span data-stu-id="1ae5d-157">System.String</span></span>

### <span data-ttu-id="1ae5d-158">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="1ae5d-158">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="1ae5d-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ae5d-159">OUTPUTS</span></span>

### <span data-ttu-id="1ae5d-160">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="1ae5d-160">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="1ae5d-161">Note</span><span class="sxs-lookup"><span data-stu-id="1ae5d-161">NOTES</span></span>

## <span data-ttu-id="1ae5d-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ae5d-162">RELATED LINKS</span></span>

<span data-ttu-id="1ae5d-163">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1ae5d-163">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
