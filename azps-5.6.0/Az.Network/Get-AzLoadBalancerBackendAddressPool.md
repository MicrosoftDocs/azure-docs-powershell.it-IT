---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 72afb446b41143348b9feaa7e1b465a41d2b9cbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956830"
---
# <span data-ttu-id="ffc51-101">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ffc51-101">Get-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="ffc51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffc51-102">SYNOPSIS</span></span>
<span data-ttu-id="ffc51-103">Get-AzLoadBalancerBackendAddressPool recupera uno o più pool di indirizzi back-end associati a un servizio di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="ffc51-103">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span> 

## <span data-ttu-id="ffc51-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ffc51-104">SYNTAX</span></span>

### <span data-ttu-id="ffc51-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffc51-105">GetByNameParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffc51-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffc51-106">GetByParentObjectParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffc51-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffc51-107">GetByResourceIdParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ffc51-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ffc51-108">DESCRIPTION</span></span>
<span data-ttu-id="ffc51-109">Get-AzLoadBalancerBackendAddressPool recupera uno o più pool di indirizzi back-end associati a un servizio di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="ffc51-109">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span>

## <span data-ttu-id="ffc51-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ffc51-110">EXAMPLES</span></span>

### <span data-ttu-id="ffc51-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ffc51-111">Example 1</span></span>
```powershell
## Get single backend under loadbalancer
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
```

```powershell
## Get all backends under loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool
```
### <span data-ttu-id="ffc51-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ffc51-112">Example 2</span></span>
```powershell
#Get specific backend from loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="ffc51-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="ffc51-113">Example 3</span></span>
```powershell
#Get a backend by resource Id
PS C:\> Get-AzLoadBalancerBackendAddressPool -ResourceId $backendPool1.Id
```

## <span data-ttu-id="ffc51-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffc51-114">PARAMETERS</span></span>

### <span data-ttu-id="ffc51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffc51-115">-DefaultProfile</span></span>
<span data-ttu-id="ffc51-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ffc51-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffc51-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ffc51-117">-LoadBalancer</span></span>
<span data-ttu-id="ffc51-118">{{ Fill LoadBalancer Description }}</span><span class="sxs-lookup"><span data-stu-id="ffc51-118">{{ Fill LoadBalancer Description }}</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc51-119">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="ffc51-119">-LoadBalancerName</span></span>
<span data-ttu-id="ffc51-120">Nome del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="ffc51-120">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc51-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ffc51-121">-Name</span></span>
<span data-ttu-id="ffc51-122">Nome del pool di indirizzi back-end.</span><span class="sxs-lookup"><span data-stu-id="ffc51-122">The name of the backend address pool.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc51-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffc51-123">-ResourceGroupName</span></span>
<span data-ttu-id="ffc51-124">Nome del gruppo di risorse per il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="ffc51-124">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc51-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ffc51-125">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc51-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffc51-126">CommonParameters</span></span>
<span data-ttu-id="ffc51-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffc51-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffc51-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ffc51-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffc51-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="ffc51-129">INPUTS</span></span>

### <span data-ttu-id="ffc51-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ffc51-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="ffc51-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ffc51-131">System.String</span></span>

## <span data-ttu-id="ffc51-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ffc51-132">OUTPUTS</span></span>

### <span data-ttu-id="ffc51-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ffc51-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="ffc51-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="ffc51-134">NOTES</span></span>

## <span data-ttu-id="ffc51-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ffc51-135">RELATED LINKS</span></span>
