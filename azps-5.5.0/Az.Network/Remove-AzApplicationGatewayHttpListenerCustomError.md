---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 82675befb6a900bacdead036f323959e1e7a72a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189623"
---
# <span data-ttu-id="6d219-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="6d219-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="6d219-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d219-102">SYNOPSIS</span></span>
<span data-ttu-id="6d219-103">Rimuove un errore personalizzato da un listener http di un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="6d219-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="6d219-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d219-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d219-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6d219-105">DESCRIPTION</span></span>
<span data-ttu-id="6d219-106">Il cmdlet **Remove-AzApplicationGatewayCustomError** rimuove un errore personalizzato da un listener http di un gateway di applicazione.</span><span class="sxs-lookup"><span data-stu-id="6d219-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="6d219-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d219-107">EXAMPLES</span></span>

### <span data-ttu-id="6d219-108">Esempio 1: Rimuove un errore personalizzato da un listener http</span><span class="sxs-lookup"><span data-stu-id="6d219-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="6d219-109">Questo comando rimuove l'errore personalizzato del codice di stato http 502 dal listener http $listener 01 e restituisce il listener aggiornato.</span><span class="sxs-lookup"><span data-stu-id="6d219-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="6d219-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d219-110">PARAMETERS</span></span>

### <span data-ttu-id="6d219-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d219-111">-DefaultProfile</span></span>
<span data-ttu-id="6d219-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d219-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d219-113">-Http Listener</span><span class="sxs-lookup"><span data-stu-id="6d219-113">-HttpListener</span></span>
<span data-ttu-id="6d219-114">Listener Http del Gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="6d219-114">The Application Gateway Http Listener</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d219-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="6d219-115">-StatusCode</span></span>
<span data-ttu-id="6d219-116">Codice di stato dell'errore del cliente del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6d219-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="6d219-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d219-117">CommonParameters</span></span>
<span data-ttu-id="6d219-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d219-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d219-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d219-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d219-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="6d219-120">INPUTS</span></span>

### <span data-ttu-id="6d219-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="6d219-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="6d219-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d219-122">OUTPUTS</span></span>

### <span data-ttu-id="6d219-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6d219-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="6d219-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="6d219-124">NOTES</span></span>

## <span data-ttu-id="6d219-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d219-125">RELATED LINKS</span></span>

[<span data-ttu-id="6d219-126">Add-AzApplicationGatewayHttpCustomError</span><span class="sxs-lookup"><span data-stu-id="6d219-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="6d219-127">Get-AzApplicationGatewayHttpCustomError</span><span class="sxs-lookup"><span data-stu-id="6d219-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="6d219-128">Set-AzApplicationGatewayHttpCustomError</span><span class="sxs-lookup"><span data-stu-id="6d219-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
