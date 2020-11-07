---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: bd99eac2ecd36039685dde53730f250754318bc7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854322"
---
# <span data-ttu-id="a6e9a-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a6e9a-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="a6e9a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="a6e9a-103">Rimuove una regola di routing delle richieste da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a6e9a-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="a6e9a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6e9a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6e9a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6e9a-105">DESCRIPTION</span></span>
<span data-ttu-id="a6e9a-106">Il cmdlet **Remove-AzApplicationGatewayRequestRoutingRule** rimuove una regola di routing delle richieste da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e9a-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="a6e9a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6e9a-107">EXAMPLES</span></span>

### <span data-ttu-id="a6e9a-108">Esempio 1: rimuovere una regola di routing delle richieste da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="a6e9a-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="a6e9a-109">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a6e9a-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a6e9a-110">Il secondo comando rimuove la regola di routing delle richieste denominata Rule02 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a6e9a-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="a6e9a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6e9a-111">PARAMETERS</span></span>

### <span data-ttu-id="a6e9a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a6e9a-112">-ApplicationGateway</span></span>
<span data-ttu-id="a6e9a-113">Specifica il gateway dell'applicazione da cui rimuovere una regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="a6e9a-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="a6e9a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6e9a-114">-DefaultProfile</span></span>
<span data-ttu-id="a6e9a-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e9a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6e9a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6e9a-116">-Name</span></span>
<span data-ttu-id="a6e9a-117">Specifica il nome della regola di routing delle richieste per cui viene rimosso questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6e9a-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="a6e9a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6e9a-118">CommonParameters</span></span>
<span data-ttu-id="a6e9a-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6e9a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6e9a-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6e9a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6e9a-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6e9a-121">INPUTS</span></span>

### <span data-ttu-id="a6e9a-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a6e9a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a6e9a-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6e9a-123">OUTPUTS</span></span>

### <span data-ttu-id="a6e9a-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a6e9a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="a6e9a-125">Note</span><span class="sxs-lookup"><span data-stu-id="a6e9a-125">NOTES</span></span>

## <span data-ttu-id="a6e9a-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6e9a-126">RELATED LINKS</span></span>

[<span data-ttu-id="a6e9a-127">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a6e9a-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="a6e9a-128">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a6e9a-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="a6e9a-129">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a6e9a-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="a6e9a-130">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a6e9a-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


