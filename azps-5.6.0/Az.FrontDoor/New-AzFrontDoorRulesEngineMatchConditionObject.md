---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorrulesenginematchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
ms.openlocfilehash: 4f35b20b7c17a0cd809cb5964fbecfa429b581bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970957"
---
# <span data-ttu-id="8a675-101">New-AzFrontDoorRulesEngineMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="8a675-101">New-AzFrontDoorRulesEngineMatchConditionObject</span></span>

## <span data-ttu-id="8a675-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a675-102">SYNOPSIS</span></span>
<span data-ttu-id="8a675-103">Creare un oggetto PSRulesMatchCondition per creare una regola del motore di regole.</span><span class="sxs-lookup"><span data-stu-id="8a675-103">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="8a675-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a675-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable <PSRulesEngineMatchVariable>
 -MatchValue <String[]> [-Selector <String>] [-Operator <PSRulesEngineOperator>] [-NegateCondition <Boolean>]
 [-Transform <PSTransform[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a675-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8a675-105">DESCRIPTION</span></span>
<span data-ttu-id="8a675-106">Creare un oggetto PSRulesMatchCondition per creare una regola del motore di regole.</span><span class="sxs-lookup"><span data-stu-id="8a675-106">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="8a675-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a675-107">EXAMPLES</span></span>

### <span data-ttu-id="8a675-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8a675-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable RequestHeader -Operator Equal -MatchValue allowoverride -Transform "LowerCase", "UpperCase"-Selector Rules-Engine-Route-Forward -NegateCondition $false

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transform                : {Lowercase, Uppercase}
```

<span data-ttu-id="8a675-109">Creare un nuovo oggetto PSRulesMatchCondition.</span><span class="sxs-lookup"><span data-stu-id="8a675-109">Greate a new PSRulesEngineMatchCondition object.</span></span>

## <span data-ttu-id="8a675-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a675-110">PARAMETERS</span></span>

### <span data-ttu-id="8a675-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a675-111">-DefaultProfile</span></span>
<span data-ttu-id="8a675-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8a675-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a675-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="8a675-113">-MatchValue</span></span>
<span data-ttu-id="8a675-114">Trovare corrispondenze per i valori in base a cui trovare una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="8a675-114">Match values to match against.</span></span>
<span data-ttu-id="8a675-115">L'operatore verrà applicato a ogni valore in questa funzione con semantica OR.</span><span class="sxs-lookup"><span data-stu-id="8a675-115">The operator will apply to each value in here with OR semantics.</span></span>
<span data-ttu-id="8a675-116">Se uno o più operatori corrispondono alla variabile con l'operatore specificato, questa condizione di corrispondenza viene considerata una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="8a675-116">If any of them match the variable with the given operator this match condition is considered a match.</span></span>

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

### <span data-ttu-id="8a675-117">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="8a675-117">-MatchVariable</span></span>
<span data-ttu-id="8a675-118">Variabile Match.</span><span class="sxs-lookup"><span data-stu-id="8a675-118">Match Variable.</span></span>
<span data-ttu-id="8a675-119">I valori possibili sono IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestHeader, RequestScheme</span><span class="sxs-lookup"><span data-stu-id="8a675-119">Possible values are IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span></span>

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

### <span data-ttu-id="8a675-120">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="8a675-120">-NegateCondition</span></span>
<span data-ttu-id="8a675-121">Descrive se la condizione è negata o meno</span><span class="sxs-lookup"><span data-stu-id="8a675-121">Describes if this is negate condition or not</span></span>

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

### <span data-ttu-id="8a675-122">-Operatore</span><span class="sxs-lookup"><span data-stu-id="8a675-122">-Operator</span></span>
<span data-ttu-id="8a675-123">Descrive l'operatore da applicare alla condizione di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="8a675-123">Describes operator to apply to the match condition.</span></span>
<span data-ttu-id="8a675-124">I valori possibili sono Any, IPMatch, GeoMatch, Equal, Contains, LessWith, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span><span class="sxs-lookup"><span data-stu-id="8a675-124">Possible values are Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span></span>

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

### <span data-ttu-id="8a675-125">-Selettore</span><span class="sxs-lookup"><span data-stu-id="8a675-125">-Selector</span></span>
<span data-ttu-id="8a675-126">Nome del selettore in RequestHeader o RequestHeader per cui trovare una corrispondenza</span><span class="sxs-lookup"><span data-stu-id="8a675-126">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="8a675-127">-Transform</span><span class="sxs-lookup"><span data-stu-id="8a675-127">-Transform</span></span>
<span data-ttu-id="8a675-128">Elenco delle trasformazioni applicate prima della corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="8a675-128">List of what transforms are applied before matching.</span></span> <span data-ttu-id="8a675-129">I singoli valori di trasformazione possibili sono Minuscole, Tutto Maiuscole, Trim, URLDecode, UrlEncode, RimuoviNull.</span><span class="sxs-lookup"><span data-stu-id="8a675-129">Possible individual transform values are Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls.</span></span>

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

### <span data-ttu-id="8a675-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a675-130">CommonParameters</span></span>
<span data-ttu-id="8a675-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a675-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a675-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8a675-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a675-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="8a675-133">INPUTS</span></span>

### <span data-ttu-id="8a675-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8a675-134">None</span></span>

## <span data-ttu-id="8a675-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a675-135">OUTPUTS</span></span>

### <span data-ttu-id="8a675-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesMatchMatchCondition</span><span class="sxs-lookup"><span data-stu-id="8a675-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span></span>

## <span data-ttu-id="8a675-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="8a675-137">NOTES</span></span>

## <span data-ttu-id="8a675-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a675-138">RELATED LINKS</span></span>
