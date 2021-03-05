---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: cf869a0de5847b1930879dbd610749746370791b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994067"
---
# <span data-ttu-id="e990d-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e990d-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="e990d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e990d-102">SYNOPSIS</span></span>
<span data-ttu-id="e990d-103">Ottiene lo SKU di un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e990d-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="e990d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e990d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e990d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e990d-105">DESCRIPTION</span></span>
<span data-ttu-id="e990d-106">Il cmdlet **Get-AzApplicationGatewaySku** ottiene l'unità di conservazione dei titoli azionari di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="e990d-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="e990d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e990d-107">EXAMPLES</span></span>

### <span data-ttu-id="e990d-108">Esempio 1: Ottenere lo SKU di un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="e990d-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="e990d-109">Il primo comando recupera il Gateway applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="e990d-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="e990d-110">Il secondo comando ottiene lo SKU di un gateway applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile $SKU.</span><span class="sxs-lookup"><span data-stu-id="e990d-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="e990d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e990d-111">PARAMETERS</span></span>

### <span data-ttu-id="e990d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e990d-112">-ApplicationGateway</span></span>
<span data-ttu-id="e990d-113">Specifica l'oggetto gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="e990d-113">Specifies the application gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e990d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e990d-114">-DefaultProfile</span></span>
<span data-ttu-id="e990d-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e990d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e990d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e990d-116">CommonParameters</span></span>
<span data-ttu-id="e990d-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e990d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e990d-118">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e990d-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e990d-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="e990d-119">INPUTS</span></span>

### <span data-ttu-id="e990d-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e990d-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e990d-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e990d-121">OUTPUTS</span></span>

### <span data-ttu-id="e990d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e990d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="e990d-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="e990d-123">NOTES</span></span>

## <span data-ttu-id="e990d-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e990d-124">RELATED LINKS</span></span>

[<span data-ttu-id="e990d-125">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e990d-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="e990d-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e990d-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


