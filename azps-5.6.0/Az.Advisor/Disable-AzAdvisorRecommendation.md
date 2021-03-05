---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/disable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
ms.openlocfilehash: 3695ee9d027733d3adea17797ffbcf669136e66b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967053"
---
# <span data-ttu-id="59916-101">Disable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="59916-101">Disable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="59916-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59916-102">SYNOPSIS</span></span>
<span data-ttu-id="59916-103">Disabilitare un consiglio di Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="59916-103">Disable an Azure Advisor recommendation.</span></span>

## <span data-ttu-id="59916-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59916-104">SYNTAX</span></span>

### <span data-ttu-id="59916-105">IdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="59916-105">IdParameterSet (Default)</span></span>
```
Disable-AzAdvisorRecommendation [-ResourceId] <String> [[-Days] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59916-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="59916-106">NameParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-RecommendationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59916-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59916-107">InputObjectParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59916-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="59916-108">DESCRIPTION</span></span>
<span data-ttu-id="59916-109">Crea un'eliminazione dei suggerimenti, in modo da posticipare un particolare consiglio per una durata specifica o infiniti.</span><span class="sxs-lookup"><span data-stu-id="59916-109">Creates a suppression for recommendation(s), this enables a particular recommendation to be postponed for a specific duration or infinitely.</span></span>

## <span data-ttu-id="59916-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59916-110">EXAMPLES</span></span>

### <span data-ttu-id="59916-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="59916-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -Name "f380a3a8-9d18-cfad-78e0-55762c72a178"

SuppressionId : d1f70547-0e72-db29-443e-c1164d5d4377
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="59916-112">Creare un'eliminazione per il nome consiglio specificato con default-SuppressionName e il valore predefinito -1 per i giorni.</span><span class="sxs-lookup"><span data-stu-id="59916-112">Create a suppression for the given recommendation name with a default-SuppressionName and default days as -1.</span></span>

### <span data-ttu-id="59916-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="59916-113">Example 2</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" -Days 12

SuppressionId : 7d1f0547-0e72-db29-443e-c1164d5d4377
Ttl           : 12.00:00:00
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="59916-114">Viene creata un'eliminazione per il dato ID-consiglio.</span><span class="sxs-lookup"><span data-stu-id="59916-114">A suppression is created for the given recommendation-Id.</span></span>

### <span data-ttu-id="59916-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="59916-115">Example 3</span></span>
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

<span data-ttu-id="59916-116">Creazione di un'eliminazione, piping da Get-AzAdvisorRecommendation a Disable-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="59916-116">Creating a suppression, piping from Get-AzAdvisorRecommendation to Disable-AzAdvisorRecommendation.</span></span>

## <span data-ttu-id="59916-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59916-117">PARAMETERS</span></span>

### <span data-ttu-id="59916-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59916-118">-Confirm</span></span>
<span data-ttu-id="59916-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59916-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59916-120">-Giorni</span><span class="sxs-lookup"><span data-stu-id="59916-120">-Days</span></span>
<span data-ttu-id="59916-121">Giorni da disabilitare.</span><span class="sxs-lookup"><span data-stu-id="59916-121">Days to disable.</span></span>

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

### <span data-ttu-id="59916-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59916-122">-DefaultProfile</span></span>
<span data-ttu-id="59916-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59916-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59916-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59916-124">-InputObject</span></span>
<span data-ttu-id="59916-125">Tipo di oggetto powershell PsAzureAdvisorResourceRecommendationBase restituito dalla Get-AzAdvisorRecommendation chiamata.</span><span class="sxs-lookup"><span data-stu-id="59916-125">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="59916-126">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="59916-126">-RecommendationName</span></span>
<span data-ttu-id="59916-127">ResourceName del suggerimento</span><span class="sxs-lookup"><span data-stu-id="59916-127">ResourceName of the recommendation</span></span>

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

### <span data-ttu-id="59916-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59916-128">-ResourceId</span></span>
<span data-ttu-id="59916-129">ID del consiglio da eliminare.</span><span class="sxs-lookup"><span data-stu-id="59916-129">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="59916-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59916-130">-WhatIf</span></span>
<span data-ttu-id="59916-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59916-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59916-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59916-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59916-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59916-133">CommonParameters</span></span>
<span data-ttu-id="59916-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59916-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="59916-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59916-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59916-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="59916-136">INPUTS</span></span>

### <span data-ttu-id="59916-137">System.String</span><span class="sxs-lookup"><span data-stu-id="59916-137">System.String</span></span>

### <span data-ttu-id="59916-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="59916-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="59916-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59916-139">OUTPUTS</span></span>

### <span data-ttu-id="59916-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span><span class="sxs-lookup"><span data-stu-id="59916-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span></span>

## <span data-ttu-id="59916-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="59916-141">NOTES</span></span>

## <span data-ttu-id="59916-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59916-142">RELATED LINKS</span></span>
