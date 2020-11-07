---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: 84be6aa60ede19e88b98ca9517fa3cbce3872c8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853546"
---
# <span data-ttu-id="84772-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="84772-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="84772-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84772-102">SYNOPSIS</span></span>
<span data-ttu-id="84772-103">Crea un set di azioni di riscrittura regola per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="84772-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="84772-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84772-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84772-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84772-105">DESCRIPTION</span></span>
<span data-ttu-id="84772-106">**Il cmdlet New-AzApplicationGatewayRewriteRuleActionSet** crea un set di azioni di riscrittura regola per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="84772-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="84772-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84772-107">EXAMPLES</span></span>

### <span data-ttu-id="84772-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="84772-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc
```

<span data-ttu-id="84772-109">Questo comando crea un set di azioni di riscrittura regola e archivia il risultato nella variabile denominata $action.</span><span class="sxs-lookup"><span data-stu-id="84772-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="84772-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84772-110">PARAMETERS</span></span>

### <span data-ttu-id="84772-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84772-111">-DefaultProfile</span></span>
<span data-ttu-id="84772-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84772-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84772-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="84772-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="84772-114">Elenco delle configurazioni delle intestazioni delle richieste</span><span class="sxs-lookup"><span data-stu-id="84772-114">List of request header configurations</span></span>

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

### <span data-ttu-id="84772-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="84772-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="84772-116">Elenco delle configurazioni delle intestazioni di risposta</span><span class="sxs-lookup"><span data-stu-id="84772-116">List of response header configurations</span></span>

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

### <span data-ttu-id="84772-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84772-117">CommonParameters</span></span>
<span data-ttu-id="84772-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84772-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84772-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84772-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84772-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84772-120">INPUTS</span></span>

### <span data-ttu-id="84772-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="84772-121">None</span></span>

## <span data-ttu-id="84772-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84772-122">OUTPUTS</span></span>

### <span data-ttu-id="84772-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="84772-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="84772-124">Note</span><span class="sxs-lookup"><span data-stu-id="84772-124">NOTES</span></span>

## <span data-ttu-id="84772-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84772-125">RELATED LINKS</span></span>

[<span data-ttu-id="84772-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="84772-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="84772-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="84772-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="84772-128">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="84772-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="84772-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="84772-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="84772-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="84772-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="84772-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="84772-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="84772-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="84772-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
