---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d7ca75fbd2d033f35fa237113bc32bdc4699955a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982622"
---
# <span data-ttu-id="b05b6-101">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b05b6-101">Add-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="b05b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b05b6-102">SYNOPSIS</span></span>
<span data-ttu-id="b05b6-103">Aggiunge un errore personalizzato a un listener http di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="b05b6-103">Adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="b05b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b05b6-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b05b6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b05b6-105">DESCRIPTION</span></span>
<span data-ttu-id="b05b6-106">Il cmdlet **Add-AzApplicationGatewayCustomError aggiunge** un errore personalizzato a un listener http di un gateway di applicazione.</span><span class="sxs-lookup"><span data-stu-id="b05b6-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="b05b6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b05b6-107">EXAMPLES</span></span>

### <span data-ttu-id="b05b6-108">Esempio 1: aggiunge un errore personalizzato al livello di listener http</span><span class="sxs-lookup"><span data-stu-id="b05b6-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="b05b6-109">Questo comando aggiunge un errore personalizzato con codice di stato http 502 al listener http $listener 01 e restituisce il listener aggiornato.</span><span class="sxs-lookup"><span data-stu-id="b05b6-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="b05b6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b05b6-110">PARAMETERS</span></span>

### <span data-ttu-id="b05b6-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="b05b6-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="b05b6-112">URL della pagina di errore dell'errore del cliente del gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="b05b6-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="b05b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b05b6-113">-DefaultProfile</span></span>
<span data-ttu-id="b05b6-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b05b6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b05b6-115">-HttpDir</span><span class="sxs-lookup"><span data-stu-id="b05b6-115">-HttpListener</span></span>
<span data-ttu-id="b05b6-116">Listener Http del Gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="b05b6-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="b05b6-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="b05b6-117">-StatusCode</span></span>
<span data-ttu-id="b05b6-118">Codice di stato dell'errore del cliente del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="b05b6-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="b05b6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b05b6-119">CommonParameters</span></span>
<span data-ttu-id="b05b6-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b05b6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b05b6-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b05b6-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b05b6-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="b05b6-122">INPUTS</span></span>

### <span data-ttu-id="b05b6-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpHttpApplication</span><span class="sxs-lookup"><span data-stu-id="b05b6-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b05b6-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b05b6-124">OUTPUTS</span></span>

### <span data-ttu-id="b05b6-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b05b6-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="b05b6-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="b05b6-126">NOTES</span></span>

## <span data-ttu-id="b05b6-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b05b6-127">RELATED LINKS</span></span>

[<span data-ttu-id="b05b6-128">Get-AzApplicationGatewayHttpCustomError</span><span class="sxs-lookup"><span data-stu-id="b05b6-128">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="b05b6-129">Remove-AzApplicationGatewayHttpCustomError</span><span class="sxs-lookup"><span data-stu-id="b05b6-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="b05b6-130">Set-AzApplicationGatewayHttpCustomError</span><span class="sxs-lookup"><span data-stu-id="b05b6-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
