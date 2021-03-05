---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 4f8764a40d536897ee71e36c1be1d691040e2ab9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970893"
---
# <span data-ttu-id="b39b5-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="b39b5-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="b39b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b39b5-102">SYNOPSIS</span></span>
<span data-ttu-id="b39b5-103">Creare un oggetto esclusione regole gestite per set di regole, gruppi o regole gestiti da WAF.</span><span class="sxs-lookup"><span data-stu-id="b39b5-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="b39b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b39b5-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b39b5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b39b5-105">DESCRIPTION</span></span>
<span data-ttu-id="b39b5-106">Creare un oggetto esclusione regole gestite per set di regole, gruppi o regole gestiti da WAF.</span><span class="sxs-lookup"><span data-stu-id="b39b5-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="b39b5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b39b5-107">EXAMPLES</span></span>

### <span data-ttu-id="b39b5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b39b5-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="b39b5-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b39b5-109">PARAMETERS</span></span>

### <span data-ttu-id="b39b5-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b39b5-110">-DefaultProfile</span></span>
<span data-ttu-id="b39b5-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b39b5-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b39b5-112">-Operatore</span><span class="sxs-lookup"><span data-stu-id="b39b5-112">-Operator</span></span>
<span data-ttu-id="b39b5-113">Operatore da usare quando si trova la corrispondenza con il selettore, UgualeAny significa nessun selettore (tutte le variabili corrispondenti del tipo specificato)</span><span class="sxs-lookup"><span data-stu-id="b39b5-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

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

### <span data-ttu-id="b39b5-114">-Selettore</span><span class="sxs-lookup"><span data-stu-id="b39b5-114">-Selector</span></span>
<span data-ttu-id="b39b5-115">Criterio di selezione di cui trovare una corrispondenza usando l'operatore (se l'operatore non è Uguale a)</span><span class="sxs-lookup"><span data-stu-id="b39b5-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

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

### <span data-ttu-id="b39b5-116">-Variabile</span><span class="sxs-lookup"><span data-stu-id="b39b5-116">-Variable</span></span>
<span data-ttu-id="b39b5-117">Variabile Match.</span><span class="sxs-lookup"><span data-stu-id="b39b5-117">Match variable.</span></span> <span data-ttu-id="b39b5-118">I valori possibili sono RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestHeaderPostArgNames.</span><span class="sxs-lookup"><span data-stu-id="b39b5-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="b39b5-119">Ad esempio, QueryStringArgNames è un'esclusione dei parametri GET che corrispondono al selettore con l'operatore specificato.</span><span class="sxs-lookup"><span data-stu-id="b39b5-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

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

### <span data-ttu-id="b39b5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b39b5-120">CommonParameters</span></span>
<span data-ttu-id="b39b5-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b39b5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b39b5-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b39b5-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b39b5-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="b39b5-123">INPUTS</span></span>

### <span data-ttu-id="b39b5-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b39b5-124">None</span></span>

## <span data-ttu-id="b39b5-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b39b5-125">OUTPUTS</span></span>

### <span data-ttu-id="b39b5-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleEx più</span><span class="sxs-lookup"><span data-stu-id="b39b5-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="b39b5-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="b39b5-127">NOTES</span></span>

## <span data-ttu-id="b39b5-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b39b5-128">RELATED LINKS</span></span>

<span data-ttu-id="b39b5-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="b39b5-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
