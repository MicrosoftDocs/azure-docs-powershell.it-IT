---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 05d74b254645a970389aae859d60583c53c07670
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676173"
---
# <span data-ttu-id="ba5de-101">Enable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="ba5de-101">Enable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="ba5de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba5de-102">SYNOPSIS</span></span>
<span data-ttu-id="ba5de-103">Abilita le raccomandazioni di Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="ba5de-103">Enables Azure Advisor recommendation(s).</span></span>

## <span data-ttu-id="ba5de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba5de-104">SYNTAX</span></span>

### <span data-ttu-id="ba5de-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ba5de-105">NameParameterSet (Default)</span></span>
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba5de-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba5de-106">IdParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba5de-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba5de-107">InputObjectParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba5de-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba5de-108">DESCRIPTION</span></span>
<span data-ttu-id="ba5de-109">Questo cmdlet Abilita una raccomandazione precedentemente eliminata.</span><span class="sxs-lookup"><span data-stu-id="ba5de-109">This cmdlet enables a previously suppressed recommendation.</span></span> <span data-ttu-id="ba5de-110">È possibile rimuovere anche tutte le eliminazioni associate a una raccomandazione.</span><span class="sxs-lookup"><span data-stu-id="ba5de-110">You can remove all the suppressions associated with a recommendation as well.</span></span>

## <span data-ttu-id="ba5de-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba5de-111">EXAMPLES</span></span>

### <span data-ttu-id="ba5de-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ba5de-112">Example 1</span></span>
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

<span data-ttu-id="ba5de-113">Rimuove tutte le eliminazioni per il suggerimento indicato con il nome "recommendation_id".</span><span class="sxs-lookup"><span data-stu-id="ba5de-113">Removes all the suppressions for the given recommendation with name "recommendation_id".</span></span>

### <span data-ttu-id="ba5de-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ba5de-114">Example 2</span></span>
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

<span data-ttu-id="ba5de-115">Rimuove tutte le eliminazioni per le singole raccomandazioni passate dalla pipeline.</span><span class="sxs-lookup"><span data-stu-id="ba5de-115">Removes all the suppressions for the given recommendation(s) passed from the pipeline.</span></span>

## <span data-ttu-id="ba5de-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba5de-116">PARAMETERS</span></span>

### <span data-ttu-id="ba5de-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ba5de-117">-Confirm</span></span>
<span data-ttu-id="ba5de-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba5de-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba5de-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba5de-119">-DefaultProfile</span></span>
<span data-ttu-id="ba5de-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba5de-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba5de-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba5de-121">-InputObject</span></span>
<span data-ttu-id="ba5de-122">Il tipo di oggetto PowerShell PsAzureAdvisorResourceRecommendationBase restituito da Get-AzAdvisorRecommendation chiamata.</span><span class="sxs-lookup"><span data-stu-id="ba5de-122">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="ba5de-123">-Recommendname</span><span class="sxs-lookup"><span data-stu-id="ba5de-123">-RecommendationName</span></span>
<span data-ttu-id="ba5de-124">ResourceName della raccomandazione.</span><span class="sxs-lookup"><span data-stu-id="ba5de-124">ResourceName of the recommendation.</span></span>

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

### <span data-ttu-id="ba5de-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba5de-125">-ResourceId</span></span>
<span data-ttu-id="ba5de-126">ID della raccomandazione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="ba5de-126">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="ba5de-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba5de-127">-WhatIf</span></span>
<span data-ttu-id="ba5de-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba5de-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba5de-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba5de-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba5de-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba5de-130">CommonParameters</span></span>
<span data-ttu-id="ba5de-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba5de-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ba5de-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba5de-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba5de-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba5de-133">INPUTS</span></span>

### <span data-ttu-id="ba5de-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ba5de-134">System.String</span></span>

### <span data-ttu-id="ba5de-135">Microsoft. Azure. Commands. Advisor. Cmdlets. Models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="ba5de-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="ba5de-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba5de-136">OUTPUTS</span></span>

### <span data-ttu-id="ba5de-137">Microsoft. Azure. Commands. Advisor. Cmdlets. Models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="ba5de-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="ba5de-138">Note</span><span class="sxs-lookup"><span data-stu-id="ba5de-138">NOTES</span></span>

## <span data-ttu-id="ba5de-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba5de-139">RELATED LINKS</span></span>