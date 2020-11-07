---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 8718d79abef18217a727916d36c09e19de2a2de4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853390"
---
# <span data-ttu-id="4a7cb-101">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="4a7cb-101">Add-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="4a7cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a7cb-102">SYNOPSIS</span></span>
<span data-ttu-id="4a7cb-103">Aggiunge un errore personalizzato a un listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4a7cb-103">Adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="4a7cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a7cb-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a7cb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a7cb-105">DESCRIPTION</span></span>
<span data-ttu-id="4a7cb-106">Il cmdlet **Add-AzApplicationGatewayCustomError** aggiunge un errore personalizzato a un listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4a7cb-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="4a7cb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a7cb-107">EXAMPLES</span></span>

### <span data-ttu-id="4a7cb-108">Esempio 1: aggiunge un errore personalizzato al livello del listener http</span><span class="sxs-lookup"><span data-stu-id="4a7cb-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="4a7cb-109">Questo comando aggiunge un errore personalizzato del codice di stato HTTP 502 al listener HTTP $listener 01 e restituisce il listener aggiornato.</span><span class="sxs-lookup"><span data-stu-id="4a7cb-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="4a7cb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a7cb-110">PARAMETERS</span></span>

### <span data-ttu-id="4a7cb-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="4a7cb-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="4a7cb-112">URL della pagina di errore dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4a7cb-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="4a7cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a7cb-113">-DefaultProfile</span></span>
<span data-ttu-id="4a7cb-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a7cb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a7cb-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="4a7cb-115">-HttpListener</span></span>
<span data-ttu-id="4a7cb-116">Listener HTTP del gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="4a7cb-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="4a7cb-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="4a7cb-117">-StatusCode</span></span>
<span data-ttu-id="4a7cb-118">Codice di stato dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4a7cb-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="4a7cb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a7cb-119">CommonParameters</span></span>
<span data-ttu-id="4a7cb-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a7cb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a7cb-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a7cb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a7cb-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a7cb-122">INPUTS</span></span>

### <span data-ttu-id="4a7cb-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4a7cb-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="4a7cb-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a7cb-124">OUTPUTS</span></span>

### <span data-ttu-id="4a7cb-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4a7cb-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="4a7cb-126">Note</span><span class="sxs-lookup"><span data-stu-id="4a7cb-126">NOTES</span></span>

## <span data-ttu-id="4a7cb-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a7cb-127">RELATED LINKS</span></span>

[<span data-ttu-id="4a7cb-128">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="4a7cb-128">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="4a7cb-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="4a7cb-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="4a7cb-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="4a7cb-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
