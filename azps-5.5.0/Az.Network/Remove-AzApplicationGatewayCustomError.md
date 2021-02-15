---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 91de215282dc05be2136237fa5fb2b244d7f0c4a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186974"
---
# <span data-ttu-id="4ecea-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4ecea-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="4ecea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ecea-102">SYNOPSIS</span></span>
<span data-ttu-id="4ecea-103">Rimuove un errore personalizzato da un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="4ecea-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="4ecea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ecea-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ecea-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4ecea-105">DESCRIPTION</span></span>
<span data-ttu-id="4ecea-106">Il cmdlet **Remove-AzApplicationGatewayCustomError** rimuove un errore personalizzato da un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="4ecea-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="4ecea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ecea-107">EXAMPLES</span></span>

### <span data-ttu-id="4ecea-108">Esempio 1: Rimuove un errore personalizzato da un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="4ecea-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="4ecea-109">Questo comando rimuove l'errore personalizzato 502 di stato http dal $appgw gateway applicazione e restituisce il gateway aggiornato.</span><span class="sxs-lookup"><span data-stu-id="4ecea-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="4ecea-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ecea-110">PARAMETERS</span></span>

### <span data-ttu-id="4ecea-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ecea-111">-ApplicationGateway</span></span>
<span data-ttu-id="4ecea-112">Gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="4ecea-112">The Application Gateway</span></span>

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

### <span data-ttu-id="4ecea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ecea-113">-DefaultProfile</span></span>
<span data-ttu-id="4ecea-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ecea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ecea-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="4ecea-115">-StatusCode</span></span>
<span data-ttu-id="4ecea-116">Codice di stato dell'errore del cliente del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="4ecea-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="4ecea-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ecea-117">CommonParameters</span></span>
<span data-ttu-id="4ecea-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ecea-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ecea-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ecea-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ecea-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="4ecea-120">INPUTS</span></span>

### <span data-ttu-id="4ecea-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ecea-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ecea-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ecea-122">OUTPUTS</span></span>

### <span data-ttu-id="4ecea-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4ecea-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="4ecea-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="4ecea-124">NOTES</span></span>

## <span data-ttu-id="4ecea-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ecea-125">RELATED LINKS</span></span>

[<span data-ttu-id="4ecea-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4ecea-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="4ecea-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4ecea-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="4ecea-128">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4ecea-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="4ecea-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4ecea-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
