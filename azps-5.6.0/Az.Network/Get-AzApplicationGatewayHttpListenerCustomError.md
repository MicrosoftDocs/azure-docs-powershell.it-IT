---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 828b5e02b73a454a2b2023c0f084d4e1c90074fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001214"
---
# <span data-ttu-id="26707-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="26707-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="26707-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26707-102">SYNOPSIS</span></span>
<span data-ttu-id="26707-103">Recupera gli errori personalizzati da un listener http di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="26707-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="26707-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26707-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26707-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="26707-105">DESCRIPTION</span></span>
<span data-ttu-id="26707-106">Il cmdlet **Get-AzApplicationGatewayCustomError** ottiene errori personalizzati da un listener http di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="26707-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="26707-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26707-107">EXAMPLES</span></span>

### <span data-ttu-id="26707-108">Esempio 1: ottiene un errore personalizzato in un listener http</span><span class="sxs-lookup"><span data-stu-id="26707-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="26707-109">Questo comando recupera e restituisce l'errore personalizzato del codice di stato http 502 dall'$listener 01 http.</span><span class="sxs-lookup"><span data-stu-id="26707-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="26707-110">Esempio 2: ottiene l'elenco di tutti gli errori personalizzati in un listener http</span><span class="sxs-lookup"><span data-stu-id="26707-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="26707-111">Questo comando ottiene e restituisce l'elenco di tutti gli errori personalizzati dal listener http $listener 01.</span><span class="sxs-lookup"><span data-stu-id="26707-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="26707-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26707-112">PARAMETERS</span></span>

### <span data-ttu-id="26707-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26707-113">-DefaultProfile</span></span>
<span data-ttu-id="26707-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26707-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26707-115">-HttpDir</span><span class="sxs-lookup"><span data-stu-id="26707-115">-HttpListener</span></span>
<span data-ttu-id="26707-116">Listener Http del Gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="26707-116">The Application Gateway Http Listener</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26707-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="26707-117">-StatusCode</span></span>
<span data-ttu-id="26707-118">Codice di stato dell'errore del cliente del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="26707-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="26707-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26707-119">CommonParameters</span></span>
<span data-ttu-id="26707-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26707-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26707-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="26707-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26707-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="26707-122">INPUTS</span></span>

### <span data-ttu-id="26707-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpHttpApplication</span><span class="sxs-lookup"><span data-stu-id="26707-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="26707-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26707-124">OUTPUTS</span></span>

### <span data-ttu-id="26707-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="26707-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="26707-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="26707-126">NOTES</span></span>

## <span data-ttu-id="26707-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26707-127">RELATED LINKS</span></span>

[<span data-ttu-id="26707-128">Add-AzApplicationGatewayHttpCustomError</span><span class="sxs-lookup"><span data-stu-id="26707-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="26707-129">Remove-AzApplicationGatewayHttpCustomError</span><span class="sxs-lookup"><span data-stu-id="26707-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="26707-130">Set-AzApplicationGatewayHttpCustomError</span><span class="sxs-lookup"><span data-stu-id="26707-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
