---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: ac18c96353e247c721f95acf83e174e18a578b2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990987"
---
# <span data-ttu-id="a2fc1-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a2fc1-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="a2fc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="a2fc1-103">Rimuove una regola di routing delle richieste da un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="a2fc1-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="a2fc1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2fc1-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2fc1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a2fc1-105">DESCRIPTION</span></span>
<span data-ttu-id="a2fc1-106">Il cmdlet **Remove-AzApplicationGatewayRequestRoutingRule** rimuove una regola di routing delle richieste da un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a2fc1-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="a2fc1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2fc1-107">EXAMPLES</span></span>

### <span data-ttu-id="a2fc1-108">Esempio 1: Rimuovere una regola di routing delle richieste da un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="a2fc1-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="a2fc1-109">Il primo comando ottiene un gateway applicazione e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="a2fc1-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a2fc1-110">Il secondo comando rimuove la regola di routing delle richieste denominata Rule02 dal gateway applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a2fc1-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="a2fc1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2fc1-111">PARAMETERS</span></span>

### <span data-ttu-id="a2fc1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a2fc1-112">-ApplicationGateway</span></span>
<span data-ttu-id="a2fc1-113">Specifica il gateway applicazione da cui rimuovere una regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="a2fc1-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="a2fc1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2fc1-114">-DefaultProfile</span></span>
<span data-ttu-id="a2fc1-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a2fc1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2fc1-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a2fc1-116">-Name</span></span>
<span data-ttu-id="a2fc1-117">Specifica il nome della regola di routing delle richieste da cui questo cmdlet rimuove.</span><span class="sxs-lookup"><span data-stu-id="a2fc1-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="a2fc1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2fc1-118">CommonParameters</span></span>
<span data-ttu-id="a2fc1-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2fc1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2fc1-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2fc1-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2fc1-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="a2fc1-121">INPUTS</span></span>

### <span data-ttu-id="a2fc1-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a2fc1-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a2fc1-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2fc1-123">OUTPUTS</span></span>

### <span data-ttu-id="a2fc1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a2fc1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="a2fc1-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="a2fc1-125">NOTES</span></span>

## <span data-ttu-id="a2fc1-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2fc1-126">RELATED LINKS</span></span>

[<span data-ttu-id="a2fc1-127">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a2fc1-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="a2fc1-128">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a2fc1-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="a2fc1-129">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a2fc1-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="a2fc1-130">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a2fc1-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


