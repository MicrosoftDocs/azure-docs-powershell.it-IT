---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafmatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
ms.openlocfilehash: e67841073d6c7342e0bb88c52809a9c45d92f82f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970845"
---
# <span data-ttu-id="0c87b-101">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="0c87b-101">New-AzFrontDoorWafMatchConditionObject</span></span>

## <span data-ttu-id="0c87b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c87b-102">SYNOPSIS</span></span>
<span data-ttu-id="0c87b-103">Creare un oggetto MatchCondition per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="0c87b-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="0c87b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c87b-104">SYNTAX</span></span>

```
New-AzFrontDoorWafMatchConditionObject -MatchVariable <String> -OperatorProperty <String>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c87b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0c87b-105">DESCRIPTION</span></span>
<span data-ttu-id="0c87b-106">Creare un oggetto MatchCondition per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="0c87b-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="0c87b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c87b-107">EXAMPLES</span></span>

### <span data-ttu-id="0c87b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0c87b-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {Windows}  User-Agent           False
```

### <span data-ttu-id="0c87b-109">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0c87b-109">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "WINDOWS" -Transform Uppercase


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {WINDOWS}  User-Agent           False {Uppercase}
```

<span data-ttu-id="0c87b-110">Creare un oggetto MatchCondition</span><span class="sxs-lookup"><span data-stu-id="0c87b-110">Create a MatchCondition object</span></span>

## <span data-ttu-id="0c87b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c87b-111">PARAMETERS</span></span>

### <span data-ttu-id="0c87b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c87b-112">-DefaultProfile</span></span>
<span data-ttu-id="0c87b-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c87b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c87b-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="0c87b-114">-MatchValue</span></span>
<span data-ttu-id="0c87b-115">Valore corrispondente.</span><span class="sxs-lookup"><span data-stu-id="0c87b-115">Match value.</span></span>

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

### <span data-ttu-id="0c87b-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="0c87b-116">-MatchVariable</span></span>
<span data-ttu-id="0c87b-117">Variabile Match.</span><span class="sxs-lookup"><span data-stu-id="0c87b-117">Match Variable.</span></span>
<span data-ttu-id="0c87b-118">I valori possibili includono: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestHeader', 'SocketAddr'</span><span class="sxs-lookup"><span data-stu-id="0c87b-118">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody', 'SocketAddr'</span></span>

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

### <span data-ttu-id="0c87b-119">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="0c87b-119">-NegateCondition</span></span>
<span data-ttu-id="0c87b-120">Descrive se questa condizione è negata o se il valore predefinito è falso</span><span class="sxs-lookup"><span data-stu-id="0c87b-120">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="0c87b-121">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="0c87b-121">-OperatorProperty</span></span>
<span data-ttu-id="0c87b-122">Descrive l'operatore di cui trovare una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="0c87b-122">Describes operator to be matched.</span></span>
<span data-ttu-id="0c87b-123">I valori possibili includono: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span><span class="sxs-lookup"><span data-stu-id="0c87b-123">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span></span>

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

### <span data-ttu-id="0c87b-124">-Selettore</span><span class="sxs-lookup"><span data-stu-id="0c87b-124">-Selector</span></span>
<span data-ttu-id="0c87b-125">Nome del selettore in RequestHeader o RequestHeader per cui trovare una corrispondenza</span><span class="sxs-lookup"><span data-stu-id="0c87b-125">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="0c87b-126">-Transform</span><span class="sxs-lookup"><span data-stu-id="0c87b-126">-Transform</span></span>
<span data-ttu-id="0c87b-127">Trasformazioni da applicare.</span><span class="sxs-lookup"><span data-stu-id="0c87b-127">Transforms to apply.</span></span> <span data-ttu-id="0c87b-128">I valori possibili includono: 'Tutto minuscole', 'Tutto maiuscole', 'Trim', 'URLDecode', 'UrlEncode', 'RemoveNulls'.</span><span class="sxs-lookup"><span data-stu-id="0c87b-128">Possible values include: 'Lowercase', 'Uppercase', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span></span>

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

### <span data-ttu-id="0c87b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c87b-129">CommonParameters</span></span>
<span data-ttu-id="0c87b-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c87b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c87b-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0c87b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c87b-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="0c87b-132">INPUTS</span></span>

### <span data-ttu-id="0c87b-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0c87b-133">None</span></span>

## <span data-ttu-id="0c87b-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c87b-134">OUTPUTS</span></span>

### <span data-ttu-id="0c87b-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="0c87b-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="0c87b-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="0c87b-136">NOTES</span></span>

## <span data-ttu-id="0c87b-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c87b-137">RELATED LINKS</span></span>

[<span data-ttu-id="0c87b-138">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="0c87b-138">New-AzFrontDoorWafCustomRuleObject</span></span>](./New-AzFrontDoorWafCustomRuleObject.md)
