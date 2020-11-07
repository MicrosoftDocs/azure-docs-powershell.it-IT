---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 31678552a43951406d18c49ee80ffaa7897fd1d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688621"
---
# <span data-ttu-id="35611-101">Remove-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="35611-101">Remove-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="35611-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35611-102">SYNOPSIS</span></span>
<span data-ttu-id="35611-103">Elimina un piano di impegni.</span><span class="sxs-lookup"><span data-stu-id="35611-103">Deletes a commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35611-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35611-104">SYNTAX</span></span>

### <span data-ttu-id="35611-105">Rimuovere un piano di impegni di Azure ML specificato per nome e gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="35611-105">Remove an Azure ML commitment plan specified by name and resource group.</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35611-106">Rimuovere un piano di impegni di Azure ML specificato come oggetto.</span><span class="sxs-lookup"><span data-stu-id="35611-106">Remove an Azure ML commitment plan specified as an object.</span></span>
```
Remove-AzureRmMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35611-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35611-107">DESCRIPTION</span></span>
<span data-ttu-id="35611-108">Elimina un piano di impegno per l'apprendimento di un computer Azure.</span><span class="sxs-lookup"><span data-stu-id="35611-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="35611-109">Tieni presente che i piani di impegno che hanno associazioni di impegni non possono essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="35611-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="35611-110">Le associazioni di impegno possono essere eliminate solo dalla risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="35611-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="35611-111">Se ad esempio si elimina un servizio Web di apprendimento di Azure Machine, verrà eliminata anche l'associazione di impegni che associa il servizio Web a un piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="35611-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="35611-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35611-112">EXAMPLES</span></span>

### <span data-ttu-id="35611-113">--------------------------Esempio 1: eliminare un piano di impegni--------------------------</span><span class="sxs-lookup"><span data-stu-id="35611-113">--------------------------  Example 1: Delete a commitment plan  --------------------------</span></span>
<span data-ttu-id="35611-114">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="35611-114">@{paragraph=PS C:\\\>}</span></span>





```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="35611-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35611-115">PARAMETERS</span></span>

### <span data-ttu-id="35611-116">-Force</span><span class="sxs-lookup"><span data-stu-id="35611-116">-Force</span></span>
<span data-ttu-id="35611-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="35611-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="35611-118">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="35611-118">-MlCommitmentPlan</span></span>
<span data-ttu-id="35611-119">Oggetto servizio Web di apprendimento automatico.</span><span class="sxs-lookup"><span data-stu-id="35611-119">The machine learning web service object.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan
Parameter Sets: Remove an Azure ML commitment plan specified as an object.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35611-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="35611-120">-Name</span></span>
<span data-ttu-id="35611-121">Il nome del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="35611-121">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML commitment plan specified by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35611-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35611-122">-ResourceGroupName</span></span>
<span data-ttu-id="35611-123">Nome del gruppo di risorse per il piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="35611-123">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML commitment plan specified by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35611-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="35611-124">-Confirm</span></span>
<span data-ttu-id="35611-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35611-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35611-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35611-126">-WhatIf</span></span>
<span data-ttu-id="35611-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35611-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35611-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35611-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35611-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35611-129">-DefaultProfile</span></span>
<span data-ttu-id="35611-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35611-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35611-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35611-131">CommonParameters</span></span>
<span data-ttu-id="35611-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35611-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35611-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35611-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35611-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35611-134">INPUTS</span></span>

### <span data-ttu-id="35611-135">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="35611-135">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="35611-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35611-136">OUTPUTS</span></span>

### <span data-ttu-id="35611-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="35611-137">None</span></span>

## <span data-ttu-id="35611-138">Note</span><span class="sxs-lookup"><span data-stu-id="35611-138">NOTES</span></span>
<span data-ttu-id="35611-139">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="35611-139">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="35611-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35611-140">RELATED LINKS</span></span>

