---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: ad4867bc97f35a6e027d0f944d936da1760d1033
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009133"
---
# <span data-ttu-id="79808-101">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="79808-101">Get-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="79808-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79808-102">SYNOPSIS</span></span>
<span data-ttu-id="79808-103">Ottiene lo stato di monitoraggio dell'installazione nel cluster.</span><span class="sxs-lookup"><span data-stu-id="79808-103">Gets the status of monitoring installation on the cluster.</span></span>

## <span data-ttu-id="79808-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79808-104">SYNTAX</span></span>

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79808-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="79808-105">DESCRIPTION</span></span>
<span data-ttu-id="79808-106">Il cmdlet **Get-AzHDInsightMonitoring** ottiene lo stato di monitoraggio dell'installazione in un cluster Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="79808-106">The **Get-AzHDInsightMonitoring** cmdlet gets the status of monitoring installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="79808-107">Se il monitoraggio è abilitato, verrà restituito anche l'ID dell'area di lavoro analisi log.</span><span class="sxs-lookup"><span data-stu-id="79808-107">If monitoring is enabled then it will also return the log analytics workspace id.</span></span>

## <span data-ttu-id="79808-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79808-108">EXAMPLES</span></span>

### <span data-ttu-id="79808-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="79808-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="79808-110">Il monitoraggio è abilitato nel cluster perché la proprietà ClusterMonitoringEnabled è true.</span><span class="sxs-lookup"><span data-stu-id="79808-110">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="79808-111">L'ID area di lavoro di monitoraggio in cui vengono scorrono i log è 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="79808-111">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="79808-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="79808-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="79808-113">Il monitoraggio è abilitato nel cluster perché la proprietà ClusterMonitoringEnabled è true.</span><span class="sxs-lookup"><span data-stu-id="79808-113">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="79808-114">L'ID area di lavoro di monitoraggio in cui vengono scorrono i log è 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="79808-114">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="79808-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="79808-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="79808-116">Il monitoraggio è disabilitato nel cluster perché la proprietà ClusterMonitoringEnabled è false.</span><span class="sxs-lookup"><span data-stu-id="79808-116">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="79808-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="79808-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="79808-118">Il monitoraggio è disabilitato nel cluster perché la proprietà ClusterMonitoringEnabled è false.</span><span class="sxs-lookup"><span data-stu-id="79808-118">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="79808-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79808-119">PARAMETERS</span></span>

### <span data-ttu-id="79808-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79808-120">-DefaultProfile</span></span>
<span data-ttu-id="79808-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="79808-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79808-122">-Name</span><span class="sxs-lookup"><span data-stu-id="79808-122">-Name</span></span>
<span data-ttu-id="79808-123">Nome del cluster per cui ottenere lo stato di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="79808-123">The name of the cluster to get the status of monitoring.</span></span>

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

### <span data-ttu-id="79808-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79808-124">-ResourceGroupName</span></span>
<span data-ttu-id="79808-125">Gruppo di risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="79808-125">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="79808-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79808-126">CommonParameters</span></span>
<span data-ttu-id="79808-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79808-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79808-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="79808-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79808-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="79808-129">INPUTS</span></span>

### <span data-ttu-id="79808-130">System.String</span><span class="sxs-lookup"><span data-stu-id="79808-130">System.String</span></span>

## <span data-ttu-id="79808-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79808-131">OUTPUTS</span></span>

### <span data-ttu-id="79808-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="79808-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span></span>

## <span data-ttu-id="79808-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="79808-133">NOTES</span></span>

## <span data-ttu-id="79808-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79808-134">RELATED LINKS</span></span>
