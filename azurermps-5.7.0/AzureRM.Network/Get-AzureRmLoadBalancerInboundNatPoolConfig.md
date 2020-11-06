---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: f2fd08abbc9a01f1a6cacb9891d82fe1c89d13ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521901"
---
# <span data-ttu-id="c7a40-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c7a40-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="c7a40-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7a40-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7a40-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7a40-103">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7a40-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7a40-104">DESCRIPTION</span></span>

## <span data-ttu-id="c7a40-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7a40-105">EXAMPLES</span></span>

### <span data-ttu-id="c7a40-106">1:</span><span class="sxs-lookup"><span data-stu-id="c7a40-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="c7a40-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7a40-107">PARAMETERS</span></span>

### <span data-ttu-id="c7a40-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a40-108">-DefaultProfile</span></span>
<span data-ttu-id="c7a40-109">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7a40-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7a40-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c7a40-110">-LoadBalancer</span></span>
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

### <span data-ttu-id="c7a40-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7a40-111">-Name</span></span>
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

### <span data-ttu-id="c7a40-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a40-112">CommonParameters</span></span>
<span data-ttu-id="c7a40-113">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7a40-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a40-114">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7a40-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a40-115">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7a40-115">INPUTS</span></span>

### <span data-ttu-id="c7a40-116">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c7a40-116">PSLoadBalancer</span></span>
<span data-ttu-id="c7a40-117">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c7a40-117">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="c7a40-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7a40-118">OUTPUTS</span></span>

### <span data-ttu-id="c7a40-119">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="c7a40-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="c7a40-120">Note</span><span class="sxs-lookup"><span data-stu-id="c7a40-120">NOTES</span></span>

## <span data-ttu-id="c7a40-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7a40-121">RELATED LINKS</span></span>

