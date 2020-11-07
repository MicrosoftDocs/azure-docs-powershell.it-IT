---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
ms.openlocfilehash: 9bbfa0aec2da00ada25fc4bb8a5334f67e80e41a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867009"
---
# <span data-ttu-id="f14a2-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f14a2-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="f14a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f14a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f14a2-103">Rimuove una configurazione del pool di indirizzi back-end da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f14a2-103">Removes a backend address pool configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f14a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f14a2-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f14a2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f14a2-105">DESCRIPTION</span></span>
<span data-ttu-id="f14a2-106">Il cmdlet **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** rimuove un pool di indirizzi back-end da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f14a2-106">The **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="f14a2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f14a2-107">EXAMPLES</span></span>

### <span data-ttu-id="f14a2-108">Esempio 1: rimuovere una configurazione del pool di indirizzi back-end da un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="f14a2-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="f14a2-109">Questo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo passa a **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , che rimuove la configurazione di BackendAddressPool02 da MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="f14a2-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="f14a2-110">Infine, il cmdlet Set-AzureRmLoadBalancer Aggiorna MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="f14a2-110">Finally, the Set-AzureRmLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="f14a2-111">Tieni presente che la configurazione del pool di indirizzi di backend deve esistere prima di poterla eliminare.</span><span class="sxs-lookup"><span data-stu-id="f14a2-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="f14a2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f14a2-112">PARAMETERS</span></span>

### <span data-ttu-id="f14a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f14a2-113">-DefaultProfile</span></span>
<span data-ttu-id="f14a2-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f14a2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f14a2-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f14a2-115">-LoadBalancer</span></span>
<span data-ttu-id="f14a2-116">Specifica il bilanciamento del carico che contiene il pool di indirizzi back-end da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f14a2-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="f14a2-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f14a2-117">-Name</span></span>
<span data-ttu-id="f14a2-118">Specifica il nome del pool di indirizzi back-end rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f14a2-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f14a2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f14a2-119">CommonParameters</span></span>
<span data-ttu-id="f14a2-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f14a2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f14a2-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f14a2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f14a2-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f14a2-122">INPUTS</span></span>

### <span data-ttu-id="f14a2-123">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f14a2-123">PSLoadBalancer</span></span>
<span data-ttu-id="f14a2-124">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f14a2-124">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="f14a2-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f14a2-125">OUTPUTS</span></span>

### <span data-ttu-id="f14a2-126">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f14a2-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f14a2-127">Note</span><span class="sxs-lookup"><span data-stu-id="f14a2-127">NOTES</span></span>

## <span data-ttu-id="f14a2-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f14a2-128">RELATED LINKS</span></span>

[<span data-ttu-id="f14a2-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f14a2-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f14a2-130">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f14a2-130">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="f14a2-131">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f14a2-131">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f14a2-132">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f14a2-132">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)


