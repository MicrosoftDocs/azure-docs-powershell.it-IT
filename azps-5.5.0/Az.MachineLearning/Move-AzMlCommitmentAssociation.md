---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/move-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
ms.openlocfilehash: c127ff40690658a98f9d0f0fa670cddfca123f89
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192278"
---
# <span data-ttu-id="c8bf4-101">Move-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="c8bf4-101">Move-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="c8bf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="c8bf4-103">Sposta un'associazione di impegno da un piano di impegno a un altro.</span><span class="sxs-lookup"><span data-stu-id="c8bf4-103">Moves a commitment association from one commitment plan to another.</span></span>

## <span data-ttu-id="c8bf4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8bf4-104">SYNTAX</span></span>

```
Move-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8bf4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c8bf4-105">DESCRIPTION</span></span>
<span data-ttu-id="c8bf4-106">Sposta una risorsa di associazione dell'impegno dal piano di impegno padre a un altro piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="c8bf4-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="c8bf4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8bf4-107">EXAMPLES</span></span>

### <span data-ttu-id="c8bf4-108">Esempio 1: Spostare un'associazione di impegno</span><span class="sxs-lookup"><span data-stu-id="c8bf4-108">Example 1: Move a commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="c8bf4-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8bf4-109">PARAMETERS</span></span>

### <span data-ttu-id="c8bf4-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="c8bf4-110">-CommitmentPlanName</span></span>
<span data-ttu-id="c8bf4-111">Nome del piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="c8bf4-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c8bf4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8bf4-112">-DefaultProfile</span></span>
<span data-ttu-id="c8bf4-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="c8bf4-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8bf4-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="c8bf4-114">-DestinationPlanId</span></span>
<span data-ttu-id="c8bf4-115">ID della risorsa Azure del piano di impegno di Azure ML di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c8bf4-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c8bf4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c8bf4-116">-Name</span></span>
<span data-ttu-id="c8bf4-117">Nome dell'associazione di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="c8bf4-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="c8bf4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8bf4-118">-ResourceGroupName</span></span>
<span data-ttu-id="c8bf4-119">Nome del gruppo di risorse per l'associazione di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="c8bf4-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="c8bf4-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8bf4-120">-Confirm</span></span>
<span data-ttu-id="c8bf4-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8bf4-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8bf4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8bf4-122">-WhatIf</span></span>
<span data-ttu-id="c8bf4-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8bf4-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8bf4-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8bf4-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8bf4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8bf4-125">CommonParameters</span></span>
<span data-ttu-id="c8bf4-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8bf4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8bf4-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8bf4-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8bf4-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="c8bf4-128">INPUTS</span></span>

### <span data-ttu-id="c8bf4-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c8bf4-129">None</span></span>

## <span data-ttu-id="c8bf4-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8bf4-130">OUTPUTS</span></span>

### <span data-ttu-id="c8bf4-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="c8bf4-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="c8bf4-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="c8bf4-132">NOTES</span></span>
<span data-ttu-id="c8bf4-133">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, computer, apprendimento automatico, azureml</span><span class="sxs-lookup"><span data-stu-id="c8bf4-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="c8bf4-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8bf4-134">RELATED LINKS</span></span>
