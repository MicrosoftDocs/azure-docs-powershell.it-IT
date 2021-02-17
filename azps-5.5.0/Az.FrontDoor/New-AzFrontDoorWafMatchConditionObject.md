---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
ms.openlocfilehash: 0340cbf8c71b0ab117f1ff967ec7c3bb3e32b8f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188415"
---
# <span data-ttu-id="50328-101">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="50328-101">New-AzFrontDoorWafMatchConditionObject</span></span>

## <span data-ttu-id="50328-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50328-102">SYNOPSIS</span></span>
<span data-ttu-id="50328-103">Creare un oggetto MatchCondition per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="50328-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="50328-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50328-104">SYNTAX</span></span>

```
New-AzFrontDoorWafMatchConditionObject -MatchVariable <String> -OperatorProperty <String>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50328-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="50328-105">DESCRIPTION</span></span>
<span data-ttu-id="50328-106">Creare un oggetto MatchCondition per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="50328-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="50328-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50328-107">EXAMPLES</span></span>

### <span data-ttu-id="50328-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="50328-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {Windows}  User-Agent           False
```

### <span data-ttu-id="50328-109">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="50328-109">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "WINDOWS" -Transform Uppercase


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {WINDOWS}  User-Agent           False {Uppercase}
```

<span data-ttu-id="50328-110">Creare un oggetto MatchCondition</span><span class="sxs-lookup"><span data-stu-id="50328-110">Create a MatchCondition object</span></span>

## <span data-ttu-id="50328-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50328-111">PARAMETERS</span></span>

### <span data-ttu-id="50328-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50328-112">-DefaultProfile</span></span>
<span data-ttu-id="50328-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50328-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50328-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="50328-114">-MatchValue</span></span>
<span data-ttu-id="50328-115">Valore corrispondente.</span><span class="sxs-lookup"><span data-stu-id="50328-115">Match value.</span></span>

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

### <span data-ttu-id="50328-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="50328-116">-MatchVariable</span></span>
<span data-ttu-id="50328-117">Variabile Match.</span><span class="sxs-lookup"><span data-stu-id="50328-117">Match Variable.</span></span>
<span data-ttu-id="50328-118">I valori possibili includono: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestHeader', 'SocketAddr'</span><span class="sxs-lookup"><span data-stu-id="50328-118">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody', 'SocketAddr'</span></span>

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

### <span data-ttu-id="50328-119">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="50328-119">-NegateCondition</span></span>
<span data-ttu-id="50328-120">Descrive se questa condizione è negata o se il valore predefinito è falso</span><span class="sxs-lookup"><span data-stu-id="50328-120">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="50328-121">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="50328-121">-OperatorProperty</span></span>
<span data-ttu-id="50328-122">Descrive l'operatore di cui trovare una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="50328-122">Describes operator to be matched.</span></span>
<span data-ttu-id="50328-123">I valori possibili includono: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span><span class="sxs-lookup"><span data-stu-id="50328-123">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span></span>

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

### <span data-ttu-id="50328-124">-Selettore</span><span class="sxs-lookup"><span data-stu-id="50328-124">-Selector</span></span>
<span data-ttu-id="50328-125">Nome del selettore in RequestHeader o RequestHeader per cui trovare una corrispondenza</span><span class="sxs-lookup"><span data-stu-id="50328-125">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="50328-126">-Transform</span><span class="sxs-lookup"><span data-stu-id="50328-126">-Transform</span></span>
<span data-ttu-id="50328-127">Trasformazioni da applicare.</span><span class="sxs-lookup"><span data-stu-id="50328-127">Transforms to apply.</span></span> <span data-ttu-id="50328-128">I valori possibili includono: 'Tutto minuscole', 'Tutto maiuscole', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span><span class="sxs-lookup"><span data-stu-id="50328-128">Possible values include: 'Lowercase', 'Uppercase', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span></span>

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

### <span data-ttu-id="50328-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50328-129">CommonParameters</span></span>
<span data-ttu-id="50328-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50328-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50328-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="50328-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50328-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="50328-132">INPUTS</span></span>

### <span data-ttu-id="50328-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="50328-133">None</span></span>

## <span data-ttu-id="50328-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50328-134">OUTPUTS</span></span>

### <span data-ttu-id="50328-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="50328-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="50328-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="50328-136">NOTES</span></span>

## <span data-ttu-id="50328-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50328-137">RELATED LINKS</span></span>

[<span data-ttu-id="50328-138">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="50328-138">New-AzFrontDoorWafCustomRuleObject</span></span>](./New-AzFrontDoorWafCustomRuleObject.md)
