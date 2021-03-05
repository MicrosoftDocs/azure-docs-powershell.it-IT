---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/new-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
ms.openlocfilehash: f5386f3c971159f2a33353efeb380164447ee295
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972718"
---
# <span data-ttu-id="d3d5a-101">New-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="d3d5a-101">New-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="d3d5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3d5a-102">SYNOPSIS</span></span>
<span data-ttu-id="d3d5a-103">Crea un nuovo piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="d3d5a-103">Creates a new commitment plan.</span></span>

## <span data-ttu-id="d3d5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3d5a-104">SYNTAX</span></span>

```
New-AzMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3d5a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d3d5a-105">DESCRIPTION</span></span>
<span data-ttu-id="d3d5a-106">Crea un piano di impegno per Azure Machine Learning in un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="d3d5a-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="d3d5a-107">Se nel gruppo di risorse è presente un piano di impegno con lo stesso nome, la chiamata funge da operazione di aggiornamento e il piano di impegno esistente viene sovrascritto.</span><span class="sxs-lookup"><span data-stu-id="d3d5a-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="d3d5a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3d5a-108">EXAMPLES</span></span>

### <span data-ttu-id="d3d5a-109">Esempio 1: Creare un nuovo piano di impegno</span><span class="sxs-lookup"><span data-stu-id="d3d5a-109">Example 1: Create a new commitment plan</span></span>
```
New-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="d3d5a-110">Crea un nuovo piano di impegno di Azure Machine Learning denominato "MyCommitmentPlanName" nel gruppo "MyResourceGroup" e nell'area sud degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="d3d5a-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="d3d5a-111">In questo esempio viene usato lo SKU DevTest/Standard, ovvero le risorse fornite dal piano di impegno saranno definite dai limiti di DevTest/Standard.</span><span class="sxs-lookup"><span data-stu-id="d3d5a-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be defined by the limits of DevTest/Standard.</span></span> <span data-ttu-id="d3d5a-112">SkuCapacity in questo esempio è 1, ovvero il costo del piano sarà 1x il costo di DevTest e le risorse contenute nel piano saranno 1x quanto fornito da DevTest.</span><span class="sxs-lookup"><span data-stu-id="d3d5a-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="d3d5a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3d5a-113">PARAMETERS</span></span>

### <span data-ttu-id="d3d5a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3d5a-114">-DefaultProfile</span></span>
<span data-ttu-id="d3d5a-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="d3d5a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3d5a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d3d5a-116">-Force</span></span>
<span data-ttu-id="d3d5a-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="d3d5a-117">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d5a-118">-Location</span><span class="sxs-lookup"><span data-stu-id="d3d5a-118">-Location</span></span>
<span data-ttu-id="d3d5a-119">Posizione del piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d3d5a-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="d3d5a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d3d5a-120">-Name</span></span>
<span data-ttu-id="d3d5a-121">Nome del piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d3d5a-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="d3d5a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3d5a-122">-ResourceGroupName</span></span>
<span data-ttu-id="d3d5a-123">Nome del gruppo di risorse per il piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d3d5a-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="d3d5a-124">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="d3d5a-124">-SkuCapacity</span></span>
<span data-ttu-id="d3d5a-125">Capacità dello SKU da usare durante il provisioning del piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d3d5a-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="d3d5a-126">-SKUName</span><span class="sxs-lookup"><span data-stu-id="d3d5a-126">-SkuName</span></span>
<span data-ttu-id="d3d5a-127">Nome dello SKU da usare durante il provisioning del piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d3d5a-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="d3d5a-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d3d5a-128">-SkuTier</span></span>
<span data-ttu-id="d3d5a-129">Livello dello SKU da usare durante il provisioning del piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d3d5a-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="d3d5a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3d5a-130">-Confirm</span></span>
<span data-ttu-id="d3d5a-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3d5a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3d5a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3d5a-132">-WhatIf</span></span>
<span data-ttu-id="d3d5a-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3d5a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3d5a-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3d5a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3d5a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3d5a-135">CommonParameters</span></span>
<span data-ttu-id="d3d5a-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3d5a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3d5a-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3d5a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3d5a-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="d3d5a-138">INPUTS</span></span>

### <span data-ttu-id="d3d5a-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d3d5a-139">None</span></span>

## <span data-ttu-id="d3d5a-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3d5a-140">OUTPUTS</span></span>

### <span data-ttu-id="d3d5a-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="d3d5a-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="d3d5a-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="d3d5a-142">NOTES</span></span>
<span data-ttu-id="d3d5a-143">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, computer, apprendimento automatico, azureml</span><span class="sxs-lookup"><span data-stu-id="d3d5a-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="d3d5a-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3d5a-144">RELATED LINKS</span></span>
