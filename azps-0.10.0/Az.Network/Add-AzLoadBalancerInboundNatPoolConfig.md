---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: a5cd44d1b4b7ac1a1494047affa721dd21d85919
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860982"
---
# <span data-ttu-id="5b820-101">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="5b820-101">Add-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="5b820-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b820-102">SYNOPSIS</span></span>

## <span data-ttu-id="5b820-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b820-103">SYNTAX</span></span>

### <span data-ttu-id="5b820-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5b820-104">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b820-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5b820-105">SetByResource</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b820-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b820-106">DESCRIPTION</span></span>

## <span data-ttu-id="5b820-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b820-107">EXAMPLES</span></span>

### <span data-ttu-id="5b820-108">1:</span><span class="sxs-lookup"><span data-stu-id="5b820-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="5b820-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b820-109">PARAMETERS</span></span>

### <span data-ttu-id="5b820-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="5b820-110">-BackendPort</span></span>
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

### <span data-ttu-id="5b820-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b820-111">-DefaultProfile</span></span>
<span data-ttu-id="5b820-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b820-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b820-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b820-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="5b820-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5b820-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="5b820-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="5b820-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="5b820-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="5b820-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="5b820-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b820-117">-LoadBalancer</span></span>
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

### <span data-ttu-id="5b820-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b820-118">-Name</span></span>
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

### <span data-ttu-id="5b820-119">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="5b820-119">-Protocol</span></span>
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

### <span data-ttu-id="5b820-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b820-120">CommonParameters</span></span>
<span data-ttu-id="5b820-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b820-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b820-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b820-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b820-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b820-123">INPUTS</span></span>

### <span data-ttu-id="5b820-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b820-124">PSLoadBalancer</span></span>
<span data-ttu-id="5b820-125">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5b820-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="5b820-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b820-126">OUTPUTS</span></span>

### <span data-ttu-id="5b820-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b820-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5b820-128">Note</span><span class="sxs-lookup"><span data-stu-id="5b820-128">NOTES</span></span>

## <span data-ttu-id="5b820-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b820-129">RELATED LINKS</span></span>

