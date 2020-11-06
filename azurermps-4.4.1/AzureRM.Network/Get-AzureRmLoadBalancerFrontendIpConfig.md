---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 02756d382cf785d4cfecfa6f73a580e125dc5e39
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519143"
---
# <span data-ttu-id="89099-101">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="89099-101">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="89099-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="89099-102">SYNOPSIS</span></span>
<span data-ttu-id="89099-103">Ottiene una configurazione IP front-end in un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="89099-103">Gets a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89099-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89099-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89099-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89099-105">DESCRIPTION</span></span>
<span data-ttu-id="89099-106">Il cmdlet **Get-AzureRmLoadBalancerFrontendIpConfig** ottiene una configurazione IP front-end o un elenco di configurazioni IP front-end in un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="89099-106">The **Get-AzureRmLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="89099-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89099-107">EXAMPLES</span></span>

### <span data-ttu-id="89099-108">Esempio 1: ottenere una configurazione IP front-end in un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="89099-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="89099-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="89099-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="89099-110">Il secondo comando consente di ottenere la configurazione IP front-end associata a tale bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="89099-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="89099-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89099-111">PARAMETERS</span></span>

### <span data-ttu-id="89099-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89099-112">-DefaultProfile</span></span>
<span data-ttu-id="89099-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="89099-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89099-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="89099-114">-LoadBalancer</span></span>
<span data-ttu-id="89099-115">Specifica il bilanciamento del carico associato alla configurazione IP front-end da ottenere.</span><span class="sxs-lookup"><span data-stu-id="89099-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="89099-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="89099-116">-Name</span></span>
<span data-ttu-id="89099-117">Specifica il nome del bilanciamento del carico che contiene la configurazione IP front-end da ottenere.</span><span class="sxs-lookup"><span data-stu-id="89099-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="89099-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89099-118">CommonParameters</span></span>
<span data-ttu-id="89099-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89099-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89099-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89099-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89099-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="89099-121">INPUTS</span></span>

### <span data-ttu-id="89099-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="89099-122">PSLoadBalancer</span></span>
<span data-ttu-id="89099-123">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="89099-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="89099-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89099-124">OUTPUTS</span></span>

### <span data-ttu-id="89099-125">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="89099-125">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="89099-126">Note</span><span class="sxs-lookup"><span data-stu-id="89099-126">NOTES</span></span>

## <span data-ttu-id="89099-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89099-127">RELATED LINKS</span></span>

[<span data-ttu-id="89099-128">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="89099-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="89099-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="89099-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="89099-130">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="89099-130">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="89099-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="89099-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="89099-132">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="89099-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


