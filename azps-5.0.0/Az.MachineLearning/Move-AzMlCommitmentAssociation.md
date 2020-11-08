---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/move-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
ms.openlocfilehash: c127ff40690658a98f9d0f0fa670cddfca123f89
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202392"
---
# <span data-ttu-id="91772-101">Move-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="91772-101">Move-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="91772-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91772-102">SYNOPSIS</span></span>
<span data-ttu-id="91772-103">Sposta un'associazione di impegni da un piano di impegno a un altro.</span><span class="sxs-lookup"><span data-stu-id="91772-103">Moves a commitment association from one commitment plan to another.</span></span>

## <span data-ttu-id="91772-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91772-104">SYNTAX</span></span>

```
Move-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91772-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91772-105">DESCRIPTION</span></span>
<span data-ttu-id="91772-106">Sposta una risorsa di associazione di impegni dal piano di impegno padre a un altro piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="91772-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="91772-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91772-107">EXAMPLES</span></span>

### <span data-ttu-id="91772-108">Esempio 1: trasferimento di un'associazione di impegni</span><span class="sxs-lookup"><span data-stu-id="91772-108">Example 1: Move a commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="91772-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91772-109">PARAMETERS</span></span>

### <span data-ttu-id="91772-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="91772-110">-CommitmentPlanName</span></span>
<span data-ttu-id="91772-111">Il nome del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="91772-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="91772-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91772-112">-DefaultProfile</span></span>
<span data-ttu-id="91772-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="91772-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91772-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="91772-114">-DestinationPlanId</span></span>
<span data-ttu-id="91772-115">ID risorsa Azure del piano di impegni di Azure ML di destinazione.</span><span class="sxs-lookup"><span data-stu-id="91772-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="91772-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="91772-116">-Name</span></span>
<span data-ttu-id="91772-117">Nome dell'associazione di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="91772-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="91772-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91772-118">-ResourceGroupName</span></span>
<span data-ttu-id="91772-119">Nome del gruppo di risorse per l'associazione di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="91772-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="91772-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="91772-120">-Confirm</span></span>
<span data-ttu-id="91772-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91772-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91772-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91772-122">-WhatIf</span></span>
<span data-ttu-id="91772-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91772-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91772-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91772-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91772-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91772-125">CommonParameters</span></span>
<span data-ttu-id="91772-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91772-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91772-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91772-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91772-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91772-128">INPUTS</span></span>

### <span data-ttu-id="91772-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="91772-129">None</span></span>

## <span data-ttu-id="91772-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91772-130">OUTPUTS</span></span>

### <span data-ttu-id="91772-131">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="91772-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="91772-132">Note</span><span class="sxs-lookup"><span data-stu-id="91772-132">NOTES</span></span>
<span data-ttu-id="91772-133">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="91772-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="91772-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91772-134">RELATED LINKS</span></span>
