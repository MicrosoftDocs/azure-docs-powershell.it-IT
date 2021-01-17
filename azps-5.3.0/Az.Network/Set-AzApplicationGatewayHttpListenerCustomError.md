---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 3f53bd59e85fa9dac03a99d7e192ce51325ca6a4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378699"
---
# <span data-ttu-id="128d7-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="128d7-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="128d7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="128d7-102">SYNOPSIS</span></span>
<span data-ttu-id="128d7-103">Aggiorna un errore personalizzato in un listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="128d7-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="128d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="128d7-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="128d7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="128d7-105">DESCRIPTION</span></span>
<span data-ttu-id="128d7-106">Il cmdlet **set-AzApplicationGatewayCustomError** aggiorna un errore personalizzato in un listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="128d7-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="128d7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="128d7-107">EXAMPLES</span></span>

### <span data-ttu-id="128d7-108">Esempio 1: aggiorna un errore personalizzato da un listener http</span><span class="sxs-lookup"><span data-stu-id="128d7-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="128d7-109">Questo comando Aggiorna l'errore personalizzato del codice di stato HTTP 502 nel listener HTTP $listener 01 e restituisce il listener aggiornato.</span><span class="sxs-lookup"><span data-stu-id="128d7-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="128d7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="128d7-110">PARAMETERS</span></span>

### <span data-ttu-id="128d7-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="128d7-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="128d7-112">URL della pagina di errore dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="128d7-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="128d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="128d7-113">-DefaultProfile</span></span>
<span data-ttu-id="128d7-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="128d7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="128d7-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="128d7-115">-HttpListener</span></span>
<span data-ttu-id="128d7-116">Listener HTTP del gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="128d7-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="128d7-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="128d7-117">-StatusCode</span></span>
<span data-ttu-id="128d7-118">Codice di stato dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="128d7-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="128d7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="128d7-119">CommonParameters</span></span>
<span data-ttu-id="128d7-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="128d7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="128d7-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="128d7-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="128d7-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="128d7-122">INPUTS</span></span>

### <span data-ttu-id="128d7-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="128d7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="128d7-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="128d7-124">OUTPUTS</span></span>

### <span data-ttu-id="128d7-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="128d7-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="128d7-126">Note</span><span class="sxs-lookup"><span data-stu-id="128d7-126">NOTES</span></span>

## <span data-ttu-id="128d7-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="128d7-127">RELATED LINKS</span></span>

[<span data-ttu-id="128d7-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="128d7-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="128d7-129">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="128d7-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="128d7-130">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="128d7-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)
