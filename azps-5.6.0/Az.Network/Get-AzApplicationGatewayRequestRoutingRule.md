---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 04c7ef7dd041ce26802f23117edab79353816283
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994081"
---
# <span data-ttu-id="0b1d8-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0b1d8-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="0b1d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b1d8-102">SYNOPSIS</span></span>
<span data-ttu-id="0b1d8-103">Ottiene la regola di routing delle richieste di un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="0b1d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b1d8-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b1d8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0b1d8-105">DESCRIPTION</span></span>
<span data-ttu-id="0b1d8-106">Il cmdlet **Get-AzApplicationGatewayRequestRoutingRule** ottiene la regola di routing delle richieste di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="0b1d8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b1d8-107">EXAMPLES</span></span>

### <span data-ttu-id="0b1d8-108">Esempio 1: Ottenere una regola di routing delle richieste specifica</span><span class="sxs-lookup"><span data-stu-id="0b1d8-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="0b1d8-109">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="0b1d8-110">Il secondo comando recupera la regola di routing delle richieste denominata Rule01 dal Gateway applicazione archiviata nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="0b1d8-111">Esempio 2: Ottenere un elenco di regole di routing delle richieste</span><span class="sxs-lookup"><span data-stu-id="0b1d8-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="0b1d8-112">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="0b1d8-113">Il secondo comando ottiene un elenco di regole di routing delle richieste dal Gateway applicazione archiviato nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="0b1d8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b1d8-114">PARAMETERS</span></span>

### <span data-ttu-id="0b1d8-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0b1d8-115">-ApplicationGateway</span></span>
<span data-ttu-id="0b1d8-116">Specifica l'oggetto gateway applicazione che contiene la regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="0b1d8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b1d8-117">-DefaultProfile</span></span>
<span data-ttu-id="0b1d8-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b1d8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0b1d8-119">-Name</span></span>
<span data-ttu-id="0b1d8-120">Specifica il nome della regola di routing delle richieste recuperata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="0b1d8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b1d8-121">CommonParameters</span></span>
<span data-ttu-id="0b1d8-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b1d8-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b1d8-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="0b1d8-124">INPUTS</span></span>

### <span data-ttu-id="0b1d8-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0b1d8-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0b1d8-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b1d8-126">OUTPUTS</span></span>

### <span data-ttu-id="0b1d8-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0b1d8-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="0b1d8-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="0b1d8-128">NOTES</span></span>

## <span data-ttu-id="0b1d8-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b1d8-129">RELATED LINKS</span></span>

[<span data-ttu-id="0b1d8-130">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0b1d8-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="0b1d8-131">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0b1d8-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="0b1d8-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0b1d8-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="0b1d8-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0b1d8-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


