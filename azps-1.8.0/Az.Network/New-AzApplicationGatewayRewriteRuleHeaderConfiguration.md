---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: ad14e461647fce3ec9471106b8bb69d4002eb590
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678342"
---
# <span data-ttu-id="96999-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="96999-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="96999-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96999-102">SYNOPSIS</span></span>
<span data-ttu-id="96999-103">Crea una configurazione di intestazione di riscrittura delle regole per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="96999-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="96999-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96999-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96999-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96999-105">DESCRIPTION</span></span>
<span data-ttu-id="96999-106">**Il cmdlet AzApplicationGatewayRewriteRuleHeaderConfiguration** crea un actiont della regola di riscrittura per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="96999-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule actionset for an Azure application gateway.</span></span>

## <span data-ttu-id="96999-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96999-107">EXAMPLES</span></span>

### <span data-ttu-id="96999-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="96999-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="96999-109">Questo comando crea una configurazione dell'intestazione della regola di riscrittura e archivia il risultato nella variabile denominata $hc.</span><span class="sxs-lookup"><span data-stu-id="96999-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="96999-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96999-110">PARAMETERS</span></span>

### <span data-ttu-id="96999-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96999-111">-DefaultProfile</span></span>
<span data-ttu-id="96999-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96999-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96999-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="96999-113">-HeaderName</span></span>
<span data-ttu-id="96999-114">Nome dell'intestazione da riscrivere</span><span class="sxs-lookup"><span data-stu-id="96999-114">Name of the Header to rewrite</span></span>

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

### <span data-ttu-id="96999-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="96999-115">-HeaderValue</span></span>
<span data-ttu-id="96999-116">Valore di intestazione per il set per il nome di intestazione indicato.</span><span class="sxs-lookup"><span data-stu-id="96999-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="96999-117">L'intestazione verrà eliminata se omessa</span><span class="sxs-lookup"><span data-stu-id="96999-117">Header will be deleted if this is omitted</span></span>

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

### <span data-ttu-id="96999-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96999-118">CommonParameters</span></span>
<span data-ttu-id="96999-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96999-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96999-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96999-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96999-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96999-121">INPUTS</span></span>

### <span data-ttu-id="96999-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="96999-122">None</span></span>

## <span data-ttu-id="96999-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96999-123">OUTPUTS</span></span>

### <span data-ttu-id="96999-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="96999-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="96999-125">Note</span><span class="sxs-lookup"><span data-stu-id="96999-125">NOTES</span></span>

## <span data-ttu-id="96999-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96999-126">RELATED LINKS</span></span>

[<span data-ttu-id="96999-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96999-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="96999-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96999-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="96999-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96999-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="96999-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96999-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="96999-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96999-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="96999-132">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="96999-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="96999-133">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="96999-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
