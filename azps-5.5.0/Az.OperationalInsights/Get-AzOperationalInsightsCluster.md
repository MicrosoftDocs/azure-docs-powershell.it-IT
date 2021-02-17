---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
ms.openlocfilehash: aaa3522afb3bf021f2bf5fbff5ec6c3d9e14928f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191486"
---
# <span data-ttu-id="2de92-101">Get-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="2de92-101">Get-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="2de92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2de92-102">SYNOPSIS</span></span>
<span data-ttu-id="2de92-103">Ottenere o elencare cluster</span><span class="sxs-lookup"><span data-stu-id="2de92-103">Get or list clusters</span></span>

## <span data-ttu-id="2de92-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2de92-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2de92-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2de92-105">DESCRIPTION</span></span>
<span data-ttu-id="2de92-106">Ottenere o elencare cluster, cluster di elenchi in un gruppo di risorse quando non è stato fornito "-ClusterName", cluster di elenchi in abbonamento quando non sono stati forniti "-ClusterName" e "ResourceGroupName".</span><span class="sxs-lookup"><span data-stu-id="2de92-106">Get or list clusters, list clusters under resource group when "-ClusterName" was not provided, list clusters under subscription when "-ClusterName" and "ResourceGroupName" were not provided.</span></span>

## <span data-ttu-id="2de92-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2de92-107">EXAMPLES</span></span>

### <span data-ttu-id="2de92-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2de92-108">Example 1</span></span>
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

<span data-ttu-id="2de92-109">Ottieni cluster</span><span class="sxs-lookup"><span data-stu-id="2de92-109">Get cluster</span></span>

## <span data-ttu-id="2de92-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2de92-110">PARAMETERS</span></span>

### <span data-ttu-id="2de92-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2de92-111">-ClusterName</span></span>
<span data-ttu-id="2de92-112">Nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="2de92-112">The cluster name.</span></span>

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

### <span data-ttu-id="2de92-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de92-113">-DefaultProfile</span></span>
<span data-ttu-id="2de92-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2de92-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2de92-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de92-115">-ResourceGroupName</span></span>
<span data-ttu-id="2de92-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2de92-116">The resource group name.</span></span>

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

### <span data-ttu-id="2de92-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de92-117">CommonParameters</span></span>
<span data-ttu-id="2de92-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2de92-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de92-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2de92-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de92-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="2de92-120">INPUTS</span></span>

### <span data-ttu-id="2de92-121">System.String</span><span class="sxs-lookup"><span data-stu-id="2de92-121">System.String</span></span>

## <span data-ttu-id="2de92-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2de92-122">OUTPUTS</span></span>

### <span data-ttu-id="2de92-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="2de92-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="2de92-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="2de92-124">NOTES</span></span>

## <span data-ttu-id="2de92-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2de92-125">RELATED LINKS</span></span>
