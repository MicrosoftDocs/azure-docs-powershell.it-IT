---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
ms.openlocfilehash: f829486dfa2ae1654678597ff79c730a49454275
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673928"
---
# <span data-ttu-id="8c52b-101">New-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="8c52b-101">New-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="8c52b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8c52b-102">SYNOPSIS</span></span>
<span data-ttu-id="8c52b-103">Crea un nuovo piano di impegni.</span><span class="sxs-lookup"><span data-stu-id="8c52b-103">Creates a new commitment plan.</span></span>

## <span data-ttu-id="8c52b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c52b-104">SYNTAX</span></span>

```
New-AzMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c52b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c52b-105">DESCRIPTION</span></span>
<span data-ttu-id="8c52b-106">Crea un piano di impegno per l'apprendimento di un computer Azure in un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="8c52b-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="8c52b-107">Se nel gruppo risorse esiste un piano di impegni con lo stesso nome, la chiamata funge da operazione di aggiornamento e il piano di impegni esistente viene sovrascritto.</span><span class="sxs-lookup"><span data-stu-id="8c52b-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="8c52b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c52b-108">EXAMPLES</span></span>

### <span data-ttu-id="8c52b-109">Esempio 1: creare un nuovo piano di impegno</span><span class="sxs-lookup"><span data-stu-id="8c52b-109">Example 1: Create a new commitment plan</span></span>
```
New-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="8c52b-110">Crea un nuovo piano di impegno per l'apprendimento di una macchina Azure denominato "MyCommitmentPlanName" nel gruppo "MyResourceGroup" e nella regione sud centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="8c52b-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="8c52b-111">In questo esempio viene usato il SKU DevTest/standard, che indica che le risorse fornite dal piano di impegno verranno definite entro i limiti di DevTest/standard.</span><span class="sxs-lookup"><span data-stu-id="8c52b-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be defined by the limits of DevTest/Standard.</span></span> <span data-ttu-id="8c52b-112">Il SkuCapacity in questo esempio è 1, il che significa che il costo del piano sarà 1x il costo di DevTest e le risorse che il piano contiene saranno 1x ciò che DevTest fornisce.</span><span class="sxs-lookup"><span data-stu-id="8c52b-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="8c52b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8c52b-113">PARAMETERS</span></span>

### <span data-ttu-id="8c52b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c52b-114">-DefaultProfile</span></span>
<span data-ttu-id="8c52b-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8c52b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c52b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8c52b-116">-Force</span></span>
<span data-ttu-id="8c52b-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="8c52b-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8c52b-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8c52b-118">-Location</span></span>
<span data-ttu-id="8c52b-119">Posizione del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="8c52b-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="8c52b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c52b-120">-Name</span></span>
<span data-ttu-id="8c52b-121">Il nome del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="8c52b-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="8c52b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c52b-122">-ResourceGroupName</span></span>
<span data-ttu-id="8c52b-123">Nome del gruppo di risorse per il piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="8c52b-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="8c52b-124">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="8c52b-124">-SkuCapacity</span></span>
<span data-ttu-id="8c52b-125">Capacità della SKU da usare per il provisioning del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="8c52b-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="8c52b-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8c52b-126">-SkuName</span></span>
<span data-ttu-id="8c52b-127">Nome dell'USK da usare per il provisioning del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="8c52b-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="8c52b-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="8c52b-128">-SkuTier</span></span>
<span data-ttu-id="8c52b-129">Il livello della SKU da usare per il provisioning del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="8c52b-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="8c52b-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8c52b-130">-Confirm</span></span>
<span data-ttu-id="8c52b-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c52b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c52b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c52b-132">-WhatIf</span></span>
<span data-ttu-id="8c52b-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c52b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c52b-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c52b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c52b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c52b-135">CommonParameters</span></span>
<span data-ttu-id="8c52b-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c52b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c52b-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c52b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c52b-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8c52b-138">INPUTS</span></span>

### <span data-ttu-id="8c52b-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8c52b-139">None</span></span>

## <span data-ttu-id="8c52b-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c52b-140">OUTPUTS</span></span>

### <span data-ttu-id="8c52b-141">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="8c52b-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="8c52b-142">Note</span><span class="sxs-lookup"><span data-stu-id="8c52b-142">NOTES</span></span>
<span data-ttu-id="8c52b-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="8c52b-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="8c52b-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c52b-144">RELATED LINKS</span></span>