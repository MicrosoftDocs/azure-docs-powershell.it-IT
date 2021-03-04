---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: e9b0b8cdbee1e4d5c488e51f537d18cca2ef681a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952189"
---
# <span data-ttu-id="e6ae8-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6ae8-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="e6ae8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6ae8-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ae8-103">Crea una configurazione dell'URL della regola di riscrittura per un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e6ae8-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="e6ae8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6ae8-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6ae8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e6ae8-105">DESCRIPTION</span></span>
<span data-ttu-id="e6ae8-106">Il cmdlet **AzApplicationGatewayRewriteRuleUrlConfiguration crea** una configurazione dell'URL della regola di riscrittura per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e6ae8-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="e6ae8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6ae8-107">EXAMPLES</span></span>

### <span data-ttu-id="e6ae8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e6ae8-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="e6ae8-109">Questo comando crea una configurazione dell'URL della regola di riscrittura e archivia il risultato nella variabile $urlConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e6ae8-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="e6ae8-110">Se si vuole aggiornare qualsiasi UrlConfiguration esistente, è possibile farlo creando una nuova UrlConfiguration e assegnando la nuova urlConfiguration alla proprietà UrlConfiguration del set di azioni della regola di Riscrivi.</span><span class="sxs-lookup"><span data-stu-id="e6ae8-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="e6ae8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6ae8-111">PARAMETERS</span></span>

### <span data-ttu-id="e6ae8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6ae8-112">-DefaultProfile</span></span>
<span data-ttu-id="e6ae8-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6ae8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6ae8-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="e6ae8-114">-ModifiedPath</span></span>
<span data-ttu-id="e6ae8-115">Valore del percorso URL.</span><span class="sxs-lookup"><span data-stu-id="e6ae8-115">Url path value.</span></span>

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

### <span data-ttu-id="e6ae8-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="e6ae8-116">-ModifiedQueryString</span></span>
<span data-ttu-id="e6ae8-117">Valore stringa della query url.</span><span class="sxs-lookup"><span data-stu-id="e6ae8-117">Url query string value.</span></span>

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

### <span data-ttu-id="e6ae8-118">-Reroute</span><span class="sxs-lookup"><span data-stu-id="e6ae8-118">-Reroute</span></span>
<span data-ttu-id="e6ae8-119">Flag per valutare di nuovo la mappa del percorso URL disponibile nelle regole di routing delle richieste basate sul percorso usando il percorso modificato.</span><span class="sxs-lookup"><span data-stu-id="e6ae8-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ae8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ae8-120">CommonParameters</span></span>
<span data-ttu-id="e6ae8-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6ae8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ae8-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e6ae8-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ae8-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="e6ae8-123">INPUTS</span></span>

### <span data-ttu-id="e6ae8-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e6ae8-124">None</span></span>

## <span data-ttu-id="e6ae8-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6ae8-125">OUTPUTS</span></span>

### <span data-ttu-id="e6ae8-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6ae8-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="e6ae8-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="e6ae8-127">NOTES</span></span>

## <span data-ttu-id="e6ae8-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6ae8-128">RELATED LINKS</span></span>

[<span data-ttu-id="e6ae8-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e6ae8-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e6ae8-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e6ae8-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e6ae8-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e6ae8-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e6ae8-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e6ae8-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e6ae8-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e6ae8-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e6ae8-134">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e6ae8-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="e6ae8-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e6ae8-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)