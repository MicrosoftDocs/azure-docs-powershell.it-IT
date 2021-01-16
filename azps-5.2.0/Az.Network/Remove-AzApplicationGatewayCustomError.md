---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 91de215282dc05be2136237fa5fb2b244d7f0c4a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369263"
---
# <span data-ttu-id="a57c2-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a57c2-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="a57c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a57c2-102">SYNOPSIS</span></span>
<span data-ttu-id="a57c2-103">Rimuove un errore personalizzato da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a57c2-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="a57c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a57c2-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a57c2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a57c2-105">DESCRIPTION</span></span>
<span data-ttu-id="a57c2-106">Il cmdlet **Remove-AzApplicationGatewayCustomError** rimuove un errore personalizzato da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a57c2-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="a57c2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a57c2-107">EXAMPLES</span></span>

### <span data-ttu-id="a57c2-108">Esempio 1: rimuove l'errore personalizzato da un gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="a57c2-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="a57c2-109">Questo comando rimuove l'errore personalizzato del codice di stato HTTP 502 dal gateway dell'applicazione $appgw e restituisce il gateway aggiornato.</span><span class="sxs-lookup"><span data-stu-id="a57c2-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="a57c2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a57c2-110">PARAMETERS</span></span>

### <span data-ttu-id="a57c2-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a57c2-111">-ApplicationGateway</span></span>
<span data-ttu-id="a57c2-112">Gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="a57c2-112">The Application Gateway</span></span>

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

### <span data-ttu-id="a57c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a57c2-113">-DefaultProfile</span></span>
<span data-ttu-id="a57c2-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a57c2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a57c2-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="a57c2-115">-StatusCode</span></span>
<span data-ttu-id="a57c2-116">Codice di stato dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a57c2-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="a57c2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a57c2-117">CommonParameters</span></span>
<span data-ttu-id="a57c2-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a57c2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a57c2-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a57c2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a57c2-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a57c2-120">INPUTS</span></span>

### <span data-ttu-id="a57c2-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a57c2-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a57c2-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a57c2-122">OUTPUTS</span></span>

### <span data-ttu-id="a57c2-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a57c2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="a57c2-124">Note</span><span class="sxs-lookup"><span data-stu-id="a57c2-124">NOTES</span></span>

## <span data-ttu-id="a57c2-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a57c2-125">RELATED LINKS</span></span>

[<span data-ttu-id="a57c2-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a57c2-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="a57c2-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a57c2-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="a57c2-128">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a57c2-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="a57c2-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a57c2-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
