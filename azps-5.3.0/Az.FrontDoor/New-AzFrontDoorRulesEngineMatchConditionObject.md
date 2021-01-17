---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesenginematchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
ms.openlocfilehash: 991d3233dd484025e699bba455b7d43e86f586e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476304"
---
# <span data-ttu-id="a598d-101">New-AzFrontDoorRulesEngineMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="a598d-101">New-AzFrontDoorRulesEngineMatchConditionObject</span></span>

## <span data-ttu-id="a598d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a598d-102">SYNOPSIS</span></span>
<span data-ttu-id="a598d-103">Crea un oggetto PSRulesEngineMatchCondition per la creazione di una regola del motore regole.</span><span class="sxs-lookup"><span data-stu-id="a598d-103">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="a598d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a598d-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable <PSRulesEngineMatchVariable>
 -MatchValue <String[]> [-Selector <String>] [-Operator <PSRulesEngineOperator>] [-NegateCondition <Boolean>]
 [-Transform <PSTransform[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a598d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a598d-105">DESCRIPTION</span></span>
<span data-ttu-id="a598d-106">Crea un oggetto PSRulesEngineMatchCondition per la creazione di una regola del motore regole.</span><span class="sxs-lookup"><span data-stu-id="a598d-106">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="a598d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a598d-107">EXAMPLES</span></span>

### <span data-ttu-id="a598d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a598d-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable RequestHeader -Operator Equal -MatchValue allowoverride -Transform "LowerCase", "UpperCase"-Selector Rules-Engine-Route-Forward -NegateCondition $false

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transform                : {Lowercase, Uppercase}
```

<span data-ttu-id="a598d-109">Greate un nuovo oggetto PSRulesEngineMatchCondition.</span><span class="sxs-lookup"><span data-stu-id="a598d-109">Greate a new PSRulesEngineMatchCondition object.</span></span>

## <span data-ttu-id="a598d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a598d-110">PARAMETERS</span></span>

### <span data-ttu-id="a598d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a598d-111">-DefaultProfile</span></span>
<span data-ttu-id="a598d-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a598d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a598d-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="a598d-113">-MatchValue</span></span>
<span data-ttu-id="a598d-114">Confrontare i valori da confrontare.</span><span class="sxs-lookup"><span data-stu-id="a598d-114">Match values to match against.</span></span>
<span data-ttu-id="a598d-115">L'operatore si applicherà a ogni valore qui con o semantica.</span><span class="sxs-lookup"><span data-stu-id="a598d-115">The operator will apply to each value in here with OR semantics.</span></span>
<span data-ttu-id="a598d-116">Se uno di essi corrisponde alla variabile con l'operatore indicato, questa condizione di corrispondenza viene considerata una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="a598d-116">If any of them match the variable with the given operator this match condition is considered a match.</span></span>

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

### <span data-ttu-id="a598d-117">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="a598d-117">-MatchVariable</span></span>
<span data-ttu-id="a598d-118">Associa variabile.</span><span class="sxs-lookup"><span data-stu-id="a598d-118">Match Variable.</span></span>
<span data-ttu-id="a598d-119">I valori possibili sono mobile, IndirizzoRemoto, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, nomefilerichiesta, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span><span class="sxs-lookup"><span data-stu-id="a598d-119">Possible values are IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span></span>

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

### <span data-ttu-id="a598d-120">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="a598d-120">-NegateCondition</span></span>
<span data-ttu-id="a598d-121">Descrive se la condizione è negata o meno</span><span class="sxs-lookup"><span data-stu-id="a598d-121">Describes if this is negate condition or not</span></span>

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

### <span data-ttu-id="a598d-122">-Operator</span><span class="sxs-lookup"><span data-stu-id="a598d-122">-Operator</span></span>
<span data-ttu-id="a598d-123">Descrive l'operatore da applicare alla condizione di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="a598d-123">Describes operator to apply to the match condition.</span></span>
<span data-ttu-id="a598d-124">I valori possibili sono any, IPMatch, geomatch, EQUAL, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, Iniziacon.</span><span class="sxs-lookup"><span data-stu-id="a598d-124">Possible values are Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span></span>

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

### <span data-ttu-id="a598d-125">-Selector</span><span class="sxs-lookup"><span data-stu-id="a598d-125">-Selector</span></span>
<span data-ttu-id="a598d-126">Nome del selettore in RequestHeader o RequestBody da associare</span><span class="sxs-lookup"><span data-stu-id="a598d-126">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="a598d-127">-Transform</span><span class="sxs-lookup"><span data-stu-id="a598d-127">-Transform</span></span>
<span data-ttu-id="a598d-128">Elenco delle trasformazioni applicate prima della corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="a598d-128">List of what transforms are applied before matching.</span></span> <span data-ttu-id="a598d-129">I singoli valori di trasformazione possibili sono minuscole, maiuscole, Trim, UrlDecode, UrlEncode, RemoveNulls.</span><span class="sxs-lookup"><span data-stu-id="a598d-129">Possible individual transform values are Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls.</span></span>

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

### <span data-ttu-id="a598d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a598d-130">CommonParameters</span></span>
<span data-ttu-id="a598d-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a598d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a598d-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a598d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a598d-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a598d-133">INPUTS</span></span>

### <span data-ttu-id="a598d-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a598d-134">None</span></span>

## <span data-ttu-id="a598d-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a598d-135">OUTPUTS</span></span>

### <span data-ttu-id="a598d-136">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngineMatchCondition</span><span class="sxs-lookup"><span data-stu-id="a598d-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span></span>

## <span data-ttu-id="a598d-137">Note</span><span class="sxs-lookup"><span data-stu-id="a598d-137">NOTES</span></span>

## <span data-ttu-id="a598d-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a598d-138">RELATED LINKS</span></span>
