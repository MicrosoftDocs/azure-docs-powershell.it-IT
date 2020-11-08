---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 7126a9c8ee11bcb5b32cc47ae31aaf821b171522
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019946"
---
# <span data-ttu-id="9d507-101">Enable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="9d507-101">Enable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="9d507-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d507-102">SYNOPSIS</span></span>
<span data-ttu-id="9d507-103">Abilita le raccomandazioni di Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="9d507-103">Enables Azure Advisor recommendation(s).</span></span>

## <span data-ttu-id="9d507-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d507-104">SYNTAX</span></span>

### <span data-ttu-id="9d507-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9d507-105">NameParameterSet (Default)</span></span>
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d507-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d507-106">IdParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d507-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d507-107">InputObjectParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d507-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d507-108">DESCRIPTION</span></span>
<span data-ttu-id="9d507-109">Questo cmdlet Abilita una raccomandazione precedentemente eliminata.</span><span class="sxs-lookup"><span data-stu-id="9d507-109">This cmdlet enables a previously suppressed recommendation.</span></span> <span data-ttu-id="9d507-110">È possibile rimuovere anche tutte le eliminazioni associate a una raccomandazione.</span><span class="sxs-lookup"><span data-stu-id="9d507-110">You can remove all the suppressions associated with a recommendation as well.</span></span>

## <span data-ttu-id="9d507-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d507-111">EXAMPLES</span></span>

### <span data-ttu-id="9d507-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9d507-112">Example 1</span></span>
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

<span data-ttu-id="9d507-113">Rimuove tutte le eliminazioni per il suggerimento indicato con il nome "recommendation_id".</span><span class="sxs-lookup"><span data-stu-id="9d507-113">Removes all the suppressions for the given recommendation with name "recommendation_id".</span></span>

### <span data-ttu-id="9d507-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9d507-114">Example 2</span></span>
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

<span data-ttu-id="9d507-115">Rimuove tutte le eliminazioni per le singole raccomandazioni passate dalla pipeline.</span><span class="sxs-lookup"><span data-stu-id="9d507-115">Removes all the suppressions for the given recommendation(s) passed from the pipeline.</span></span>

## <span data-ttu-id="9d507-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d507-116">PARAMETERS</span></span>

### <span data-ttu-id="9d507-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9d507-117">-Confirm</span></span>
<span data-ttu-id="9d507-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d507-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d507-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d507-119">-DefaultProfile</span></span>
<span data-ttu-id="9d507-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d507-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d507-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d507-121">-InputObject</span></span>
<span data-ttu-id="9d507-122">Il tipo di oggetto PowerShell PsAzureAdvisorResourceRecommendationBase restituito da Get-AzAdvisorRecommendation chiamata.</span><span class="sxs-lookup"><span data-stu-id="9d507-122">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="9d507-123">-Recommendname</span><span class="sxs-lookup"><span data-stu-id="9d507-123">-RecommendationName</span></span>
<span data-ttu-id="9d507-124">ResourceName della raccomandazione.</span><span class="sxs-lookup"><span data-stu-id="9d507-124">ResourceName of the recommendation.</span></span>

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

### <span data-ttu-id="9d507-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d507-125">-ResourceId</span></span>
<span data-ttu-id="9d507-126">ID della raccomandazione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="9d507-126">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="9d507-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d507-127">-WhatIf</span></span>
<span data-ttu-id="9d507-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d507-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d507-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d507-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d507-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d507-130">CommonParameters</span></span>
<span data-ttu-id="9d507-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d507-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9d507-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d507-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d507-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d507-133">INPUTS</span></span>

### <span data-ttu-id="9d507-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9d507-134">System.String</span></span>

### <span data-ttu-id="9d507-135">Microsoft. Azure. Commands. Advisor. Cmdlets. Models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="9d507-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="9d507-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d507-136">OUTPUTS</span></span>

### <span data-ttu-id="9d507-137">Microsoft. Azure. Commands. Advisor. Cmdlets. Models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="9d507-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="9d507-138">Note</span><span class="sxs-lookup"><span data-stu-id="9d507-138">NOTES</span></span>

## <span data-ttu-id="9d507-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d507-139">RELATED LINKS</span></span>
