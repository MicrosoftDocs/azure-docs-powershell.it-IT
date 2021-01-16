---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 34f92bfa7566679c4cee9f7a4281ac15c55676b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326292"
---
# <span data-ttu-id="26558-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="26558-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="26558-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26558-102">SYNOPSIS</span></span>
<span data-ttu-id="26558-103">Ottiene gli errori personalizzati da un listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="26558-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="26558-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26558-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26558-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26558-105">DESCRIPTION</span></span>
<span data-ttu-id="26558-106">Il cmdlet **Get-AzApplicationGatewayCustomError** ottiene gli errori personalizzati da un listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="26558-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="26558-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26558-107">EXAMPLES</span></span>

### <span data-ttu-id="26558-108">Esempio 1: ottiene un errore personalizzato in un listener http</span><span class="sxs-lookup"><span data-stu-id="26558-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="26558-109">Questo comando ottiene e restituisce l'errore personalizzato del codice di stato HTTP 502 dal listener HTTP $listener 01.</span><span class="sxs-lookup"><span data-stu-id="26558-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="26558-110">Esempio 2: Ottiene l'elenco di tutti gli errori personalizzati in un listener http</span><span class="sxs-lookup"><span data-stu-id="26558-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="26558-111">Questo comando ottiene e restituisce l'elenco di tutti gli errori personalizzati dal listener HTTP $listener 01.</span><span class="sxs-lookup"><span data-stu-id="26558-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="26558-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26558-112">PARAMETERS</span></span>

### <span data-ttu-id="26558-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26558-113">-DefaultProfile</span></span>
<span data-ttu-id="26558-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26558-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26558-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="26558-115">-HttpListener</span></span>
<span data-ttu-id="26558-116">Listener HTTP del gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="26558-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="26558-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="26558-117">-StatusCode</span></span>
<span data-ttu-id="26558-118">Codice di stato dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="26558-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="26558-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26558-119">CommonParameters</span></span>
<span data-ttu-id="26558-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26558-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26558-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26558-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26558-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26558-122">INPUTS</span></span>

### <span data-ttu-id="26558-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="26558-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="26558-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26558-124">OUTPUTS</span></span>

### <span data-ttu-id="26558-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="26558-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="26558-126">Note</span><span class="sxs-lookup"><span data-stu-id="26558-126">NOTES</span></span>

## <span data-ttu-id="26558-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26558-127">RELATED LINKS</span></span>

[<span data-ttu-id="26558-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="26558-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="26558-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="26558-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="26558-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="26558-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
