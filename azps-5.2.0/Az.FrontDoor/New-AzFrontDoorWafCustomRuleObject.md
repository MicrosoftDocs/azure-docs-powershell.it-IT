---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 4612f1ef1dac22d87b6794e35f9541a39f6312ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352747"
---
# <span data-ttu-id="1299a-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="1299a-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="1299a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1299a-102">SYNOPSIS</span></span>
<span data-ttu-id="1299a-103">Creare un oggetto CustomRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="1299a-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="1299a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1299a-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1299a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1299a-105">DESCRIPTION</span></span>
<span data-ttu-id="1299a-106">Creare un oggetto CustomRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="1299a-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="1299a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1299a-107">EXAMPLES</span></span>

### <span data-ttu-id="1299a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1299a-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="1299a-109">Creare un oggetto CustomRule</span><span class="sxs-lookup"><span data-stu-id="1299a-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="1299a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1299a-110">PARAMETERS</span></span>

### <span data-ttu-id="1299a-111">-Azione</span><span class="sxs-lookup"><span data-stu-id="1299a-111">-Action</span></span>
<span data-ttu-id="1299a-112">Tipo di azioni.</span><span class="sxs-lookup"><span data-stu-id="1299a-112">Type of Actions.</span></span>
<span data-ttu-id="1299a-113">I valori possibili includono:' Consenti ',' blocco ',' log '</span><span class="sxs-lookup"><span data-stu-id="1299a-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="1299a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1299a-114">-DefaultProfile</span></span>
<span data-ttu-id="1299a-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1299a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1299a-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="1299a-116">-EnabledState</span></span>
<span data-ttu-id="1299a-117">Stato abilitato.</span><span class="sxs-lookup"><span data-stu-id="1299a-117">Enabled State.</span></span> <span data-ttu-id="1299a-118">I valori possibili includono:' Enabled ',' disabled '.</span><span class="sxs-lookup"><span data-stu-id="1299a-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="1299a-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="1299a-119">-MatchCondition</span></span>
<span data-ttu-id="1299a-120">Elenco delle condizioni di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="1299a-120">List of match conditions.</span></span>

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

### <span data-ttu-id="1299a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1299a-121">-Name</span></span>
<span data-ttu-id="1299a-122">Nome della regola</span><span class="sxs-lookup"><span data-stu-id="1299a-122">Name of the rule</span></span>

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

### <span data-ttu-id="1299a-123">-Priorità</span><span class="sxs-lookup"><span data-stu-id="1299a-123">-Priority</span></span>
<span data-ttu-id="1299a-124">Descrive la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="1299a-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="1299a-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="1299a-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="1299a-126">Durata del limite di frequenza.</span><span class="sxs-lookup"><span data-stu-id="1299a-126">Rate limit duration.</span></span> <span data-ttu-id="1299a-127">Impostazione predefinita: 1 minuto</span><span class="sxs-lookup"><span data-stu-id="1299a-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="1299a-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="1299a-128">-RateLimitThreshold</span></span>
<span data-ttu-id="1299a-129">Soglia limite tasso</span><span class="sxs-lookup"><span data-stu-id="1299a-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="1299a-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="1299a-130">-RuleType</span></span>
<span data-ttu-id="1299a-131">Tipo della regola.</span><span class="sxs-lookup"><span data-stu-id="1299a-131">Type of the rule.</span></span>
<span data-ttu-id="1299a-132">I valori possibili includono: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="1299a-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="1299a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1299a-133">CommonParameters</span></span>
<span data-ttu-id="1299a-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1299a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1299a-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1299a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1299a-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1299a-136">INPUTS</span></span>

### <span data-ttu-id="1299a-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1299a-137">None</span></span>

## <span data-ttu-id="1299a-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1299a-138">OUTPUTS</span></span>

### <span data-ttu-id="1299a-139">Microsoft. Azure. Commands. FrontDoor. Models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="1299a-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="1299a-140">Note</span><span class="sxs-lookup"><span data-stu-id="1299a-140">NOTES</span></span>

## <span data-ttu-id="1299a-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1299a-141">RELATED LINKS</span></span>

<span data-ttu-id="1299a-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="1299a-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
