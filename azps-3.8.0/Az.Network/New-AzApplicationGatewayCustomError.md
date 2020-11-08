---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 162e9a5cd869b6ea50e6d72dc7041ab14dc9a8e6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022793"
---
# <span data-ttu-id="6be06-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6be06-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="6be06-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6be06-102">SYNOPSIS</span></span>
<span data-ttu-id="6be06-103">Crea un errore personalizzato con il codice di stato HTTP e l'URL della pagina di errore personalizzato</span><span class="sxs-lookup"><span data-stu-id="6be06-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="6be06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6be06-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6be06-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6be06-105">DESCRIPTION</span></span>
<span data-ttu-id="6be06-106">Il cmdlet **New-AzApplicationGatewayCustomError** crea un errore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="6be06-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="6be06-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6be06-107">EXAMPLES</span></span>

### <span data-ttu-id="6be06-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6be06-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="6be06-109">Questo comando crea l'errore personalizzato del codice di stato HTTP 403.</span><span class="sxs-lookup"><span data-stu-id="6be06-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="6be06-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6be06-110">PARAMETERS</span></span>

### <span data-ttu-id="6be06-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="6be06-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="6be06-112">URL della pagina di errore dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6be06-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="6be06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6be06-113">-DefaultProfile</span></span>
<span data-ttu-id="6be06-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6be06-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6be06-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="6be06-115">-StatusCode</span></span>
<span data-ttu-id="6be06-116">Codice di stato dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6be06-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="6be06-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6be06-117">CommonParameters</span></span>
<span data-ttu-id="6be06-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6be06-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6be06-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6be06-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6be06-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6be06-120">INPUTS</span></span>

### <span data-ttu-id="6be06-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6be06-121">None</span></span>

## <span data-ttu-id="6be06-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6be06-122">OUTPUTS</span></span>

### <span data-ttu-id="6be06-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6be06-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="6be06-124">Note</span><span class="sxs-lookup"><span data-stu-id="6be06-124">NOTES</span></span>

## <span data-ttu-id="6be06-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6be06-125">RELATED LINKS</span></span>

[<span data-ttu-id="6be06-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6be06-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="6be06-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6be06-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="6be06-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6be06-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="6be06-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6be06-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
