---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: 9e05684f40223711db7a8a6aaaf1cfb684efced4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520167"
---
# <span data-ttu-id="7c8ba-101">New-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7c8ba-101">New-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="7c8ba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c8ba-102">SYNOPSIS</span></span>
<span data-ttu-id="7c8ba-103">Crea un errore personalizzato con il codice di stato HTTP e l'URL della pagina di errore personalizzato</span><span class="sxs-lookup"><span data-stu-id="7c8ba-103">Creates a custom error with http status code and custom error page url</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c8ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c8ba-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c8ba-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c8ba-105">DESCRIPTION</span></span>
<span data-ttu-id="7c8ba-106">Il cmdlet **New-AzureRmApplicationGatewayCustomError** crea un errore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="7c8ba-106">The **New-AzureRmApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="7c8ba-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c8ba-107">EXAMPLES</span></span>

### <span data-ttu-id="7c8ba-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c8ba-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzureRmApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="7c8ba-109">Questo comando crea l'errore personalizzato del codice di stato HTTP 403.</span><span class="sxs-lookup"><span data-stu-id="7c8ba-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="7c8ba-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c8ba-110">PARAMETERS</span></span>

### <span data-ttu-id="7c8ba-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="7c8ba-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="7c8ba-112">URL della pagina di errore dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7c8ba-112">Error page URL of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8ba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c8ba-113">-DefaultProfile</span></span>
<span data-ttu-id="7c8ba-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c8ba-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8ba-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="7c8ba-115">-StatusCode</span></span>
<span data-ttu-id="7c8ba-116">Codice di stato dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7c8ba-116">Status code of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8ba-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c8ba-117">CommonParameters</span></span>
<span data-ttu-id="7c8ba-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c8ba-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7c8ba-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c8ba-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c8ba-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c8ba-120">INPUTS</span></span>

### <span data-ttu-id="7c8ba-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7c8ba-121">None</span></span>

## <span data-ttu-id="7c8ba-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c8ba-122">OUTPUTS</span></span>

### <span data-ttu-id="7c8ba-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7c8ba-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="7c8ba-124">Note</span><span class="sxs-lookup"><span data-stu-id="7c8ba-124">NOTES</span></span>

## <span data-ttu-id="7c8ba-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c8ba-125">RELATED LINKS</span></span>
