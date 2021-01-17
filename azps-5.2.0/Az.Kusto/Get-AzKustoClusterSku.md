---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclustersku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
ms.openlocfilehash: 88b3104512b1cad4cddf98f521b44c6b638c05b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371111"
---
# <span data-ttu-id="ecbf1-101">Get-AzKustoClusterSku</span><span class="sxs-lookup"><span data-stu-id="ecbf1-101">Get-AzKustoClusterSku</span></span>

## <span data-ttu-id="ecbf1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ecbf1-102">SYNOPSIS</span></span>
<span data-ttu-id="ecbf1-103">Elenca SKU idonee per il provider di risorse kusto.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-103">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="ecbf1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecbf1-104">SYNTAX</span></span>

### <span data-ttu-id="ecbf1-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ecbf1-105">List (Default)</span></span>
```
Get-AzKustoClusterSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ecbf1-106">List1</span><span class="sxs-lookup"><span data-stu-id="ecbf1-106">List1</span></span>
```
Get-AzKustoClusterSku -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ecbf1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ecbf1-107">DESCRIPTION</span></span>
<span data-ttu-id="ecbf1-108">Elenca SKU idonee per il provider di risorse kusto.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-108">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="ecbf1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecbf1-109">EXAMPLES</span></span>

### <span data-ttu-id="ecbf1-110">Esempio 1: elenca le SKU idonee</span><span class="sxs-lookup"><span data-stu-id="ecbf1-110">Example 1: Lists eligible SKUs</span></span>
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

<span data-ttu-id="ecbf1-111">Il comando precedente elenca gli SKU idonei.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-111">The above command lists eligible SKUs.</span></span>

### <span data-ttu-id="ecbf1-112">Esempio 2: elenca SKU idonee per un cluster specifico</span><span class="sxs-lookup"><span data-stu-id="ecbf1-112">Example 2: Lists eligible SKUs for specific cluster</span></span>
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

<span data-ttu-id="ecbf1-113">Il comando precedente elenca SKU idonee per un cluster specifico</span><span class="sxs-lookup"><span data-stu-id="ecbf1-113">The above command lists eligible SKUs for specific cluster</span></span>

## <span data-ttu-id="ecbf1-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ecbf1-114">PARAMETERS</span></span>

### <span data-ttu-id="ecbf1-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="ecbf1-115">-ClusterName</span></span>
<span data-ttu-id="ecbf1-116">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ecbf1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecbf1-117">-DefaultProfile</span></span>
<span data-ttu-id="ecbf1-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecbf1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecbf1-119">-ResourceGroupName</span></span>
<span data-ttu-id="ecbf1-120">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-120">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ecbf1-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ecbf1-121">-SubscriptionId</span></span>
<span data-ttu-id="ecbf1-122">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-122">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ecbf1-123">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ecbf1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecbf1-124">CommonParameters</span></span>
<span data-ttu-id="ecbf1-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecbf1-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecbf1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecbf1-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ecbf1-127">INPUTS</span></span>

## <span data-ttu-id="ecbf1-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecbf1-128">OUTPUTS</span></span>

### <span data-ttu-id="ecbf1-129">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. IAzureResourceSku</span><span class="sxs-lookup"><span data-stu-id="ecbf1-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAzureResourceSku</span></span>

### <span data-ttu-id="ecbf1-130">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. ISkuDescription</span><span class="sxs-lookup"><span data-stu-id="ecbf1-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ISkuDescription</span></span>

## <span data-ttu-id="ecbf1-131">Note</span><span class="sxs-lookup"><span data-stu-id="ecbf1-131">NOTES</span></span>

<span data-ttu-id="ecbf1-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ecbf1-132">ALIASES</span></span>

## <span data-ttu-id="ecbf1-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecbf1-133">RELATED LINKS</span></span>

