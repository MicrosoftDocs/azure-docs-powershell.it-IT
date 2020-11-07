---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 4c92c3c6b66e1b1208c7a0425b27a7e966bf6689
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852825"
---
# <span data-ttu-id="3f2b4-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3f2b4-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="3f2b4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3f2b4-102">SYNOPSIS</span></span>
<span data-ttu-id="3f2b4-103">Rimuove un errore personalizzato da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f2b4-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="3f2b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f2b4-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f2b4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f2b4-105">DESCRIPTION</span></span>
<span data-ttu-id="3f2b4-106">Il cmdlet **Remove-AzApplicationGatewayCustomError** rimuove un errore personalizzato da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f2b4-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="3f2b4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f2b4-107">EXAMPLES</span></span>

### <span data-ttu-id="3f2b4-108">Esempio 1: rimuove l'errore personalizzato da un gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="3f2b4-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="3f2b4-109">Questo comando rimuove l'errore personalizzato del codice di stato HTTP 502 dal gateway dell'applicazione $appgw e restituisce il gateway aggiornato.</span><span class="sxs-lookup"><span data-stu-id="3f2b4-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="3f2b4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3f2b4-110">PARAMETERS</span></span>

### <span data-ttu-id="3f2b4-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3f2b4-111">-ApplicationGateway</span></span>
<span data-ttu-id="3f2b4-112">Gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="3f2b4-112">The Application Gateway</span></span>

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

### <span data-ttu-id="3f2b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f2b4-113">-DefaultProfile</span></span>
<span data-ttu-id="3f2b4-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3f2b4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f2b4-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="3f2b4-115">-StatusCode</span></span>
<span data-ttu-id="3f2b4-116">Codice di stato dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f2b4-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="3f2b4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f2b4-117">CommonParameters</span></span>
<span data-ttu-id="3f2b4-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f2b4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f2b4-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f2b4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f2b4-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3f2b4-120">INPUTS</span></span>

### <span data-ttu-id="3f2b4-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3f2b4-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3f2b4-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f2b4-122">OUTPUTS</span></span>

### <span data-ttu-id="3f2b4-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3f2b4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="3f2b4-124">Note</span><span class="sxs-lookup"><span data-stu-id="3f2b4-124">NOTES</span></span>

## <span data-ttu-id="3f2b4-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f2b4-125">RELATED LINKS</span></span>

[<span data-ttu-id="3f2b4-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3f2b4-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="3f2b4-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3f2b4-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="3f2b4-128">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3f2b4-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="3f2b4-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3f2b4-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
