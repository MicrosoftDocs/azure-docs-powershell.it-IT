---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 11de4e8966b5e57e817b6c5d829536deacf229f8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860289"
---
# <span data-ttu-id="eeaed-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="eeaed-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="eeaed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eeaed-102">SYNOPSIS</span></span>
<span data-ttu-id="eeaed-103">Rimuove la configurazione di una sonda da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="eeaed-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="eeaed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eeaed-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eeaed-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eeaed-105">DESCRIPTION</span></span>
<span data-ttu-id="eeaed-106">Il cmdlet **Remove-AzLoadBalancerProbeConfig** rimuove una configurazione di probe da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="eeaed-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="eeaed-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eeaed-107">EXAMPLES</span></span>

### <span data-ttu-id="eeaed-108">Esempio 1: rimuovere una configurazione di una sonda da un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="eeaed-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="eeaed-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="eeaed-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="eeaed-110">Il secondo comando Elimina la configurazione denominata Probe dal bilanciamento del carico in $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="eeaed-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="eeaed-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eeaed-111">PARAMETERS</span></span>

### <span data-ttu-id="eeaed-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeaed-112">-DefaultProfile</span></span>
<span data-ttu-id="eeaed-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eeaed-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eeaed-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eeaed-114">-LoadBalancer</span></span>
<span data-ttu-id="eeaed-115">Specifica il bilanciamento del carico che contiene la configurazione della sonda rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeaed-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="eeaed-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="eeaed-116">-Name</span></span>
<span data-ttu-id="eeaed-117">Specifica il nome della configurazione della sonda rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeaed-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="eeaed-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeaed-118">CommonParameters</span></span>
<span data-ttu-id="eeaed-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeaed-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeaed-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeaed-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeaed-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eeaed-121">INPUTS</span></span>

### <span data-ttu-id="eeaed-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eeaed-122">PSLoadBalancer</span></span>
<span data-ttu-id="eeaed-123">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="eeaed-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="eeaed-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eeaed-124">OUTPUTS</span></span>

### <span data-ttu-id="eeaed-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eeaed-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="eeaed-126">Note</span><span class="sxs-lookup"><span data-stu-id="eeaed-126">NOTES</span></span>

## <span data-ttu-id="eeaed-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eeaed-127">RELATED LINKS</span></span>

[<span data-ttu-id="eeaed-128">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="eeaed-128">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="eeaed-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eeaed-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="eeaed-130">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="eeaed-130">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="eeaed-131">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="eeaed-131">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="eeaed-132">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="eeaed-132">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


