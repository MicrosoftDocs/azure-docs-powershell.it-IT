---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/move-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
ms.openlocfilehash: 019ff5b50eb366947f82004d60ae38888532ac10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952365"
---
# <span data-ttu-id="6c8de-101">Move-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="6c8de-101">Move-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="6c8de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c8de-102">SYNOPSIS</span></span>
<span data-ttu-id="6c8de-103">Sposta un'associazione di impegno da un piano di impegno a un altro.</span><span class="sxs-lookup"><span data-stu-id="6c8de-103">Moves a commitment association from one commitment plan to another.</span></span>

## <span data-ttu-id="6c8de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c8de-104">SYNTAX</span></span>

```
Move-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c8de-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6c8de-105">DESCRIPTION</span></span>
<span data-ttu-id="6c8de-106">Sposta una risorsa di associazione dell'impegno dal piano di impegno padre a un altro piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="6c8de-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="6c8de-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c8de-107">EXAMPLES</span></span>

### <span data-ttu-id="6c8de-108">Esempio 1: Spostare un'associazione di impegno</span><span class="sxs-lookup"><span data-stu-id="6c8de-108">Example 1: Move a commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="6c8de-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c8de-109">PARAMETERS</span></span>

### <span data-ttu-id="6c8de-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="6c8de-110">-CommitmentPlanName</span></span>
<span data-ttu-id="6c8de-111">Nome del piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="6c8de-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="6c8de-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c8de-112">-DefaultProfile</span></span>
<span data-ttu-id="6c8de-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6c8de-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c8de-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="6c8de-114">-DestinationPlanId</span></span>
<span data-ttu-id="6c8de-115">ID della risorsa Azure del piano di impegno di Azure ML di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6c8de-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="6c8de-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6c8de-116">-Name</span></span>
<span data-ttu-id="6c8de-117">Nome dell'associazione di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="6c8de-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="6c8de-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c8de-118">-ResourceGroupName</span></span>
<span data-ttu-id="6c8de-119">Nome del gruppo di risorse per l'associazione di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="6c8de-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="6c8de-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c8de-120">-Confirm</span></span>
<span data-ttu-id="6c8de-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c8de-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c8de-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c8de-122">-WhatIf</span></span>
<span data-ttu-id="6c8de-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c8de-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c8de-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c8de-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c8de-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c8de-125">CommonParameters</span></span>
<span data-ttu-id="6c8de-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c8de-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c8de-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c8de-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c8de-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="6c8de-128">INPUTS</span></span>

### <span data-ttu-id="6c8de-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6c8de-129">None</span></span>

## <span data-ttu-id="6c8de-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c8de-130">OUTPUTS</span></span>

### <span data-ttu-id="6c8de-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="6c8de-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="6c8de-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="6c8de-132">NOTES</span></span>
<span data-ttu-id="6c8de-133">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, computer, apprendimento automatico, azureml</span><span class="sxs-lookup"><span data-stu-id="6c8de-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="6c8de-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c8de-134">RELATED LINKS</span></span>
