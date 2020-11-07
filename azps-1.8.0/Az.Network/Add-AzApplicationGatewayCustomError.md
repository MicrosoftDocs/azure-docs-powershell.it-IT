---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 0df6ae98692b7497448b0d3f15e88f1a18a87ae8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678706"
---
# <span data-ttu-id="6c286-101">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6c286-101">Add-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="6c286-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c286-102">SYNOPSIS</span></span>
<span data-ttu-id="6c286-103">Aggiunge un errore personalizzato a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6c286-103">Adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="6c286-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c286-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c286-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c286-105">DESCRIPTION</span></span>
<span data-ttu-id="6c286-106">Il cmdlet **Add-AzApplicationGatewayCustomError** aggiunge un errore personalizzato a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6c286-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="6c286-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c286-107">EXAMPLES</span></span>

### <span data-ttu-id="6c286-108">Esempio 1: aggiunge un errore personalizzato al livello del gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="6c286-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="6c286-109">Questo comando aggiunge un errore personalizzato del codice di stato HTTP 502 al gateway dell'applicazione $appgw e restituisce il gateway aggiornato.</span><span class="sxs-lookup"><span data-stu-id="6c286-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

### <span data-ttu-id="6c286-110">Esempio 2: aggiunge un errore personalizzato al livello del listener del gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="6c286-110">Example 2: Adds custom error to application gateway listener level</span></span>
```powershell
PS C:\> $resourceGroup = "resourceGroupName"
PS C:\> $AppGWName = "applicationGatewayName"
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $listenerName = "listenerName"
PS C:\> $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroupName $rg
PS C:\> $listener = Get-AzApplicationGatewayHttpListener -ApplicationGateway $AppGW -Name $listenerName
PS C:\> $updatedListener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url 
PS C:\> Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="6c286-111">Questo comando aggiunge un errore personalizzato del codice di stato HTTP 502 al gateway dell'applicazione $appgw a livello di listener e restituisce il gateway aggiornato.</span><span class="sxs-lookup"><span data-stu-id="6c286-111">This command adds a custom error of http status code 502 to the application gateway $appgw at the listener level, and return the updated gateway.</span></span>

## <span data-ttu-id="6c286-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c286-112">PARAMETERS</span></span>

### <span data-ttu-id="6c286-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c286-113">-ApplicationGateway</span></span>
<span data-ttu-id="6c286-114">Gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="6c286-114">The Application Gateway</span></span>

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

### <span data-ttu-id="6c286-115">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="6c286-115">-CustomErrorPageUrl</span></span>
<span data-ttu-id="6c286-116">URL della pagina di errore dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6c286-116">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="6c286-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c286-117">-DefaultProfile</span></span>
<span data-ttu-id="6c286-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c286-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c286-119">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="6c286-119">-StatusCode</span></span>
<span data-ttu-id="6c286-120">Codice di stato dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6c286-120">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="6c286-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c286-121">CommonParameters</span></span>
<span data-ttu-id="6c286-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c286-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c286-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c286-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c286-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c286-124">INPUTS</span></span>

### <span data-ttu-id="6c286-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c286-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6c286-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c286-126">OUTPUTS</span></span>

### <span data-ttu-id="6c286-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6c286-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="6c286-128">Note</span><span class="sxs-lookup"><span data-stu-id="6c286-128">NOTES</span></span>

## <span data-ttu-id="6c286-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c286-129">RELATED LINKS</span></span>

[<span data-ttu-id="6c286-130">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6c286-130">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="6c286-131">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6c286-131">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="6c286-132">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6c286-132">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="6c286-133">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6c286-133">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
