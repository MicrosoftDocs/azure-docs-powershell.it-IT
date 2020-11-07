---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/new-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 1c3c7d0dce441ecc6048e9ab98d56bf79b90020e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688453"
---
# <span data-ttu-id="07572-101">New-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="07572-101">New-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="07572-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07572-102">SYNOPSIS</span></span>
<span data-ttu-id="07572-103">Crea un nuovo piano di impegni.</span><span class="sxs-lookup"><span data-stu-id="07572-103">Creates a new commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07572-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07572-104">SYNTAX</span></span>

```
New-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07572-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07572-105">DESCRIPTION</span></span>
<span data-ttu-id="07572-106">Crea un piano di impegno per l'apprendimento di un computer Azure in un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="07572-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="07572-107">Se nel gruppo risorse esiste un piano di impegni con lo stesso nome, la chiamata funge da operazione di aggiornamento e il piano di impegni esistente viene sovrascritto.</span><span class="sxs-lookup"><span data-stu-id="07572-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="07572-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07572-108">EXAMPLES</span></span>

### <span data-ttu-id="07572-109">--------------------------Esempio 1: creare un nuovo piano di impegni--------------------------</span><span class="sxs-lookup"><span data-stu-id="07572-109">--------------------------  Example 1: Create a new commitment plan  --------------------------</span></span>
```
New-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="07572-110">Crea un nuovo piano di impegno per l'apprendimento di una macchina Azure denominato "MyCommitmentPlanName" nel gruppo "MyResourceGroup" e nella regione sud centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="07572-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="07572-111">In questo esempio viene usato il SKU DevTest/standard, che indica che le risorse fornite dal piano di impegno verranno definite per i limiti di DevTest/standard.</span><span class="sxs-lookup"><span data-stu-id="07572-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be definied by the limits of DevTest/Standard.</span></span> <span data-ttu-id="07572-112">Il SkuCapacity in questo esempio è 1, il che significa che il costo del piano sarà 1x il costo di DevTest e le risorse che il piano contiene saranno 1x ciò che DevTest fornisce.</span><span class="sxs-lookup"><span data-stu-id="07572-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="07572-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07572-113">PARAMETERS</span></span>

### <span data-ttu-id="07572-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07572-114">-DefaultProfile</span></span>
<span data-ttu-id="07572-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="07572-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07572-116">-Force</span><span class="sxs-lookup"><span data-stu-id="07572-116">-Force</span></span>
<span data-ttu-id="07572-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="07572-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="07572-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="07572-118">-Location</span></span>
<span data-ttu-id="07572-119">Posizione del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="07572-119">The location of the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07572-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="07572-120">-Name</span></span>
<span data-ttu-id="07572-121">Il nome del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="07572-121">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07572-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07572-122">-ResourceGroupName</span></span>
<span data-ttu-id="07572-123">Nome del gruppo di risorse per il piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="07572-123">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07572-124">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="07572-124">-SkuCapacity</span></span>
<span data-ttu-id="07572-125">Capacità della SKU da usare per il provisioning del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="07572-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07572-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="07572-126">-SkuName</span></span>
<span data-ttu-id="07572-127">Nome dell'USK da usare per il provisioning del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="07572-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07572-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="07572-128">-SkuTier</span></span>
<span data-ttu-id="07572-129">Il livello della SKU da usare per il provisioning del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="07572-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07572-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="07572-130">-Confirm</span></span>
<span data-ttu-id="07572-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07572-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07572-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07572-132">-WhatIf</span></span>
<span data-ttu-id="07572-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07572-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07572-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07572-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07572-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07572-135">CommonParameters</span></span>
<span data-ttu-id="07572-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07572-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07572-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07572-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07572-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07572-138">INPUTS</span></span>

### <span data-ttu-id="07572-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="07572-139">None</span></span>
<span data-ttu-id="07572-140">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="07572-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="07572-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07572-141">OUTPUTS</span></span>

### <span data-ttu-id="07572-142">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="07572-142">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="07572-143">Note</span><span class="sxs-lookup"><span data-stu-id="07572-143">NOTES</span></span>
<span data-ttu-id="07572-144">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="07572-144">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="07572-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07572-145">RELATED LINKS</span></span>

