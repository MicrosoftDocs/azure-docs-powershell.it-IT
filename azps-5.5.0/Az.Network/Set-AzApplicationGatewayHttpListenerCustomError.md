---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 3f53bd59e85fa9dac03a99d7e192ce51325ca6a4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179383"
---
# <span data-ttu-id="5f710-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="5f710-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="5f710-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f710-102">SYNOPSIS</span></span>
<span data-ttu-id="5f710-103">Aggiorna un errore personalizzato in un listener http di un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="5f710-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="5f710-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f710-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f710-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5f710-105">DESCRIPTION</span></span>
<span data-ttu-id="5f710-106">Il cmdlet **Set-AzApplicationGatewayCustomError** aggiorna un errore personalizzato in un listener http di un gateway di applicazione.</span><span class="sxs-lookup"><span data-stu-id="5f710-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="5f710-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f710-107">EXAMPLES</span></span>

### <span data-ttu-id="5f710-108">Esempio 1: Aggiorna un errore personalizzato da un listener http</span><span class="sxs-lookup"><span data-stu-id="5f710-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="5f710-109">Questo comando aggiorna l'errore personalizzato del codice di stato http 502 nel listener http $listener 01 e restituisce il listener aggiornato.</span><span class="sxs-lookup"><span data-stu-id="5f710-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="5f710-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f710-110">PARAMETERS</span></span>

### <span data-ttu-id="5f710-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="5f710-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="5f710-112">URL della pagina di errore dell'errore del cliente del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="5f710-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="5f710-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f710-113">-DefaultProfile</span></span>
<span data-ttu-id="5f710-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5f710-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f710-115">-Http Listener</span><span class="sxs-lookup"><span data-stu-id="5f710-115">-HttpListener</span></span>
<span data-ttu-id="5f710-116">Listener Http del Gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="5f710-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="5f710-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="5f710-117">-StatusCode</span></span>
<span data-ttu-id="5f710-118">Codice di stato dell'errore del cliente del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="5f710-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="5f710-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f710-119">CommonParameters</span></span>
<span data-ttu-id="5f710-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f710-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f710-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f710-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f710-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="5f710-122">INPUTS</span></span>

### <span data-ttu-id="5f710-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="5f710-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="5f710-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f710-124">OUTPUTS</span></span>

### <span data-ttu-id="5f710-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="5f710-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="5f710-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="5f710-126">NOTES</span></span>

## <span data-ttu-id="5f710-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f710-127">RELATED LINKS</span></span>

[<span data-ttu-id="5f710-128">Add-AzApplicationGatewayHttpCustomError</span><span class="sxs-lookup"><span data-stu-id="5f710-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="5f710-129">Get-AzApplicationGatewayHttpCustomError</span><span class="sxs-lookup"><span data-stu-id="5f710-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="5f710-130">Remove-AzApplicationGatewayHttpCustomError</span><span class="sxs-lookup"><span data-stu-id="5f710-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)
