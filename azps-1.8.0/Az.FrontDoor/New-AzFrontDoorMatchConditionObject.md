---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorMatchConditionObject.md
ms.openlocfilehash: ed711160bf761fe7b28f02a94d1ab4ffa6fdb59f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836136"
---
# <span data-ttu-id="121e2-101">New-AzFrontDoorMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="121e2-101">New-AzFrontDoorMatchConditionObject</span></span>

## <span data-ttu-id="121e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="121e2-102">SYNOPSIS</span></span>
<span data-ttu-id="121e2-103">Creare un oggetto MatchCondition per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="121e2-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="121e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="121e2-104">SYNTAX</span></span>

```
New-AzFrontDoorMatchConditionObject -MatchVariable <PSMatchVariable> -OperatorProperty <PSOperatorProperty>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="121e2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="121e2-105">DESCRIPTION</span></span>
<span data-ttu-id="121e2-106">Creare un oggetto MatchCondition per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="121e2-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="121e2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="121e2-107">EXAMPLES</span></span>

### <span data-ttu-id="121e2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="121e2-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition
------------- ---------------- ---------- --------   ---------------
RequestHeader         Contains {Windows}  User-Agent           False
```

<span data-ttu-id="121e2-109">Creare un oggetto MatchCondition</span><span class="sxs-lookup"><span data-stu-id="121e2-109">Create a MatchCondition object</span></span>

## <span data-ttu-id="121e2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="121e2-110">PARAMETERS</span></span>

### <span data-ttu-id="121e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="121e2-111">-DefaultProfile</span></span>
<span data-ttu-id="121e2-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="121e2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="121e2-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="121e2-113">-MatchValue</span></span>
<span data-ttu-id="121e2-114">Valore di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="121e2-114">Match value.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="121e2-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="121e2-115">-MatchVariable</span></span>
<span data-ttu-id="121e2-116">Associa variabile.</span><span class="sxs-lookup"><span data-stu-id="121e2-116">Match Variable.</span></span>
<span data-ttu-id="121e2-117">I valori possibili includono: "IndirizzoRemoto", "RequestMethod", "QueryString", "postargs", "RequestUri", "RequestHeader", "RequestBody"</span><span class="sxs-lookup"><span data-stu-id="121e2-117">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeader, RequestBody

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="121e2-118">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="121e2-118">-NegateCondition</span></span>
<span data-ttu-id="121e2-119">Descrive se si tratta di una condizione di negazione o se non il valore predefinito è false</span><span class="sxs-lookup"><span data-stu-id="121e2-119">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="121e2-120">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="121e2-120">-OperatorProperty</span></span>
<span data-ttu-id="121e2-121">Descrive l'operatore che deve essere abbinato.</span><span class="sxs-lookup"><span data-stu-id="121e2-121">Describes operator to be matched.</span></span>
<span data-ttu-id="121e2-122">I valori possibili includono: "qualsiasi", "IPMatch", "geomatch", "equal", "Contains", "LessThan", "GreaterThan", "LessThanOrEqual", "GreaterThanOrEqual", "BeginsWith", "Iniziacon" "</span><span class="sxs-lookup"><span data-stu-id="121e2-122">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith''</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSOperatorProperty
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="121e2-123">-Selector</span><span class="sxs-lookup"><span data-stu-id="121e2-123">-Selector</span></span>
<span data-ttu-id="121e2-124">Nome del selettore in RequestHeader o RequestBody da associare</span><span class="sxs-lookup"><span data-stu-id="121e2-124">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="121e2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="121e2-125">CommonParameters</span></span>
<span data-ttu-id="121e2-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="121e2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="121e2-127">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="121e2-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="121e2-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="121e2-128">INPUTS</span></span>

### <span data-ttu-id="121e2-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="121e2-129">None</span></span>

## <span data-ttu-id="121e2-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="121e2-130">OUTPUTS</span></span>

### <span data-ttu-id="121e2-131">Microsoft. Azure. Commands. FrontDoor. Models. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="121e2-131">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="121e2-132">Note</span><span class="sxs-lookup"><span data-stu-id="121e2-132">NOTES</span></span>

## <span data-ttu-id="121e2-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="121e2-133">RELATED LINKS</span></span>

[<span data-ttu-id="121e2-134">New-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="121e2-134">New-AzFrontDoorCustomRuleObject</span></span>](./New-AzFrontDoorCustomRuleObject.md)
