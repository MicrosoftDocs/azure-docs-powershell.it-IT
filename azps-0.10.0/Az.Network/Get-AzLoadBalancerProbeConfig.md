---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: bf106b9fbe4c8f069f2d7b5b1b2a9beae95cd51b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860765"
---
# <span data-ttu-id="8fd87-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8fd87-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="8fd87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8fd87-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd87-103">Ottiene una configurazione Probe per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="8fd87-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="8fd87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8fd87-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fd87-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fd87-105">DESCRIPTION</span></span>
<span data-ttu-id="8fd87-106">Il cmdlet **Get-AzLoadBalancerProbeConfig** ottiene una o più configurazioni di sonde per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="8fd87-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="8fd87-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8fd87-107">EXAMPLES</span></span>

### <span data-ttu-id="8fd87-108">Esempio 1: ottenere la configurazione Probe di un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="8fd87-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="8fd87-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="8fd87-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="8fd87-110">Il secondo comando ottiene la configurazione di probe associata denominata Probe dal bilanciamento del carico in $slb.</span><span class="sxs-lookup"><span data-stu-id="8fd87-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="8fd87-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8fd87-111">PARAMETERS</span></span>

### <span data-ttu-id="8fd87-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd87-112">-DefaultProfile</span></span>
<span data-ttu-id="8fd87-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8fd87-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fd87-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8fd87-114">-LoadBalancer</span></span>
<span data-ttu-id="8fd87-115">Specifica il bilanciamento del carico associato alla configurazione della sonda da ottenere.</span><span class="sxs-lookup"><span data-stu-id="8fd87-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="8fd87-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="8fd87-116">-Name</span></span>
<span data-ttu-id="8fd87-117">Specifica il nome della configurazione della sonda da ottenere.</span><span class="sxs-lookup"><span data-stu-id="8fd87-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="8fd87-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd87-118">CommonParameters</span></span>
<span data-ttu-id="8fd87-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fd87-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fd87-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fd87-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd87-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8fd87-121">INPUTS</span></span>

### <span data-ttu-id="8fd87-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8fd87-122">PSLoadBalancer</span></span>
<span data-ttu-id="8fd87-123">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="8fd87-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="8fd87-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8fd87-124">OUTPUTS</span></span>

### <span data-ttu-id="8fd87-125">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="8fd87-125">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="8fd87-126">Note</span><span class="sxs-lookup"><span data-stu-id="8fd87-126">NOTES</span></span>

## <span data-ttu-id="8fd87-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8fd87-127">RELATED LINKS</span></span>

[<span data-ttu-id="8fd87-128">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8fd87-128">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="8fd87-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8fd87-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="8fd87-130">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8fd87-130">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="8fd87-131">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8fd87-131">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="8fd87-132">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8fd87-132">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


