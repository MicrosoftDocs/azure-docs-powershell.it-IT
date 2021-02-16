---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/disable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
ms.openlocfilehash: c9ad0e4b6744c00e9b3f4e7894daa52d2575dd90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176527"
---
# <span data-ttu-id="ecfc9-101">Disable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="ecfc9-101">Disable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="ecfc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecfc9-102">SYNOPSIS</span></span>
<span data-ttu-id="ecfc9-103">Disabilitare un consiglio di Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="ecfc9-103">Disable an Azure Advisor recommendation.</span></span>

## <span data-ttu-id="ecfc9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecfc9-104">SYNTAX</span></span>

### <span data-ttu-id="ecfc9-105">IdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ecfc9-105">IdParameterSet (Default)</span></span>
```
Disable-AzAdvisorRecommendation [-ResourceId] <String> [[-Days] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecfc9-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecfc9-106">NameParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-RecommendationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecfc9-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecfc9-107">InputObjectParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecfc9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ecfc9-108">DESCRIPTION</span></span>
<span data-ttu-id="ecfc9-109">Crea un'eliminazione dei suggerimenti, in modo da posticipare un particolare consiglio per una durata specifica o infiniti.</span><span class="sxs-lookup"><span data-stu-id="ecfc9-109">Creates a suppression for recommendation(s), this enables a particular recommendation to be postponed for a specific duration or infinitely.</span></span>

## <span data-ttu-id="ecfc9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecfc9-110">EXAMPLES</span></span>

### <span data-ttu-id="ecfc9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ecfc9-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -Name "f380a3a8-9d18-cfad-78e0-55762c72a178"

SuppressionId : d1f70547-0e72-db29-443e-c1164d5d4377
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="ecfc9-112">Creare un'eliminazione per il nome consiglio specificato con default-SuppressionName e il valore predefinito -1 per i giorni.</span><span class="sxs-lookup"><span data-stu-id="ecfc9-112">Create a suppression for the given recommendation name with a default-SuppressionName and default days as -1.</span></span>

### <span data-ttu-id="ecfc9-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ecfc9-113">Example 2</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" -Days 12

SuppressionId : 7d1f0547-0e72-db29-443e-c1164d5d4377
Ttl           : 12.00:00:00
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="ecfc9-114">Viene creata un'eliminazione per il dato ID-consiglio.</span><span class="sxs-lookup"><span data-stu-id="ecfc9-114">A suppression is created for the given recommendation-Id.</span></span>

### <span data-ttu-id="ecfc9-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="ecfc9-115">Example 3</span></span>
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

<span data-ttu-id="ecfc9-116">Creazione di un'eliminazione, piping da Get-AzAdvisorRecommendation a Disable-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="ecfc9-116">Creating a suppression, piping from Get-AzAdvisorRecommendation to Disable-AzAdvisorRecommendation.</span></span>

## <span data-ttu-id="ecfc9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecfc9-117">PARAMETERS</span></span>

### <span data-ttu-id="ecfc9-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecfc9-118">-Confirm</span></span>
<span data-ttu-id="ecfc9-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecfc9-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecfc9-120">-Giorni</span><span class="sxs-lookup"><span data-stu-id="ecfc9-120">-Days</span></span>
<span data-ttu-id="ecfc9-121">Giorni da disabilitare.</span><span class="sxs-lookup"><span data-stu-id="ecfc9-121">Days to disable.</span></span>

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

### <span data-ttu-id="ecfc9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecfc9-122">-DefaultProfile</span></span>
<span data-ttu-id="ecfc9-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ecfc9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecfc9-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecfc9-124">-InputObject</span></span>
<span data-ttu-id="ecfc9-125">Tipo di oggetto powershell PsAzureAdvisorResourceRecommendationBase restituito dalla Get-AzAdvisorRecommendation chiamata.</span><span class="sxs-lookup"><span data-stu-id="ecfc9-125">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="ecfc9-126">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="ecfc9-126">-RecommendationName</span></span>
<span data-ttu-id="ecfc9-127">ResourceName del suggerimento</span><span class="sxs-lookup"><span data-stu-id="ecfc9-127">ResourceName of the recommendation</span></span>

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

### <span data-ttu-id="ecfc9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecfc9-128">-ResourceId</span></span>
<span data-ttu-id="ecfc9-129">ID del consiglio da eliminare.</span><span class="sxs-lookup"><span data-stu-id="ecfc9-129">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="ecfc9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecfc9-130">-WhatIf</span></span>
<span data-ttu-id="ecfc9-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecfc9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecfc9-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecfc9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecfc9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecfc9-133">CommonParameters</span></span>
<span data-ttu-id="ecfc9-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecfc9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ecfc9-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecfc9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecfc9-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="ecfc9-136">INPUTS</span></span>

### <span data-ttu-id="ecfc9-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ecfc9-137">System.String</span></span>

### <span data-ttu-id="ecfc9-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="ecfc9-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="ecfc9-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecfc9-139">OUTPUTS</span></span>

### <span data-ttu-id="ecfc9-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span><span class="sxs-lookup"><span data-stu-id="ecfc9-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span></span>

## <span data-ttu-id="ecfc9-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="ecfc9-141">NOTES</span></span>

## <span data-ttu-id="ecfc9-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecfc9-142">RELATED LINKS</span></span>
