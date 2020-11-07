---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
ms.openlocfilehash: b53b6ed8ba5b4a79ee1913040ef58e236c22c44d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867088"
---
# <span data-ttu-id="42150-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="42150-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="42150-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42150-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42150-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42150-103">SYNTAX</span></span>

### <span data-ttu-id="42150-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="42150-104">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42150-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="42150-105">SetByResource</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42150-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42150-106">DESCRIPTION</span></span>

## <span data-ttu-id="42150-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42150-107">EXAMPLES</span></span>

### <span data-ttu-id="42150-108">1:</span><span class="sxs-lookup"><span data-stu-id="42150-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="42150-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42150-109">PARAMETERS</span></span>

### <span data-ttu-id="42150-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="42150-110">-BackendPort</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42150-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42150-111">-DefaultProfile</span></span>
<span data-ttu-id="42150-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42150-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42150-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="42150-113">-FrontendIpConfiguration</span></span>
```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42150-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="42150-114">-FrontendIpConfigurationId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42150-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="42150-115">-FrontendPortRangeEnd</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42150-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="42150-116">-FrontendPortRangeStart</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42150-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="42150-117">-LoadBalancer</span></span>
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

### <span data-ttu-id="42150-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="42150-118">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42150-119">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="42150-119">-Protocol</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42150-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42150-120">CommonParameters</span></span>
<span data-ttu-id="42150-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42150-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42150-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42150-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42150-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42150-123">INPUTS</span></span>

### <span data-ttu-id="42150-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="42150-124">PSLoadBalancer</span></span>
<span data-ttu-id="42150-125">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="42150-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="42150-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42150-126">OUTPUTS</span></span>

### <span data-ttu-id="42150-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="42150-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="42150-128">Note</span><span class="sxs-lookup"><span data-stu-id="42150-128">NOTES</span></span>

## <span data-ttu-id="42150-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42150-129">RELATED LINKS</span></span>

