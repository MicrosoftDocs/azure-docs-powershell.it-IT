---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 30abb6f2d11eeae9749e7285a91ddeb93a1bf743
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860313"
---
# <span data-ttu-id="7cfcd-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7cfcd-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="7cfcd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7cfcd-102">SYNOPSIS</span></span>
<span data-ttu-id="7cfcd-103">Rimuove una configurazione del pool di indirizzi back-end da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="7cfcd-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="7cfcd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7cfcd-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cfcd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cfcd-105">DESCRIPTION</span></span>
<span data-ttu-id="7cfcd-106">Il cmdlet **Remove-AzLoadBalancerBackendAddressPoolConfig** rimuove un pool di indirizzi back-end da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="7cfcd-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="7cfcd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7cfcd-107">EXAMPLES</span></span>

### <span data-ttu-id="7cfcd-108">Esempio 1: rimuovere una configurazione del pool di indirizzi back-end da un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="7cfcd-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="7cfcd-109">Questo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo passa a **Remove-AzLoadBalancerBackendAddressPoolConfig** , che rimuove la configurazione di BackendAddressPool02 da MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="7cfcd-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="7cfcd-110">Infine, il cmdlet Set-AzLoadBalancer Aggiorna MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="7cfcd-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="7cfcd-111">Tieni presente che la configurazione del pool di indirizzi di backend deve esistere prima di poterla eliminare.</span><span class="sxs-lookup"><span data-stu-id="7cfcd-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="7cfcd-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7cfcd-112">PARAMETERS</span></span>

### <span data-ttu-id="7cfcd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cfcd-113">-DefaultProfile</span></span>
<span data-ttu-id="7cfcd-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7cfcd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cfcd-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7cfcd-115">-LoadBalancer</span></span>
<span data-ttu-id="7cfcd-116">Specifica il bilanciamento del carico che contiene il pool di indirizzi back-end da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7cfcd-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="7cfcd-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7cfcd-117">-Name</span></span>
<span data-ttu-id="7cfcd-118">Specifica il nome del pool di indirizzi back-end rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cfcd-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7cfcd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cfcd-119">CommonParameters</span></span>
<span data-ttu-id="7cfcd-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cfcd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cfcd-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cfcd-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cfcd-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7cfcd-122">INPUTS</span></span>

### <span data-ttu-id="7cfcd-123">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7cfcd-123">PSLoadBalancer</span></span>
<span data-ttu-id="7cfcd-124">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7cfcd-124">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="7cfcd-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7cfcd-125">OUTPUTS</span></span>

### <span data-ttu-id="7cfcd-126">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7cfcd-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7cfcd-127">Note</span><span class="sxs-lookup"><span data-stu-id="7cfcd-127">NOTES</span></span>

## <span data-ttu-id="7cfcd-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7cfcd-128">RELATED LINKS</span></span>

[<span data-ttu-id="7cfcd-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7cfcd-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="7cfcd-130">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7cfcd-130">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="7cfcd-131">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7cfcd-131">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="7cfcd-132">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7cfcd-132">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


