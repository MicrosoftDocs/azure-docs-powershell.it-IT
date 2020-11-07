---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: 30989d3b9c71821c2eae3cdfd97f9e4e5fc0cb15
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867048"
---
# <span data-ttu-id="f6c7b-101">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f6c7b-101">Get-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="f6c7b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f6c7b-102">SYNOPSIS</span></span>
<span data-ttu-id="f6c7b-103">Ottiene una configurazione Probe per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f6c7b-103">Gets a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6c7b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6c7b-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6c7b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6c7b-105">DESCRIPTION</span></span>
<span data-ttu-id="f6c7b-106">Il cmdlet **Get-AzureRmLoadBalancerProbeConfig** ottiene una o più configurazioni di sonde per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f6c7b-106">The **Get-AzureRmLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="f6c7b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6c7b-107">EXAMPLES</span></span>

### <span data-ttu-id="f6c7b-108">Esempio 1: ottenere la configurazione Probe di un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="f6c7b-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="f6c7b-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="f6c7b-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="f6c7b-110">Il secondo comando ottiene la configurazione di probe associata denominata Probe dal bilanciamento del carico in $slb.</span><span class="sxs-lookup"><span data-stu-id="f6c7b-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="f6c7b-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f6c7b-111">PARAMETERS</span></span>

### <span data-ttu-id="f6c7b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6c7b-112">-DefaultProfile</span></span>
<span data-ttu-id="f6c7b-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f6c7b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6c7b-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f6c7b-114">-LoadBalancer</span></span>
<span data-ttu-id="f6c7b-115">Specifica il bilanciamento del carico associato alla configurazione della sonda da ottenere.</span><span class="sxs-lookup"><span data-stu-id="f6c7b-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6c7b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6c7b-116">-Name</span></span>
<span data-ttu-id="f6c7b-117">Specifica il nome della configurazione della sonda da ottenere.</span><span class="sxs-lookup"><span data-stu-id="f6c7b-117">Specifies the name of the probe configuration to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6c7b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6c7b-118">CommonParameters</span></span>
<span data-ttu-id="f6c7b-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6c7b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6c7b-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6c7b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6c7b-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f6c7b-121">INPUTS</span></span>

### <span data-ttu-id="f6c7b-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f6c7b-122">PSLoadBalancer</span></span>
<span data-ttu-id="f6c7b-123">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f6c7b-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="f6c7b-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6c7b-124">OUTPUTS</span></span>

### <span data-ttu-id="f6c7b-125">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="f6c7b-125">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="f6c7b-126">Note</span><span class="sxs-lookup"><span data-stu-id="f6c7b-126">NOTES</span></span>

## <span data-ttu-id="f6c7b-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6c7b-127">RELATED LINKS</span></span>

[<span data-ttu-id="f6c7b-128">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f6c7b-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="f6c7b-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f6c7b-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="f6c7b-130">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f6c7b-130">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="f6c7b-131">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f6c7b-131">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="f6c7b-132">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f6c7b-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


