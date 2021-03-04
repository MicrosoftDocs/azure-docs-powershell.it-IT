---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 990c9624d949fa695b815a9530125a90693816ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952158"
---
# <span data-ttu-id="7d4f2-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7d4f2-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="7d4f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d4f2-102">SYNOPSIS</span></span>
<span data-ttu-id="7d4f2-103">Rimuove un errore personalizzato da un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="7d4f2-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="7d4f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d4f2-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d4f2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7d4f2-105">DESCRIPTION</span></span>
<span data-ttu-id="7d4f2-106">Il cmdlet **Remove-AzApplicationGatewayCustomError** rimuove un errore personalizzato da un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="7d4f2-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="7d4f2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d4f2-107">EXAMPLES</span></span>

### <span data-ttu-id="7d4f2-108">Esempio 1: Rimuove un errore personalizzato da un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="7d4f2-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="7d4f2-109">Questo comando rimuove l'errore personalizzato 502 di stato http dal $appgw gateway applicazione e restituisce il gateway aggiornato.</span><span class="sxs-lookup"><span data-stu-id="7d4f2-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="7d4f2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d4f2-110">PARAMETERS</span></span>

### <span data-ttu-id="7d4f2-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7d4f2-111">-ApplicationGateway</span></span>
<span data-ttu-id="7d4f2-112">Gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="7d4f2-112">The Application Gateway</span></span>

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

### <span data-ttu-id="7d4f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d4f2-113">-DefaultProfile</span></span>
<span data-ttu-id="7d4f2-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d4f2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d4f2-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="7d4f2-115">-StatusCode</span></span>
<span data-ttu-id="7d4f2-116">Codice di stato dell'errore del cliente del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="7d4f2-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="7d4f2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d4f2-117">CommonParameters</span></span>
<span data-ttu-id="7d4f2-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d4f2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d4f2-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d4f2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d4f2-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="7d4f2-120">INPUTS</span></span>

### <span data-ttu-id="7d4f2-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7d4f2-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7d4f2-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d4f2-122">OUTPUTS</span></span>

### <span data-ttu-id="7d4f2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7d4f2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="7d4f2-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="7d4f2-124">NOTES</span></span>

## <span data-ttu-id="7d4f2-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d4f2-125">RELATED LINKS</span></span>

[<span data-ttu-id="7d4f2-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7d4f2-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="7d4f2-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7d4f2-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="7d4f2-128">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7d4f2-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="7d4f2-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7d4f2-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
