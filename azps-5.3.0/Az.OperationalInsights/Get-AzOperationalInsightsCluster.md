---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
ms.openlocfilehash: aaa3522afb3bf021f2bf5fbff5ec6c3d9e14928f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488840"
---
# <span data-ttu-id="dc1e9-101">Get-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="dc1e9-101">Get-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="dc1e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dc1e9-102">SYNOPSIS</span></span>
<span data-ttu-id="dc1e9-103">Ottenere o elencare i cluster</span><span class="sxs-lookup"><span data-stu-id="dc1e9-103">Get or list clusters</span></span>

## <span data-ttu-id="dc1e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc1e9-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc1e9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc1e9-105">DESCRIPTION</span></span>
<span data-ttu-id="dc1e9-106">Ottenere o elencare i cluster, i cluster di elenco in gruppo risorse quando non è stato fornito "-clustername", elencare i cluster in abbonamento quando non sono stati forniti "-clustername" e "ResourceGroupName".</span><span class="sxs-lookup"><span data-stu-id="dc1e9-106">Get or list clusters, list clusters under resource group when "-ClusterName" was not provided, list clusters under subscription when "-ClusterName" and "ResourceGroupName" were not provided.</span></span>

## <span data-ttu-id="dc1e9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc1e9-107">EXAMPLES</span></span>

### <span data-ttu-id="dc1e9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dc1e9-108">Example 1</span></span>
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

<span data-ttu-id="dc1e9-109">Ottenere un cluster</span><span class="sxs-lookup"><span data-stu-id="dc1e9-109">Get cluster</span></span>

## <span data-ttu-id="dc1e9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dc1e9-110">PARAMETERS</span></span>

### <span data-ttu-id="dc1e9-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="dc1e9-111">-ClusterName</span></span>
<span data-ttu-id="dc1e9-112">Nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="dc1e9-112">The cluster name.</span></span>

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

### <span data-ttu-id="dc1e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc1e9-113">-DefaultProfile</span></span>
<span data-ttu-id="dc1e9-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dc1e9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc1e9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc1e9-115">-ResourceGroupName</span></span>
<span data-ttu-id="dc1e9-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dc1e9-116">The resource group name.</span></span>

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

### <span data-ttu-id="dc1e9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc1e9-117">CommonParameters</span></span>
<span data-ttu-id="dc1e9-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc1e9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc1e9-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc1e9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc1e9-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dc1e9-120">INPUTS</span></span>

### <span data-ttu-id="dc1e9-121">System. String</span><span class="sxs-lookup"><span data-stu-id="dc1e9-121">System.String</span></span>

## <span data-ttu-id="dc1e9-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc1e9-122">OUTPUTS</span></span>

### <span data-ttu-id="dc1e9-123">Microsoft. Azure. Commands. OperationalInsights. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="dc1e9-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="dc1e9-124">Note</span><span class="sxs-lookup"><span data-stu-id="dc1e9-124">NOTES</span></span>

## <span data-ttu-id="dc1e9-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc1e9-125">RELATED LINKS</span></span>
