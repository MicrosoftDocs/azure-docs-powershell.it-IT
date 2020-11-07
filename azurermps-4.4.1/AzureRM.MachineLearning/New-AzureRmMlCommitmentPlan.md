---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 984e1f9d75a7c5a56e6a9bda71a07b193df5be15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688283"
---
# <span data-ttu-id="ef0ec-101">New-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ef0ec-101">New-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="ef0ec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ef0ec-102">SYNOPSIS</span></span>
<span data-ttu-id="ef0ec-103">Crea un nuovo piano di impegni.</span><span class="sxs-lookup"><span data-stu-id="ef0ec-103">Creates a new commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef0ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef0ec-104">SYNTAX</span></span>

```
New-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef0ec-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef0ec-105">DESCRIPTION</span></span>
<span data-ttu-id="ef0ec-106">Crea un piano di impegno per l'apprendimento di un computer Azure in un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="ef0ec-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="ef0ec-107">Se nel gruppo risorse esiste un piano di impegni con lo stesso nome, la chiamata funge da operazione di aggiornamento e il piano di impegni esistente viene sovrascritto.</span><span class="sxs-lookup"><span data-stu-id="ef0ec-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="ef0ec-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef0ec-108">EXAMPLES</span></span>

### <span data-ttu-id="ef0ec-109">--------------------------Esempio 1: creare un nuovo piano di impegni--------------------------</span><span class="sxs-lookup"><span data-stu-id="ef0ec-109">--------------------------  Example 1: Create a new commitment plan  --------------------------</span></span>
<span data-ttu-id="ef0ec-110">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="ef0ec-110">@{paragraph=PS C:\\\>}</span></span>





```
New-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="ef0ec-111">Crea un nuovo piano di impegno per l'apprendimento di una macchina Azure denominato "MyCommitmentPlanName" nel gruppo "MyResourceGroup" e nella regione sud centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="ef0ec-111">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="ef0ec-112">In questo esempio viene usato il SKU DevTest/standard, che indica che le risorse fornite dal piano di impegno verranno definite per i limiti di DevTest/standard.</span><span class="sxs-lookup"><span data-stu-id="ef0ec-112">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be definied by the limits of DevTest/Standard.</span></span> <span data-ttu-id="ef0ec-113">Il SkuCapacity in questo esempio è 1, il che significa che il costo del piano sarà 1x il costo di DevTest e le risorse che il piano contiene saranno 1x ciò che DevTest fornisce.</span><span class="sxs-lookup"><span data-stu-id="ef0ec-113">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="ef0ec-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ef0ec-114">PARAMETERS</span></span>

### <span data-ttu-id="ef0ec-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ef0ec-115">-Force</span></span>
<span data-ttu-id="ef0ec-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ef0ec-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ef0ec-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ef0ec-117">-Location</span></span>
<span data-ttu-id="ef0ec-118">Posizione del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ef0ec-118">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ef0ec-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef0ec-119">-Name</span></span>
<span data-ttu-id="ef0ec-120">Il nome del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ef0ec-120">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ef0ec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef0ec-121">-ResourceGroupName</span></span>
<span data-ttu-id="ef0ec-122">Nome del gruppo di risorse per il piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ef0ec-122">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ef0ec-123">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ef0ec-123">-SkuCapacity</span></span>
<span data-ttu-id="ef0ec-124">Capacità della SKU da usare per il provisioning del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ef0ec-124">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ef0ec-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ef0ec-125">-SkuName</span></span>
<span data-ttu-id="ef0ec-126">Nome dell'USK da usare per il provisioning del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ef0ec-126">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ef0ec-127">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ef0ec-127">-SkuTier</span></span>
<span data-ttu-id="ef0ec-128">Il livello della SKU da usare per il provisioning del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ef0ec-128">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ef0ec-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ef0ec-129">-Confirm</span></span>
<span data-ttu-id="ef0ec-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef0ec-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef0ec-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef0ec-131">-WhatIf</span></span>
<span data-ttu-id="ef0ec-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ef0ec-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef0ec-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ef0ec-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef0ec-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef0ec-134">-DefaultProfile</span></span>
<span data-ttu-id="ef0ec-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ef0ec-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef0ec-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef0ec-136">CommonParameters</span></span>
<span data-ttu-id="ef0ec-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef0ec-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef0ec-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef0ec-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef0ec-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ef0ec-139">INPUTS</span></span>

## <span data-ttu-id="ef0ec-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef0ec-140">OUTPUTS</span></span>

### <span data-ttu-id="ef0ec-141">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ef0ec-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="ef0ec-142">Note</span><span class="sxs-lookup"><span data-stu-id="ef0ec-142">NOTES</span></span>
<span data-ttu-id="ef0ec-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="ef0ec-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ef0ec-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef0ec-144">RELATED LINKS</span></span>

