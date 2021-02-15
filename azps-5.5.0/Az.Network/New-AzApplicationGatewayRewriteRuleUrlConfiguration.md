---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: ca77d1c3490c8e22a22c98682065bcd32a5b98bc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187110"
---
# <span data-ttu-id="82798-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="82798-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="82798-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82798-102">SYNOPSIS</span></span>
<span data-ttu-id="82798-103">Crea una configurazione dell'URL della regola di riscrittura per un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="82798-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="82798-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82798-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82798-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="82798-105">DESCRIPTION</span></span>
<span data-ttu-id="82798-106">Il cmdlet **AzApplicationGatewayRewriteRuleUrlConfiguration crea** una configurazione dell'URL della regola di riscrittura per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="82798-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="82798-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82798-107">EXAMPLES</span></span>

### <span data-ttu-id="82798-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="82798-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="82798-109">Questo comando crea una configurazione dell'URL della regola di riscrittura e archivia il risultato nella variabile $urlConfiguration.</span><span class="sxs-lookup"><span data-stu-id="82798-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="82798-110">Se si vuole aggiornare qualsiasi UrlConfiguration esistente, è possibile farlo creando una nuova UrlConfiguration e assegnando la nuova urlConfiguration alla proprietà UrlConfiguration del set di azioni Della regola di Riscrivi.</span><span class="sxs-lookup"><span data-stu-id="82798-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="82798-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82798-111">PARAMETERS</span></span>

### <span data-ttu-id="82798-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82798-112">-DefaultProfile</span></span>
<span data-ttu-id="82798-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82798-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82798-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="82798-114">-ModifiedPath</span></span>
<span data-ttu-id="82798-115">Valore del percorso URL.</span><span class="sxs-lookup"><span data-stu-id="82798-115">Url path value.</span></span>

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

### <span data-ttu-id="82798-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="82798-116">-ModifiedQueryString</span></span>
<span data-ttu-id="82798-117">Valore stringa della query url.</span><span class="sxs-lookup"><span data-stu-id="82798-117">Url query string value.</span></span>

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

### <span data-ttu-id="82798-118">-Reroute</span><span class="sxs-lookup"><span data-stu-id="82798-118">-Reroute</span></span>
<span data-ttu-id="82798-119">Flag per valutare di nuovo la mappa del percorso URL disponibile nelle regole di routing delle richieste basate sul percorso usando il percorso modificato.</span><span class="sxs-lookup"><span data-stu-id="82798-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

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

### <span data-ttu-id="82798-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82798-120">CommonParameters</span></span>
<span data-ttu-id="82798-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82798-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82798-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="82798-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82798-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="82798-123">INPUTS</span></span>

### <span data-ttu-id="82798-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="82798-124">None</span></span>

## <span data-ttu-id="82798-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82798-125">OUTPUTS</span></span>

### <span data-ttu-id="82798-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="82798-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="82798-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="82798-127">NOTES</span></span>

## <span data-ttu-id="82798-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82798-128">RELATED LINKS</span></span>

[<span data-ttu-id="82798-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82798-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="82798-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82798-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="82798-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82798-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="82798-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82798-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="82798-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82798-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="82798-134">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="82798-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="82798-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="82798-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)