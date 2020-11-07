---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
ms.openlocfilehash: 1c022d8ae97ac9f1e51bbabaff15a9dec61f5d87
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673924"
---
# <span data-ttu-id="aabfe-101">Remove-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="aabfe-101">Remove-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="aabfe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aabfe-102">SYNOPSIS</span></span>
<span data-ttu-id="aabfe-103">Elimina un piano di impegni.</span><span class="sxs-lookup"><span data-stu-id="aabfe-103">Deletes a commitment plan.</span></span>

## <span data-ttu-id="aabfe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aabfe-104">SYNTAX</span></span>

### <span data-ttu-id="aabfe-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="aabfe-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aabfe-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="aabfe-106">RemoveByObject</span></span>
```
Remove-AzMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aabfe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aabfe-107">DESCRIPTION</span></span>
<span data-ttu-id="aabfe-108">Elimina un piano di impegno per l'apprendimento di un computer Azure.</span><span class="sxs-lookup"><span data-stu-id="aabfe-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="aabfe-109">Tieni presente che i piani di impegno che hanno associazioni di impegni non possono essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="aabfe-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="aabfe-110">Le associazioni di impegno possono essere eliminate solo dalla risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="aabfe-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="aabfe-111">Se ad esempio si elimina un servizio Web di apprendimento di Azure Machine, verrà eliminata anche l'associazione di impegni che associa il servizio Web a un piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="aabfe-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="aabfe-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aabfe-112">EXAMPLES</span></span>

### <span data-ttu-id="aabfe-113">Esempio 1: eliminare un piano di impegno</span><span class="sxs-lookup"><span data-stu-id="aabfe-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="aabfe-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aabfe-114">PARAMETERS</span></span>

### <span data-ttu-id="aabfe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aabfe-115">-DefaultProfile</span></span>
<span data-ttu-id="aabfe-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="aabfe-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aabfe-117">-Force</span><span class="sxs-lookup"><span data-stu-id="aabfe-117">-Force</span></span>
<span data-ttu-id="aabfe-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="aabfe-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="aabfe-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="aabfe-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="aabfe-120">Oggetto servizio Web di apprendimento automatico.</span><span class="sxs-lookup"><span data-stu-id="aabfe-120">The machine learning web service object.</span></span>

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

### <span data-ttu-id="aabfe-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="aabfe-121">-Name</span></span>
<span data-ttu-id="aabfe-122">Il nome del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="aabfe-122">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="aabfe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aabfe-123">-ResourceGroupName</span></span>
<span data-ttu-id="aabfe-124">Nome del gruppo di risorse per il piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="aabfe-124">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="aabfe-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aabfe-125">-Confirm</span></span>
<span data-ttu-id="aabfe-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aabfe-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aabfe-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aabfe-127">-WhatIf</span></span>
<span data-ttu-id="aabfe-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aabfe-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aabfe-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aabfe-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aabfe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aabfe-130">CommonParameters</span></span>
<span data-ttu-id="aabfe-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aabfe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aabfe-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aabfe-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aabfe-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aabfe-133">INPUTS</span></span>

### <span data-ttu-id="aabfe-134">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="aabfe-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="aabfe-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aabfe-135">OUTPUTS</span></span>

### <span data-ttu-id="aabfe-136">System. void</span><span class="sxs-lookup"><span data-stu-id="aabfe-136">System.Void</span></span>

## <span data-ttu-id="aabfe-137">Note</span><span class="sxs-lookup"><span data-stu-id="aabfe-137">NOTES</span></span>
<span data-ttu-id="aabfe-138">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="aabfe-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="aabfe-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aabfe-139">RELATED LINKS</span></span>
