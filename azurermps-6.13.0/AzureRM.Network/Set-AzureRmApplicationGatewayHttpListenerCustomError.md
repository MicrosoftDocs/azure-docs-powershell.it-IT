---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: cb54299a1d3c06f9416ed574588a1bc77d9993a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685426"
---
# <span data-ttu-id="006be-101">Set-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="006be-101">Set-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="006be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="006be-102">SYNOPSIS</span></span>
<span data-ttu-id="006be-103">Aggiorna un errore personalizzato in un listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="006be-103">Updates a custom error in a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="006be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="006be-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="006be-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="006be-105">DESCRIPTION</span></span>
<span data-ttu-id="006be-106">Il cmdlet **set-AzureRmApplicationGatewayCustomError** aggiorna un errore personalizzato in un listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="006be-106">The **Set-AzureRmApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="006be-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="006be-107">EXAMPLES</span></span>

### <span data-ttu-id="006be-108">Esempio 1: aggiorna un errore personalizzato da un listener http</span><span class="sxs-lookup"><span data-stu-id="006be-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="006be-109">Questo comando Aggiorna l'errore personalizzato del codice di stato HTTP 502 nel listener HTTP $listener 01 e restituisce il listener aggiornato.</span><span class="sxs-lookup"><span data-stu-id="006be-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="006be-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="006be-110">PARAMETERS</span></span>

### <span data-ttu-id="006be-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="006be-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="006be-112">URL della pagina di errore dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="006be-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="006be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="006be-113">-DefaultProfile</span></span>
<span data-ttu-id="006be-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="006be-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="006be-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="006be-115">-HttpListener</span></span>
<span data-ttu-id="006be-116">Listener HTTP del gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="006be-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="006be-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="006be-117">-StatusCode</span></span>
<span data-ttu-id="006be-118">Codice di stato dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="006be-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="006be-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="006be-119">CommonParameters</span></span>
<span data-ttu-id="006be-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="006be-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="006be-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="006be-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="006be-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="006be-122">INPUTS</span></span>

### <span data-ttu-id="006be-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="006be-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="006be-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="006be-124">OUTPUTS</span></span>

### <span data-ttu-id="006be-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="006be-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="006be-126">Note</span><span class="sxs-lookup"><span data-stu-id="006be-126">NOTES</span></span>

## <span data-ttu-id="006be-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="006be-127">RELATED LINKS</span></span>
