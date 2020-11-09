---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 91de215282dc05be2136237fa5fb2b244d7f0c4a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311406"
---
# <span data-ttu-id="4dd09-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4dd09-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="4dd09-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4dd09-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd09-103">Rimuove un errore personalizzato da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4dd09-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="4dd09-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4dd09-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4dd09-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4dd09-105">DESCRIPTION</span></span>
<span data-ttu-id="4dd09-106">Il cmdlet **Remove-AzApplicationGatewayCustomError** rimuove un errore personalizzato da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4dd09-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="4dd09-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4dd09-107">EXAMPLES</span></span>

### <span data-ttu-id="4dd09-108">Esempio 1: rimuove l'errore personalizzato da un gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="4dd09-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="4dd09-109">Questo comando rimuove l'errore personalizzato del codice di stato HTTP 502 dal gateway dell'applicazione $appgw e restituisce il gateway aggiornato.</span><span class="sxs-lookup"><span data-stu-id="4dd09-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="4dd09-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4dd09-110">PARAMETERS</span></span>

### <span data-ttu-id="4dd09-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4dd09-111">-ApplicationGateway</span></span>
<span data-ttu-id="4dd09-112">Gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="4dd09-112">The Application Gateway</span></span>

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

### <span data-ttu-id="4dd09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dd09-113">-DefaultProfile</span></span>
<span data-ttu-id="4dd09-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4dd09-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dd09-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="4dd09-115">-StatusCode</span></span>
<span data-ttu-id="4dd09-116">Codice di stato dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4dd09-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="4dd09-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd09-117">CommonParameters</span></span>
<span data-ttu-id="4dd09-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dd09-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd09-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dd09-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd09-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4dd09-120">INPUTS</span></span>

### <span data-ttu-id="4dd09-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4dd09-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4dd09-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4dd09-122">OUTPUTS</span></span>

### <span data-ttu-id="4dd09-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4dd09-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="4dd09-124">Note</span><span class="sxs-lookup"><span data-stu-id="4dd09-124">NOTES</span></span>

## <span data-ttu-id="4dd09-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4dd09-125">RELATED LINKS</span></span>

[<span data-ttu-id="4dd09-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4dd09-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="4dd09-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4dd09-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="4dd09-128">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4dd09-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="4dd09-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4dd09-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
