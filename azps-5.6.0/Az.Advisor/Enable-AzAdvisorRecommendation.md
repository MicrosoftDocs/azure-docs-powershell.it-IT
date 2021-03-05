---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 6bf98fad2b1604f88293b81c55d49e9de3f0c33c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967038"
---
# <span data-ttu-id="919f3-101">Enable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="919f3-101">Enable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="919f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="919f3-102">SYNOPSIS</span></span>
<span data-ttu-id="919f3-103">Abilita i suggerimenti di Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="919f3-103">Enables Azure Advisor recommendation(s).</span></span>

## <span data-ttu-id="919f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="919f3-104">SYNTAX</span></span>

### <span data-ttu-id="919f3-105">NameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="919f3-105">NameParameterSet (Default)</span></span>
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="919f3-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="919f3-106">IdParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="919f3-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="919f3-107">InputObjectParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="919f3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="919f3-108">DESCRIPTION</span></span>
<span data-ttu-id="919f3-109">Questo cmdlet abilita un suggerimento non eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="919f3-109">This cmdlet enables a previously suppressed recommendation.</span></span> <span data-ttu-id="919f3-110">È possibile rimuovere anche tutte le eliminazioni associate a un consiglio.</span><span class="sxs-lookup"><span data-stu-id="919f3-110">You can remove all the suppressions associated with a recommendation as well.</span></span>

## <span data-ttu-id="919f3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="919f3-111">EXAMPLES</span></span>

### <span data-ttu-id="919f3-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="919f3-112">Example 1</span></span>
```powershell
PS C:\> Enable-AzAdvisorRecommendation -ResourceId c3621337-f131-4bf4-92f2-3fb9c8cfa0d8 

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Type                 : Microsoft.Advisor/recommendations
```

<span data-ttu-id="919f3-113">Rimuove tutte le eliminazioni per il consiglio specificato con il nome "recommendation_id".</span><span class="sxs-lookup"><span data-stu-id="919f3-113">Removes all the suppressions for the given recommendation with name "recommendation_id".</span></span>

### <span data-ttu-id="919f3-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="919f3-114">Example 2</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" 
| Enable-AzAdvisorRecommendation

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/{recommendation_id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : {recommendation_id}
Type                 : Microsoft.Advisor/recommendations
```

<span data-ttu-id="919f3-115">Rimuove tutte le eliminazioni per i suggerimenti dati passati dalla pipeline.</span><span class="sxs-lookup"><span data-stu-id="919f3-115">Removes all the suppressions for the given recommendation(s) passed from the pipeline.</span></span>

## <span data-ttu-id="919f3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="919f3-116">PARAMETERS</span></span>

### <span data-ttu-id="919f3-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="919f3-117">-Confirm</span></span>
<span data-ttu-id="919f3-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="919f3-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919f3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="919f3-119">-DefaultProfile</span></span>
<span data-ttu-id="919f3-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="919f3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919f3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="919f3-121">-InputObject</span></span>
<span data-ttu-id="919f3-122">Tipo di oggetto powershell PsAzureAdvisorResourceRecommendationBase restituito dalla Get-AzAdvisorRecommendation chiamata.</span><span class="sxs-lookup"><span data-stu-id="919f3-122">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

```yaml
Type: PsAzureAdvisorResourceRecommendationBase
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="919f3-123">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="919f3-123">-RecommendationName</span></span>
<span data-ttu-id="919f3-124">ResourceName del consiglio.</span><span class="sxs-lookup"><span data-stu-id="919f3-124">ResourceName of the recommendation.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919f3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="919f3-125">-ResourceId</span></span>
<span data-ttu-id="919f3-126">ID del consiglio da eliminare.</span><span class="sxs-lookup"><span data-stu-id="919f3-126">Id of the recommendation to be suppressed.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="919f3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="919f3-127">-WhatIf</span></span>
<span data-ttu-id="919f3-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="919f3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="919f3-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="919f3-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919f3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="919f3-130">CommonParameters</span></span>
<span data-ttu-id="919f3-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="919f3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="919f3-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="919f3-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="919f3-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="919f3-133">INPUTS</span></span>

### <span data-ttu-id="919f3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="919f3-134">System.String</span></span>

### <span data-ttu-id="919f3-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="919f3-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="919f3-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="919f3-136">OUTPUTS</span></span>

### <span data-ttu-id="919f3-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="919f3-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="919f3-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="919f3-138">NOTES</span></span>

## <span data-ttu-id="919f3-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="919f3-139">RELATED LINKS</span></span>
