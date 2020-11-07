---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: a80fa84beaaea0307447f25767d665c465e8c2aa
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865770"
---
# <span data-ttu-id="e964b-101">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e964b-101">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="e964b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e964b-102">SYNOPSIS</span></span>
<span data-ttu-id="e964b-103">Ottiene una configurazione IP front-end in un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e964b-103">Gets a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e964b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e964b-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e964b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e964b-105">DESCRIPTION</span></span>
<span data-ttu-id="e964b-106">Il cmdlet **Get-AzureRmLoadBalancerFrontendIpConfig** ottiene una configurazione IP front-end o un elenco di configurazioni IP front-end in un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e964b-106">The **Get-AzureRmLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="e964b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e964b-107">EXAMPLES</span></span>

### <span data-ttu-id="e964b-108">Esempio 1: ottenere una configurazione IP front-end in un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="e964b-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="e964b-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="e964b-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="e964b-110">Il secondo comando consente di ottenere la configurazione IP front-end associata a tale bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e964b-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="e964b-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e964b-111">PARAMETERS</span></span>

### <span data-ttu-id="e964b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e964b-112">-DefaultProfile</span></span>
<span data-ttu-id="e964b-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e964b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e964b-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e964b-114">-LoadBalancer</span></span>
<span data-ttu-id="e964b-115">Specifica il bilanciamento del carico associato alla configurazione IP front-end da ottenere.</span><span class="sxs-lookup"><span data-stu-id="e964b-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="e964b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="e964b-116">-Name</span></span>
<span data-ttu-id="e964b-117">Specifica il nome del bilanciamento del carico che contiene la configurazione IP front-end da ottenere.</span><span class="sxs-lookup"><span data-stu-id="e964b-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="e964b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e964b-118">CommonParameters</span></span>
<span data-ttu-id="e964b-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e964b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e964b-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e964b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e964b-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e964b-121">INPUTS</span></span>

### <span data-ttu-id="e964b-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e964b-122">PSLoadBalancer</span></span>
<span data-ttu-id="e964b-123">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e964b-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="e964b-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e964b-124">OUTPUTS</span></span>

### <span data-ttu-id="e964b-125">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e964b-125">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="e964b-126">Note</span><span class="sxs-lookup"><span data-stu-id="e964b-126">NOTES</span></span>

## <span data-ttu-id="e964b-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e964b-127">RELATED LINKS</span></span>

[<span data-ttu-id="e964b-128">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e964b-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="e964b-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e964b-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="e964b-130">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e964b-130">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="e964b-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e964b-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="e964b-132">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e964b-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


