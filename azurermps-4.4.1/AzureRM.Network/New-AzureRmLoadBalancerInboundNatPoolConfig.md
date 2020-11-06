---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 85d58154d8dd1d93e37a55b9fd0b9d306283b899
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521183"
---
# <span data-ttu-id="7f8e9-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7f8e9-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="7f8e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f8e9-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f8e9-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f8e9-103">SYNTAX</span></span>

### <span data-ttu-id="7f8e9-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7f8e9-104">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f8e9-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7f8e9-105">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f8e9-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f8e9-106">DESCRIPTION</span></span>

## <span data-ttu-id="7f8e9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f8e9-107">EXAMPLES</span></span>

## <span data-ttu-id="7f8e9-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f8e9-108">PARAMETERS</span></span>

### <span data-ttu-id="7f8e9-109">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="7f8e9-109">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8e9-110">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f8e9-110">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8e9-111">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7f8e9-111">-FrontendIpConfigurationId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8e9-112">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="7f8e9-112">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8e9-113">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="7f8e9-113">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8e9-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f8e9-114">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8e9-115">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="7f8e9-115">-Protocol</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8e9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f8e9-116">-DefaultProfile</span></span>
<span data-ttu-id="7f8e9-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f8e9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f8e9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f8e9-118">CommonParameters</span></span>
<span data-ttu-id="7f8e9-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f8e9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f8e9-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f8e9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f8e9-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f8e9-121">INPUTS</span></span>

## <span data-ttu-id="7f8e9-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f8e9-122">OUTPUTS</span></span>

### <span data-ttu-id="7f8e9-123">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="7f8e9-123">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="7f8e9-124">Note</span><span class="sxs-lookup"><span data-stu-id="7f8e9-124">NOTES</span></span>

## <span data-ttu-id="7f8e9-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f8e9-125">RELATED LINKS</span></span>

