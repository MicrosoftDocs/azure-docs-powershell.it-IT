---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 5fbc34f3a5a2a7b87c0e7319c5d6243e1207dc61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686070"
---
# <span data-ttu-id="968a5-101">Get-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="968a5-101">Get-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="968a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="968a5-102">SYNOPSIS</span></span>
<span data-ttu-id="968a5-103">Ottiene lo stato dell'installazione di Operations Management Suite (OMS) nel cluster.</span><span class="sxs-lookup"><span data-stu-id="968a5-103">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="968a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="968a5-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="968a5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="968a5-105">DESCRIPTION</span></span>
<span data-ttu-id="968a5-106">Il cmdlet **Get-AzureRmHDInsightOperationsManagementSuite** ottiene lo stato dell'installazione OMS in un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="968a5-106">The **Get-AzureRmHDInsightOperationsManagementSuite** cmdlet gets the status of OMS installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="968a5-107">Se OMS è abilitato, restituirà anche l'ID area di lavoro OMS.</span><span class="sxs-lookup"><span data-stu-id="968a5-107">If OMS is enabled then it will also return the OMS workspace id.</span></span>

## <span data-ttu-id="968a5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="968a5-108">EXAMPLES</span></span>

### <span data-ttu-id="968a5-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="968a5-109">Example 1</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="968a5-110">L'OMS (Operations Management Suite) è abilitato nel cluster perché la proprietà ClusterMonitoringEnabled è true.</span><span class="sxs-lookup"><span data-stu-id="968a5-110">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="968a5-111">L'ID area di lavoro OMS in cui scorrono i registri è 1d364e89-BB71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="968a5-111">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="968a5-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="968a5-112">Example 2</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="968a5-113">L'OMS (Operations Management Suite) è abilitato nel cluster perché la proprietà ClusterMonitoringEnabled è true.</span><span class="sxs-lookup"><span data-stu-id="968a5-113">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="968a5-114">L'ID area di lavoro OMS in cui scorrono i registri è 1d364e89-BB71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="968a5-114">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="968a5-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="968a5-115">Example 3</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="968a5-116">L'OMS (Operations Management Suite) è disabilitata nel cluster perché la proprietà ClusterMonitoringEnabled è false.</span><span class="sxs-lookup"><span data-stu-id="968a5-116">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="968a5-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="968a5-117">Example 4</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="968a5-118">L'OMS (Operations Management Suite) è disabilitata nel cluster perché la proprietà ClusterMonitoringEnabled è false.</span><span class="sxs-lookup"><span data-stu-id="968a5-118">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="968a5-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="968a5-119">PARAMETERS</span></span>

### <span data-ttu-id="968a5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="968a5-120">-DefaultProfile</span></span>
<span data-ttu-id="968a5-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="968a5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="968a5-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="968a5-122">-Name</span></span>
<span data-ttu-id="968a5-123">Nome del cluster per ottenere lo stato di Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="968a5-123">The name of the cluster to get the status of Operations Management Suite(OMS).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="968a5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="968a5-124">-ResourceGroupName</span></span>
<span data-ttu-id="968a5-125">Gruppo di risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="968a5-125">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="968a5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="968a5-126">CommonParameters</span></span>
<span data-ttu-id="968a5-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="968a5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="968a5-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="968a5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="968a5-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="968a5-129">INPUTS</span></span>

### <span data-ttu-id="968a5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="968a5-130">System.String</span></span>

## <span data-ttu-id="968a5-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="968a5-131">OUTPUTS</span></span>

### <span data-ttu-id="968a5-132">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="968a5-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightOMS</span></span>

## <span data-ttu-id="968a5-133">Note</span><span class="sxs-lookup"><span data-stu-id="968a5-133">NOTES</span></span>

## <span data-ttu-id="968a5-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="968a5-134">RELATED LINKS</span></span>
