---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 84c80ba4469d8003344d99b7dfbb89ff7d6660b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189839"
---
# <span data-ttu-id="6fc72-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6fc72-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="6fc72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fc72-102">SYNOPSIS</span></span>
<span data-ttu-id="6fc72-103">Recupera gli errori personalizzati da un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="6fc72-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="6fc72-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6fc72-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fc72-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6fc72-105">DESCRIPTION</span></span>
<span data-ttu-id="6fc72-106">Il cmdlet **Get-AzApplicationGatewayCustomError** ottiene errori personalizzati da un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6fc72-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="6fc72-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6fc72-107">EXAMPLES</span></span>

### <span data-ttu-id="6fc72-108">Esempio 1: Recupera un errore personalizzato in un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="6fc72-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="6fc72-109">Questo comando recupera e restituisce l'errore personalizzato del codice di stato http 502 dal gateway $appgw.</span><span class="sxs-lookup"><span data-stu-id="6fc72-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="6fc72-110">Esempio 2: ottiene l'elenco di tutti gli errori personalizzati in un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="6fc72-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="6fc72-111">Questo comando recupera e restituisce l'elenco di tutti gli errori personalizzati dal gateway applicazione $appgw.</span><span class="sxs-lookup"><span data-stu-id="6fc72-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="6fc72-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fc72-112">PARAMETERS</span></span>

### <span data-ttu-id="6fc72-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6fc72-113">-ApplicationGateway</span></span>
<span data-ttu-id="6fc72-114">Gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="6fc72-114">The Application Gateway</span></span>

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

### <span data-ttu-id="6fc72-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fc72-115">-DefaultProfile</span></span>
<span data-ttu-id="6fc72-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6fc72-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fc72-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="6fc72-117">-StatusCode</span></span>
<span data-ttu-id="6fc72-118">Codice di stato dell'errore del cliente del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6fc72-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fc72-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fc72-119">CommonParameters</span></span>
<span data-ttu-id="6fc72-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fc72-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fc72-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6fc72-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fc72-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="6fc72-122">INPUTS</span></span>

### <span data-ttu-id="6fc72-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6fc72-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6fc72-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6fc72-124">OUTPUTS</span></span>

### <span data-ttu-id="6fc72-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6fc72-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="6fc72-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="6fc72-126">NOTES</span></span>

## <span data-ttu-id="6fc72-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6fc72-127">RELATED LINKS</span></span>

[<span data-ttu-id="6fc72-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6fc72-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="6fc72-129">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6fc72-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="6fc72-130">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6fc72-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="6fc72-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6fc72-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
