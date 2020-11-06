---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 6f9fd09aa87c8a812bf43a14068feb1604d8de8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507423"
---
# <span data-ttu-id="22045-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="22045-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="22045-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22045-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22045-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22045-103">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22045-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22045-104">DESCRIPTION</span></span>

## <span data-ttu-id="22045-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22045-105">EXAMPLES</span></span>

### <span data-ttu-id="22045-106">1: rimuovere</span><span class="sxs-lookup"><span data-stu-id="22045-106">1: Remove</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="22045-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22045-107">PARAMETERS</span></span>

### <span data-ttu-id="22045-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22045-108">-DefaultProfile</span></span>
<span data-ttu-id="22045-109">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22045-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22045-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="22045-110">-LoadBalancer</span></span>
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

### <span data-ttu-id="22045-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="22045-111">-Name</span></span>
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

### <span data-ttu-id="22045-112">-Confermare</span><span class="sxs-lookup"><span data-stu-id="22045-112">-Confirm</span></span>
<span data-ttu-id="22045-113">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22045-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22045-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22045-114">-WhatIf</span></span>
<span data-ttu-id="22045-115">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22045-115">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22045-116">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22045-116">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22045-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22045-117">CommonParameters</span></span>
<span data-ttu-id="22045-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22045-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22045-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22045-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22045-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22045-120">INPUTS</span></span>

### <span data-ttu-id="22045-121">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="22045-121">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="22045-122">Parametri: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="22045-122">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="22045-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22045-123">OUTPUTS</span></span>

### <span data-ttu-id="22045-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="22045-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="22045-125">Note</span><span class="sxs-lookup"><span data-stu-id="22045-125">NOTES</span></span>

## <span data-ttu-id="22045-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22045-126">RELATED LINKS</span></span>
