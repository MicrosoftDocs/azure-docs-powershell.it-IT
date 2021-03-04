---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
ms.openlocfilehash: bc78b7d791d0988ee692c12537aed3207066ba26
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997526"
---
# <span data-ttu-id="5d6be-101">Get-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="5d6be-101">Get-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="5d6be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d6be-102">SYNOPSIS</span></span>
<span data-ttu-id="5d6be-103">Ottenere o elencare cluster</span><span class="sxs-lookup"><span data-stu-id="5d6be-103">Get or list clusters</span></span>

## <span data-ttu-id="5d6be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d6be-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d6be-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5d6be-105">DESCRIPTION</span></span>
<span data-ttu-id="5d6be-106">Ottenere o elencare cluster, cluster di elenchi in un gruppo di risorse quando non è stato fornito "-ClusterName", cluster di elenchi in abbonamento quando non sono stati forniti "-ClusterName" e "ResourceGroupName".</span><span class="sxs-lookup"><span data-stu-id="5d6be-106">Get or list clusters, list clusters under resource group when "-ClusterName" was not provided, list clusters under subscription when "-ClusterName" and "ResourceGroupName" were not provided.</span></span>

## <span data-ttu-id="5d6be-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d6be-107">EXAMPLES</span></span>

### <span data-ttu-id="5d6be-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5d6be-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : Succeeded
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="5d6be-109">Ottieni cluster</span><span class="sxs-lookup"><span data-stu-id="5d6be-109">Get cluster</span></span>

## <span data-ttu-id="5d6be-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d6be-110">PARAMETERS</span></span>

### <span data-ttu-id="5d6be-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5d6be-111">-ClusterName</span></span>
<span data-ttu-id="5d6be-112">Nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="5d6be-112">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d6be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d6be-113">-DefaultProfile</span></span>
<span data-ttu-id="5d6be-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d6be-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d6be-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d6be-115">-ResourceGroupName</span></span>
<span data-ttu-id="5d6be-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5d6be-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d6be-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d6be-117">CommonParameters</span></span>
<span data-ttu-id="5d6be-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d6be-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d6be-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5d6be-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d6be-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="5d6be-120">INPUTS</span></span>

### <span data-ttu-id="5d6be-121">System.String</span><span class="sxs-lookup"><span data-stu-id="5d6be-121">System.String</span></span>

## <span data-ttu-id="5d6be-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d6be-122">OUTPUTS</span></span>

### <span data-ttu-id="5d6be-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="5d6be-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="5d6be-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="5d6be-124">NOTES</span></span>

## <span data-ttu-id="5d6be-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d6be-125">RELATED LINKS</span></span>
