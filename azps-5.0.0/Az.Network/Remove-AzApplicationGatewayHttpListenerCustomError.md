---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 82675befb6a900bacdead036f323959e1e7a72a9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310861"
---
# <span data-ttu-id="1c2c6-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1c2c6-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="1c2c6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c2c6-102">SYNOPSIS</span></span>
<span data-ttu-id="1c2c6-103">Rimuove un errore personalizzato da un listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="1c2c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c2c6-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c2c6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c2c6-105">DESCRIPTION</span></span>
<span data-ttu-id="1c2c6-106">Il cmdlet **Remove-AzApplicationGatewayCustomError** rimuove un errore personalizzato da un listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="1c2c6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c2c6-107">EXAMPLES</span></span>

### <span data-ttu-id="1c2c6-108">Esempio 1: rimuove l'errore personalizzato da un listener http</span><span class="sxs-lookup"><span data-stu-id="1c2c6-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="1c2c6-109">Questo comando rimuove l'errore personalizzato del codice di stato HTTP 502 dal listener HTTP $listener 01 e restituisce il listener aggiornato.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="1c2c6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c2c6-110">PARAMETERS</span></span>

### <span data-ttu-id="1c2c6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c2c6-111">-DefaultProfile</span></span>
<span data-ttu-id="1c2c6-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c2c6-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="1c2c6-113">-HttpListener</span></span>
<span data-ttu-id="1c2c6-114">Listener HTTP del gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="1c2c6-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="1c2c6-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="1c2c6-115">-StatusCode</span></span>
<span data-ttu-id="1c2c6-116">Codice di stato dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="1c2c6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c2c6-117">CommonParameters</span></span>
<span data-ttu-id="1c2c6-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c2c6-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c2c6-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c2c6-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c2c6-120">INPUTS</span></span>

### <span data-ttu-id="1c2c6-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1c2c6-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="1c2c6-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c2c6-122">OUTPUTS</span></span>

### <span data-ttu-id="1c2c6-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1c2c6-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="1c2c6-124">Note</span><span class="sxs-lookup"><span data-stu-id="1c2c6-124">NOTES</span></span>

## <span data-ttu-id="1c2c6-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c2c6-125">RELATED LINKS</span></span>

[<span data-ttu-id="1c2c6-126">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1c2c6-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="1c2c6-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1c2c6-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="1c2c6-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1c2c6-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
