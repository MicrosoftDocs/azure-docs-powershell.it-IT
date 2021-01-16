---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesenginematchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
ms.openlocfilehash: 991d3233dd484025e699bba455b7d43e86f586e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328658"
---
# <span data-ttu-id="eedfe-101">New-AzFrontDoorRulesEngineMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="eedfe-101">New-AzFrontDoorRulesEngineMatchConditionObject</span></span>

## <span data-ttu-id="eedfe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eedfe-102">SYNOPSIS</span></span>
<span data-ttu-id="eedfe-103">Crea un oggetto PSRulesEngineMatchCondition per la creazione di una regola del motore regole.</span><span class="sxs-lookup"><span data-stu-id="eedfe-103">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="eedfe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eedfe-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable <PSRulesEngineMatchVariable>
 -MatchValue <String[]> [-Selector <String>] [-Operator <PSRulesEngineOperator>] [-NegateCondition <Boolean>]
 [-Transform <PSTransform[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eedfe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eedfe-105">DESCRIPTION</span></span>
<span data-ttu-id="eedfe-106">Crea un oggetto PSRulesEngineMatchCondition per la creazione di una regola del motore regole.</span><span class="sxs-lookup"><span data-stu-id="eedfe-106">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="eedfe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eedfe-107">EXAMPLES</span></span>

### <span data-ttu-id="eedfe-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eedfe-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable RequestHeader -Operator Equal -MatchValue allowoverride -Transform "LowerCase", "UpperCase"-Selector Rules-Engine-Route-Forward -NegateCondition $false

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transform                : {Lowercase, Uppercase}
```

<span data-ttu-id="eedfe-109">Greate un nuovo oggetto PSRulesEngineMatchCondition.</span><span class="sxs-lookup"><span data-stu-id="eedfe-109">Greate a new PSRulesEngineMatchCondition object.</span></span>

## <span data-ttu-id="eedfe-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eedfe-110">PARAMETERS</span></span>

### <span data-ttu-id="eedfe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eedfe-111">-DefaultProfile</span></span>
<span data-ttu-id="eedfe-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eedfe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eedfe-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="eedfe-113">-MatchValue</span></span>
<span data-ttu-id="eedfe-114">Confrontare i valori da confrontare.</span><span class="sxs-lookup"><span data-stu-id="eedfe-114">Match values to match against.</span></span>
<span data-ttu-id="eedfe-115">L'operatore si applicherà a ogni valore qui con o semantica.</span><span class="sxs-lookup"><span data-stu-id="eedfe-115">The operator will apply to each value in here with OR semantics.</span></span>
<span data-ttu-id="eedfe-116">Se uno di essi corrisponde alla variabile con l'operatore indicato, questa condizione di corrispondenza viene considerata una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="eedfe-116">If any of them match the variable with the given operator this match condition is considered a match.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eedfe-117">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="eedfe-117">-MatchVariable</span></span>
<span data-ttu-id="eedfe-118">Associa variabile.</span><span class="sxs-lookup"><span data-stu-id="eedfe-118">Match Variable.</span></span>
<span data-ttu-id="eedfe-119">I valori possibili sono mobile, IndirizzoRemoto, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, nomefilerichiesta, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span><span class="sxs-lookup"><span data-stu-id="eedfe-119">Possible values are IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: IsMobile, RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestPath, RequestFilename, RequestFilenameExtension, RequestHeader, RequestBody, RequestScheme

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eedfe-120">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="eedfe-120">-NegateCondition</span></span>
<span data-ttu-id="eedfe-121">Descrive se la condizione è negata o meno</span><span class="sxs-lookup"><span data-stu-id="eedfe-121">Describes if this is negate condition or not</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eedfe-122">-Operator</span><span class="sxs-lookup"><span data-stu-id="eedfe-122">-Operator</span></span>
<span data-ttu-id="eedfe-123">Descrive l'operatore da applicare alla condizione di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="eedfe-123">Describes operator to apply to the match condition.</span></span>
<span data-ttu-id="eedfe-124">I valori possibili sono any, IPMatch, geomatch, EQUAL, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, Iniziacon.</span><span class="sxs-lookup"><span data-stu-id="eedfe-124">Possible values are Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineOperator
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eedfe-125">-Selector</span><span class="sxs-lookup"><span data-stu-id="eedfe-125">-Selector</span></span>
<span data-ttu-id="eedfe-126">Nome del selettore in RequestHeader o RequestBody da associare</span><span class="sxs-lookup"><span data-stu-id="eedfe-126">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="eedfe-127">-Transform</span><span class="sxs-lookup"><span data-stu-id="eedfe-127">-Transform</span></span>
<span data-ttu-id="eedfe-128">Elenco delle trasformazioni applicate prima della corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="eedfe-128">List of what transforms are applied before matching.</span></span> <span data-ttu-id="eedfe-129">I singoli valori di trasformazione possibili sono minuscole, maiuscole, Trim, UrlDecode, UrlEncode, RemoveNulls.</span><span class="sxs-lookup"><span data-stu-id="eedfe-129">Possible individual transform values are Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSTransform[]
Parameter Sets: (All)
Aliases:
Accepted values: Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eedfe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eedfe-130">CommonParameters</span></span>
<span data-ttu-id="eedfe-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eedfe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eedfe-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eedfe-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eedfe-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eedfe-133">INPUTS</span></span>

### <span data-ttu-id="eedfe-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="eedfe-134">None</span></span>

## <span data-ttu-id="eedfe-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eedfe-135">OUTPUTS</span></span>

### <span data-ttu-id="eedfe-136">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngineMatchCondition</span><span class="sxs-lookup"><span data-stu-id="eedfe-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span></span>

## <span data-ttu-id="eedfe-137">Note</span><span class="sxs-lookup"><span data-stu-id="eedfe-137">NOTES</span></span>

## <span data-ttu-id="eedfe-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eedfe-138">RELATED LINKS</span></span>
