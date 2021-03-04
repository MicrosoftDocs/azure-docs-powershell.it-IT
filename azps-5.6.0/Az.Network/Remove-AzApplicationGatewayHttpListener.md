---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 46cf3a786642262c1f6d0df0e2c1fd770d61ec6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959486"
---
# <span data-ttu-id="5d79f-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5d79f-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="5d79f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d79f-102">SYNOPSIS</span></span>
<span data-ttu-id="5d79f-103">Rimuove un listener HTTP da un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="5d79f-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="5d79f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d79f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d79f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5d79f-105">DESCRIPTION</span></span>
<span data-ttu-id="5d79f-106">Il cmdlet **Remove-AzApplicationGatewayHttpHttp Listener** rimuove un listener HTTP da un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5d79f-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="5d79f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d79f-107">EXAMPLES</span></span>

### <span data-ttu-id="5d79f-108">Esempio 1: Rimuovere un listener HTTP del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="5d79f-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="5d79f-109">Il primo comando ottiene un gateway applicazione e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="5d79f-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5d79f-110">Il secondo comando rimuove il listener HTTP denominato Listener02 dal gateway di applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="5d79f-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="5d79f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d79f-111">PARAMETERS</span></span>

### <span data-ttu-id="5d79f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5d79f-112">-ApplicationGateway</span></span>
<span data-ttu-id="5d79f-113">Specifica il gateway applicazione da cui rimuovere un listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="5d79f-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="5d79f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d79f-114">-DefaultProfile</span></span>
<span data-ttu-id="5d79f-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d79f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d79f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5d79f-116">-Name</span></span>
<span data-ttu-id="5d79f-117">Specifica il nome del listener HTTP rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d79f-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5d79f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d79f-118">CommonParameters</span></span>
<span data-ttu-id="5d79f-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d79f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d79f-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d79f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d79f-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="5d79f-121">INPUTS</span></span>

### <span data-ttu-id="5d79f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5d79f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5d79f-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d79f-123">OUTPUTS</span></span>

### <span data-ttu-id="5d79f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpHttpApplication</span><span class="sxs-lookup"><span data-stu-id="5d79f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="5d79f-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="5d79f-125">NOTES</span></span>

## <span data-ttu-id="5d79f-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d79f-126">RELATED LINKS</span></span>

[<span data-ttu-id="5d79f-127">Add-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="5d79f-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5d79f-128">Get-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="5d79f-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5d79f-129">New-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="5d79f-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5d79f-130">Set-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="5d79f-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


