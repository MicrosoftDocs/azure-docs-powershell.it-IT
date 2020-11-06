---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 155d2ab8a1e43264a3598a0ea44011ebb66e9e58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514256"
---
# <span data-ttu-id="582a3-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="582a3-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="582a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="582a3-102">SYNOPSIS</span></span>
<span data-ttu-id="582a3-103">Rimuove una configurazione IP front-end da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="582a3-103">Removes a front-end IP configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="582a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="582a3-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="582a3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="582a3-105">DESCRIPTION</span></span>
<span data-ttu-id="582a3-106">Il cmdlet **Remove-AzureRmLoadBalancerFrontendIpConfig** rimuove una configurazione IP front-end da un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="582a3-106">The **Remove-AzureRmLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="582a3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="582a3-107">EXAMPLES</span></span>

### <span data-ttu-id="582a3-108">Esempio 1: rimuovere una configurazione IP front-end da un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="582a3-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="582a3-109">Il primo comando ottiene il bilanciamento del carico associato alla configurazione IP front-end che si vuole rimuovere, quindi lo archivia nella variabile $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="582a3-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="582a3-110">Il secondo comando rimuove la configurazione IP di frontend associata dal bilanciamento del carico in $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="582a3-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="582a3-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="582a3-111">PARAMETERS</span></span>

### <span data-ttu-id="582a3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="582a3-112">-DefaultProfile</span></span>
<span data-ttu-id="582a3-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="582a3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="582a3-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="582a3-114">-LoadBalancer</span></span>
<span data-ttu-id="582a3-115">Specifica il bilanciamento del carico che contiene la configurazione IP front-end da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="582a3-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="582a3-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="582a3-116">-Name</span></span>
<span data-ttu-id="582a3-117">Specifica il nome della configurazione dell'indirizzo IP front-end da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="582a3-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="582a3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="582a3-118">CommonParameters</span></span>
<span data-ttu-id="582a3-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="582a3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="582a3-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="582a3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="582a3-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="582a3-121">INPUTS</span></span>

### <span data-ttu-id="582a3-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="582a3-122">PSLoadBalancer</span></span>
<span data-ttu-id="582a3-123">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="582a3-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="582a3-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="582a3-124">OUTPUTS</span></span>

### <span data-ttu-id="582a3-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="582a3-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="582a3-126">Note</span><span class="sxs-lookup"><span data-stu-id="582a3-126">NOTES</span></span>

## <span data-ttu-id="582a3-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="582a3-127">RELATED LINKS</span></span>

[<span data-ttu-id="582a3-128">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="582a3-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="582a3-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="582a3-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="582a3-130">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="582a3-130">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="582a3-131">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="582a3-131">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="582a3-132">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="582a3-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


