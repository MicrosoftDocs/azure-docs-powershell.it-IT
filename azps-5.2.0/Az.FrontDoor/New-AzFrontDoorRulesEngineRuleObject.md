---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
ms.openlocfilehash: c02fa092532f70567405f314dc8943e4e2ce51f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328647"
---
# <span data-ttu-id="7e0af-101">New-AzFrontDoorRulesEngineRuleObject</span><span class="sxs-lookup"><span data-stu-id="7e0af-101">New-AzFrontDoorRulesEngineRuleObject</span></span>

## <span data-ttu-id="7e0af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e0af-102">SYNOPSIS</span></span>
<span data-ttu-id="7e0af-103">Crea un oggetto PSRulesEngineRule per la creazione di motore di regole.</span><span class="sxs-lookup"><span data-stu-id="7e0af-103">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

## <span data-ttu-id="7e0af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e0af-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineRuleObject -Name <String> -Priority <Int32> -Action <PSRulesEngineAction>
 [-MatchProcessingBehavior <PSMatchProcessingBehavior>] [-MatchCondition <PSRulesEngineMatchCondition[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e0af-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e0af-105">DESCRIPTION</span></span>
<span data-ttu-id="7e0af-106">Crea un oggetto PSRulesEngineRule per la creazione di motore di regole.</span><span class="sxs-lookup"><span data-stu-id="7e0af-106">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

<span data-ttu-id="7e0af-107">Usa il cmdlet "New-AzFrontDoorRulesEngineActionObject" per creare un oggetto PSRulesEngineAction per passare al parametro "-Action".</span><span class="sxs-lookup"><span data-stu-id="7e0af-107">Use cmdlet "New-AzFrontDoorRulesEngineActionObject" to create PSRulesEngineAction object to pass into the "-Action" parameter.</span></span>
<span data-ttu-id="7e0af-108">Usa il cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" per creare un oggetto PSRulesEngineMatchCondition per passare al parametro "-MatchCondition".</span><span class="sxs-lookup"><span data-stu-id="7e0af-108">Use cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" to create PSRulesEngineMatchCondition object to pass into the "-MatchCondition" parameter.</span></span>

## <span data-ttu-id="7e0af-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e0af-109">EXAMPLES</span></span>

### <span data-ttu-id="7e0af-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7e0af-110">Example 1</span></span>
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

<span data-ttu-id="7e0af-111">Crea un nuovo oggetto PSRulesEngineRule e Mostra come visualizzare i sottocampi.</span><span class="sxs-lookup"><span data-stu-id="7e0af-111">Create new PSRulesEngineRule object and demonstrate how to see the subfields.</span></span>

### <span data-ttu-id="7e0af-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7e0af-112">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
New-AzFrontDoorRulesEngineRuleObject : Cannot validate argument on parameter 'Priority'. The -1 argument is less than the minimum allowed range of 0. Supply an argument that is greater than or equal to 0 and then try the command again.
At line:1 char:81
+ ... ule1 = New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
+                                                                        ~~
+ CategoryInfo          : InvalidData: (:) [New-AzFrontDoorRulesEngineRuleObject], ParameterBindingValidationException
+ FullyQualifiedErrorId : ParameterArgumentValidationError,Microsoft.Azure.Commands.FrontDoor.Cmdlets.NewFrontDoorRulesEngineRuleObject
```

<span data-ttu-id="7e0af-113">Prevedere l'output quando si passa il valore Priority non valido.</span><span class="sxs-lookup"><span data-stu-id="7e0af-113">Expect output when passing in invalid priority value.</span></span>

## <span data-ttu-id="7e0af-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e0af-114">PARAMETERS</span></span>

### <span data-ttu-id="7e0af-115">-Azione</span><span class="sxs-lookup"><span data-stu-id="7e0af-115">-Action</span></span>
<span data-ttu-id="7e0af-116">Azioni da eseguire su richiesta e risposta se tutte le condizioni di corrispondenza sono soddisfatte.</span><span class="sxs-lookup"><span data-stu-id="7e0af-116">Actions to perform on the request and response if all of the match conditions are met.</span></span>

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

### <span data-ttu-id="7e0af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e0af-117">-DefaultProfile</span></span>
<span data-ttu-id="7e0af-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e0af-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e0af-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="7e0af-119">-MatchCondition</span></span>
<span data-ttu-id="7e0af-120">Un elenco di condizioni di corrispondenza che devono essere soddisfatte in modo che le azioni di questa regola vengano eseguite.</span><span class="sxs-lookup"><span data-stu-id="7e0af-120">A list of match conditions that must meet in order for the actions of this rule to run.</span></span> <span data-ttu-id="7e0af-121">Se non ci sono condizioni per le corrispondenze, le azioni verranno eseguite sempre.</span><span class="sxs-lookup"><span data-stu-id="7e0af-121">Having no match conditions means the actions will always run.</span></span>

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

### <span data-ttu-id="7e0af-122">-MatchProcessingBehavior</span><span class="sxs-lookup"><span data-stu-id="7e0af-122">-MatchProcessingBehavior</span></span>
<span data-ttu-id="7e0af-123">Se questa regola corrisponde a una corrispondenza, il motore regole continuerà a eseguire le regole rimanenti o l'interruzione.</span><span class="sxs-lookup"><span data-stu-id="7e0af-123">If this rule is a match should the rules engine continue running the remaining rules or stop.</span></span>
<span data-ttu-id="7e0af-124">I valori possibili sono continue e stop.</span><span class="sxs-lookup"><span data-stu-id="7e0af-124">Possible values are Continue and Stop.</span></span>
<span data-ttu-id="7e0af-125">Se non è presente, il valore predefinito è continue.</span><span class="sxs-lookup"><span data-stu-id="7e0af-125">If not present, defaults to Continue.</span></span>

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

### <span data-ttu-id="7e0af-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e0af-126">-Name</span></span>
<span data-ttu-id="7e0af-127">Un nome per fare riferimento a questa regola specifica.</span><span class="sxs-lookup"><span data-stu-id="7e0af-127">A name to refer to this specific rule.</span></span>

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

### <span data-ttu-id="7e0af-128">-Priorità</span><span class="sxs-lookup"><span data-stu-id="7e0af-128">-Priority</span></span>
<span data-ttu-id="7e0af-129">Priorità assegnata a questa regola.</span><span class="sxs-lookup"><span data-stu-id="7e0af-129">A priority assigned to this rule.</span></span>
<span data-ttu-id="7e0af-130">Non può essere negativo.</span><span class="sxs-lookup"><span data-stu-id="7e0af-130">Cannot be negative.</span></span>

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

### <span data-ttu-id="7e0af-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e0af-131">CommonParameters</span></span>
<span data-ttu-id="7e0af-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e0af-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e0af-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e0af-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e0af-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e0af-134">INPUTS</span></span>

### <span data-ttu-id="7e0af-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7e0af-135">None</span></span>

## <span data-ttu-id="7e0af-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e0af-136">OUTPUTS</span></span>

### <span data-ttu-id="7e0af-137">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngineRule</span><span class="sxs-lookup"><span data-stu-id="7e0af-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span></span>

## <span data-ttu-id="7e0af-138">Note</span><span class="sxs-lookup"><span data-stu-id="7e0af-138">NOTES</span></span>

## <span data-ttu-id="7e0af-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e0af-139">RELATED LINKS</span></span>
