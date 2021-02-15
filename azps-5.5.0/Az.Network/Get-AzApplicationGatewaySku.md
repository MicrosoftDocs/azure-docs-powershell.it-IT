---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: c8bd4a0070aa0e5635fad7cb20a627a7d23f5922
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189823"
---
# <span data-ttu-id="7d9c2-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7d9c2-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="7d9c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d9c2-102">SYNOPSIS</span></span>
<span data-ttu-id="7d9c2-103">Ottiene lo SKU di un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="7d9c2-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="7d9c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d9c2-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d9c2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7d9c2-105">DESCRIPTION</span></span>
<span data-ttu-id="7d9c2-106">Il cmdlet **Get-AzApplicationGatewaySku** ottiene l'unità di conservazione dei titoli azionari di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="7d9c2-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="7d9c2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d9c2-107">EXAMPLES</span></span>

### <span data-ttu-id="7d9c2-108">Esempio 1: Ottenere lo SKU di un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="7d9c2-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="7d9c2-109">Il primo comando recupera il Gateway applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="7d9c2-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="7d9c2-110">Il secondo comando ottiene lo SKU di un gateway applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile $SKU.</span><span class="sxs-lookup"><span data-stu-id="7d9c2-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="7d9c2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d9c2-111">PARAMETERS</span></span>

### <span data-ttu-id="7d9c2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7d9c2-112">-ApplicationGateway</span></span>
<span data-ttu-id="7d9c2-113">Specifica l'oggetto gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="7d9c2-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="7d9c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d9c2-114">-DefaultProfile</span></span>
<span data-ttu-id="7d9c2-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d9c2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d9c2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d9c2-116">CommonParameters</span></span>
<span data-ttu-id="7d9c2-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d9c2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d9c2-118">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7d9c2-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d9c2-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="7d9c2-119">INPUTS</span></span>

### <span data-ttu-id="7d9c2-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7d9c2-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7d9c2-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d9c2-121">OUTPUTS</span></span>

### <span data-ttu-id="7d9c2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7d9c2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="7d9c2-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="7d9c2-123">NOTES</span></span>

## <span data-ttu-id="7d9c2-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d9c2-124">RELATED LINKS</span></span>

[<span data-ttu-id="7d9c2-125">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7d9c2-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="7d9c2-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7d9c2-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


