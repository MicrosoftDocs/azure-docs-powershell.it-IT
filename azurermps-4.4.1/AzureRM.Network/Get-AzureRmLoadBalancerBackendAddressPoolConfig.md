---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 3df754ddb267abe915724d6d709f4b59a1eda265
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519561"
---
# <span data-ttu-id="92c4c-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="92c4c-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="92c4c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="92c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="92c4c-103">Ottiene una configurazione del pool di indirizzi back-end per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="92c4c-103">Gets a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92c4c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92c4c-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92c4c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92c4c-105">DESCRIPTION</span></span>
<span data-ttu-id="92c4c-106">Il cmdlet **Get-AzureRmLoadBalancerBackendAddressPoolConfig** ottiene un singolo pool di indirizzi back-end o un elenco di pool di indirizzi backend all'interno di un gruppo di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="92c4c-106">The **Get-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="92c4c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92c4c-107">EXAMPLES</span></span>

### <span data-ttu-id="92c4c-108">Esempio 1: ottenere il pool di indirizzi back-end</span><span class="sxs-lookup"><span data-stu-id="92c4c-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="92c4c-109">Il primo comando ottiene un bilanciamento del carico esistente denominato MyLoadBalancer nel gruppo di risorse denominato MyResourceGroup e lo archivia nella variabile $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="92c4c-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="92c4c-110">Il secondo comando ottiene la configurazione del pool di indirizzi back-end associata denominata BackendAddressPool02 per il bilanciamento del carico in $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="92c4c-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="92c4c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="92c4c-111">PARAMETERS</span></span>

### <span data-ttu-id="92c4c-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="92c4c-112">-LoadBalancer</span></span>
<span data-ttu-id="92c4c-113">Specifica il bilanciamento del carico associato al pool di indirizzi back-end da ottenere.</span><span class="sxs-lookup"><span data-stu-id="92c4c-113">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="92c4c-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="92c4c-114">-Name</span></span>
<span data-ttu-id="92c4c-115">Specifica il nome del bilanciamento del carico che contiene il pool di indirizzi di backend da ottenere.</span><span class="sxs-lookup"><span data-stu-id="92c4c-115">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="92c4c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92c4c-116">-DefaultProfile</span></span>
<span data-ttu-id="92c4c-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="92c4c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92c4c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92c4c-118">CommonParameters</span></span>
<span data-ttu-id="92c4c-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92c4c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92c4c-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92c4c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92c4c-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="92c4c-121">INPUTS</span></span>

### <span data-ttu-id="92c4c-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="92c4c-122">PSLoadBalancer</span></span>
<span data-ttu-id="92c4c-123">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="92c4c-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="92c4c-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92c4c-124">OUTPUTS</span></span>

### <span data-ttu-id="92c4c-125">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="92c4c-125">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="92c4c-126">Note</span><span class="sxs-lookup"><span data-stu-id="92c4c-126">NOTES</span></span>

## <span data-ttu-id="92c4c-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92c4c-127">RELATED LINKS</span></span>

[<span data-ttu-id="92c4c-128">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="92c4c-128">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="92c4c-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="92c4c-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="92c4c-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="92c4c-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="92c4c-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="92c4c-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


