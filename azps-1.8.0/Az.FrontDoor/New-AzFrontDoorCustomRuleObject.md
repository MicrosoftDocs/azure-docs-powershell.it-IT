---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
ms.openlocfilehash: 19f8215f8feaa1765da871f0fa38cc0120d842ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836171"
---
# <span data-ttu-id="d25c9-101">New-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="d25c9-101">New-AzFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="d25c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d25c9-102">SYNOPSIS</span></span>
<span data-ttu-id="d25c9-103">Creare un oggetto CustomRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="d25c9-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="d25c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d25c9-104">SYNTAX</span></span>

```
New-AzFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d25c9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d25c9-105">DESCRIPTION</span></span>
<span data-ttu-id="d25c9-106">Creare un oggetto CustomRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="d25c9-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="d25c9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d25c9-107">EXAMPLES</span></span>

### <span data-ttu-id="d25c9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d25c9-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="d25c9-109">Creare un oggetto CustomRule</span><span class="sxs-lookup"><span data-stu-id="d25c9-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="d25c9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d25c9-110">PARAMETERS</span></span>

### <span data-ttu-id="d25c9-111">-Azione</span><span class="sxs-lookup"><span data-stu-id="d25c9-111">-Action</span></span>
<span data-ttu-id="d25c9-112">Tipo di azioni.</span><span class="sxs-lookup"><span data-stu-id="d25c9-112">Type of Actions.</span></span>
<span data-ttu-id="d25c9-113">I valori possibili includono:' Consenti ',' blocco ',' log '</span><span class="sxs-lookup"><span data-stu-id="d25c9-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log, Redirect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25c9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d25c9-114">-DefaultProfile</span></span>
<span data-ttu-id="d25c9-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d25c9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d25c9-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="d25c9-116">-MatchCondition</span></span>
<span data-ttu-id="d25c9-117">Elenco delle condizioni di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="d25c9-117">List of match conditions.</span></span>

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

### <span data-ttu-id="d25c9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d25c9-118">-Name</span></span>
<span data-ttu-id="d25c9-119">Nome della regola</span><span class="sxs-lookup"><span data-stu-id="d25c9-119">Name of the rule</span></span>

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

### <span data-ttu-id="d25c9-120">-Priorità</span><span class="sxs-lookup"><span data-stu-id="d25c9-120">-Priority</span></span>
<span data-ttu-id="d25c9-121">Descrive la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="d25c9-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="d25c9-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="d25c9-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="d25c9-123">Durata del limite di frequenza.</span><span class="sxs-lookup"><span data-stu-id="d25c9-123">Rate limit duration.</span></span> <span data-ttu-id="d25c9-124">Impostazione predefinita: 1 minuto</span><span class="sxs-lookup"><span data-stu-id="d25c9-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="d25c9-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="d25c9-125">-RateLimitThreshold</span></span>
<span data-ttu-id="d25c9-126">Tasso limite Thresold</span><span class="sxs-lookup"><span data-stu-id="d25c9-126">Rate limit thresold</span></span>

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

### <span data-ttu-id="d25c9-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="d25c9-127">-RuleType</span></span>
<span data-ttu-id="d25c9-128">Tipo della regola.</span><span class="sxs-lookup"><span data-stu-id="d25c9-128">Type of the rule.</span></span>
<span data-ttu-id="d25c9-129">I valori possibili includono: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="d25c9-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRuleType
Parameter Sets: (All)
Aliases:
Accepted values: RateLimitRule, MatchRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25c9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d25c9-130">CommonParameters</span></span>
<span data-ttu-id="d25c9-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d25c9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d25c9-132">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d25c9-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d25c9-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d25c9-133">INPUTS</span></span>

### <span data-ttu-id="d25c9-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d25c9-134">None</span></span>

## <span data-ttu-id="d25c9-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d25c9-135">OUTPUTS</span></span>

### <span data-ttu-id="d25c9-136">Microsoft. Azure. Commands. FrontDoor. Models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="d25c9-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="d25c9-137">Note</span><span class="sxs-lookup"><span data-stu-id="d25c9-137">NOTES</span></span>

## <span data-ttu-id="d25c9-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d25c9-138">RELATED LINKS</span></span>

<span data-ttu-id="d25c9-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="d25c9-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)</span></span>
