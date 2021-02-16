---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
ms.openlocfilehash: 8593853817739438176b70424ab529f0811d90de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190294"
---
# <span data-ttu-id="59618-101">Remove-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="59618-101">Remove-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="59618-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59618-102">SYNOPSIS</span></span>
<span data-ttu-id="59618-103">Elimina un piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="59618-103">Deletes a commitment plan.</span></span>

## <span data-ttu-id="59618-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59618-104">SYNTAX</span></span>

### <span data-ttu-id="59618-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="59618-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59618-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="59618-106">RemoveByObject</span></span>
```
Remove-AzMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59618-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="59618-107">DESCRIPTION</span></span>
<span data-ttu-id="59618-108">Elimina un piano di impegno di Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="59618-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="59618-109">Si noti che i piani di impegno con associazioni di impegno non possono essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="59618-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="59618-110">Le associazioni di impegno possono essere eliminate solo dalla risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="59618-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="59618-111">Ad esempio, se si elimina un servizio Web di Apprendimento automatico di Azure, verrà eliminata anche l'associazione di impegno che associa il servizio Web a un piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="59618-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="59618-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59618-112">EXAMPLES</span></span>

### <span data-ttu-id="59618-113">Esempio 1: Eliminare un piano di impegno</span><span class="sxs-lookup"><span data-stu-id="59618-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="59618-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59618-114">PARAMETERS</span></span>

### <span data-ttu-id="59618-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59618-115">-DefaultProfile</span></span>
<span data-ttu-id="59618-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="59618-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59618-117">-Force</span><span class="sxs-lookup"><span data-stu-id="59618-117">-Force</span></span>
<span data-ttu-id="59618-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="59618-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="59618-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="59618-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="59618-120">Oggetto del servizio Web di apprendimento automatico.</span><span class="sxs-lookup"><span data-stu-id="59618-120">The machine learning web service object.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59618-121">-Name</span><span class="sxs-lookup"><span data-stu-id="59618-121">-Name</span></span>
<span data-ttu-id="59618-122">Nome del piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="59618-122">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59618-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59618-123">-ResourceGroupName</span></span>
<span data-ttu-id="59618-124">Nome del gruppo di risorse per il piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="59618-124">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59618-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59618-125">-Confirm</span></span>
<span data-ttu-id="59618-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59618-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59618-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59618-127">-WhatIf</span></span>
<span data-ttu-id="59618-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59618-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59618-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59618-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59618-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59618-130">CommonParameters</span></span>
<span data-ttu-id="59618-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59618-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59618-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59618-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59618-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="59618-133">INPUTS</span></span>

### <span data-ttu-id="59618-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="59618-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="59618-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59618-135">OUTPUTS</span></span>

### <span data-ttu-id="59618-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="59618-136">System.Void</span></span>

## <span data-ttu-id="59618-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="59618-137">NOTES</span></span>
<span data-ttu-id="59618-138">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, computer, apprendimento automatico, azureml</span><span class="sxs-lookup"><span data-stu-id="59618-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="59618-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59618-139">RELATED LINKS</span></span>
