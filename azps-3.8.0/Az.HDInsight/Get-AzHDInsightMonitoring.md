---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: 2d91c96d20797988a7def2d11d633f36b08cb8cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865472"
---
# <span data-ttu-id="b3082-101">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="b3082-101">Get-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="b3082-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3082-102">SYNOPSIS</span></span>
<span data-ttu-id="b3082-103">Ottiene lo stato dell'installazione di monitoraggio nel cluster.</span><span class="sxs-lookup"><span data-stu-id="b3082-103">Gets the status of monitoring installation on the cluster.</span></span>

## <span data-ttu-id="b3082-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3082-104">SYNTAX</span></span>

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3082-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3082-105">DESCRIPTION</span></span>
<span data-ttu-id="b3082-106">Il cmdlet **Get-AzHDInsightMonitoring** ottiene lo stato di monitoraggio dell'installazione in un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="b3082-106">The **Get-AzHDInsightMonitoring** cmdlet gets the status of monitoring installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="b3082-107">Se il monitoraggio è abilitato, verrà restituito anche l'ID area di lavoro analisi log.</span><span class="sxs-lookup"><span data-stu-id="b3082-107">If monitoring is enabled then it will also return the log analytics workspace id.</span></span>

## <span data-ttu-id="b3082-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3082-108">EXAMPLES</span></span>

### <span data-ttu-id="b3082-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b3082-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="b3082-110">Il monitoraggio è abilitato nel cluster perché la proprietà ClusterMonitoringEnabled è true.</span><span class="sxs-lookup"><span data-stu-id="b3082-110">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="b3082-111">L'ID area di lavoro di monitoraggio in cui scorrono i registri è 1d364e89-BB71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="b3082-111">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="b3082-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b3082-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="b3082-113">Il monitoraggio è abilitato nel cluster perché la proprietà ClusterMonitoringEnabled è true.</span><span class="sxs-lookup"><span data-stu-id="b3082-113">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="b3082-114">L'ID area di lavoro di monitoraggio in cui scorrono i registri è 1d364e89-BB71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="b3082-114">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="b3082-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b3082-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="b3082-116">Il monitoraggio è disabilitato nel cluster perché la proprietà ClusterMonitoringEnabled è false.</span><span class="sxs-lookup"><span data-stu-id="b3082-116">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="b3082-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="b3082-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="b3082-118">Il monitoraggio è disabilitato nel cluster perché la proprietà ClusterMonitoringEnabled è false.</span><span class="sxs-lookup"><span data-stu-id="b3082-118">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="b3082-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3082-119">PARAMETERS</span></span>

### <span data-ttu-id="b3082-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3082-120">-DefaultProfile</span></span>
<span data-ttu-id="b3082-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b3082-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3082-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3082-122">-Name</span></span>
<span data-ttu-id="b3082-123">Nome del cluster per ottenere lo stato di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="b3082-123">The name of the cluster to get the status of monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3082-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3082-124">-ResourceGroupName</span></span>
<span data-ttu-id="b3082-125">Gruppo di risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="b3082-125">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3082-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3082-126">CommonParameters</span></span>
<span data-ttu-id="b3082-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3082-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3082-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3082-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3082-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3082-129">INPUTS</span></span>

### <span data-ttu-id="b3082-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b3082-130">System.String</span></span>

## <span data-ttu-id="b3082-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3082-131">OUTPUTS</span></span>

### <span data-ttu-id="b3082-132">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="b3082-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span></span>

## <span data-ttu-id="b3082-133">Note</span><span class="sxs-lookup"><span data-stu-id="b3082-133">NOTES</span></span>

## <span data-ttu-id="b3082-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3082-134">RELATED LINKS</span></span>
