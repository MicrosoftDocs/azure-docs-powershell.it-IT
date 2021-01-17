---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: ed8cda03debbb69c2fa65d7c209889c4cd3d2446
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358886"
---
# <span data-ttu-id="04cec-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="04cec-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="04cec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="04cec-102">SYNOPSIS</span></span>
<span data-ttu-id="04cec-103">Crea una configurazione di intestazione di riscrittura delle regole per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="04cec-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="04cec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04cec-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04cec-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04cec-105">DESCRIPTION</span></span>
<span data-ttu-id="04cec-106">**Il cmdlet AzApplicationGatewayRewriteRuleHeaderConfiguration** crea un set di azioni di riscrittura regola per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="04cec-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="04cec-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04cec-107">EXAMPLES</span></span>

### <span data-ttu-id="04cec-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="04cec-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="04cec-109">Questo comando crea una configurazione dell'intestazione della regola di riscrittura e archivia il risultato nella variabile denominata $hc.</span><span class="sxs-lookup"><span data-stu-id="04cec-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="04cec-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="04cec-110">PARAMETERS</span></span>

### <span data-ttu-id="04cec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04cec-111">-DefaultProfile</span></span>
<span data-ttu-id="04cec-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="04cec-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04cec-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="04cec-113">-HeaderName</span></span>
<span data-ttu-id="04cec-114">Nome dell'intestazione da riscrivere</span><span class="sxs-lookup"><span data-stu-id="04cec-114">Name of the Header to rewrite</span></span>

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

### <span data-ttu-id="04cec-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="04cec-115">-HeaderValue</span></span>
<span data-ttu-id="04cec-116">Valore di intestazione per il set per il nome di intestazione indicato.</span><span class="sxs-lookup"><span data-stu-id="04cec-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="04cec-117">L'intestazione verrà eliminata se omessa</span><span class="sxs-lookup"><span data-stu-id="04cec-117">Header will be deleted if this is omitted</span></span>

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

### <span data-ttu-id="04cec-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04cec-118">CommonParameters</span></span>
<span data-ttu-id="04cec-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04cec-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04cec-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04cec-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04cec-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="04cec-121">INPUTS</span></span>

### <span data-ttu-id="04cec-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="04cec-122">None</span></span>

## <span data-ttu-id="04cec-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04cec-123">OUTPUTS</span></span>

### <span data-ttu-id="04cec-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="04cec-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="04cec-125">Note</span><span class="sxs-lookup"><span data-stu-id="04cec-125">NOTES</span></span>

## <span data-ttu-id="04cec-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04cec-126">RELATED LINKS</span></span>

[<span data-ttu-id="04cec-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="04cec-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="04cec-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="04cec-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="04cec-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="04cec-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="04cec-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="04cec-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="04cec-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="04cec-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="04cec-132">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="04cec-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="04cec-133">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="04cec-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
