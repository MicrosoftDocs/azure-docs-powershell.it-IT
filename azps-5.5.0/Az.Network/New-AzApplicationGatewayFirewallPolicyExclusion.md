---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicyexclusion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
ms.openlocfilehash: e5ad76625a171e1fd12fc583c6ad8acf593ed817
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179775"
---
# <span data-ttu-id="ef7c9-101">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="ef7c9-101">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="ef7c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef7c9-102">SYNOPSIS</span></span>
<span data-ttu-id="ef7c9-103">Crea un'esclusione nel criterio del firewall</span><span class="sxs-lookup"><span data-stu-id="ef7c9-103">Creates an exclusion on the Firewall Policy</span></span>

## <span data-ttu-id="ef7c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef7c9-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable <String> -SelectorMatchOperator <String>
 -Selector <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef7c9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ef7c9-105">DESCRIPTION</span></span>
<span data-ttu-id="ef7c9-106">Il cmdlet **New-AzApplicationGatewayFirewallPolicyExapplication è** un nuovo elenco di regole di esclusione per i criteri del firewall.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span></span>

## <span data-ttu-id="ef7c9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef7c9-107">EXAMPLES</span></span>

### <span data-ttu-id="ef7c9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ef7c9-108">Example 1</span></span>
```powershell
PS C:\> $exclusionEntry = New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable "RequestHeaderNames" -SelectorMatchOperator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="ef7c9-109">Questo comando crea una nuova voce di esclusione per la variabile denominata RequestHeaderNames e l'operatore StartsWith e Selector denominati xyz.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-109">This command creates a new exclusion-entry for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="ef7c9-110">La voce di esclusione viene salvata in $exclusionEntry.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-110">The exclusion entry is saved in $exclusionEntry.</span></span>

## <span data-ttu-id="ef7c9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef7c9-111">PARAMETERS</span></span>

### <span data-ttu-id="ef7c9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef7c9-112">-DefaultProfile</span></span>
<span data-ttu-id="ef7c9-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef7c9-114">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="ef7c9-114">-MatchVariable</span></span>
<span data-ttu-id="ef7c9-115">La variabile da escludere.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-115">The variable to be excluded.</span></span>

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

### <span data-ttu-id="ef7c9-116">-Selettore</span><span class="sxs-lookup"><span data-stu-id="ef7c9-116">-Selector</span></span>
<span data-ttu-id="ef7c9-117">Quando la variabile è una raccolta, l'operatore usato per specificare a quali elementi della raccolta si applica questa esclusione.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="ef7c9-118">-SelectorMatchOperator</span><span class="sxs-lookup"><span data-stu-id="ef7c9-118">-SelectorMatchOperator</span></span>
<span data-ttu-id="ef7c9-119">Quando la variabile è una raccolta, usare il selettore per specificare a quali elementi della raccolta si applica questa esclusione.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-119">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="ef7c9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef7c9-120">CommonParameters</span></span>
<span data-ttu-id="ef7c9-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef7c9-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef7c9-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="ef7c9-123">INPUTS</span></span>

### <span data-ttu-id="ef7c9-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ef7c9-124">None</span></span>

## <span data-ttu-id="ef7c9-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef7c9-125">OUTPUTS</span></span>

### <span data-ttu-id="ef7c9-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExapplication</span><span class="sxs-lookup"><span data-stu-id="ef7c9-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="ef7c9-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="ef7c9-127">NOTES</span></span>

## <span data-ttu-id="ef7c9-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef7c9-128">RELATED LINKS</span></span>
