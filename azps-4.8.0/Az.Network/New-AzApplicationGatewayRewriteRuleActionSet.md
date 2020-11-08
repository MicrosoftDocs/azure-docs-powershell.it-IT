---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: f20647613a6e484d46a8785cfebea304b6a7ff23
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192340"
---
# <span data-ttu-id="f17d3-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f17d3-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="f17d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f17d3-102">SYNOPSIS</span></span>
<span data-ttu-id="f17d3-103">Crea un set di azioni di riscrittura regola per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f17d3-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="f17d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f17d3-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-UrlConfiguration [Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration]]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f17d3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f17d3-105">DESCRIPTION</span></span>
<span data-ttu-id="f17d3-106">**Il cmdlet New-AzApplicationGatewayRewriteRuleActionSet** crea un set di azioni di riscrittura regola per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="f17d3-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="f17d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f17d3-107">EXAMPLES</span></span>

### <span data-ttu-id="f17d3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f17d3-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc -UrlConfiguration $urlConfiguration
```

<span data-ttu-id="f17d3-109">Questo comando crea un set di azioni di riscrittura regola e archivia il risultato nella variabile denominata $action.</span><span class="sxs-lookup"><span data-stu-id="f17d3-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="f17d3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f17d3-110">PARAMETERS</span></span>

### <span data-ttu-id="f17d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f17d3-111">-DefaultProfile</span></span>
<span data-ttu-id="f17d3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f17d3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f17d3-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f17d3-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="f17d3-114">Elenco delle configurazioni delle intestazioni delle richieste</span><span class="sxs-lookup"><span data-stu-id="f17d3-114">List of request header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f17d3-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f17d3-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="f17d3-116">Elenco delle configurazioni delle intestazioni di risposta</span><span class="sxs-lookup"><span data-stu-id="f17d3-116">List of response header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f17d3-117">-UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="f17d3-117">-UrlConfiguration</span></span>
<span data-ttu-id="f17d3-118">Configurazione URL per set di azioni</span><span class="sxs-lookup"><span data-stu-id="f17d3-118">Url Configuration for action set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f17d3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f17d3-119">CommonParameters</span></span>
<span data-ttu-id="f17d3-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f17d3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f17d3-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f17d3-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f17d3-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f17d3-122">INPUTS</span></span>

### <span data-ttu-id="f17d3-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f17d3-123">None</span></span>

## <span data-ttu-id="f17d3-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f17d3-124">OUTPUTS</span></span>

### <span data-ttu-id="f17d3-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f17d3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="f17d3-126">Note</span><span class="sxs-lookup"><span data-stu-id="f17d3-126">NOTES</span></span>

## <span data-ttu-id="f17d3-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f17d3-127">RELATED LINKS</span></span>

[<span data-ttu-id="f17d3-128">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f17d3-128">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f17d3-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f17d3-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f17d3-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f17d3-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f17d3-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f17d3-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f17d3-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f17d3-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f17d3-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f17d3-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="f17d3-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f17d3-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)

[<span data-ttu-id="f17d3-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="f17d3-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleUrlConfiguration.md)