---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 63d90b646b639d7978dfbf734256976f423a3092
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953758"
---
# <span data-ttu-id="f5d59-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f5d59-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="f5d59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5d59-102">SYNOPSIS</span></span>
<span data-ttu-id="f5d59-103">Aggiorna un errore personalizzato in un listener http di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="f5d59-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="f5d59-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f5d59-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5d59-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f5d59-105">DESCRIPTION</span></span>
<span data-ttu-id="f5d59-106">Il cmdlet **Set-AzApplicationGatewayCustomError** aggiorna un errore personalizzato in un listener http di un gateway di applicazione.</span><span class="sxs-lookup"><span data-stu-id="f5d59-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="f5d59-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f5d59-107">EXAMPLES</span></span>

### <span data-ttu-id="f5d59-108">Esempio 1: Aggiorna un errore personalizzato da un listener http</span><span class="sxs-lookup"><span data-stu-id="f5d59-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="f5d59-109">Questo comando aggiorna l'errore personalizzato del codice di stato http 502 nel listener http $listener 01 e restituisce il listener aggiornato.</span><span class="sxs-lookup"><span data-stu-id="f5d59-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="f5d59-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5d59-110">PARAMETERS</span></span>

### <span data-ttu-id="f5d59-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="f5d59-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="f5d59-112">URL della pagina di errore dell'errore del cliente del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="f5d59-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f5d59-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5d59-113">-DefaultProfile</span></span>
<span data-ttu-id="f5d59-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f5d59-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5d59-115">-Http Listener</span><span class="sxs-lookup"><span data-stu-id="f5d59-115">-HttpListener</span></span>
<span data-ttu-id="f5d59-116">Listener Http del Gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="f5d59-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="f5d59-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="f5d59-117">-StatusCode</span></span>
<span data-ttu-id="f5d59-118">Codice di stato dell'errore del cliente del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="f5d59-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f5d59-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5d59-119">CommonParameters</span></span>
<span data-ttu-id="f5d59-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5d59-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5d59-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5d59-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5d59-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="f5d59-122">INPUTS</span></span>

### <span data-ttu-id="f5d59-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpHttpApplication</span><span class="sxs-lookup"><span data-stu-id="f5d59-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f5d59-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f5d59-124">OUTPUTS</span></span>

### <span data-ttu-id="f5d59-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f5d59-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f5d59-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="f5d59-126">NOTES</span></span>

## <span data-ttu-id="f5d59-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f5d59-127">RELATED LINKS</span></span>

[<span data-ttu-id="f5d59-128">Add-AzApplicationGatewayHttpCustomError</span><span class="sxs-lookup"><span data-stu-id="f5d59-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="f5d59-129">Get-AzApplicationGatewayHttpCustomError</span><span class="sxs-lookup"><span data-stu-id="f5d59-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="f5d59-130">Remove-AzApplicationGatewayHttpCustomError</span><span class="sxs-lookup"><span data-stu-id="f5d59-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)
