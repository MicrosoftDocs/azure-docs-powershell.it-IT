---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: a59646c6214b3c4372eef9def61f67fe4a5bd912
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678020"
---
# <span data-ttu-id="7f3bc-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7f3bc-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="7f3bc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f3bc-102">SYNOPSIS</span></span>
<span data-ttu-id="7f3bc-103">Aggiorna un errore personalizzato in un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="7f3bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f3bc-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f3bc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f3bc-105">DESCRIPTION</span></span>
<span data-ttu-id="7f3bc-106">Il cmdlet **set-AzApplicationGatewayCustomError** aggiorna un errore personalizzato in un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="7f3bc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f3bc-107">EXAMPLES</span></span>

### <span data-ttu-id="7f3bc-108">Esempio 1: aggiorna l'errore personalizzato in un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="7f3bc-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="7f3bc-109">Questo comando Aggiorna l'errore personalizzato del codice di stato HTTP 502 nel gateway dell'applicazione $appgw e restituisce il gateway aggiornato.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="7f3bc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f3bc-110">PARAMETERS</span></span>

### <span data-ttu-id="7f3bc-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f3bc-111">-ApplicationGateway</span></span>
<span data-ttu-id="7f3bc-112">Gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="7f3bc-112">The Application Gateway</span></span>

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

### <span data-ttu-id="7f3bc-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="7f3bc-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="7f3bc-114">URL della pagina di errore dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="7f3bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f3bc-115">-DefaultProfile</span></span>
<span data-ttu-id="7f3bc-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f3bc-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="7f3bc-117">-StatusCode</span></span>
<span data-ttu-id="7f3bc-118">Codice di stato dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="7f3bc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f3bc-119">CommonParameters</span></span>
<span data-ttu-id="7f3bc-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f3bc-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f3bc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f3bc-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f3bc-122">INPUTS</span></span>

### <span data-ttu-id="7f3bc-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f3bc-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7f3bc-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f3bc-124">OUTPUTS</span></span>

### <span data-ttu-id="7f3bc-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7f3bc-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="7f3bc-126">Note</span><span class="sxs-lookup"><span data-stu-id="7f3bc-126">NOTES</span></span>

## <span data-ttu-id="7f3bc-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f3bc-127">RELATED LINKS</span></span>

[<span data-ttu-id="7f3bc-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7f3bc-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="7f3bc-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7f3bc-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="7f3bc-130">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7f3bc-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="7f3bc-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7f3bc-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
