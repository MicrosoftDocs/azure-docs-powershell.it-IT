---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: b9782d56fb18f0f00c52e9ff37ef0d62a609f980
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860306"
---
# <span data-ttu-id="a99e6-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a99e6-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="a99e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a99e6-102">SYNOPSIS</span></span>
<span data-ttu-id="a99e6-103">Rimuove una configurazione IP front-end da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="a99e6-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="a99e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a99e6-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a99e6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a99e6-105">DESCRIPTION</span></span>
<span data-ttu-id="a99e6-106">Il cmdlet **Remove-AzLoadBalancerFrontendIpConfig** rimuove una configurazione IP front-end da un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="a99e6-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="a99e6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a99e6-107">EXAMPLES</span></span>

### <span data-ttu-id="a99e6-108">Esempio 1: rimuovere una configurazione IP front-end da un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="a99e6-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="a99e6-109">Il primo comando ottiene il bilanciamento del carico associato alla configurazione IP front-end che si vuole rimuovere, quindi lo archivia nella variabile $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="a99e6-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="a99e6-110">Il secondo comando rimuove la configurazione IP di frontend associata dal bilanciamento del carico in $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="a99e6-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="a99e6-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a99e6-111">PARAMETERS</span></span>

### <span data-ttu-id="a99e6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a99e6-112">-DefaultProfile</span></span>
<span data-ttu-id="a99e6-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a99e6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a99e6-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a99e6-114">-LoadBalancer</span></span>
<span data-ttu-id="a99e6-115">Specifica il bilanciamento del carico che contiene la configurazione IP front-end da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a99e6-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="a99e6-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a99e6-116">-Name</span></span>
<span data-ttu-id="a99e6-117">Specifica il nome della configurazione dell'indirizzo IP front-end da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a99e6-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="a99e6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a99e6-118">CommonParameters</span></span>
<span data-ttu-id="a99e6-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a99e6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a99e6-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a99e6-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a99e6-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a99e6-121">INPUTS</span></span>

### <span data-ttu-id="a99e6-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a99e6-122">PSLoadBalancer</span></span>
<span data-ttu-id="a99e6-123">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a99e6-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="a99e6-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a99e6-124">OUTPUTS</span></span>

### <span data-ttu-id="a99e6-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a99e6-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a99e6-126">Note</span><span class="sxs-lookup"><span data-stu-id="a99e6-126">NOTES</span></span>

## <span data-ttu-id="a99e6-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a99e6-127">RELATED LINKS</span></span>

[<span data-ttu-id="a99e6-128">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a99e6-128">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a99e6-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a99e6-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a99e6-130">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a99e6-130">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a99e6-131">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a99e6-131">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a99e6-132">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a99e6-132">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


