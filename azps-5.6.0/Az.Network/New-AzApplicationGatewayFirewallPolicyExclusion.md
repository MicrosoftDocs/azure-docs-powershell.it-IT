---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicyexclusion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
ms.openlocfilehash: 04cf39f9c0d8774ffb02688e4edf5804029df669
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974797"
---
# <span data-ttu-id="60fbc-101">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="60fbc-101">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="60fbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60fbc-102">SYNOPSIS</span></span>
<span data-ttu-id="60fbc-103">Crea un'esclusione nel criterio del firewall</span><span class="sxs-lookup"><span data-stu-id="60fbc-103">Creates an exclusion on the Firewall Policy</span></span>

## <span data-ttu-id="60fbc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60fbc-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable <String> -SelectorMatchOperator <String>
 -Selector <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60fbc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="60fbc-105">DESCRIPTION</span></span>
<span data-ttu-id="60fbc-106">Il cmdlet **New-AzApplicationGatewayFirewallPolicyExapplication è** un nuovo elenco di regole di esclusione per i criteri del firewall.</span><span class="sxs-lookup"><span data-stu-id="60fbc-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span></span>

## <span data-ttu-id="60fbc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60fbc-107">EXAMPLES</span></span>

### <span data-ttu-id="60fbc-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="60fbc-108">Example 1</span></span>
```powershell
PS C:\> $exclusionEntry = New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable "RequestHeaderNames" -SelectorMatchOperator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="60fbc-109">Questo comando crea una nuova voce di esclusione per la variabile denominata RequestHeaderNames e l'operatore StartsWith e Selector denominati xyz.</span><span class="sxs-lookup"><span data-stu-id="60fbc-109">This command creates a new exclusion-entry for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="60fbc-110">La voce di esclusione viene salvata in $exclusionEntry.</span><span class="sxs-lookup"><span data-stu-id="60fbc-110">The exclusion entry is saved in $exclusionEntry.</span></span>

## <span data-ttu-id="60fbc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60fbc-111">PARAMETERS</span></span>

### <span data-ttu-id="60fbc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60fbc-112">-DefaultProfile</span></span>
<span data-ttu-id="60fbc-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60fbc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60fbc-114">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="60fbc-114">-MatchVariable</span></span>
<span data-ttu-id="60fbc-115">La variabile da escludere.</span><span class="sxs-lookup"><span data-stu-id="60fbc-115">The variable to be excluded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestHeaderNames, RequestCookieNames, RequestArgNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60fbc-116">-Selettore</span><span class="sxs-lookup"><span data-stu-id="60fbc-116">-Selector</span></span>
<span data-ttu-id="60fbc-117">Quando la variabile è una raccolta, l'operatore usato per specificare a quali elementi della raccolta si applica questa esclusione.</span><span class="sxs-lookup"><span data-stu-id="60fbc-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="60fbc-118">-SelectorMatchOperator</span><span class="sxs-lookup"><span data-stu-id="60fbc-118">-SelectorMatchOperator</span></span>
<span data-ttu-id="60fbc-119">Quando la variabile è una raccolta, usare il selettore per specificare a quali elementi della raccolta si applica questa esclusione.</span><span class="sxs-lookup"><span data-stu-id="60fbc-119">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Equals, Contains, StartsWith, EndsWith, EqualsAny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60fbc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60fbc-120">CommonParameters</span></span>
<span data-ttu-id="60fbc-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60fbc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60fbc-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="60fbc-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60fbc-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="60fbc-123">INPUTS</span></span>

### <span data-ttu-id="60fbc-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="60fbc-124">None</span></span>

## <span data-ttu-id="60fbc-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60fbc-125">OUTPUTS</span></span>

### <span data-ttu-id="60fbc-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExapplication</span><span class="sxs-lookup"><span data-stu-id="60fbc-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="60fbc-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="60fbc-127">NOTES</span></span>

## <span data-ttu-id="60fbc-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60fbc-128">RELATED LINKS</span></span>
