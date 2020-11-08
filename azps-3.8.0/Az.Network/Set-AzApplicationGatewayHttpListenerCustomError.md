---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 3f53bd59e85fa9dac03a99d7e192ce51325ca6a4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019309"
---
# <span data-ttu-id="1a3ea-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1a3ea-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="1a3ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a3ea-102">SYNOPSIS</span></span>
<span data-ttu-id="1a3ea-103">Aggiorna un errore personalizzato in un listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1a3ea-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="1a3ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a3ea-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a3ea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a3ea-105">DESCRIPTION</span></span>
<span data-ttu-id="1a3ea-106">Il cmdlet **set-AzApplicationGatewayCustomError** aggiorna un errore personalizzato in un listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1a3ea-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="1a3ea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a3ea-107">EXAMPLES</span></span>

### <span data-ttu-id="1a3ea-108">Esempio 1: aggiorna un errore personalizzato da un listener http</span><span class="sxs-lookup"><span data-stu-id="1a3ea-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="1a3ea-109">Questo comando Aggiorna l'errore personalizzato del codice di stato HTTP 502 nel listener HTTP $listener 01 e restituisce il listener aggiornato.</span><span class="sxs-lookup"><span data-stu-id="1a3ea-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="1a3ea-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a3ea-110">PARAMETERS</span></span>

### <span data-ttu-id="1a3ea-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="1a3ea-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="1a3ea-112">URL della pagina di errore dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1a3ea-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="1a3ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a3ea-113">-DefaultProfile</span></span>
<span data-ttu-id="1a3ea-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a3ea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a3ea-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="1a3ea-115">-HttpListener</span></span>
<span data-ttu-id="1a3ea-116">Listener HTTP del gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="1a3ea-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="1a3ea-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="1a3ea-117">-StatusCode</span></span>
<span data-ttu-id="1a3ea-118">Codice di stato dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1a3ea-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="1a3ea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a3ea-119">CommonParameters</span></span>
<span data-ttu-id="1a3ea-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a3ea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a3ea-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a3ea-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a3ea-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a3ea-122">INPUTS</span></span>

### <span data-ttu-id="1a3ea-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1a3ea-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="1a3ea-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a3ea-124">OUTPUTS</span></span>

### <span data-ttu-id="1a3ea-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1a3ea-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="1a3ea-126">Note</span><span class="sxs-lookup"><span data-stu-id="1a3ea-126">NOTES</span></span>

## <span data-ttu-id="1a3ea-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a3ea-127">RELATED LINKS</span></span>

[<span data-ttu-id="1a3ea-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1a3ea-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="1a3ea-129">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1a3ea-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="1a3ea-130">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1a3ea-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)
