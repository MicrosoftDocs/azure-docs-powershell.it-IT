---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/move-azurermmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 2bd650e86a1a4b59694dc88dc915da0fd7713e5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521910"
---
# <span data-ttu-id="18e6e-101">Move-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="18e6e-101">Move-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="18e6e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18e6e-102">SYNOPSIS</span></span>
<span data-ttu-id="18e6e-103">Sposta un'associazione di impegni da un piano di impegno a un altro.</span><span class="sxs-lookup"><span data-stu-id="18e6e-103">Moves a commitment association from one commitment plan to another.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18e6e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18e6e-104">SYNTAX</span></span>

```
Move-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18e6e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18e6e-105">DESCRIPTION</span></span>
<span data-ttu-id="18e6e-106">Sposta una risorsa di associazione di impegni dal piano di impegno padre a un altro piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="18e6e-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="18e6e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18e6e-107">EXAMPLES</span></span>

### <span data-ttu-id="18e6e-108">--------------------------Esempio 1: trasferire un'associazione di impegni--------------------------</span><span class="sxs-lookup"><span data-stu-id="18e6e-108">--------------------------  Example 1: Move a commitment association  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="18e6e-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18e6e-109">PARAMETERS</span></span>

### <span data-ttu-id="18e6e-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="18e6e-110">-CommitmentPlanName</span></span>
<span data-ttu-id="18e6e-111">Il nome del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="18e6e-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="18e6e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18e6e-112">-DefaultProfile</span></span>
<span data-ttu-id="18e6e-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="18e6e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18e6e-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="18e6e-114">-DestinationPlanId</span></span>
<span data-ttu-id="18e6e-115">ID risorsa Azure del piano di impegni di Azure ML di destinazione.</span><span class="sxs-lookup"><span data-stu-id="18e6e-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="18e6e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="18e6e-116">-Name</span></span>
<span data-ttu-id="18e6e-117">Nome dell'associazione di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="18e6e-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="18e6e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18e6e-118">-ResourceGroupName</span></span>
<span data-ttu-id="18e6e-119">Nome del gruppo di risorse per l'associazione di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="18e6e-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="18e6e-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="18e6e-120">-Confirm</span></span>
<span data-ttu-id="18e6e-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18e6e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18e6e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18e6e-122">-WhatIf</span></span>
<span data-ttu-id="18e6e-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18e6e-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18e6e-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18e6e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18e6e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18e6e-125">CommonParameters</span></span>
<span data-ttu-id="18e6e-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18e6e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18e6e-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18e6e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18e6e-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18e6e-128">INPUTS</span></span>

### <span data-ttu-id="18e6e-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="18e6e-129">None</span></span>
<span data-ttu-id="18e6e-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="18e6e-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="18e6e-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18e6e-131">OUTPUTS</span></span>

### <span data-ttu-id="18e6e-132">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="18e6e-132">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="18e6e-133">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="18e6e-133">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="18e6e-134">Note</span><span class="sxs-lookup"><span data-stu-id="18e6e-134">NOTES</span></span>
<span data-ttu-id="18e6e-135">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="18e6e-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="18e6e-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18e6e-136">RELATED LINKS</span></span>

