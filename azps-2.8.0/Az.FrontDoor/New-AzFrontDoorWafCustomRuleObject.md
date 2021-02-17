---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: c59e0f90ae8b6d7839c7bb845b56e31a42b2d033
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412793"
---
# <span data-ttu-id="6c7b2-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="6c7b2-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="6c7b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c7b2-102">SYNOPSIS</span></span>
<span data-ttu-id="6c7b2-103">Creare un oggetto CustomRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="6c7b2-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="6c7b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c7b2-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c7b2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6c7b2-105">DESCRIPTION</span></span>
<span data-ttu-id="6c7b2-106">Creare un oggetto CustomRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="6c7b2-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="6c7b2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c7b2-107">EXAMPLES</span></span>

### <span data-ttu-id="6c7b2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6c7b2-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="6c7b2-109">Creare un oggetto CustomRule</span><span class="sxs-lookup"><span data-stu-id="6c7b2-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="6c7b2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c7b2-110">PARAMETERS</span></span>

### <span data-ttu-id="6c7b2-111">-Action</span><span class="sxs-lookup"><span data-stu-id="6c7b2-111">-Action</span></span>
<span data-ttu-id="6c7b2-112">Tipo di azioni.</span><span class="sxs-lookup"><span data-stu-id="6c7b2-112">Type of Actions.</span></span>
<span data-ttu-id="6c7b2-113">I valori possibili includono: 'Consenti', 'Blocca', 'Log'</span><span class="sxs-lookup"><span data-stu-id="6c7b2-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="6c7b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c7b2-114">-DefaultProfile</span></span>
<span data-ttu-id="6c7b2-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c7b2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c7b2-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="6c7b2-116">-MatchCondition</span></span>
<span data-ttu-id="6c7b2-117">Elenco di condizioni di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="6c7b2-117">List of match conditions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c7b2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6c7b2-118">-Name</span></span>
<span data-ttu-id="6c7b2-119">Nome della regola</span><span class="sxs-lookup"><span data-stu-id="6c7b2-119">Name of the rule</span></span>

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

### <span data-ttu-id="6c7b2-120">-Priority</span><span class="sxs-lookup"><span data-stu-id="6c7b2-120">-Priority</span></span>
<span data-ttu-id="6c7b2-121">Descrive la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="6c7b2-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="6c7b2-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="6c7b2-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="6c7b2-123">Durata del limite di tariffa.</span><span class="sxs-lookup"><span data-stu-id="6c7b2-123">Rate limit duration.</span></span> <span data-ttu-id="6c7b2-124">Impostazione predefinita - 1 minuto</span><span class="sxs-lookup"><span data-stu-id="6c7b2-124">Default - 1 minute</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c7b2-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="6c7b2-125">-RateLimitThreshold</span></span>
<span data-ttu-id="6c7b2-126">Soglia del limite di tariffa</span><span class="sxs-lookup"><span data-stu-id="6c7b2-126">Rate limit threshold</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c7b2-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="6c7b2-127">-RuleType</span></span>
<span data-ttu-id="6c7b2-128">Tipo di regola.</span><span class="sxs-lookup"><span data-stu-id="6c7b2-128">Type of the rule.</span></span>
<span data-ttu-id="6c7b2-129">I valori possibili includono: 'MatchRule', 'RateLimitRule'</span><span class="sxs-lookup"><span data-stu-id="6c7b2-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="6c7b2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c7b2-130">CommonParameters</span></span>
<span data-ttu-id="6c7b2-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c7b2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c7b2-132">Per altre informazioni, [vedere](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6c7b2-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c7b2-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="6c7b2-133">INPUTS</span></span>

### <span data-ttu-id="6c7b2-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6c7b2-134">None</span></span>

## <span data-ttu-id="6c7b2-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c7b2-135">OUTPUTS</span></span>

### <span data-ttu-id="6c7b2-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="6c7b2-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="6c7b2-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="6c7b2-137">NOTES</span></span>

## <span data-ttu-id="6c7b2-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c7b2-138">RELATED LINKS</span></span>

<span data-ttu-id="6c7b2-139">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="6c7b2-139">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
