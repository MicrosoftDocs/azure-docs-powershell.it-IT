---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 08447949836af59223572bac1b8fec54f3704d9d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201981"
---
# <span data-ttu-id="243d4-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="243d4-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="243d4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="243d4-102">SYNOPSIS</span></span>
<span data-ttu-id="243d4-103">Aggiorna un errore personalizzato in un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="243d4-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="243d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="243d4-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="243d4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="243d4-105">DESCRIPTION</span></span>
<span data-ttu-id="243d4-106">Il cmdlet **set-AzApplicationGatewayCustomError** aggiorna un errore personalizzato in un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="243d4-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="243d4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="243d4-107">EXAMPLES</span></span>

### <span data-ttu-id="243d4-108">Esempio 1: aggiorna l'errore personalizzato in un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="243d4-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="243d4-109">Questo comando Aggiorna l'errore personalizzato del codice di stato HTTP 502 nel gateway dell'applicazione $appgw e restituisce il gateway aggiornato.</span><span class="sxs-lookup"><span data-stu-id="243d4-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="243d4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="243d4-110">PARAMETERS</span></span>

### <span data-ttu-id="243d4-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="243d4-111">-ApplicationGateway</span></span>
<span data-ttu-id="243d4-112">Gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="243d4-112">The Application Gateway</span></span>

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

### <span data-ttu-id="243d4-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="243d4-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="243d4-114">URL della pagina di errore dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="243d4-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="243d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="243d4-115">-DefaultProfile</span></span>
<span data-ttu-id="243d4-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="243d4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="243d4-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="243d4-117">-StatusCode</span></span>
<span data-ttu-id="243d4-118">Codice di stato dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="243d4-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="243d4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="243d4-119">CommonParameters</span></span>
<span data-ttu-id="243d4-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="243d4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="243d4-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="243d4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="243d4-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="243d4-122">INPUTS</span></span>

### <span data-ttu-id="243d4-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="243d4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="243d4-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="243d4-124">OUTPUTS</span></span>

### <span data-ttu-id="243d4-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="243d4-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="243d4-126">Note</span><span class="sxs-lookup"><span data-stu-id="243d4-126">NOTES</span></span>

## <span data-ttu-id="243d4-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="243d4-127">RELATED LINKS</span></span>

[<span data-ttu-id="243d4-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="243d4-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="243d4-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="243d4-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="243d4-130">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="243d4-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="243d4-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="243d4-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
