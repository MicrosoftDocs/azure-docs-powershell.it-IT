---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 82675befb6a900bacdead036f323959e1e7a72a9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486711"
---
# <span data-ttu-id="d9ae4-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="d9ae4-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="d9ae4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ae4-103">Rimuove un errore personalizzato da un listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d9ae4-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="d9ae4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9ae4-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9ae4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9ae4-105">DESCRIPTION</span></span>
<span data-ttu-id="d9ae4-106">Il cmdlet **Remove-AzApplicationGatewayCustomError** rimuove un errore personalizzato da un listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d9ae4-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="d9ae4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9ae4-107">EXAMPLES</span></span>

### <span data-ttu-id="d9ae4-108">Esempio 1: rimuove l'errore personalizzato da un listener http</span><span class="sxs-lookup"><span data-stu-id="d9ae4-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="d9ae4-109">Questo comando rimuove l'errore personalizzato del codice di stato HTTP 502 dal listener HTTP $listener 01 e restituisce il listener aggiornato.</span><span class="sxs-lookup"><span data-stu-id="d9ae4-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="d9ae4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9ae4-110">PARAMETERS</span></span>

### <span data-ttu-id="d9ae4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ae4-111">-DefaultProfile</span></span>
<span data-ttu-id="d9ae4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9ae4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9ae4-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="d9ae4-113">-HttpListener</span></span>
<span data-ttu-id="d9ae4-114">Listener HTTP del gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="d9ae4-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="d9ae4-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="d9ae4-115">-StatusCode</span></span>
<span data-ttu-id="d9ae4-116">Codice di stato dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d9ae4-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="d9ae4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ae4-117">CommonParameters</span></span>
<span data-ttu-id="d9ae4-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9ae4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ae4-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9ae4-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ae4-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9ae4-120">INPUTS</span></span>

### <span data-ttu-id="d9ae4-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d9ae4-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="d9ae4-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9ae4-122">OUTPUTS</span></span>

### <span data-ttu-id="d9ae4-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d9ae4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="d9ae4-124">Note</span><span class="sxs-lookup"><span data-stu-id="d9ae4-124">NOTES</span></span>

## <span data-ttu-id="d9ae4-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9ae4-125">RELATED LINKS</span></span>

[<span data-ttu-id="d9ae4-126">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="d9ae4-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="d9ae4-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="d9ae4-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="d9ae4-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="d9ae4-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
