---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 246675a2473bb20e5040f3898b6931f1b3ee6933
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192114"
---
# <span data-ttu-id="b3429-101">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="b3429-101">Get-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="b3429-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3429-102">SYNOPSIS</span></span>
<span data-ttu-id="b3429-103">Ottenere l'identità assegnata a un ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b3429-103">Get identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="b3429-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3429-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3429-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3429-105">DESCRIPTION</span></span>
<span data-ttu-id="b3429-106">Il cmdlet **Get-AzExpressRoutePortIdentity** Ottiene l'identità assegnata a un oggetto ExpressRoutePort Azure locale.</span><span class="sxs-lookup"><span data-stu-id="b3429-106">The **Get-AzExpressRoutePortIdentity** cmdlet gets identity assigned to a local Azure ExpressRoutePort object.</span></span>

## <span data-ttu-id="b3429-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3429-107">EXAMPLES</span></span>

### <span data-ttu-id="b3429-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b3429-108">Example 1</span></span>
```powershell
PS C:\> $exrPort = Get-AzExpressRoutePort -Name $exrPortName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzExpressRoutePortIdentity -ExpressRoutePort $exrPort
```

## <span data-ttu-id="b3429-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3429-109">PARAMETERS</span></span>

### <span data-ttu-id="b3429-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3429-110">-DefaultProfile</span></span>
<span data-ttu-id="b3429-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3429-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3429-112">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b3429-112">-ExpressRoutePort</span></span>
<span data-ttu-id="b3429-113">La porta ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="b3429-113">The ExpressRoute Port</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3429-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3429-114">CommonParameters</span></span>
<span data-ttu-id="b3429-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3429-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3429-116">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3429-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3429-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3429-117">INPUTS</span></span>

### <span data-ttu-id="b3429-118">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b3429-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="b3429-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3429-119">OUTPUTS</span></span>

### <span data-ttu-id="b3429-120">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="b3429-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="b3429-121">Note</span><span class="sxs-lookup"><span data-stu-id="b3429-121">NOTES</span></span>

## <span data-ttu-id="b3429-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3429-122">RELATED LINKS</span></span>
[<span data-ttu-id="b3429-123">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="b3429-123">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="b3429-124">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="b3429-124">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="b3429-125">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="b3429-125">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)