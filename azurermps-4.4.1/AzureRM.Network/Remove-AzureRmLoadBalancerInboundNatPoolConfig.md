---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 5b9bd91dd87ddcd7666eae825b7d908a4514e94d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685518"
---
# <span data-ttu-id="3e7d6-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3e7d6-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="3e7d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e7d6-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e7d6-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e7d6-103">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e7d6-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e7d6-104">DESCRIPTION</span></span>

## <span data-ttu-id="3e7d6-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e7d6-105">EXAMPLES</span></span>

### <span data-ttu-id="3e7d6-106">1:</span><span class="sxs-lookup"><span data-stu-id="3e7d6-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="3e7d6-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e7d6-107">PARAMETERS</span></span>

### <span data-ttu-id="3e7d6-108">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3e7d6-108">-LoadBalancer</span></span>
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

### <span data-ttu-id="3e7d6-109">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e7d6-109">-Name</span></span>
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

### <span data-ttu-id="3e7d6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e7d6-110">-DefaultProfile</span></span>
<span data-ttu-id="3e7d6-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e7d6-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e7d6-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e7d6-112">CommonParameters</span></span>
<span data-ttu-id="3e7d6-113">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e7d6-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e7d6-114">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e7d6-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e7d6-115">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e7d6-115">INPUTS</span></span>

### <span data-ttu-id="3e7d6-116">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3e7d6-116">PSLoadBalancer</span></span>
<span data-ttu-id="3e7d6-117">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3e7d6-117">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="3e7d6-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e7d6-118">OUTPUTS</span></span>

### <span data-ttu-id="3e7d6-119">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3e7d6-119">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3e7d6-120">Note</span><span class="sxs-lookup"><span data-stu-id="3e7d6-120">NOTES</span></span>

## <span data-ttu-id="3e7d6-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e7d6-121">RELATED LINKS</span></span>

