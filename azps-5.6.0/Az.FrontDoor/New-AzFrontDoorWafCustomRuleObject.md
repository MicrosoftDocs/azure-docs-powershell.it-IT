---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: cf74b21d2b07ddf8f92203c43e7005f81cbb2a69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970926"
---
# <span data-ttu-id="9cec2-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="9cec2-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="9cec2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cec2-102">SYNOPSIS</span></span>
<span data-ttu-id="9cec2-103">Creare un oggetto CustomRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="9cec2-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="9cec2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9cec2-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cec2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9cec2-105">DESCRIPTION</span></span>
<span data-ttu-id="9cec2-106">Creare un oggetto CustomRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="9cec2-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="9cec2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9cec2-107">EXAMPLES</span></span>

### <span data-ttu-id="9cec2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9cec2-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="9cec2-109">Creare un oggetto CustomRule</span><span class="sxs-lookup"><span data-stu-id="9cec2-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="9cec2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cec2-110">PARAMETERS</span></span>

### <span data-ttu-id="9cec2-111">-Action</span><span class="sxs-lookup"><span data-stu-id="9cec2-111">-Action</span></span>
<span data-ttu-id="9cec2-112">Tipo di azioni.</span><span class="sxs-lookup"><span data-stu-id="9cec2-112">Type of Actions.</span></span>
<span data-ttu-id="9cec2-113">I valori possibili includono: 'Consenti', 'Blocca', 'Log'</span><span class="sxs-lookup"><span data-stu-id="9cec2-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="9cec2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cec2-114">-DefaultProfile</span></span>
<span data-ttu-id="9cec2-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9cec2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cec2-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="9cec2-116">-EnabledState</span></span>
<span data-ttu-id="9cec2-117">Stato abilitato.</span><span class="sxs-lookup"><span data-stu-id="9cec2-117">Enabled State.</span></span> <span data-ttu-id="9cec2-118">I valori possibili includono: "Abilitato", "Disabilitato".</span><span class="sxs-lookup"><span data-stu-id="9cec2-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="9cec2-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="9cec2-119">-MatchCondition</span></span>
<span data-ttu-id="9cec2-120">Elenco di condizioni di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="9cec2-120">List of match conditions.</span></span>

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

### <span data-ttu-id="9cec2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9cec2-121">-Name</span></span>
<span data-ttu-id="9cec2-122">Nome della regola</span><span class="sxs-lookup"><span data-stu-id="9cec2-122">Name of the rule</span></span>

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

### <span data-ttu-id="9cec2-123">-Priority</span><span class="sxs-lookup"><span data-stu-id="9cec2-123">-Priority</span></span>
<span data-ttu-id="9cec2-124">Descrive la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="9cec2-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="9cec2-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="9cec2-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="9cec2-126">Durata del limite di tariffa.</span><span class="sxs-lookup"><span data-stu-id="9cec2-126">Rate limit duration.</span></span> <span data-ttu-id="9cec2-127">Impostazione predefinita - 1 minuto</span><span class="sxs-lookup"><span data-stu-id="9cec2-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="9cec2-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="9cec2-128">-RateLimitThreshold</span></span>
<span data-ttu-id="9cec2-129">Soglia del limite di tariffa</span><span class="sxs-lookup"><span data-stu-id="9cec2-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="9cec2-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="9cec2-130">-RuleType</span></span>
<span data-ttu-id="9cec2-131">Tipo di regola.</span><span class="sxs-lookup"><span data-stu-id="9cec2-131">Type of the rule.</span></span>
<span data-ttu-id="9cec2-132">I valori possibili includono: 'MatchRule', 'RateLimitRule'</span><span class="sxs-lookup"><span data-stu-id="9cec2-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="9cec2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cec2-133">CommonParameters</span></span>
<span data-ttu-id="9cec2-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cec2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cec2-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9cec2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cec2-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="9cec2-136">INPUTS</span></span>

### <span data-ttu-id="9cec2-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9cec2-137">None</span></span>

## <span data-ttu-id="9cec2-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9cec2-138">OUTPUTS</span></span>

### <span data-ttu-id="9cec2-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="9cec2-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="9cec2-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="9cec2-140">NOTES</span></span>

## <span data-ttu-id="9cec2-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9cec2-141">RELATED LINKS</span></span>

<span data-ttu-id="9cec2-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="9cec2-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
