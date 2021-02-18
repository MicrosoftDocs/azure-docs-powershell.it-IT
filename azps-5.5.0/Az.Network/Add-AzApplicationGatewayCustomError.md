---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
ms.openlocfilehash: e3bac58fca1c405aeef3366cb3ec1ee1b01a0891
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184799"
---
# <span data-ttu-id="5a391-101">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="5a391-101">Add-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="5a391-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a391-102">SYNOPSIS</span></span>
<span data-ttu-id="5a391-103">Aggiunge un errore personalizzato a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="5a391-103">Adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="5a391-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a391-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a391-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5a391-105">DESCRIPTION</span></span>
<span data-ttu-id="5a391-106">Il cmdlet **Add-AzApplicationGatewayCustomError** aggiunge un errore personalizzato a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="5a391-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="5a391-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a391-107">EXAMPLES</span></span>

### <span data-ttu-id="5a391-108">Esempio 1: aggiunge un errore personalizzato a livello di gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="5a391-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $resourceGroupName = "resourceGroupName"
PS C:\> $AppGWName = "applicationGatewayName"
PS C:\> $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroup $resourceGroupName
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzApplicationGatewayCustomError -ApplicationGateway $AppGw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
PS C:\> Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="5a391-109">Questo comando aggiunge un errore personalizzato con codice di stato http 502 al gateway $appgw applicazione e restituisce il gateway aggiornato.</span><span class="sxs-lookup"><span data-stu-id="5a391-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

### <span data-ttu-id="5a391-110">Esempio 2: aggiunge un errore personalizzato al livello di listener del gateway di applicazione</span><span class="sxs-lookup"><span data-stu-id="5a391-110">Example 2: Adds custom error to application gateway listener level</span></span>
```powershell
 $resourceGroupName = "resourceGroupName"
 $AppGWName = "applicationGatewayName"
 $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
 $listenerName = "listenerName"
 $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroupName $resourceGroupName
 $listener = Get-AzApplicationGatewayHttpListener -ApplicationGateway $AppGW -Name $listenerName
 $updatedListener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url 
 Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="5a391-111">Questo comando aggiunge un errore personalizzato con codice di stato http 502 al $appgw gateway applicazione a livello di listener e restituisce il gateway aggiornato.</span><span class="sxs-lookup"><span data-stu-id="5a391-111">This command adds a custom error of http status code 502 to the application gateway $appgw at the listener level, and return the updated gateway.</span></span>

## <span data-ttu-id="5a391-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a391-112">PARAMETERS</span></span>

### <span data-ttu-id="5a391-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a391-113">-ApplicationGateway</span></span>
<span data-ttu-id="5a391-114">Gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="5a391-114">The Application Gateway</span></span>

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

### <span data-ttu-id="5a391-115">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="5a391-115">-CustomErrorPageUrl</span></span>
<span data-ttu-id="5a391-116">URL della pagina di errore dell'errore del cliente del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="5a391-116">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="5a391-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a391-117">-DefaultProfile</span></span>
<span data-ttu-id="5a391-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a391-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a391-119">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="5a391-119">-StatusCode</span></span>
<span data-ttu-id="5a391-120">Codice di stato dell'errore del cliente del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="5a391-120">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="5a391-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a391-121">CommonParameters</span></span>
<span data-ttu-id="5a391-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a391-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a391-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a391-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a391-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="5a391-124">INPUTS</span></span>

### <span data-ttu-id="5a391-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a391-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5a391-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a391-126">OUTPUTS</span></span>

### <span data-ttu-id="5a391-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="5a391-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="5a391-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="5a391-128">NOTES</span></span>

## <span data-ttu-id="5a391-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a391-129">RELATED LINKS</span></span>

[<span data-ttu-id="5a391-130">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="5a391-130">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="5a391-131">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="5a391-131">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="5a391-132">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="5a391-132">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="5a391-133">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="5a391-133">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
