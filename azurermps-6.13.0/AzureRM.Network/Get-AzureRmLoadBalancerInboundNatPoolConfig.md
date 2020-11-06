---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: dbd49a948108d23c0f824adaea2e06105152a36b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517484"
---
# <span data-ttu-id="db57d-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="db57d-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="db57d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db57d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db57d-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db57d-103">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db57d-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db57d-104">DESCRIPTION</span></span>

## <span data-ttu-id="db57d-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db57d-105">EXAMPLES</span></span>

### <span data-ttu-id="db57d-106">1: ottenere</span><span class="sxs-lookup"><span data-stu-id="db57d-106">1: Get</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzureRmLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="db57d-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db57d-107">PARAMETERS</span></span>

### <span data-ttu-id="db57d-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db57d-108">-DefaultProfile</span></span>
<span data-ttu-id="db57d-109">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db57d-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db57d-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="db57d-110">-LoadBalancer</span></span>
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

### <span data-ttu-id="db57d-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="db57d-111">-Name</span></span>
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

### <span data-ttu-id="db57d-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db57d-112">CommonParameters</span></span>
<span data-ttu-id="db57d-113">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db57d-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db57d-114">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db57d-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db57d-115">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db57d-115">INPUTS</span></span>

### <span data-ttu-id="db57d-116">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="db57d-116">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="db57d-117">Parametri: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="db57d-117">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="db57d-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db57d-118">OUTPUTS</span></span>

### <span data-ttu-id="db57d-119">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="db57d-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="db57d-120">Note</span><span class="sxs-lookup"><span data-stu-id="db57d-120">NOTES</span></span>

## <span data-ttu-id="db57d-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db57d-121">RELATED LINKS</span></span>
