---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 23cb65073f25f65a4e09f3b4a28891cff4e49c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687817"
---
# <span data-ttu-id="bcd1d-101">Add-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="bcd1d-101">Add-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="bcd1d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bcd1d-102">SYNOPSIS</span></span>
<span data-ttu-id="bcd1d-103">Aggiunge un errore personalizzato a un listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bcd1d-103">Adds a custom error to a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcd1d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcd1d-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bcd1d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcd1d-105">DESCRIPTION</span></span>
<span data-ttu-id="bcd1d-106">Il cmdlet **Add-AzureRmApplicationGatewayCustomError** aggiunge un errore personalizzato a un listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bcd1d-106">The **Add-AzureRmApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="bcd1d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcd1d-107">EXAMPLES</span></span>

### <span data-ttu-id="bcd1d-108">Esempio 1: aggiunge un errore personalizzato al livello del listener http</span><span class="sxs-lookup"><span data-stu-id="bcd1d-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="bcd1d-109">Questo comando aggiunge un errore personalizzato del codice di stato HTTP 502 al listener HTTP $listener 01 e restituisce il listener aggiornato.</span><span class="sxs-lookup"><span data-stu-id="bcd1d-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="bcd1d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bcd1d-110">PARAMETERS</span></span>

### <span data-ttu-id="bcd1d-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="bcd1d-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="bcd1d-112">URL della pagina di errore dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bcd1d-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="bcd1d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcd1d-113">-DefaultProfile</span></span>
<span data-ttu-id="bcd1d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bcd1d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcd1d-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="bcd1d-115">-HttpListener</span></span>
<span data-ttu-id="bcd1d-116">Listener HTTP del gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="bcd1d-116">The Application Gateway Http Listener</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcd1d-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="bcd1d-117">-StatusCode</span></span>
<span data-ttu-id="bcd1d-118">Codice di stato dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bcd1d-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="bcd1d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcd1d-119">CommonParameters</span></span>
<span data-ttu-id="bcd1d-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcd1d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bcd1d-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcd1d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcd1d-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bcd1d-122">INPUTS</span></span>

### <span data-ttu-id="bcd1d-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bcd1d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="bcd1d-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcd1d-124">OUTPUTS</span></span>

### <span data-ttu-id="bcd1d-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bcd1d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="bcd1d-126">Note</span><span class="sxs-lookup"><span data-stu-id="bcd1d-126">NOTES</span></span>

## <span data-ttu-id="bcd1d-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcd1d-127">RELATED LINKS</span></span>
