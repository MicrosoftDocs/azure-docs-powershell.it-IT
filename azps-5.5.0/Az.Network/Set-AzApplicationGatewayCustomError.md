---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 08447949836af59223572bac1b8fec54f3704d9d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193406"
---
# <span data-ttu-id="f05f3-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f05f3-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f05f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f05f3-102">SYNOPSIS</span></span>
<span data-ttu-id="f05f3-103">Aggiorna un errore personalizzato in un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f05f3-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="f05f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f05f3-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f05f3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f05f3-105">DESCRIPTION</span></span>
<span data-ttu-id="f05f3-106">Il cmdlet **Set-AzApplicationGatewayCustomError** aggiorna un errore personalizzato in un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f05f3-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="f05f3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f05f3-107">EXAMPLES</span></span>

### <span data-ttu-id="f05f3-108">Esempio 1: Aggiornamento dell'errore personalizzato in un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="f05f3-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="f05f3-109">Questo comando aggiorna l'errore personalizzato 502 del codice di stato http nel $appgw gateway applicazione e restituisce il gateway aggiornato.</span><span class="sxs-lookup"><span data-stu-id="f05f3-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="f05f3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f05f3-110">PARAMETERS</span></span>

### <span data-ttu-id="f05f3-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f05f3-111">-ApplicationGateway</span></span>
<span data-ttu-id="f05f3-112">Gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="f05f3-112">The Application Gateway</span></span>

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

### <span data-ttu-id="f05f3-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="f05f3-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="f05f3-114">URL della pagina di errore dell'errore del cliente del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="f05f3-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f05f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f05f3-115">-DefaultProfile</span></span>
<span data-ttu-id="f05f3-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f05f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f05f3-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="f05f3-117">-StatusCode</span></span>
<span data-ttu-id="f05f3-118">Codice di stato dell'errore del cliente del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="f05f3-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f05f3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f05f3-119">CommonParameters</span></span>
<span data-ttu-id="f05f3-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f05f3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f05f3-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f05f3-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f05f3-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="f05f3-122">INPUTS</span></span>

### <span data-ttu-id="f05f3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f05f3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f05f3-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f05f3-124">OUTPUTS</span></span>

### <span data-ttu-id="f05f3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f05f3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f05f3-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="f05f3-126">NOTES</span></span>

## <span data-ttu-id="f05f3-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f05f3-127">RELATED LINKS</span></span>

[<span data-ttu-id="f05f3-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f05f3-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f05f3-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f05f3-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f05f3-130">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f05f3-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f05f3-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f05f3-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
