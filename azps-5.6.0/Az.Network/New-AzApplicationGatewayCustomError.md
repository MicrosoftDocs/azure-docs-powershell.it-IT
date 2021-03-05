---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 377145933832c587691ed30db08754ef1e6f1f64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971918"
---
# <span data-ttu-id="9d912-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9d912-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="9d912-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d912-102">SYNOPSIS</span></span>
<span data-ttu-id="9d912-103">Crea un errore personalizzato con il codice di stato http e l'URL della pagina di errore personalizzata</span><span class="sxs-lookup"><span data-stu-id="9d912-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="9d912-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d912-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d912-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9d912-105">DESCRIPTION</span></span>
<span data-ttu-id="9d912-106">Il cmdlet **New-AzApplicationGatewayCustomError** crea un errore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="9d912-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="9d912-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d912-107">EXAMPLES</span></span>

### <span data-ttu-id="9d912-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9d912-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="9d912-109">Questo comando crea l'errore personalizzato del codice di stato http 403.</span><span class="sxs-lookup"><span data-stu-id="9d912-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="9d912-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d912-110">PARAMETERS</span></span>

### <span data-ttu-id="9d912-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="9d912-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="9d912-112">URL della pagina di errore dell'errore del cliente del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="9d912-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="9d912-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d912-113">-DefaultProfile</span></span>
<span data-ttu-id="9d912-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d912-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d912-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="9d912-115">-StatusCode</span></span>
<span data-ttu-id="9d912-116">Codice di stato dell'errore del cliente del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="9d912-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="9d912-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d912-117">CommonParameters</span></span>
<span data-ttu-id="9d912-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d912-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d912-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d912-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d912-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="9d912-120">INPUTS</span></span>

### <span data-ttu-id="9d912-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9d912-121">None</span></span>

## <span data-ttu-id="9d912-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d912-122">OUTPUTS</span></span>

### <span data-ttu-id="9d912-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9d912-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="9d912-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="9d912-124">NOTES</span></span>

## <span data-ttu-id="9d912-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d912-125">RELATED LINKS</span></span>

[<span data-ttu-id="9d912-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9d912-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9d912-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9d912-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9d912-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9d912-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9d912-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9d912-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
