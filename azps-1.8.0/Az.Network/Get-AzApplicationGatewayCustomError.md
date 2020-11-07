---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: fbf10b3cfc323a25a7d7a63dc047a4b24141c5d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678619"
---
# <span data-ttu-id="9c68b-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9c68b-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="9c68b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9c68b-102">SYNOPSIS</span></span>
<span data-ttu-id="9c68b-103">Ottiene gli errori personalizzati da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9c68b-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="9c68b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c68b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c68b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c68b-105">DESCRIPTION</span></span>
<span data-ttu-id="9c68b-106">Il cmdlet **Get-AzApplicationGatewayCustomError** ottiene gli errori personalizzati da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9c68b-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="9c68b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c68b-107">EXAMPLES</span></span>

### <span data-ttu-id="9c68b-108">Esempio 1: ottiene un errore personalizzato in un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="9c68b-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="9c68b-109">Questo comando ottiene e restituisce l'errore personalizzato del codice di stato HTTP 502 dal gateway dell'applicazione $appgw.</span><span class="sxs-lookup"><span data-stu-id="9c68b-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="9c68b-110">Esempio 2: Ottiene l'elenco di tutti gli errori personalizzati in un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="9c68b-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="9c68b-111">Questo comando ottiene e restituisce l'elenco di tutti gli errori personalizzati dal gateway dell'applicazione $appgw.</span><span class="sxs-lookup"><span data-stu-id="9c68b-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="9c68b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9c68b-112">PARAMETERS</span></span>

### <span data-ttu-id="9c68b-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c68b-113">-ApplicationGateway</span></span>
<span data-ttu-id="9c68b-114">Gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="9c68b-114">The Application Gateway</span></span>

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

### <span data-ttu-id="9c68b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c68b-115">-DefaultProfile</span></span>
<span data-ttu-id="9c68b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c68b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c68b-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="9c68b-117">-StatusCode</span></span>
<span data-ttu-id="9c68b-118">Codice di stato dell'errore del cliente del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9c68b-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="9c68b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c68b-119">CommonParameters</span></span>
<span data-ttu-id="9c68b-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c68b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c68b-121">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c68b-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c68b-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9c68b-122">INPUTS</span></span>

### <span data-ttu-id="9c68b-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c68b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9c68b-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c68b-124">OUTPUTS</span></span>

### <span data-ttu-id="9c68b-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9c68b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="9c68b-126">Note</span><span class="sxs-lookup"><span data-stu-id="9c68b-126">NOTES</span></span>

## <span data-ttu-id="9c68b-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c68b-127">RELATED LINKS</span></span>

[<span data-ttu-id="9c68b-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9c68b-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9c68b-129">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9c68b-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9c68b-130">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9c68b-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9c68b-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9c68b-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
