---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 132ec5259a6d03591860dceaaa215f8db57c27dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685517"
---
# <span data-ttu-id="2cc5d-101">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2cc5d-101">Remove-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="2cc5d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2cc5d-102">SYNOPSIS</span></span>
<span data-ttu-id="2cc5d-103">Rimuove la configurazione di una sonda da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="2cc5d-103">Removes a probe configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cc5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2cc5d-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cc5d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2cc5d-105">DESCRIPTION</span></span>
<span data-ttu-id="2cc5d-106">Il cmdlet **Remove-AzureRmLoadBalancerProbeConfig** rimuove una configurazione di probe da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="2cc5d-106">The **Remove-AzureRmLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="2cc5d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2cc5d-107">EXAMPLES</span></span>

### <span data-ttu-id="2cc5d-108">Esempio 1: rimuovere una configurazione di una sonda da un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="2cc5d-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="2cc5d-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="2cc5d-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="2cc5d-110">Il secondo comando Elimina la configurazione denominata Probe dal bilanciamento del carico in $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="2cc5d-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="2cc5d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2cc5d-111">PARAMETERS</span></span>

### <span data-ttu-id="2cc5d-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2cc5d-112">-LoadBalancer</span></span>
<span data-ttu-id="2cc5d-113">Specifica il bilanciamento del carico che contiene la configurazione della sonda rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cc5d-113">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cc5d-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="2cc5d-114">-Name</span></span>
<span data-ttu-id="2cc5d-115">Specifica il nome della configurazione della sonda rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cc5d-115">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc5d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cc5d-116">-DefaultProfile</span></span>
<span data-ttu-id="2cc5d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2cc5d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cc5d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cc5d-118">CommonParameters</span></span>
<span data-ttu-id="2cc5d-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cc5d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cc5d-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cc5d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cc5d-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2cc5d-121">INPUTS</span></span>

### <span data-ttu-id="2cc5d-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2cc5d-122">PSLoadBalancer</span></span>
<span data-ttu-id="2cc5d-123">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="2cc5d-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="2cc5d-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2cc5d-124">OUTPUTS</span></span>

### <span data-ttu-id="2cc5d-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2cc5d-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2cc5d-126">Note</span><span class="sxs-lookup"><span data-stu-id="2cc5d-126">NOTES</span></span>

## <span data-ttu-id="2cc5d-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2cc5d-127">RELATED LINKS</span></span>

[<span data-ttu-id="2cc5d-128">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2cc5d-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="2cc5d-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2cc5d-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="2cc5d-130">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2cc5d-130">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="2cc5d-131">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2cc5d-131">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="2cc5d-132">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2cc5d-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)

