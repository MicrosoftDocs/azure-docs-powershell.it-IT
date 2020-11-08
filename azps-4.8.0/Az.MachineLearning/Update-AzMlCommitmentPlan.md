---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
ms.openlocfilehash: 733f473ed09807c33355ac6bc22491a160e5481a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189624"
---
# <span data-ttu-id="045fd-101">Update-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="045fd-101">Update-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="045fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="045fd-102">SYNOPSIS</span></span>
<span data-ttu-id="045fd-103">Aggiorna le proprietà di una risorsa del piano di impegni esistente.</span><span class="sxs-lookup"><span data-stu-id="045fd-103">Updates properties of an existing commitment plan resource.</span></span>

## <span data-ttu-id="045fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="045fd-104">SYNTAX</span></span>

```
Update-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="045fd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="045fd-105">DESCRIPTION</span></span>
<span data-ttu-id="045fd-106">Aggiorna una risorsa del piano di impegni esistente.</span><span class="sxs-lookup"><span data-stu-id="045fd-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="045fd-107">Tieni presente che la maggior parte delle proprietà del piano di impegni non è modificabile e non può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="045fd-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="045fd-108">Le proprietà che possono essere modificate includono SKU (che consente di eseguire la migrazione del piano di impegno da una SKU a un'altra) e i contrassegni.</span><span class="sxs-lookup"><span data-stu-id="045fd-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="045fd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="045fd-109">EXAMPLES</span></span>

### <span data-ttu-id="045fd-110">Esempio 1: aggiornare un piano di impegno</span><span class="sxs-lookup"><span data-stu-id="045fd-110">Example 1: Update a commitment plan</span></span>
```
Update-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="045fd-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="045fd-111">PARAMETERS</span></span>

### <span data-ttu-id="045fd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="045fd-112">-DefaultProfile</span></span>
<span data-ttu-id="045fd-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="045fd-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="045fd-114">-Force</span><span class="sxs-lookup"><span data-stu-id="045fd-114">-Force</span></span>
<span data-ttu-id="045fd-115">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="045fd-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="045fd-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="045fd-116">-Name</span></span>
<span data-ttu-id="045fd-117">Il nome del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="045fd-117">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="045fd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="045fd-118">-ResourceGroupName</span></span>
<span data-ttu-id="045fd-119">Nome del gruppo di risorse per il piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="045fd-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="045fd-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="045fd-120">-SkuCapacity</span></span>
<span data-ttu-id="045fd-121">Capacità dell'USK da usare quando si aggiorna il piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="045fd-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="045fd-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="045fd-122">-SkuName</span></span>
<span data-ttu-id="045fd-123">Nome dell'USK da usare per l'aggiornamento del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="045fd-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="045fd-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="045fd-124">-SkuTier</span></span>
<span data-ttu-id="045fd-125">Livello dell'USK da usare per l'aggiornamento del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="045fd-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="045fd-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="045fd-126">-Tag</span></span>
<span data-ttu-id="045fd-127">Tag per la risorsa piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="045fd-127">Tags for the commitment plan resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="045fd-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="045fd-128">-Confirm</span></span>
<span data-ttu-id="045fd-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="045fd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="045fd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="045fd-130">-WhatIf</span></span>
<span data-ttu-id="045fd-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="045fd-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="045fd-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="045fd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="045fd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="045fd-133">CommonParameters</span></span>
<span data-ttu-id="045fd-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="045fd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="045fd-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="045fd-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="045fd-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="045fd-136">INPUTS</span></span>

### <span data-ttu-id="045fd-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="045fd-137">None</span></span>

## <span data-ttu-id="045fd-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="045fd-138">OUTPUTS</span></span>

### <span data-ttu-id="045fd-139">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="045fd-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="045fd-140">Note</span><span class="sxs-lookup"><span data-stu-id="045fd-140">NOTES</span></span>
<span data-ttu-id="045fd-141">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="045fd-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="045fd-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="045fd-142">RELATED LINKS</span></span>