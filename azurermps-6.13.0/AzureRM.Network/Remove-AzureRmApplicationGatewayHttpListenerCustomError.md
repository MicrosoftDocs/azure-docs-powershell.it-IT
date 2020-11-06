---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d0f26991498d8efc88eaacf9d01ed7e95d92e2cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510871"
---
# <span data-ttu-id="21838-101">Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="21838-101">Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="21838-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="21838-102">SYNOPSIS</span></span>
<span data-ttu-id="21838-103">Rimuove un errore personalizzato da un listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="21838-103">Removes a custom error from a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21838-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21838-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21838-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21838-105">DESCRIPTION</span></span>
<span data-ttu-id="21838-106">Il cmdlet **Remove-AzureRmApplicationGatewayCustomError** rimuove un errore personalizzato da un listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="21838-106">The **Remove-AzureRmApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="21838-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21838-107">EXAMPLES</span></span>

### <span data-ttu-id="21838-108">Esempio 1: rimuove l'errore personalizzato da un listener http</span><span class="sxs-lookup"><span data-stu-id="21838-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="21838-109">Questo comando rimuove l'errore personalizzato del codice di stato HTTP 502 dal listener HTTP $listener 01 e restituisce il listener aggiornato.</span><span class="sxs-lookup"><span data-stu-id="21838-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="21838-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="21838-110">PARAMETERS</span></span>

### <span data-ttu-id="21838-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21838-111">-DefaultProfile</span></span>
<span data-ttu-id="21838-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="21838-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21838-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="21838-113">-HttpListener</span></span>
<span data-ttu-id="21838-114">Listener HTTP del gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="21838-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="21838-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="21838-115">-StatusCode</span></span>
<span data-ttu-id="21838-116">Codice di stato dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="21838-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="21838-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21838-117">CommonParameters</span></span>
<span data-ttu-id="21838-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21838-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="21838-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21838-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21838-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="21838-120">INPUTS</span></span>

### <span data-ttu-id="21838-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="21838-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="21838-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21838-122">OUTPUTS</span></span>

### <span data-ttu-id="21838-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="21838-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="21838-124">Note</span><span class="sxs-lookup"><span data-stu-id="21838-124">NOTES</span></span>

## <span data-ttu-id="21838-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21838-125">RELATED LINKS</span></span>
