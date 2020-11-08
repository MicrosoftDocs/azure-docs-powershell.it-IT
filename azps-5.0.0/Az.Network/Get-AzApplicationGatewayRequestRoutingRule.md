---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 75666d2f897adeda4031b03309979366949a0040
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203449"
---
# <span data-ttu-id="c1ecb-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c1ecb-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="c1ecb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c1ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="c1ecb-103">Ottiene la regola di routing delle richieste di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c1ecb-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="c1ecb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1ecb-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1ecb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1ecb-105">DESCRIPTION</span></span>
<span data-ttu-id="c1ecb-106">Il cmdlet **Get-AzApplicationGatewayRequestRoutingRule** ottiene la regola di routing delle richieste di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c1ecb-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="c1ecb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1ecb-107">EXAMPLES</span></span>

### <span data-ttu-id="c1ecb-108">Esempio 1: ottenere una specifica regola di routing delle richieste</span><span class="sxs-lookup"><span data-stu-id="c1ecb-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="c1ecb-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="c1ecb-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="c1ecb-110">Il secondo comando consente di ottenere la regola di routing delle richieste denominata Rule01 dal gateway dell'applicazione archiviato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="c1ecb-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="c1ecb-111">Esempio 2: ottenere un elenco delle regole di routing delle richieste</span><span class="sxs-lookup"><span data-stu-id="c1ecb-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="c1ecb-112">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="c1ecb-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="c1ecb-113">Il secondo comando ottiene un elenco delle regole di routing delle richieste dal gateway dell'applicazione archiviato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="c1ecb-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="c1ecb-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1ecb-114">PARAMETERS</span></span>

### <span data-ttu-id="c1ecb-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1ecb-115">-ApplicationGateway</span></span>
<span data-ttu-id="c1ecb-116">Specifica l'oggetto gateway dell'applicazione che contiene la regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="c1ecb-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="c1ecb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1ecb-117">-DefaultProfile</span></span>
<span data-ttu-id="c1ecb-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1ecb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1ecb-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1ecb-119">-Name</span></span>
<span data-ttu-id="c1ecb-120">Specifica il nome della regola di routing delle richieste ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1ecb-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="c1ecb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1ecb-121">CommonParameters</span></span>
<span data-ttu-id="c1ecb-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1ecb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1ecb-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1ecb-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1ecb-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c1ecb-124">INPUTS</span></span>

### <span data-ttu-id="c1ecb-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1ecb-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c1ecb-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1ecb-126">OUTPUTS</span></span>

### <span data-ttu-id="c1ecb-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c1ecb-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="c1ecb-128">Note</span><span class="sxs-lookup"><span data-stu-id="c1ecb-128">NOTES</span></span>

## <span data-ttu-id="c1ecb-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1ecb-129">RELATED LINKS</span></span>

[<span data-ttu-id="c1ecb-130">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c1ecb-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c1ecb-131">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c1ecb-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c1ecb-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c1ecb-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c1ecb-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c1ecb-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


