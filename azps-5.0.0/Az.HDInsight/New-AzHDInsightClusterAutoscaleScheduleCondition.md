---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleschedulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
ms.openlocfilehash: 4f046344942e244d6bd220034f7cbe85c48681ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193321"
---
# <span data-ttu-id="e9183-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="e9183-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>

## <span data-ttu-id="e9183-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e9183-102">SYNOPSIS</span></span>
<span data-ttu-id="e9183-103">Crea una condizione di Autoscala basata su pianificazione.</span><span class="sxs-lookup"><span data-stu-id="e9183-103">Creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="e9183-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9183-104">SYNTAX</span></span>

```
New-AzHDInsightClusterAutoscaleScheduleCondition -Time <DateTime> -WorkerNodeCount <Int32>
 -Day <AzureHDInsightDaysOfWeek[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9183-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9183-105">DESCRIPTION</span></span>
<span data-ttu-id="e9183-106">Il cmdlet **New-AzHDInsightClusterAutoscaleScheduleCondition** crea una condizione di scala automatica basata su pianificazione.</span><span class="sxs-lookup"><span data-stu-id="e9183-106">The **New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="e9183-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9183-107">EXAMPLES</span></span>

### <span data-ttu-id="e9183-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e9183-108">Example 1</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
```

<span data-ttu-id="e9183-109">Questo comando crea una condizione in cui il cluster viene ridimensionato automaticamente a 5 nodi di lavoro a 09:00 ogni lunedì, mercoledì.</span><span class="sxs-lookup"><span data-stu-id="e9183-109">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

### <span data-ttu-id="e9183-110">Esempio 2: abilitare la scala automatica basata su pianificazione di un cluster con la condizione di scala automatica.</span><span class="sxs-lookup"><span data-stu-id="e9183-110">Example 2: Enable Schedule-based autoscale of a cluster with autoscale condition.</span></span>
```powershell
# create a autoscale condition
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday

# Set the cluster autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition
```

<span data-ttu-id="e9183-111">Questo comando crea una condizione in cui il cluster viene ridimensionato automaticamente a 5 nodi di lavoro a 09:00 ogni lunedì, mercoledì.</span><span class="sxs-lookup"><span data-stu-id="e9183-111">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

## <span data-ttu-id="e9183-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e9183-112">PARAMETERS</span></span>

### <span data-ttu-id="e9183-113">-Giorno</span><span class="sxs-lookup"><span data-stu-id="e9183-113">-Day</span></span>
<span data-ttu-id="e9183-114">Ottiene o imposta i giorni della condizione di pianificazione della scala automatica.</span><span class="sxs-lookup"><span data-stu-id="e9183-114">Gets or sets the days of Autoscale schedule condition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightDaysOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9183-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9183-115">-DefaultProfile</span></span>
<span data-ttu-id="e9183-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e9183-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9183-117">-Ora</span><span class="sxs-lookup"><span data-stu-id="e9183-117">-Time</span></span>
<span data-ttu-id="e9183-118">Ottiene o imposta l'ora della condizione di programmazione di scala automatica.</span><span class="sxs-lookup"><span data-stu-id="e9183-118">Gets or sets the time of Autoscale schedule condition.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9183-119">-WorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="e9183-119">-WorkerNodeCount</span></span>
<span data-ttu-id="e9183-120">Ottiene o imposta il conteggio workernode pianificazione della condizione di pianificazione della scala automatica.</span><span class="sxs-lookup"><span data-stu-id="e9183-120">Gets or sets the schedule workernode count of Autoscale schedule condition.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9183-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9183-121">CommonParameters</span></span>
<span data-ttu-id="e9183-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9183-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9183-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9183-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9183-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e9183-124">INPUTS</span></span>

### <span data-ttu-id="e9183-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e9183-125">None</span></span>

## <span data-ttu-id="e9183-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9183-126">OUTPUTS</span></span>

### <span data-ttu-id="e9183-127">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightAutoscaleCondition</span><span class="sxs-lookup"><span data-stu-id="e9183-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span></span>

## <span data-ttu-id="e9183-128">Note</span><span class="sxs-lookup"><span data-stu-id="e9183-128">NOTES</span></span>

## <span data-ttu-id="e9183-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9183-129">RELATED LINKS</span></span>

<span data-ttu-id="e9183-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e9183-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>