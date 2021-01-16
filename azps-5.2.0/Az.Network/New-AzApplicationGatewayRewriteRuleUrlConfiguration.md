---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: ca77d1c3490c8e22a22c98682065bcd32a5b98bc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340219"
---
# <span data-ttu-id="b7557-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7557-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="b7557-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7557-102">SYNOPSIS</span></span>
<span data-ttu-id="b7557-103">Crea una configurazione di URL della regola di riscrittura per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7557-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="b7557-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7557-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7557-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7557-105">DESCRIPTION</span></span>
<span data-ttu-id="b7557-106">**Il cmdlet AzApplicationGatewayRewriteRuleUrlConfiguration** crea una configurazione di URL della regola di riscrittura per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="b7557-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="b7557-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7557-107">EXAMPLES</span></span>

### <span data-ttu-id="b7557-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b7557-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="b7557-109">Questo comando crea una configurazione dell'URL della regola di riscrittura e archivia il risultato nella variabile denominata $urlConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b7557-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="b7557-110">Se si vuole aggiornare qualsiasi UrlConfiguration esistente, è possibile crearne uno nuovo UrlConfiguration e assegnare il nuovo UrlConfiguration alla proprietà UrlConfiguration del set di azioni di riscrittura regola.</span><span class="sxs-lookup"><span data-stu-id="b7557-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="b7557-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7557-111">PARAMETERS</span></span>

### <span data-ttu-id="b7557-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7557-112">-DefaultProfile</span></span>
<span data-ttu-id="b7557-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7557-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7557-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="b7557-114">-ModifiedPath</span></span>
<span data-ttu-id="b7557-115">Valore percorso URL.</span><span class="sxs-lookup"><span data-stu-id="b7557-115">Url path value.</span></span>

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

### <span data-ttu-id="b7557-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="b7557-116">-ModifiedQueryString</span></span>
<span data-ttu-id="b7557-117">Valore stringa di query URL.</span><span class="sxs-lookup"><span data-stu-id="b7557-117">Url query string value.</span></span>

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

### <span data-ttu-id="b7557-118">-Reinstradare</span><span class="sxs-lookup"><span data-stu-id="b7557-118">-Reroute</span></span>
<span data-ttu-id="b7557-119">Contrassegna per rivalutare la mappa di percorso URL specificata in regole di routing per le richieste basate su percorso tramite il percorso modificato.</span><span class="sxs-lookup"><span data-stu-id="b7557-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

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

### <span data-ttu-id="b7557-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7557-120">CommonParameters</span></span>
<span data-ttu-id="b7557-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7557-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7557-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7557-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7557-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7557-123">INPUTS</span></span>

### <span data-ttu-id="b7557-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b7557-124">None</span></span>

## <span data-ttu-id="b7557-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7557-125">OUTPUTS</span></span>

### <span data-ttu-id="b7557-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7557-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="b7557-127">Note</span><span class="sxs-lookup"><span data-stu-id="b7557-127">NOTES</span></span>

## <span data-ttu-id="b7557-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7557-128">RELATED LINKS</span></span>

[<span data-ttu-id="b7557-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7557-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b7557-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7557-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b7557-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7557-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b7557-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7557-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b7557-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7557-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b7557-134">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b7557-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="b7557-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b7557-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)