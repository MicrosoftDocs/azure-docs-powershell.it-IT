---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 6c40a54dd230bc4c7e45f97b4fa6f969940e1673
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674374"
---
# <span data-ttu-id="021e5-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="021e5-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="021e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="021e5-102">SYNOPSIS</span></span>
<span data-ttu-id="021e5-103">Creare un oggetto CustomRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="021e5-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="021e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="021e5-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="021e5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="021e5-105">DESCRIPTION</span></span>
<span data-ttu-id="021e5-106">Creare un oggetto CustomRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="021e5-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="021e5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="021e5-107">EXAMPLES</span></span>

### <span data-ttu-id="021e5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="021e5-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="021e5-109">Creare un oggetto CustomRule</span><span class="sxs-lookup"><span data-stu-id="021e5-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="021e5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="021e5-110">PARAMETERS</span></span>

### <span data-ttu-id="021e5-111">-Azione</span><span class="sxs-lookup"><span data-stu-id="021e5-111">-Action</span></span>
<span data-ttu-id="021e5-112">Tipo di azioni.</span><span class="sxs-lookup"><span data-stu-id="021e5-112">Type of Actions.</span></span>
<span data-ttu-id="021e5-113">I valori possibili includono:' Consenti ',' blocco ',' log '</span><span class="sxs-lookup"><span data-stu-id="021e5-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="021e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="021e5-114">-DefaultProfile</span></span>
<span data-ttu-id="021e5-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="021e5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="021e5-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="021e5-116">-MatchCondition</span></span>
<span data-ttu-id="021e5-117">Elenco delle condizioni di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="021e5-117">List of match conditions.</span></span>

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

### <span data-ttu-id="021e5-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="021e5-118">-Name</span></span>
<span data-ttu-id="021e5-119">Nome della regola</span><span class="sxs-lookup"><span data-stu-id="021e5-119">Name of the rule</span></span>

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

### <span data-ttu-id="021e5-120">-Priorità</span><span class="sxs-lookup"><span data-stu-id="021e5-120">-Priority</span></span>
<span data-ttu-id="021e5-121">Descrive la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="021e5-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="021e5-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="021e5-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="021e5-123">Durata del limite di frequenza.</span><span class="sxs-lookup"><span data-stu-id="021e5-123">Rate limit duration.</span></span> <span data-ttu-id="021e5-124">Impostazione predefinita: 1 minuto</span><span class="sxs-lookup"><span data-stu-id="021e5-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="021e5-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="021e5-125">-RateLimitThreshold</span></span>
<span data-ttu-id="021e5-126">Soglia limite tasso</span><span class="sxs-lookup"><span data-stu-id="021e5-126">Rate limit threshold</span></span>

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

### <span data-ttu-id="021e5-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="021e5-127">-RuleType</span></span>
<span data-ttu-id="021e5-128">Tipo della regola.</span><span class="sxs-lookup"><span data-stu-id="021e5-128">Type of the rule.</span></span>
<span data-ttu-id="021e5-129">I valori possibili includono: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="021e5-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="021e5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="021e5-130">CommonParameters</span></span>
<span data-ttu-id="021e5-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="021e5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="021e5-132">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="021e5-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="021e5-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="021e5-133">INPUTS</span></span>

### <span data-ttu-id="021e5-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="021e5-134">None</span></span>

## <span data-ttu-id="021e5-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="021e5-135">OUTPUTS</span></span>

### <span data-ttu-id="021e5-136">Microsoft. Azure. Commands. FrontDoor. Models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="021e5-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="021e5-137">Note</span><span class="sxs-lookup"><span data-stu-id="021e5-137">NOTES</span></span>

## <span data-ttu-id="021e5-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="021e5-138">RELATED LINKS</span></span>

<span data-ttu-id="021e5-139">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="021e5-139">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span></span>
