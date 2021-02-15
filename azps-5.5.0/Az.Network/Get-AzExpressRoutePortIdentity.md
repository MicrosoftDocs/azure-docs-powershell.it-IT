---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 246675a2473bb20e5040f3898b6931f1b3ee6933
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187158"
---
# <span data-ttu-id="6c2fb-101">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="6c2fb-101">Get-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="6c2fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c2fb-102">SYNOPSIS</span></span>
<span data-ttu-id="6c2fb-103">Ottenere l'identità assegnata a expressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="6c2fb-103">Get identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="6c2fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c2fb-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c2fb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6c2fb-105">DESCRIPTION</span></span>
<span data-ttu-id="6c2fb-106">Il cmdlet **Get-AzExpressRoutePortIdentity** ottiene l'identità assegnata a un oggetto Azure ExpressRoutePort locale.</span><span class="sxs-lookup"><span data-stu-id="6c2fb-106">The **Get-AzExpressRoutePortIdentity** cmdlet gets identity assigned to a local Azure ExpressRoutePort object.</span></span>

## <span data-ttu-id="6c2fb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c2fb-107">EXAMPLES</span></span>

### <span data-ttu-id="6c2fb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6c2fb-108">Example 1</span></span>
```powershell
PS C:\> $exrPort = Get-AzExpressRoutePort -Name $exrPortName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzExpressRoutePortIdentity -ExpressRoutePort $exrPort
```

## <span data-ttu-id="6c2fb-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c2fb-109">PARAMETERS</span></span>

### <span data-ttu-id="6c2fb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c2fb-110">-DefaultProfile</span></span>
<span data-ttu-id="6c2fb-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c2fb-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c2fb-112">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6c2fb-112">-ExpressRoutePort</span></span>
<span data-ttu-id="6c2fb-113">La porta ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="6c2fb-113">The ExpressRoute Port</span></span>

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

### <span data-ttu-id="6c2fb-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c2fb-114">CommonParameters</span></span>
<span data-ttu-id="6c2fb-115">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c2fb-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c2fb-116">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6c2fb-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c2fb-117">INPUT</span><span class="sxs-lookup"><span data-stu-id="6c2fb-117">INPUTS</span></span>

### <span data-ttu-id="6c2fb-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6c2fb-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="6c2fb-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c2fb-119">OUTPUTS</span></span>

### <span data-ttu-id="6c2fb-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="6c2fb-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="6c2fb-121">NOTE</span><span class="sxs-lookup"><span data-stu-id="6c2fb-121">NOTES</span></span>

## <span data-ttu-id="6c2fb-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c2fb-122">RELATED LINKS</span></span>
[<span data-ttu-id="6c2fb-123">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="6c2fb-123">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="6c2fb-124">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="6c2fb-124">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="6c2fb-125">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="6c2fb-125">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)