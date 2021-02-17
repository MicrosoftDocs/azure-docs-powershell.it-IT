---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclustersku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
ms.openlocfilehash: 42fed776d1f77211c7967dd6313d0ddd1e04b65a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185263"
---
# <span data-ttu-id="870a4-101">Get-AzKustoClusterSku</span><span class="sxs-lookup"><span data-stu-id="870a4-101">Get-AzKustoClusterSku</span></span>

## <span data-ttu-id="870a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="870a4-102">SYNOPSIS</span></span>
<span data-ttu-id="870a4-103">Elenca gli SKU idonei per il provider di risorse Kusto.</span><span class="sxs-lookup"><span data-stu-id="870a4-103">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="870a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="870a4-104">SYNTAX</span></span>

### <span data-ttu-id="870a4-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="870a4-105">List (Default)</span></span>
```
Get-AzKustoClusterSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="870a4-106">Elenco1</span><span class="sxs-lookup"><span data-stu-id="870a4-106">List1</span></span>
```
Get-AzKustoClusterSku -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="870a4-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="870a4-107">DESCRIPTION</span></span>
<span data-ttu-id="870a4-108">Elenca gli SKU idonei per il provider di risorse Kusto.</span><span class="sxs-lookup"><span data-stu-id="870a4-108">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="870a4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="870a4-109">EXAMPLES</span></span>

### <span data-ttu-id="870a4-110">Esempio 1: Elenca gli SKU idonei</span><span class="sxs-lookup"><span data-stu-id="870a4-110">Example 1: Lists eligible SKUs</span></span>
```powershell
PS C:\> Get-AzKustoClusterSku

Location             Name                        ResourceType Tier
--------             ----                        ------------ ----
{eastus2}            D13_v2                      clusters     Standard
{eastus2}            D14_v2                      clusters     Standard
{eastus2}            L8                          clusters     Standard
{eastus2}            L16                         clusters     Standard
{eastus2}            D11_v2                      clusters     Standard
{eastus2}            D12_v2                      clusters     Standard
{eastus2}            L4                          clusters     Standard
{eastus2}            Standard_D13_v2             clusters     Standard
{eastus2}            Standard_D14_v2             clusters     Standard
{eastus2}            Standard_L8s                clusters     Standard
{eastus2}            Standard_L16s               clusters     Standard
{eastus2}            Standard_D11_v2             clusters     Standard
{eastus2}            Standard_D12_v2             clusters     Standard
{eastus2}            Standard_L4s                clusters     Standard
{eastus2}            Standard_DS13_v2+1TB_PS     clusters     Standard
{eastus2}            Standard_DS13_v2+2TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+3TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+4TB_PS     clusters     Standard
{eastus2}            Dev(No SLA)_Standard_D11_v2 clusters     Basic
{westcentralus}      D13_v2                      clusters     Standard
{westcentralus}      D14_v2                      clusters     Standard
{westcentralus}      D11_v2                      clusters     Standard
{westcentralus}      D12_v2                      clusters     Standard
{westcentralus}      Standard_D13_v2             clusters     Standard
{westcentralus}      Standard_D14_v2             clusters     Standard
{westcentralus}      Standard_D11_v2             clusters     Standard
{westcentralus}      Standard_D12_v2             clusters     Standard
{westcentralus}      Standard_DS13_v2+1TB_PS     clusters     Standard
{westcentralus}      Standard_DS13_v2+2TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+3TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+4TB_PS     clusters     Standard
...
```

<span data-ttu-id="870a4-111">Il comando precedente elenca gli SKU idonei.</span><span class="sxs-lookup"><span data-stu-id="870a4-111">The above command lists eligible SKUs.</span></span>

### <span data-ttu-id="870a4-112">Esempio 2: elenca gli SKU idonei per un cluster specifico</span><span class="sxs-lookup"><span data-stu-id="870a4-112">Example 2: Lists eligible SKUs for specific cluster</span></span>
```powershell
PS C:\>  Get-AzKustoClusterSku -ResourceGroupName testrg -ClusterName testnewkustocluster

ResourceType
------------
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
...
```

<span data-ttu-id="870a4-113">Il comando precedente elenca gli SKU idonei per un cluster specifico</span><span class="sxs-lookup"><span data-stu-id="870a4-113">The above command lists eligible SKUs for specific cluster</span></span>

## <span data-ttu-id="870a4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="870a4-114">PARAMETERS</span></span>

### <span data-ttu-id="870a4-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="870a4-115">-ClusterName</span></span>
<span data-ttu-id="870a4-116">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="870a4-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="870a4-117">-DefaultProfile</span></span>
<span data-ttu-id="870a4-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="870a4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870a4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="870a4-119">-ResourceGroupName</span></span>
<span data-ttu-id="870a4-120">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="870a4-120">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870a4-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="870a4-121">-SubscriptionId</span></span>
<span data-ttu-id="870a4-122">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="870a4-122">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="870a4-123">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="870a4-123">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870a4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="870a4-124">CommonParameters</span></span>
<span data-ttu-id="870a4-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="870a4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="870a4-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="870a4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="870a4-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="870a4-127">INPUTS</span></span>

## <span data-ttu-id="870a4-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="870a4-128">OUTPUTS</span></span>

### <span data-ttu-id="870a4-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAzureResourceSku</span><span class="sxs-lookup"><span data-stu-id="870a4-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAzureResourceSku</span></span>

### <span data-ttu-id="870a4-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ISkuDescription</span><span class="sxs-lookup"><span data-stu-id="870a4-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ISkuDescription</span></span>

## <span data-ttu-id="870a4-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="870a4-131">NOTES</span></span>

<span data-ttu-id="870a4-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="870a4-132">ALIASES</span></span>

## <span data-ttu-id="870a4-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="870a4-133">RELATED LINKS</span></span>

