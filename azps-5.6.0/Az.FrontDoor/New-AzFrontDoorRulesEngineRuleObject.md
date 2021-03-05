---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorrulesengineruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
ms.openlocfilehash: 7bef36412f8b1b5977e94b32d0645ccdaa8d0324
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970941"
---
# <span data-ttu-id="21730-101">New-AzFrontDoorRulesEngineRuleObject</span><span class="sxs-lookup"><span data-stu-id="21730-101">New-AzFrontDoorRulesEngineRuleObject</span></span>

## <span data-ttu-id="21730-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21730-102">SYNOPSIS</span></span>
<span data-ttu-id="21730-103">Creare un oggetto PSRulesRuleRule per la creazione del motore di regole.</span><span class="sxs-lookup"><span data-stu-id="21730-103">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

## <span data-ttu-id="21730-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21730-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineRuleObject -Name <String> -Priority <Int32> -Action <PSRulesEngineAction>
 [-MatchProcessingBehavior <PSMatchProcessingBehavior>] [-MatchCondition <PSRulesEngineMatchCondition[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21730-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="21730-105">DESCRIPTION</span></span>
<span data-ttu-id="21730-106">Creare un oggetto PSRulesRule per la creazione del motore di regole.</span><span class="sxs-lookup"><span data-stu-id="21730-106">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

<span data-ttu-id="21730-107">Usare il cmdlet "New-AzFrontDoorRulesActionActionObject" per creare l'oggetto PSRulesActionAction da passare al parametro "-Action".</span><span class="sxs-lookup"><span data-stu-id="21730-107">Use cmdlet "New-AzFrontDoorRulesEngineActionObject" to create PSRulesEngineAction object to pass into the "-Action" parameter.</span></span>
<span data-ttu-id="21730-108">Usare il cmdlet "New-AzFrontDoorRulesMatchConditionObject" per creare l'oggetto PSRulesConditionMatchCondition da passare al parametro "-MatchCondition".</span><span class="sxs-lookup"><span data-stu-id="21730-108">Use cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" to create PSRulesEngineMatchCondition object to pass into the "-MatchCondition" parameter.</span></span>

## <span data-ttu-id="21730-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21730-109">EXAMPLES</span></span>

### <span data-ttu-id="21730-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="21730-110">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority 0 -Action $rulesEngineAction -MatchProcessingBehavior Stop -MatchCondition $rulesEngineMatchCondition

Name                    : rules1
Priority                : 0
MatchProcessingBehavior : Stop
MatchCondition          : {Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition}
Action                  : Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction


PS C:\> $rulesEngineRule1.Action

RequestHeaderActions           ResponseHeaderActions RouteConfigurationOverride
--------------------           --------------------- --------------------------
{headeraction1, headeraction2} {}                    Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfigurati�

PS C:\> $rulesEngineRule1.MatchCondition[0]

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transforms               : {Lowercase, Uppercase}
```

<span data-ttu-id="21730-111">Creare un nuovo oggetto PSRulesRule e illustrare come visualizzare i campi secondari.</span><span class="sxs-lookup"><span data-stu-id="21730-111">Create new PSRulesEngineRule object and demonstrate how to see the subfields.</span></span>

### <span data-ttu-id="21730-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="21730-112">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
New-AzFrontDoorRulesEngineRuleObject : Cannot validate argument on parameter 'Priority'. The -1 argument is less than the minimum allowed range of 0. Supply an argument that is greater than or equal to 0 and then try the command again.
At line:1 char:81
+ ... ule1 = New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
+                                                                        ~~
+ CategoryInfo          : InvalidData: (:) [New-AzFrontDoorRulesEngineRuleObject], ParameterBindingValidationException
+ FullyQualifiedErrorId : ParameterArgumentValidationError,Microsoft.Azure.Commands.FrontDoor.Cmdlets.NewFrontDoorRulesEngineRuleObject
```

<span data-ttu-id="21730-113">Output previsto quando si passa un valore di priorità non valido.</span><span class="sxs-lookup"><span data-stu-id="21730-113">Expect output when passing in invalid priority value.</span></span>

## <span data-ttu-id="21730-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21730-114">PARAMETERS</span></span>

### <span data-ttu-id="21730-115">-Action</span><span class="sxs-lookup"><span data-stu-id="21730-115">-Action</span></span>
<span data-ttu-id="21730-116">Azioni da eseguire sulla richiesta e sulla risposta se vengono soddisfatte tutte le condizioni di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="21730-116">Actions to perform on the request and response if all of the match conditions are met.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21730-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21730-117">-DefaultProfile</span></span>
<span data-ttu-id="21730-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="21730-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21730-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="21730-119">-MatchCondition</span></span>
<span data-ttu-id="21730-120">Elenco di condizioni di corrispondenza che devono essere soddisfatte per l'esecuzione delle azioni della regola.</span><span class="sxs-lookup"><span data-stu-id="21730-120">A list of match conditions that must meet in order for the actions of this rule to run.</span></span> <span data-ttu-id="21730-121">Se non ci sono condizioni di corrispondenza, le azioni vengono sempre eseguite.</span><span class="sxs-lookup"><span data-stu-id="21730-121">Having no match conditions means the actions will always run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21730-122">-MatchProcessingBehavior</span><span class="sxs-lookup"><span data-stu-id="21730-122">-MatchProcessingBehavior</span></span>
<span data-ttu-id="21730-123">Se questa regola corrisponde, il motore di regole continuerà a eseguire le regole rimanenti o a interrompersi.</span><span class="sxs-lookup"><span data-stu-id="21730-123">If this rule is a match should the rules engine continue running the remaining rules or stop.</span></span>
<span data-ttu-id="21730-124">I valori possibili sono Continua e Interrompi.</span><span class="sxs-lookup"><span data-stu-id="21730-124">Possible values are Continue and Stop.</span></span>
<span data-ttu-id="21730-125">Se non è presente, l'impostazione predefinita è Continua.</span><span class="sxs-lookup"><span data-stu-id="21730-125">If not present, defaults to Continue.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchProcessingBehavior
Parameter Sets: (All)
Aliases:
Accepted values: Continue, Stop

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21730-126">-Name</span><span class="sxs-lookup"><span data-stu-id="21730-126">-Name</span></span>
<span data-ttu-id="21730-127">Nome che fa riferimento a questa regola specifica.</span><span class="sxs-lookup"><span data-stu-id="21730-127">A name to refer to this specific rule.</span></span>

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

### <span data-ttu-id="21730-128">-Priority</span><span class="sxs-lookup"><span data-stu-id="21730-128">-Priority</span></span>
<span data-ttu-id="21730-129">Priorità assegnata a questa regola.</span><span class="sxs-lookup"><span data-stu-id="21730-129">A priority assigned to this rule.</span></span>
<span data-ttu-id="21730-130">Non può essere negativo.</span><span class="sxs-lookup"><span data-stu-id="21730-130">Cannot be negative.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21730-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21730-131">CommonParameters</span></span>
<span data-ttu-id="21730-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21730-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21730-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="21730-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21730-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="21730-134">INPUTS</span></span>

### <span data-ttu-id="21730-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="21730-135">None</span></span>

## <span data-ttu-id="21730-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21730-136">OUTPUTS</span></span>

### <span data-ttu-id="21730-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesRulesRule</span><span class="sxs-lookup"><span data-stu-id="21730-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span></span>

## <span data-ttu-id="21730-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="21730-138">NOTES</span></span>

## <span data-ttu-id="21730-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21730-139">RELATED LINKS</span></span>
