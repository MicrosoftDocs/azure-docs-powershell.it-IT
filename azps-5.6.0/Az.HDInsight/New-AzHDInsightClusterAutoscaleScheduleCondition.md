---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleschedulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
ms.openlocfilehash: c2fcc4112bb2fb62b73531bd6bd580ba3bcd7648
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009037"
---
# <span data-ttu-id="704bd-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="704bd-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>

## <span data-ttu-id="704bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="704bd-102">SYNOPSIS</span></span>
<span data-ttu-id="704bd-103">Crea una condizione di gradazioni automatica basata su pianificazione.</span><span class="sxs-lookup"><span data-stu-id="704bd-103">Creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="704bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="704bd-104">SYNTAX</span></span>

```
New-AzHDInsightClusterAutoscaleScheduleCondition -Time <DateTime> -WorkerNodeCount <Int32>
 -Day <AzureHDInsightDaysOfWeek[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="704bd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="704bd-105">DESCRIPTION</span></span>
<span data-ttu-id="704bd-106">Il cmdlet **New-AzHDInsightClusterAutoscaleScheduleCondition crea** una condizione di gradazione automatica basata su pianificazione.</span><span class="sxs-lookup"><span data-stu-id="704bd-106">The **New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="704bd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="704bd-107">EXAMPLES</span></span>

### <span data-ttu-id="704bd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="704bd-108">Example 1</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
```

<span data-ttu-id="704bd-109">Questo comando crea una condizione in cui il cluster viene ridimensionato automaticamente su 5 nodi di lavoro alle 09:00 ogni lunedì, mercoledì.</span><span class="sxs-lookup"><span data-stu-id="704bd-109">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

### <span data-ttu-id="704bd-110">Esempio 2: Abilitare la scala automatica basata sulla pianificazione di un cluster con una condizione di gradazione automatica.</span><span class="sxs-lookup"><span data-stu-id="704bd-110">Example 2: Enable Schedule-based autoscale of a cluster with autoscale condition.</span></span>
```powershell
# create a autoscale condition
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday

# Set the cluster autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition
```

<span data-ttu-id="704bd-111">Questo comando crea una condizione in cui il cluster viene ridimensionato automaticamente su 5 nodi di lavoro alle 09:00 ogni lunedì, mercoledì.</span><span class="sxs-lookup"><span data-stu-id="704bd-111">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

## <span data-ttu-id="704bd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="704bd-112">PARAMETERS</span></span>

### <span data-ttu-id="704bd-113">-Day</span><span class="sxs-lookup"><span data-stu-id="704bd-113">-Day</span></span>
<span data-ttu-id="704bd-114">Ottiene o imposta i giorni della condizione di pianificazione di scala automatica.</span><span class="sxs-lookup"><span data-stu-id="704bd-114">Gets or sets the days of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="704bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="704bd-115">-DefaultProfile</span></span>
<span data-ttu-id="704bd-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="704bd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="704bd-117">-Time</span><span class="sxs-lookup"><span data-stu-id="704bd-117">-Time</span></span>
<span data-ttu-id="704bd-118">Ottiene o imposta l'ora della condizione di pianificazione di Scala automatica.</span><span class="sxs-lookup"><span data-stu-id="704bd-118">Gets or sets the time of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="704bd-119">-WorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="704bd-119">-WorkerNodeCount</span></span>
<span data-ttu-id="704bd-120">Ottiene o imposta il numero di elementi workernode della condizione di pianificazione di gradazioni automatica.</span><span class="sxs-lookup"><span data-stu-id="704bd-120">Gets or sets the schedule workernode count of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="704bd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="704bd-121">CommonParameters</span></span>
<span data-ttu-id="704bd-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="704bd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="704bd-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="704bd-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="704bd-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="704bd-124">INPUTS</span></span>

### <span data-ttu-id="704bd-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="704bd-125">None</span></span>

## <span data-ttu-id="704bd-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="704bd-126">OUTPUTS</span></span>

### <span data-ttu-id="704bd-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span><span class="sxs-lookup"><span data-stu-id="704bd-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span></span>

## <span data-ttu-id="704bd-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="704bd-128">NOTES</span></span>

## <span data-ttu-id="704bd-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="704bd-129">RELATED LINKS</span></span>

<span data-ttu-id="704bd-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="704bd-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
