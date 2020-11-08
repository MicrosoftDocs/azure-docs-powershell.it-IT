---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: ca77d1c3490c8e22a22c98682065bcd32a5b98bc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022730"
---
# <span data-ttu-id="a438e-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a438e-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="a438e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a438e-102">SYNOPSIS</span></span>
<span data-ttu-id="a438e-103">Crea una configurazione di URL della regola di riscrittura per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a438e-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="a438e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a438e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a438e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a438e-105">DESCRIPTION</span></span>
<span data-ttu-id="a438e-106">**Il cmdlet AzApplicationGatewayRewriteRuleUrlConfiguration** crea una configurazione di URL della regola di riscrittura per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="a438e-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="a438e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a438e-107">EXAMPLES</span></span>

### <span data-ttu-id="a438e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a438e-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="a438e-109">Questo comando crea una configurazione dell'URL della regola di riscrittura e archivia il risultato nella variabile denominata $urlConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a438e-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="a438e-110">Se si vuole aggiornare qualsiasi UrlConfiguration esistente, è possibile crearne uno nuovo UrlConfiguration e assegnare il nuovo UrlConfiguration alla proprietà UrlConfiguration del set di azioni di riscrittura regola.</span><span class="sxs-lookup"><span data-stu-id="a438e-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="a438e-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a438e-111">PARAMETERS</span></span>

### <span data-ttu-id="a438e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a438e-112">-DefaultProfile</span></span>
<span data-ttu-id="a438e-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a438e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a438e-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="a438e-114">-ModifiedPath</span></span>
<span data-ttu-id="a438e-115">Valore percorso URL.</span><span class="sxs-lookup"><span data-stu-id="a438e-115">Url path value.</span></span>

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

### <span data-ttu-id="a438e-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="a438e-116">-ModifiedQueryString</span></span>
<span data-ttu-id="a438e-117">Valore stringa di query URL.</span><span class="sxs-lookup"><span data-stu-id="a438e-117">Url query string value.</span></span>

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

### <span data-ttu-id="a438e-118">-Reinstradare</span><span class="sxs-lookup"><span data-stu-id="a438e-118">-Reroute</span></span>
<span data-ttu-id="a438e-119">Contrassegna per rivalutare la mappa di percorso URL specificata in regole di routing per le richieste basate su percorso tramite il percorso modificato.</span><span class="sxs-lookup"><span data-stu-id="a438e-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

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

### <span data-ttu-id="a438e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a438e-120">CommonParameters</span></span>
<span data-ttu-id="a438e-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a438e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a438e-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a438e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a438e-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a438e-123">INPUTS</span></span>

### <span data-ttu-id="a438e-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a438e-124">None</span></span>

## <span data-ttu-id="a438e-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a438e-125">OUTPUTS</span></span>

### <span data-ttu-id="a438e-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a438e-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="a438e-127">Note</span><span class="sxs-lookup"><span data-stu-id="a438e-127">NOTES</span></span>

## <span data-ttu-id="a438e-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a438e-128">RELATED LINKS</span></span>

[<span data-ttu-id="a438e-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a438e-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a438e-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a438e-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a438e-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a438e-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a438e-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a438e-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a438e-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a438e-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a438e-134">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a438e-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="a438e-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a438e-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)