---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 81b750188a85add491e519c023c765f302e31dea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018318"
---
# <span data-ttu-id="ac4f2-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ac4f2-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="ac4f2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac4f2-102">SYNOPSIS</span></span>
<span data-ttu-id="ac4f2-103">Rimuove un listener HTTP da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ac4f2-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="ac4f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac4f2-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac4f2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac4f2-105">DESCRIPTION</span></span>
<span data-ttu-id="ac4f2-106">Il cmdlet **Remove-AzApplicationGatewayHttpListener** rimuove un listener HTTP da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="ac4f2-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="ac4f2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac4f2-107">EXAMPLES</span></span>

### <span data-ttu-id="ac4f2-108">Esempio 1: rimuovere un listener HTTP gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="ac4f2-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="ac4f2-109">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ac4f2-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ac4f2-110">Il secondo comando rimuove il listener HTTP denominato Listener02 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ac4f2-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="ac4f2-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac4f2-111">PARAMETERS</span></span>

### <span data-ttu-id="ac4f2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac4f2-112">-ApplicationGateway</span></span>
<span data-ttu-id="ac4f2-113">Specifica il gateway dell'applicazione da cui rimuovere un listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="ac4f2-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="ac4f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac4f2-114">-DefaultProfile</span></span>
<span data-ttu-id="ac4f2-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac4f2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac4f2-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac4f2-116">-Name</span></span>
<span data-ttu-id="ac4f2-117">Specifica il nome del listener HTTP rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac4f2-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ac4f2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac4f2-118">CommonParameters</span></span>
<span data-ttu-id="ac4f2-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac4f2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac4f2-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac4f2-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac4f2-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac4f2-121">INPUTS</span></span>

### <span data-ttu-id="ac4f2-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac4f2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ac4f2-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac4f2-123">OUTPUTS</span></span>

### <span data-ttu-id="ac4f2-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ac4f2-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="ac4f2-125">Note</span><span class="sxs-lookup"><span data-stu-id="ac4f2-125">NOTES</span></span>

## <span data-ttu-id="ac4f2-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac4f2-126">RELATED LINKS</span></span>

[<span data-ttu-id="ac4f2-127">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ac4f2-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ac4f2-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ac4f2-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ac4f2-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ac4f2-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ac4f2-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ac4f2-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


