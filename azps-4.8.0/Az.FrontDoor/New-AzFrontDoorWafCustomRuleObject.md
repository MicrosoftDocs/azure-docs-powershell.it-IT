---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 4612f1ef1dac22d87b6794e35f9541a39f6312ea
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192485"
---
# <span data-ttu-id="8c7d3-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="8c7d3-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="8c7d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8c7d3-102">SYNOPSIS</span></span>
<span data-ttu-id="8c7d3-103">Creare un oggetto CustomRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="8c7d3-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="8c7d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c7d3-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c7d3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c7d3-105">DESCRIPTION</span></span>
<span data-ttu-id="8c7d3-106">Creare un oggetto CustomRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="8c7d3-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="8c7d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c7d3-107">EXAMPLES</span></span>

### <span data-ttu-id="8c7d3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8c7d3-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="8c7d3-109">Creare un oggetto CustomRule</span><span class="sxs-lookup"><span data-stu-id="8c7d3-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="8c7d3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8c7d3-110">PARAMETERS</span></span>

### <span data-ttu-id="8c7d3-111">-Azione</span><span class="sxs-lookup"><span data-stu-id="8c7d3-111">-Action</span></span>
<span data-ttu-id="8c7d3-112">Tipo di azioni.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-112">Type of Actions.</span></span>
<span data-ttu-id="8c7d3-113">I valori possibili includono:' Consenti ',' blocco ',' log '</span><span class="sxs-lookup"><span data-stu-id="8c7d3-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="8c7d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c7d3-114">-DefaultProfile</span></span>
<span data-ttu-id="8c7d3-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c7d3-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="8c7d3-116">-EnabledState</span></span>
<span data-ttu-id="8c7d3-117">Stato abilitato.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-117">Enabled State.</span></span> <span data-ttu-id="8c7d3-118">I valori possibili includono:' Enabled ',' disabled '.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="8c7d3-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="8c7d3-119">-MatchCondition</span></span>
<span data-ttu-id="8c7d3-120">Elenco delle condizioni di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-120">List of match conditions.</span></span>

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

### <span data-ttu-id="8c7d3-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c7d3-121">-Name</span></span>
<span data-ttu-id="8c7d3-122">Nome della regola</span><span class="sxs-lookup"><span data-stu-id="8c7d3-122">Name of the rule</span></span>

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

### <span data-ttu-id="8c7d3-123">-Priorità</span><span class="sxs-lookup"><span data-stu-id="8c7d3-123">-Priority</span></span>
<span data-ttu-id="8c7d3-124">Descrive la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="8c7d3-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="8c7d3-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="8c7d3-126">Durata del limite di frequenza.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-126">Rate limit duration.</span></span> <span data-ttu-id="8c7d3-127">Impostazione predefinita: 1 minuto</span><span class="sxs-lookup"><span data-stu-id="8c7d3-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="8c7d3-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="8c7d3-128">-RateLimitThreshold</span></span>
<span data-ttu-id="8c7d3-129">Soglia limite tasso</span><span class="sxs-lookup"><span data-stu-id="8c7d3-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="8c7d3-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="8c7d3-130">-RuleType</span></span>
<span data-ttu-id="8c7d3-131">Tipo della regola.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-131">Type of the rule.</span></span>
<span data-ttu-id="8c7d3-132">I valori possibili includono: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="8c7d3-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="8c7d3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c7d3-133">CommonParameters</span></span>
<span data-ttu-id="8c7d3-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c7d3-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c7d3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c7d3-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8c7d3-136">INPUTS</span></span>

### <span data-ttu-id="8c7d3-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8c7d3-137">None</span></span>

## <span data-ttu-id="8c7d3-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c7d3-138">OUTPUTS</span></span>

### <span data-ttu-id="8c7d3-139">Microsoft. Azure. Commands. FrontDoor. Models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="8c7d3-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="8c7d3-140">Note</span><span class="sxs-lookup"><span data-stu-id="8c7d3-140">NOTES</span></span>

## <span data-ttu-id="8c7d3-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c7d3-141">RELATED LINKS</span></span>

<span data-ttu-id="8c7d3-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="8c7d3-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
