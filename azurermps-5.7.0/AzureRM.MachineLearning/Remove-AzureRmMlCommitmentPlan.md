---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/remove-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 6c02b076de3d3f63685938a84e4a437e22c1e16f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521903"
---
# <span data-ttu-id="d80b0-101">Remove-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="d80b0-101">Remove-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="d80b0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d80b0-102">SYNOPSIS</span></span>
<span data-ttu-id="d80b0-103">Elimina un piano di impegni.</span><span class="sxs-lookup"><span data-stu-id="d80b0-103">Deletes a commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d80b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d80b0-104">SYNTAX</span></span>

### <span data-ttu-id="d80b0-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d80b0-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d80b0-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="d80b0-106">RemoveByObject</span></span>
```
Remove-AzureRmMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d80b0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d80b0-107">DESCRIPTION</span></span>
<span data-ttu-id="d80b0-108">Elimina un piano di impegno per l'apprendimento di un computer Azure.</span><span class="sxs-lookup"><span data-stu-id="d80b0-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="d80b0-109">Tieni presente che i piani di impegno che hanno associazioni di impegni non possono essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="d80b0-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="d80b0-110">Le associazioni di impegno possono essere eliminate solo dalla risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d80b0-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="d80b0-111">Se ad esempio si elimina un servizio Web di apprendimento di Azure Machine, verrà eliminata anche l'associazione di impegni che associa il servizio Web a un piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="d80b0-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="d80b0-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d80b0-112">EXAMPLES</span></span>

### <span data-ttu-id="d80b0-113">--------------------------Esempio 1: eliminare un piano di impegni--------------------------</span><span class="sxs-lookup"><span data-stu-id="d80b0-113">--------------------------  Example 1: Delete a commitment plan  --------------------------</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="d80b0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d80b0-114">PARAMETERS</span></span>

### <span data-ttu-id="d80b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d80b0-115">-DefaultProfile</span></span>
<span data-ttu-id="d80b0-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d80b0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d80b0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d80b0-117">-Force</span></span>
<span data-ttu-id="d80b0-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="d80b0-118">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80b0-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="d80b0-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="d80b0-120">Oggetto servizio Web di apprendimento automatico.</span><span class="sxs-lookup"><span data-stu-id="d80b0-120">The machine learning web service object.</span></span>

```yaml
Type: CommitmentPlan
Parameter Sets: RemoveByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d80b0-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d80b0-121">-Name</span></span>
<span data-ttu-id="d80b0-122">Il nome del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d80b0-122">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80b0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d80b0-123">-ResourceGroupName</span></span>
<span data-ttu-id="d80b0-124">Nome del gruppo di risorse per il piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d80b0-124">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80b0-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d80b0-125">-Confirm</span></span>
<span data-ttu-id="d80b0-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d80b0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d80b0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d80b0-127">-WhatIf</span></span>
<span data-ttu-id="d80b0-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d80b0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d80b0-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d80b0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d80b0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d80b0-130">CommonParameters</span></span>
<span data-ttu-id="d80b0-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d80b0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d80b0-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d80b0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d80b0-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d80b0-133">INPUTS</span></span>

### <span data-ttu-id="d80b0-134">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="d80b0-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="d80b0-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d80b0-135">OUTPUTS</span></span>

### <span data-ttu-id="d80b0-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d80b0-136">None</span></span>

## <span data-ttu-id="d80b0-137">Note</span><span class="sxs-lookup"><span data-stu-id="d80b0-137">NOTES</span></span>
<span data-ttu-id="d80b0-138">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="d80b0-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="d80b0-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d80b0-139">RELATED LINKS</span></span>

