---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 4612f1ef1dac22d87b6794e35f9541a39f6312ea
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403987"
---
# <span data-ttu-id="75a12-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="75a12-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="75a12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75a12-102">SYNOPSIS</span></span>
<span data-ttu-id="75a12-103">Creare un oggetto CustomRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="75a12-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="75a12-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75a12-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75a12-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="75a12-105">DESCRIPTION</span></span>
<span data-ttu-id="75a12-106">Creare un oggetto CustomRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="75a12-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="75a12-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75a12-107">EXAMPLES</span></span>

### <span data-ttu-id="75a12-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="75a12-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="75a12-109">Creare un oggetto CustomRule</span><span class="sxs-lookup"><span data-stu-id="75a12-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="75a12-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75a12-110">PARAMETERS</span></span>

### <span data-ttu-id="75a12-111">-Action</span><span class="sxs-lookup"><span data-stu-id="75a12-111">-Action</span></span>
<span data-ttu-id="75a12-112">Tipo di azioni.</span><span class="sxs-lookup"><span data-stu-id="75a12-112">Type of Actions.</span></span>
<span data-ttu-id="75a12-113">I valori possibili includono: 'Consenti', 'Blocca', 'Log'</span><span class="sxs-lookup"><span data-stu-id="75a12-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="75a12-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a12-114">-DefaultProfile</span></span>
<span data-ttu-id="75a12-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75a12-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75a12-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="75a12-116">-EnabledState</span></span>
<span data-ttu-id="75a12-117">Stato abilitato.</span><span class="sxs-lookup"><span data-stu-id="75a12-117">Enabled State.</span></span> <span data-ttu-id="75a12-118">I valori possibili includono: "Abilitato", "Disabilitato".</span><span class="sxs-lookup"><span data-stu-id="75a12-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="75a12-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="75a12-119">-MatchCondition</span></span>
<span data-ttu-id="75a12-120">Elenco di condizioni di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="75a12-120">List of match conditions.</span></span>

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

### <span data-ttu-id="75a12-121">-Name</span><span class="sxs-lookup"><span data-stu-id="75a12-121">-Name</span></span>
<span data-ttu-id="75a12-122">Nome della regola</span><span class="sxs-lookup"><span data-stu-id="75a12-122">Name of the rule</span></span>

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

### <span data-ttu-id="75a12-123">-Priority</span><span class="sxs-lookup"><span data-stu-id="75a12-123">-Priority</span></span>
<span data-ttu-id="75a12-124">Descrive la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="75a12-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="75a12-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="75a12-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="75a12-126">Durata del limite di tariffa.</span><span class="sxs-lookup"><span data-stu-id="75a12-126">Rate limit duration.</span></span> <span data-ttu-id="75a12-127">Impostazione predefinita : 1 minuto</span><span class="sxs-lookup"><span data-stu-id="75a12-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="75a12-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="75a12-128">-RateLimitThreshold</span></span>
<span data-ttu-id="75a12-129">Soglia del limite di tariffa</span><span class="sxs-lookup"><span data-stu-id="75a12-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="75a12-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="75a12-130">-RuleType</span></span>
<span data-ttu-id="75a12-131">Tipo di regola.</span><span class="sxs-lookup"><span data-stu-id="75a12-131">Type of the rule.</span></span>
<span data-ttu-id="75a12-132">I valori possibili includono: 'MatchRule', 'RateLimitRule'</span><span class="sxs-lookup"><span data-stu-id="75a12-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="75a12-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a12-133">CommonParameters</span></span>
<span data-ttu-id="75a12-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75a12-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a12-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="75a12-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a12-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="75a12-136">INPUTS</span></span>

### <span data-ttu-id="75a12-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="75a12-137">None</span></span>

## <span data-ttu-id="75a12-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75a12-138">OUTPUTS</span></span>

### <span data-ttu-id="75a12-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="75a12-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="75a12-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="75a12-140">NOTES</span></span>

## <span data-ttu-id="75a12-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75a12-141">RELATED LINKS</span></span>

<span data-ttu-id="75a12-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="75a12-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
