---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorCustomRuleObject.md
ms.openlocfilehash: a5a1494bd217147a4e6f4c94a85140313429898f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507451"
---
# <span data-ttu-id="1aef2-101">New-AzureRmFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="1aef2-101">New-AzureRmFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="1aef2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1aef2-102">SYNOPSIS</span></span>
<span data-ttu-id="1aef2-103">Creare un oggetto CustomRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="1aef2-103">Create CustomRule Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1aef2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1aef2-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1aef2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1aef2-105">DESCRIPTION</span></span>
<span data-ttu-id="1aef2-106">Creare un oggetto CustomRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="1aef2-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="1aef2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1aef2-107">EXAMPLES</span></span>

### <span data-ttu-id="1aef2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1aef2-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

RuleType                   : MatchRule
Action                     : Block
MatchConditions            : {Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition}
Priority                   : 2
RateLimitDurationInMinutes : 1
RateLimitThreshold         :
Name                       : Rule1
Etag                       :
Transforms                 :
```

<span data-ttu-id="1aef2-109">Creare un oggetto CustomRule</span><span class="sxs-lookup"><span data-stu-id="1aef2-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="1aef2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1aef2-110">PARAMETERS</span></span>

### <span data-ttu-id="1aef2-111">-Azione</span><span class="sxs-lookup"><span data-stu-id="1aef2-111">-Action</span></span>
<span data-ttu-id="1aef2-112">Tipo di azioni.</span><span class="sxs-lookup"><span data-stu-id="1aef2-112">Type of Actions.</span></span>
<span data-ttu-id="1aef2-113">I valori possibili includono:' Consenti ',' blocco ',' log '</span><span class="sxs-lookup"><span data-stu-id="1aef2-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aef2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aef2-114">-DefaultProfile</span></span>
<span data-ttu-id="1aef2-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1aef2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1aef2-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="1aef2-116">-MatchCondition</span></span>
<span data-ttu-id="1aef2-117">Elenco delle condizioni di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="1aef2-117">List of match conditions.</span></span>

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

### <span data-ttu-id="1aef2-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1aef2-118">-Name</span></span>
<span data-ttu-id="1aef2-119">Nome della regola</span><span class="sxs-lookup"><span data-stu-id="1aef2-119">Name of the rule</span></span>

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

### <span data-ttu-id="1aef2-120">-Priorità</span><span class="sxs-lookup"><span data-stu-id="1aef2-120">-Priority</span></span>
<span data-ttu-id="1aef2-121">Descrive la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="1aef2-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="1aef2-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="1aef2-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="1aef2-123">Durata del limite di frequenza.</span><span class="sxs-lookup"><span data-stu-id="1aef2-123">Rate limit duration.</span></span> <span data-ttu-id="1aef2-124">Impostazione predefinita: 1 minuto</span><span class="sxs-lookup"><span data-stu-id="1aef2-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="1aef2-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="1aef2-125">-RateLimitThreshold</span></span>
<span data-ttu-id="1aef2-126">Tasso limite Thresold</span><span class="sxs-lookup"><span data-stu-id="1aef2-126">Rate limit thresold</span></span>

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

### <span data-ttu-id="1aef2-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="1aef2-127">-RuleType</span></span>
<span data-ttu-id="1aef2-128">Tipo della regola.</span><span class="sxs-lookup"><span data-stu-id="1aef2-128">Type of the rule.</span></span>
<span data-ttu-id="1aef2-129">I valori possibili includono: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="1aef2-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="1aef2-130">-Transform</span><span class="sxs-lookup"><span data-stu-id="1aef2-130">-Transform</span></span>
<span data-ttu-id="1aef2-131">Elenco delle trasformazioni</span><span class="sxs-lookup"><span data-stu-id="1aef2-131">List of transforms</span></span>

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

### <span data-ttu-id="1aef2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aef2-132">CommonParameters</span></span>
<span data-ttu-id="1aef2-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aef2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aef2-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1aef2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aef2-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1aef2-135">INPUTS</span></span>

### <span data-ttu-id="1aef2-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1aef2-136">None</span></span>

## <span data-ttu-id="1aef2-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1aef2-137">OUTPUTS</span></span>

### <span data-ttu-id="1aef2-138">Microsoft. Azure. Commands. FrontDoor. Models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="1aef2-138">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="1aef2-139">Note</span><span class="sxs-lookup"><span data-stu-id="1aef2-139">NOTES</span></span>

## <span data-ttu-id="1aef2-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1aef2-140">RELATED LINKS</span></span>

<span data-ttu-id="1aef2-141">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="1aef2-141">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)</span></span>
