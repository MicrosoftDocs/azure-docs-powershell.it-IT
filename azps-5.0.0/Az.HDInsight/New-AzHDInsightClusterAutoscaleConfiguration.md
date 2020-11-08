---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: c2d8e3c2f3da4ebd2d07d16965a24878af34e262
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193322"
---
# <span data-ttu-id="5b19f-101">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b19f-101">New-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="5b19f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b19f-102">SYNOPSIS</span></span>
<span data-ttu-id="5b19f-103">Crea un oggetto non persistente che descrive la configurazione di scala automatica di un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="5b19f-103">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="5b19f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b19f-104">SYNTAX</span></span>

### <span data-ttu-id="5b19f-105">LoadAutoscaleParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5b19f-105">LoadAutoscaleParameterSet (Default)</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount <Int32> -MaxWorkerNodeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b19f-106">ScheduleAutoscaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b19f-106">ScheduleAutoscaleParameterSet</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -TimeZone <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b19f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b19f-107">DESCRIPTION</span></span>
<span data-ttu-id="5b19f-108">Il cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** crea un oggetto non persistente che descrive la configurazione di scala automatica di un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="5b19f-108">The cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="5b19f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b19f-109">EXAMPLES</span></span>

### <span data-ttu-id="5b19f-110">Esempio 1: creare un oggetto che descrive la configurazione della scala automatica basata sul caricamento</span><span class="sxs-lookup"><span data-stu-id="5b19f-110">Example 1: Create an object which describes Load-based autoscale configuration</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="5b19f-111">Questo comando crea un oggetto che descrive la configurazione della scala automatica basata sul caricamento.</span><span class="sxs-lookup"><span data-stu-id="5b19f-111">This command creates an object which describes Load-based autoscale configuration.</span></span>

### <span data-ttu-id="5b19f-112">Esempio 2: creare un oggetto che descrive la configurazione di scala automatica basata su pianificazione</span><span class="sxs-lookup"><span data-stu-id="5b19f-112">Example 2: Create an object which describes Schedule-based autoscale configuration</span></span>
```powershell
# Create an autoscale condition firstly
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Day Monday -Time 09:00 -WorkerNodeCount 5
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -TimeZone ([System.TimeZoneInfo]::Local).Id `
        -Condition $condition
```

<span data-ttu-id="5b19f-113">Questo comando crea un oggetto che descrive la configurazione della scala automatica basata su pianificazione.</span><span class="sxs-lookup"><span data-stu-id="5b19f-113">This command creates an object which describes Schedule-based autoscale configuration.</span></span>

## <span data-ttu-id="5b19f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b19f-114">PARAMETERS</span></span>

### <span data-ttu-id="5b19f-115">-Condition</span><span class="sxs-lookup"><span data-stu-id="5b19f-115">-Condition</span></span>
<span data-ttu-id="5b19f-116">Ottiene o imposta la condizione di scala automatica basata su pianificazione.</span><span class="sxs-lookup"><span data-stu-id="5b19f-116">Gets or sets the condition of schedule-based autoscale.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b19f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b19f-117">-DefaultProfile</span></span>
<span data-ttu-id="5b19f-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b19f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b19f-119">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="5b19f-119">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="5b19f-120">Ottiene o imposta il numero massimo di workernode di scala di ridimensionamento basato su carico.</span><span class="sxs-lookup"><span data-stu-id="5b19f-120">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b19f-121">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="5b19f-121">-MinWorkerNodeCount</span></span>
<span data-ttu-id="5b19f-122">Ottiene o imposta il numero minimo di workernode di scala di ridimensionamento basato su carico.</span><span class="sxs-lookup"><span data-stu-id="5b19f-122">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b19f-123">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="5b19f-123">-TimeZone</span></span>
<span data-ttu-id="5b19f-124">Ottiene o imposta il fuso orario di scala automatica basata su pianificazione.</span><span class="sxs-lookup"><span data-stu-id="5b19f-124">Gets or sets the time zone of schedule-based autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b19f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b19f-125">CommonParameters</span></span>
<span data-ttu-id="5b19f-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b19f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b19f-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b19f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b19f-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b19f-128">INPUTS</span></span>

### <span data-ttu-id="5b19f-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5b19f-129">None</span></span>

## <span data-ttu-id="5b19f-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b19f-130">OUTPUTS</span></span>

### <span data-ttu-id="5b19f-131">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="5b19f-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="5b19f-132">Note</span><span class="sxs-lookup"><span data-stu-id="5b19f-132">NOTES</span></span>

## <span data-ttu-id="5b19f-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b19f-133">RELATED LINKS</span></span>

<span data-ttu-id="5b19f-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5b19f-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
