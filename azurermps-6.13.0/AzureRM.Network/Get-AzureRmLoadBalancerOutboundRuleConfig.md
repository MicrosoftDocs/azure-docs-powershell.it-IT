---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 1bcaab526ac2fbb82d696db7197bbc8d69c0078f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688562"
---
# <span data-ttu-id="c29b7-101">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c29b7-101">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="c29b7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c29b7-102">SYNOPSIS</span></span>
<span data-ttu-id="c29b7-103">Ottiene una configurazione della regola in uscita in un programma di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c29b7-103">Gets an outbound rule configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c29b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c29b7-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c29b7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c29b7-105">DESCRIPTION</span></span>
<span data-ttu-id="c29b7-106">Il cmdlet **Get-AzureRmLoadBalancerOutboundRuleConfig** ottiene una configurazione della regola in uscita o un elenco di configurazioni di regole in uscita in un programma di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c29b7-106">The **Get-AzureRmLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="c29b7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c29b7-107">EXAMPLES</span></span>

### <span data-ttu-id="c29b7-108">Esempio 1: ottenere una configurazione della regola in uscita in un programma di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="c29b7-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="c29b7-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="c29b7-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="c29b7-110">Il secondo comando ottiene la configurazione della regola in uscita denominata regola associata al bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c29b7-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="c29b7-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c29b7-111">PARAMETERS</span></span>

### <span data-ttu-id="c29b7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c29b7-112">-DefaultProfile</span></span>
<span data-ttu-id="c29b7-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c29b7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c29b7-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c29b7-114">-LoadBalancer</span></span>
<span data-ttu-id="c29b7-115">Riferimento della risorsa di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c29b7-115">The reference of the load balancer resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c29b7-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c29b7-116">-Name</span></span>
<span data-ttu-id="c29b7-117">Nome della regola in uscita.</span><span class="sxs-lookup"><span data-stu-id="c29b7-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="c29b7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c29b7-118">CommonParameters</span></span>
<span data-ttu-id="c29b7-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c29b7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c29b7-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c29b7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c29b7-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c29b7-121">INPUTS</span></span>

### <span data-ttu-id="c29b7-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c29b7-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c29b7-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c29b7-123">OUTPUTS</span></span>

### <span data-ttu-id="c29b7-124">Microsoft. Azure. Commands. Network. Models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="c29b7-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="c29b7-125">Note</span><span class="sxs-lookup"><span data-stu-id="c29b7-125">NOTES</span></span>

## <span data-ttu-id="c29b7-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c29b7-126">RELATED LINKS</span></span>
