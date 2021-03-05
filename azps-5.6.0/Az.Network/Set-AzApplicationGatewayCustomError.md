---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 4c06b78062500ddb5c33353c00814a46e919bd8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987725"
---
# <span data-ttu-id="ebd92-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ebd92-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="ebd92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebd92-102">SYNOPSIS</span></span>
<span data-ttu-id="ebd92-103">Aggiorna un errore personalizzato in un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ebd92-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="ebd92-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ebd92-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebd92-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ebd92-105">DESCRIPTION</span></span>
<span data-ttu-id="ebd92-106">Il cmdlet **Set-AzApplicationGatewayCustomError** aggiorna un errore personalizzato in un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="ebd92-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="ebd92-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ebd92-107">EXAMPLES</span></span>

### <span data-ttu-id="ebd92-108">Esempio 1: Aggiornamento dell'errore personalizzato in un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="ebd92-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="ebd92-109">Questo comando aggiorna l'errore personalizzato 502 del codice di stato http nel $appgw gateway applicazione e restituisce il gateway aggiornato.</span><span class="sxs-lookup"><span data-stu-id="ebd92-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="ebd92-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebd92-110">PARAMETERS</span></span>

### <span data-ttu-id="ebd92-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ebd92-111">-ApplicationGateway</span></span>
<span data-ttu-id="ebd92-112">Gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="ebd92-112">The Application Gateway</span></span>

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

### <span data-ttu-id="ebd92-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="ebd92-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="ebd92-114">URL della pagina di errore dell'errore del cliente del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="ebd92-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="ebd92-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebd92-115">-DefaultProfile</span></span>
<span data-ttu-id="ebd92-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ebd92-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebd92-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="ebd92-117">-StatusCode</span></span>
<span data-ttu-id="ebd92-118">Codice di stato dell'errore del cliente del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="ebd92-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="ebd92-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebd92-119">CommonParameters</span></span>
<span data-ttu-id="ebd92-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebd92-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebd92-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebd92-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebd92-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="ebd92-122">INPUTS</span></span>

### <span data-ttu-id="ebd92-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ebd92-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ebd92-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ebd92-124">OUTPUTS</span></span>

### <span data-ttu-id="ebd92-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ebd92-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="ebd92-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="ebd92-126">NOTES</span></span>

## <span data-ttu-id="ebd92-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ebd92-127">RELATED LINKS</span></span>

[<span data-ttu-id="ebd92-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ebd92-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="ebd92-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ebd92-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="ebd92-130">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ebd92-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="ebd92-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ebd92-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
