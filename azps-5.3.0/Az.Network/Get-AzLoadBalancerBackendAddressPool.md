---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 5d1c561af678086671927d3782a1fafbd9de503b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473966"
---
# <span data-ttu-id="95de1-101">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="95de1-101">Get-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="95de1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="95de1-102">SYNOPSIS</span></span>
<span data-ttu-id="95de1-103">Get-AzLoadBalancerBackendAddressPool recupera uno o più pool di indirizzi backend associati a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="95de1-103">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span> 

## <span data-ttu-id="95de1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95de1-104">SYNTAX</span></span>

### <span data-ttu-id="95de1-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="95de1-105">GetByNameParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95de1-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95de1-106">GetByParentObjectParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95de1-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="95de1-107">GetByResourceIdParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95de1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95de1-108">DESCRIPTION</span></span>
<span data-ttu-id="95de1-109">Get-AzLoadBalancerBackendAddressPool recupera uno o più pool di indirizzi backend associati a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="95de1-109">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span>

## <span data-ttu-id="95de1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95de1-110">EXAMPLES</span></span>

### <span data-ttu-id="95de1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="95de1-111">Example 1</span></span>
```powershell
## Get single backend under loadbalancer
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
```

```powershell
## Get all backends under loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool
```
### <span data-ttu-id="95de1-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="95de1-112">Example 2</span></span>
```powershell
#Get specific backend from loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="95de1-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="95de1-113">Example 3</span></span>
```powershell
#Get a backend by resource Id
PS C:\> Get-AzLoadBalancerBackendAddressPool -ResourceId $backendPool1.Id
```

## <span data-ttu-id="95de1-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="95de1-114">PARAMETERS</span></span>

### <span data-ttu-id="95de1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95de1-115">-DefaultProfile</span></span>
<span data-ttu-id="95de1-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="95de1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95de1-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95de1-117">-LoadBalancer</span></span>
<span data-ttu-id="95de1-118">{{Fill LoadBalancer Description}}</span><span class="sxs-lookup"><span data-stu-id="95de1-118">{{ Fill LoadBalancer Description }}</span></span>

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

### <span data-ttu-id="95de1-119">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="95de1-119">-LoadBalancerName</span></span>
<span data-ttu-id="95de1-120">Nome del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="95de1-120">The name of the load balancer.</span></span>

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

### <span data-ttu-id="95de1-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="95de1-121">-Name</span></span>
<span data-ttu-id="95de1-122">Nome del pool di indirizzi back-end.</span><span class="sxs-lookup"><span data-stu-id="95de1-122">The name of the backend address pool.</span></span>

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

### <span data-ttu-id="95de1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95de1-123">-ResourceGroupName</span></span>
<span data-ttu-id="95de1-124">Nome del gruppo di risorse del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="95de1-124">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="95de1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95de1-125">-ResourceId</span></span>

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

### <span data-ttu-id="95de1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95de1-126">CommonParameters</span></span>
<span data-ttu-id="95de1-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95de1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95de1-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95de1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95de1-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="95de1-129">INPUTS</span></span>

### <span data-ttu-id="95de1-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95de1-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="95de1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="95de1-131">System.String</span></span>

## <span data-ttu-id="95de1-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95de1-132">OUTPUTS</span></span>

### <span data-ttu-id="95de1-133">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="95de1-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="95de1-134">Note</span><span class="sxs-lookup"><span data-stu-id="95de1-134">NOTES</span></span>

## <span data-ttu-id="95de1-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95de1-135">RELATED LINKS</span></span>
