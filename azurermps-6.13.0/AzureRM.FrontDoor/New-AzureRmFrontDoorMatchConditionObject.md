---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
ms.openlocfilehash: 70ab8b592c550280f424f9c0a4bfced877942edc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686391"
---
# <span data-ttu-id="28f0c-101">New-AzureRmFrontDoorMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="28f0c-101">New-AzureRmFrontDoorMatchConditionObject</span></span>

## <span data-ttu-id="28f0c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28f0c-102">SYNOPSIS</span></span>
<span data-ttu-id="28f0c-103">Creare un oggetto MatchCondition per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="28f0c-103">Create MatchCondition Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28f0c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28f0c-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorMatchConditionObject -MatchVariable <PSMatchVariable>
 -OperatorProperty <PSOperatorProperty> -MatchValue <String[]> [-Selector <String>]
 [-NegateCondition <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28f0c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28f0c-105">DESCRIPTION</span></span>
<span data-ttu-id="28f0c-106">Creare un oggetto MatchCondition per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="28f0c-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="28f0c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28f0c-107">EXAMPLES</span></span>

### <span data-ttu-id="28f0c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="28f0c-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "UserAgent" -MatchValue "Windows"


MatchVariable    : RequestHeader
OperatorProperty : Contains
MatchValue       : {Windows}
Selector         : UserAgent
NegateCondition  : False
```

<span data-ttu-id="28f0c-109">Creare un oggetto MatchCondition</span><span class="sxs-lookup"><span data-stu-id="28f0c-109">Create a MatchCondition object</span></span>

## <span data-ttu-id="28f0c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28f0c-110">PARAMETERS</span></span>

### <span data-ttu-id="28f0c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28f0c-111">-DefaultProfile</span></span>
<span data-ttu-id="28f0c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28f0c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f0c-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="28f0c-113">-MatchValue</span></span>
<span data-ttu-id="28f0c-114">Valore di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="28f0c-114">Match value.</span></span>

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

### <span data-ttu-id="28f0c-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="28f0c-115">-MatchVariable</span></span>
<span data-ttu-id="28f0c-116">Associa variabile.</span><span class="sxs-lookup"><span data-stu-id="28f0c-116">Match Variable.</span></span>
<span data-ttu-id="28f0c-117">I valori possibili includono: "IndirizzoRemoto", "RequestMethod", "QueryString", "postargs", "RequestUri", "RequestHeader", "RequestBody"</span><span class="sxs-lookup"><span data-stu-id="28f0c-117">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

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

### <span data-ttu-id="28f0c-118">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="28f0c-118">-NegateCondition</span></span>
<span data-ttu-id="28f0c-119">Descrive se si tratta di una condizione di negazione o se non il valore predefinito è false</span><span class="sxs-lookup"><span data-stu-id="28f0c-119">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="28f0c-120">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="28f0c-120">-OperatorProperty</span></span>
<span data-ttu-id="28f0c-121">Descrive l'operatore che deve essere abbinato.</span><span class="sxs-lookup"><span data-stu-id="28f0c-121">Describes operator to be matched.</span></span>
<span data-ttu-id="28f0c-122">I valori possibili includono: "qualsiasi", "IPMatch", "geomatch", "equal", "Contains", "LessThan", "GreaterThan", "LessThanOrEqual", "GreaterThanOrEqual", "BeginsWith", "Iniziacon" "</span><span class="sxs-lookup"><span data-stu-id="28f0c-122">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith''</span></span>

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

### <span data-ttu-id="28f0c-123">-Selector</span><span class="sxs-lookup"><span data-stu-id="28f0c-123">-Selector</span></span>
<span data-ttu-id="28f0c-124">Nome del selettore in RequestHeader o RequestBody da associare</span><span class="sxs-lookup"><span data-stu-id="28f0c-124">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="28f0c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28f0c-125">CommonParameters</span></span>
<span data-ttu-id="28f0c-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28f0c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28f0c-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28f0c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28f0c-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28f0c-128">INPUTS</span></span>

### <span data-ttu-id="28f0c-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="28f0c-129">None</span></span>

## <span data-ttu-id="28f0c-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28f0c-130">OUTPUTS</span></span>

### <span data-ttu-id="28f0c-131">Microsoft. Azure. Commands. FrontDoor. Models. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="28f0c-131">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="28f0c-132">Note</span><span class="sxs-lookup"><span data-stu-id="28f0c-132">NOTES</span></span>

## <span data-ttu-id="28f0c-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28f0c-133">RELATED LINKS</span></span>

[<span data-ttu-id="28f0c-134">New-AzureRmFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="28f0c-134">New-AzureRmFrontDoorCustomRuleObject</span></span>](./New-AzureRmFrontDoorCustomRuleObject.md)
