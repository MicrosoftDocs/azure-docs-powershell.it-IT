---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: c8bd4a0070aa0e5635fad7cb20a627a7d23f5922
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190452"
---
# <span data-ttu-id="9d073-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="9d073-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="9d073-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d073-102">SYNOPSIS</span></span>
<span data-ttu-id="9d073-103">Ottiene l'USK di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9d073-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="9d073-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d073-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d073-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d073-105">DESCRIPTION</span></span>
<span data-ttu-id="9d073-106">Il cmdlet **Get-AzApplicationGatewaySku** Ottiene l'unità di conservazione delle scorte (SKU) di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9d073-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="9d073-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d073-107">EXAMPLES</span></span>

### <span data-ttu-id="9d073-108">Esempio 1: ottenere una SKU gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="9d073-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="9d073-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="9d073-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="9d073-110">Il secondo comando ottiene l'USK di un gateway applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $SKU.</span><span class="sxs-lookup"><span data-stu-id="9d073-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="9d073-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d073-111">PARAMETERS</span></span>

### <span data-ttu-id="9d073-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d073-112">-ApplicationGateway</span></span>
<span data-ttu-id="9d073-113">Specifica l'oggetto gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9d073-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="9d073-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d073-114">-DefaultProfile</span></span>
<span data-ttu-id="9d073-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d073-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d073-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d073-116">CommonParameters</span></span>
<span data-ttu-id="9d073-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d073-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d073-118">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d073-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d073-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d073-119">INPUTS</span></span>

### <span data-ttu-id="9d073-120">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d073-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9d073-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d073-121">OUTPUTS</span></span>

### <span data-ttu-id="9d073-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="9d073-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="9d073-123">Note</span><span class="sxs-lookup"><span data-stu-id="9d073-123">NOTES</span></span>

## <span data-ttu-id="9d073-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d073-124">RELATED LINKS</span></span>

[<span data-ttu-id="9d073-125">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="9d073-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="9d073-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="9d073-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


