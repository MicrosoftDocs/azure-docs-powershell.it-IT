---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 1f59a7366106c59f6dc5e5af3a32368594a00537
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473866"
---
# <span data-ttu-id="fbfc2-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="fbfc2-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="fbfc2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fbfc2-102">SYNOPSIS</span></span>
<span data-ttu-id="fbfc2-103">Creare un oggetto di esclusione delle regole gestite per set di regole, gruppi o regole gestite da WAF.</span><span class="sxs-lookup"><span data-stu-id="fbfc2-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="fbfc2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fbfc2-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbfc2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbfc2-105">DESCRIPTION</span></span>
<span data-ttu-id="fbfc2-106">Creare un oggetto di esclusione delle regole gestite per set di regole, gruppi o regole gestite da WAF.</span><span class="sxs-lookup"><span data-stu-id="fbfc2-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="fbfc2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fbfc2-107">EXAMPLES</span></span>

### <span data-ttu-id="fbfc2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fbfc2-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="fbfc2-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fbfc2-109">PARAMETERS</span></span>

### <span data-ttu-id="fbfc2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbfc2-110">-DefaultProfile</span></span>
<span data-ttu-id="fbfc2-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fbfc2-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbfc2-112">-Operator</span><span class="sxs-lookup"><span data-stu-id="fbfc2-112">-Operator</span></span>
<span data-ttu-id="fbfc2-113">Operatore da usare per la corrispondenza del selettore, EqualsAny significa nessun selettore (tutte le variabili di corrispondenza del tipo specificato)</span><span class="sxs-lookup"><span data-stu-id="fbfc2-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

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

### <span data-ttu-id="fbfc2-114">-Selector</span><span class="sxs-lookup"><span data-stu-id="fbfc2-114">-Selector</span></span>
<span data-ttu-id="fbfc2-115">Modello di selezione in base all'operatore (se l'operatore non è EqualsAny)</span><span class="sxs-lookup"><span data-stu-id="fbfc2-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

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

### <span data-ttu-id="fbfc2-116">-Variabile</span><span class="sxs-lookup"><span data-stu-id="fbfc2-116">-Variable</span></span>
<span data-ttu-id="fbfc2-117">Associa variabile.</span><span class="sxs-lookup"><span data-stu-id="fbfc2-117">Match variable.</span></span> <span data-ttu-id="fbfc2-118">I valori possibili sono RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span><span class="sxs-lookup"><span data-stu-id="fbfc2-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="fbfc2-119">Ad esempio, QueryStringArgNames è un'esclusione dei parametri GET che corrispondono al selettore con l'operatore indicato.</span><span class="sxs-lookup"><span data-stu-id="fbfc2-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

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

### <span data-ttu-id="fbfc2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbfc2-120">CommonParameters</span></span>
<span data-ttu-id="fbfc2-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbfc2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbfc2-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbfc2-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbfc2-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fbfc2-123">INPUTS</span></span>

### <span data-ttu-id="fbfc2-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fbfc2-124">None</span></span>

## <span data-ttu-id="fbfc2-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fbfc2-125">OUTPUTS</span></span>

### <span data-ttu-id="fbfc2-126">Microsoft. Azure. Commands. FrontDoor. Models. PSManagedRuleExclusion</span><span class="sxs-lookup"><span data-stu-id="fbfc2-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="fbfc2-127">Note</span><span class="sxs-lookup"><span data-stu-id="fbfc2-127">NOTES</span></span>

## <span data-ttu-id="fbfc2-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fbfc2-128">RELATED LINKS</span></span>

<span data-ttu-id="fbfc2-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="fbfc2-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
