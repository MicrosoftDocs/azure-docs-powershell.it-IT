---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: b56c358a208683e513844e36e561efa9e76cbede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510924"
---
# <span data-ttu-id="b7edf-101">Add-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b7edf-101">Add-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="b7edf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7edf-102">SYNOPSIS</span></span>
<span data-ttu-id="b7edf-103">Aggiunge un errore personalizzato a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7edf-103">Adds a custom error to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7edf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7edf-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7edf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7edf-105">DESCRIPTION</span></span>
<span data-ttu-id="b7edf-106">Il cmdlet **Add-AzureRmApplicationGatewayCustomError** aggiunge un errore personalizzato a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7edf-106">The **Add-AzureRmApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="b7edf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7edf-107">EXAMPLES</span></span>

### <span data-ttu-id="b7edf-108">Esempio 1: aggiunge un errore personalizzato al livello del gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="b7edf-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="b7edf-109">Questo comando aggiunge un errore personalizzato del codice di stato HTTP 502 al gateway dell'applicazione $appgw e restituisce il gateway aggiornato.</span><span class="sxs-lookup"><span data-stu-id="b7edf-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="b7edf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7edf-110">PARAMETERS</span></span>

### <span data-ttu-id="b7edf-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7edf-111">-ApplicationGateway</span></span>
<span data-ttu-id="b7edf-112">Gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="b7edf-112">The Application Gateway</span></span>

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

### <span data-ttu-id="b7edf-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="b7edf-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="b7edf-114">URL della pagina di errore dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7edf-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="b7edf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7edf-115">-DefaultProfile</span></span>
<span data-ttu-id="b7edf-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7edf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7edf-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="b7edf-117">-StatusCode</span></span>
<span data-ttu-id="b7edf-118">Codice di stato dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7edf-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="b7edf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7edf-119">CommonParameters</span></span>
<span data-ttu-id="b7edf-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7edf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7edf-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7edf-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7edf-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7edf-122">INPUTS</span></span>

### <span data-ttu-id="b7edf-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7edf-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b7edf-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7edf-124">OUTPUTS</span></span>

### <span data-ttu-id="b7edf-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7edf-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b7edf-126">Note</span><span class="sxs-lookup"><span data-stu-id="b7edf-126">NOTES</span></span>

## <span data-ttu-id="b7edf-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7edf-127">RELATED LINKS</span></span>
