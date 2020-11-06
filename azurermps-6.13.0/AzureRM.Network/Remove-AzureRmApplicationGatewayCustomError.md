---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: cc1f6b487d0faf58999a0326a77e01bea74d8c91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510879"
---
# <span data-ttu-id="95065-101">Remove-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="95065-101">Remove-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="95065-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="95065-102">SYNOPSIS</span></span>
<span data-ttu-id="95065-103">Rimuove un errore personalizzato da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="95065-103">Removes a custom error from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95065-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95065-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95065-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95065-105">DESCRIPTION</span></span>
<span data-ttu-id="95065-106">Il cmdlet **Remove-AzureRmApplicationGatewayCustomError** rimuove un errore personalizzato da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="95065-106">The **Remove-AzureRmApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="95065-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95065-107">EXAMPLES</span></span>

### <span data-ttu-id="95065-108">Esempio 1: rimuove l'errore personalizzato da un gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="95065-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="95065-109">Questo comando rimuove l'errore personalizzato del codice di stato HTTP 502 dal gateway dell'applicazione $appgw e restituisce il gateway aggiornato.</span><span class="sxs-lookup"><span data-stu-id="95065-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="95065-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="95065-110">PARAMETERS</span></span>

### <span data-ttu-id="95065-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="95065-111">-ApplicationGateway</span></span>
<span data-ttu-id="95065-112">Gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="95065-112">The Application Gateway</span></span>

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

### <span data-ttu-id="95065-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95065-113">-DefaultProfile</span></span>
<span data-ttu-id="95065-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="95065-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95065-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="95065-115">-StatusCode</span></span>
<span data-ttu-id="95065-116">Codice di stato dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="95065-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="95065-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95065-117">CommonParameters</span></span>
<span data-ttu-id="95065-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95065-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95065-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95065-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95065-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="95065-120">INPUTS</span></span>

### <span data-ttu-id="95065-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="95065-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="95065-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95065-122">OUTPUTS</span></span>

### <span data-ttu-id="95065-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="95065-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="95065-124">Note</span><span class="sxs-lookup"><span data-stu-id="95065-124">NOTES</span></span>

## <span data-ttu-id="95065-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95065-125">RELATED LINKS</span></span>
