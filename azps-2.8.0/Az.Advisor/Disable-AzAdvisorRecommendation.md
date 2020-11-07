---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/disable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
ms.openlocfilehash: 06e161ef2e1a2b6470144453bd9fe77ade13f832
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676177"
---
# <span data-ttu-id="48c84-101">Disable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="48c84-101">Disable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="48c84-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="48c84-102">SYNOPSIS</span></span>
<span data-ttu-id="48c84-103">Disabilitare una raccomandazione di Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="48c84-103">Disable an Azure Advisor recommendation.</span></span>

## <span data-ttu-id="48c84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48c84-104">SYNTAX</span></span>

### <span data-ttu-id="48c84-105">IdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="48c84-105">IdParameterSet (Default)</span></span>
```
Disable-AzAdvisorRecommendation [-ResourceId] <String> [[-Days] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48c84-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="48c84-106">NameParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-RecommendationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48c84-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48c84-107">InputObjectParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48c84-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48c84-108">DESCRIPTION</span></span>
<span data-ttu-id="48c84-109">Crea una soppressione per le raccomandazioni, che consente di rinviare una specifica raccomandazione per una determinata durata o infinitamente.</span><span class="sxs-lookup"><span data-stu-id="48c84-109">Creates a suppression for recommendation(s), this enables a particular recommendation to be postponed for a specific duration or infinitely.</span></span>

## <span data-ttu-id="48c84-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48c84-110">EXAMPLES</span></span>

### <span data-ttu-id="48c84-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="48c84-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -Name "f380a3a8-9d18-cfad-78e0-55762c72a178"

SuppressionId : d1f70547-0e72-db29-443e-c1164d5d4377
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="48c84-112">Creare un'eliminazione per il nome di raccomandazione indicato con una soppressione predefinita e i giorni predefiniti come-1.</span><span class="sxs-lookup"><span data-stu-id="48c84-112">Create a suppression for the given recommendation name with a default-SuppressionName and default days as -1.</span></span>

### <span data-ttu-id="48c84-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="48c84-113">Example 2</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" -Days 12

SuppressionId : 7d1f0547-0e72-db29-443e-c1164d5d4377
Ttl           : 12.00:00:00
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="48c84-114">Viene creata un'eliminazione per il suggerimento-ID indicato.</span><span class="sxs-lookup"><span data-stu-id="48c84-114">A suppression is created for the given recommendation-Id.</span></span>

### <span data-ttu-id="48c84-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="48c84-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzAdvisorRecommendation -ResourceId "/subscriptions/user_subscription/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" | Disable-A
zAdvisorRecommendation

SuppressionId : daf24e78-af2d-e8d3-9c50-fa970edc2937
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="48c84-116">Creazione di una soppressione, piping da Get-AzAdvisorRecommendation a Disable-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="48c84-116">Creating a suppression, piping from Get-AzAdvisorRecommendation to Disable-AzAdvisorRecommendation.</span></span>

## <span data-ttu-id="48c84-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="48c84-117">PARAMETERS</span></span>

### <span data-ttu-id="48c84-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="48c84-118">-Confirm</span></span>
<span data-ttu-id="48c84-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48c84-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48c84-120">Giorni</span><span class="sxs-lookup"><span data-stu-id="48c84-120">-Days</span></span>
<span data-ttu-id="48c84-121">Giorni da disabilitare.</span><span class="sxs-lookup"><span data-stu-id="48c84-121">Days to disable.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c84-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48c84-122">-DefaultProfile</span></span>
<span data-ttu-id="48c84-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48c84-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48c84-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48c84-124">-InputObject</span></span>
<span data-ttu-id="48c84-125">Il tipo di oggetto PowerShell PsAzureAdvisorResourceRecommendationBase restituito da Get-AzAdvisorRecommendation chiamata.</span><span class="sxs-lookup"><span data-stu-id="48c84-125">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="48c84-126">-Recommendname</span><span class="sxs-lookup"><span data-stu-id="48c84-126">-RecommendationName</span></span>
<span data-ttu-id="48c84-127">ResourceName della raccomandazione</span><span class="sxs-lookup"><span data-stu-id="48c84-127">ResourceName of the recommendation</span></span>

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

### <span data-ttu-id="48c84-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48c84-128">-ResourceId</span></span>
<span data-ttu-id="48c84-129">ID della raccomandazione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="48c84-129">Id of the recommendation to be suppressed.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c84-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48c84-130">-WhatIf</span></span>
<span data-ttu-id="48c84-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48c84-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48c84-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48c84-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48c84-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48c84-133">CommonParameters</span></span>
<span data-ttu-id="48c84-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48c84-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="48c84-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48c84-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48c84-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="48c84-136">INPUTS</span></span>

### <span data-ttu-id="48c84-137">System. String</span><span class="sxs-lookup"><span data-stu-id="48c84-137">System.String</span></span>

### <span data-ttu-id="48c84-138">Microsoft. Azure. Commands. Advisor. Cmdlets. Models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="48c84-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="48c84-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48c84-139">OUTPUTS</span></span>

### <span data-ttu-id="48c84-140">Microsoft. Azure. Commands. Advisor. Cmdlets. Models. PsAzureAdvisorSuppressionContract</span><span class="sxs-lookup"><span data-stu-id="48c84-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span></span>

## <span data-ttu-id="48c84-141">Note</span><span class="sxs-lookup"><span data-stu-id="48c84-141">NOTES</span></span>

## <span data-ttu-id="48c84-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48c84-142">RELATED LINKS</span></span>