---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: b2f748bca68bff772026237f3bb6205ca6bc1923
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687806"
---
# <span data-ttu-id="05405-101">Get-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="05405-101">Get-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="05405-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05405-102">SYNOPSIS</span></span>
<span data-ttu-id="05405-103">Ottiene gli errori personalizzati da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="05405-103">Gets custom error(s) from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05405-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05405-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05405-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05405-105">DESCRIPTION</span></span>
<span data-ttu-id="05405-106">Il cmdlet **Get-AzureRmApplicationGatewayCustomError** ottiene gli errori personalizzati da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="05405-106">The **Get-AzureRmApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="05405-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05405-107">EXAMPLES</span></span>

### <span data-ttu-id="05405-108">Esempio 1: ottiene un errore personalizzato in un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="05405-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="05405-109">Questo comando ottiene e restituisce l'errore personalizzato del codice di stato HTTP 502 dal gateway dell'applicazione $appgw.</span><span class="sxs-lookup"><span data-stu-id="05405-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="05405-110">Esempio 2: Ottiene l'elenco di tutti gli errori personalizzati in un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="05405-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="05405-111">Questo comando ottiene e restituisce l'elenco di tutti gli errori personalizzati dal gateway dell'applicazione $appgw.</span><span class="sxs-lookup"><span data-stu-id="05405-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="05405-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05405-112">PARAMETERS</span></span>

### <span data-ttu-id="05405-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="05405-113">-ApplicationGateway</span></span>
<span data-ttu-id="05405-114">Gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="05405-114">The Application Gateway</span></span>

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

### <span data-ttu-id="05405-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05405-115">-DefaultProfile</span></span>
<span data-ttu-id="05405-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05405-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05405-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="05405-117">-StatusCode</span></span>
<span data-ttu-id="05405-118">Codice di stato dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="05405-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05405-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05405-119">CommonParameters</span></span>
<span data-ttu-id="05405-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05405-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05405-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05405-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05405-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05405-122">INPUTS</span></span>

### <span data-ttu-id="05405-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="05405-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="05405-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05405-124">OUTPUTS</span></span>

### <span data-ttu-id="05405-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="05405-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="05405-126">Note</span><span class="sxs-lookup"><span data-stu-id="05405-126">NOTES</span></span>

## <span data-ttu-id="05405-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05405-127">RELATED LINKS</span></span>
