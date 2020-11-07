---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 0f3e9e542ff1d05a9872096a784c8dabfed1910b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688312"
---
# <span data-ttu-id="c6c8e-101">Get-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="c6c8e-101">Get-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="c6c8e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c6c8e-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c8e-103">Ottiene lo stato dell'installazione di Operations Management Suite (OMS) nel cluster.</span><span class="sxs-lookup"><span data-stu-id="c6c8e-103">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6c8e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6c8e-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6c8e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6c8e-105">DESCRIPTION</span></span>
<span data-ttu-id="c6c8e-106">Il cmdlet **Get-AzureRmHDInsightOperationsManagementSuite** ottiene lo stato dell'installazione OMS in un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="c6c8e-106">The **Get-AzureRmHDInsightOperationsManagementSuite** cmdlet gets the status of OMS installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="c6c8e-107">Se OMS è abilitato, restituirà anche l'ID area di lavoro OMS.</span><span class="sxs-lookup"><span data-stu-id="c6c8e-107">If OMS is enabled then it will also return the OMS workspace id.</span></span>

## <span data-ttu-id="c6c8e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6c8e-108">EXAMPLES</span></span>

### <span data-ttu-id="c6c8e-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c6c8e-109">Example 1</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="c6c8e-110">L'OMS (Operations Management Suite) è abilitato nel cluster perché la proprietà ClusterMonitoringEnabled è true.</span><span class="sxs-lookup"><span data-stu-id="c6c8e-110">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="c6c8e-111">L'ID area di lavoro OMS in cui scorrono i registri è 1d364e89-BB71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="c6c8e-111">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="c6c8e-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c6c8e-112">Example 2</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="c6c8e-113">L'OMS (Operations Management Suite) è abilitato nel cluster perché la proprietà ClusterMonitoringEnabled è true.</span><span class="sxs-lookup"><span data-stu-id="c6c8e-113">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="c6c8e-114">L'ID area di lavoro OMS in cui scorrono i registri è 1d364e89-BB71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="c6c8e-114">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="c6c8e-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c6c8e-115">Example 3</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="c6c8e-116">L'OMS (Operations Management Suite) è disabilitata nel cluster perché la proprietà ClusterMonitoringEnabled è false.</span><span class="sxs-lookup"><span data-stu-id="c6c8e-116">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="c6c8e-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="c6c8e-117">Example 4</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="c6c8e-118">L'OMS (Operations Management Suite) è disabilitata nel cluster perché la proprietà ClusterMonitoringEnabled è false.</span><span class="sxs-lookup"><span data-stu-id="c6c8e-118">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="c6c8e-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c6c8e-119">PARAMETERS</span></span>

### <span data-ttu-id="c6c8e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6c8e-120">-Name</span></span>
<span data-ttu-id="c6c8e-121">Nome del cluster per ottenere lo stato di Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="c6c8e-121">The name of the cluster to get the status of Operations Management Suite(OMS).</span></span>

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

### <span data-ttu-id="c6c8e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6c8e-122">-ResourceGroupName</span></span>
<span data-ttu-id="c6c8e-123">Gruppo di risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="c6c8e-123">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="c6c8e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6c8e-124">-DefaultProfile</span></span>
<span data-ttu-id="c6c8e-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6c8e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6c8e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c8e-126">CommonParameters</span></span>
<span data-ttu-id="c6c8e-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6c8e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c8e-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6c8e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c8e-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c6c8e-129">INPUTS</span></span>

### <span data-ttu-id="c6c8e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c6c8e-130">System.String</span></span>

## <span data-ttu-id="c6c8e-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6c8e-131">OUTPUTS</span></span>

### <span data-ttu-id="c6c8e-132">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="c6c8e-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightOMS</span></span>

## <span data-ttu-id="c6c8e-133">Note</span><span class="sxs-lookup"><span data-stu-id="c6c8e-133">NOTES</span></span>

## <span data-ttu-id="c6c8e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6c8e-134">RELATED LINKS</span></span>

