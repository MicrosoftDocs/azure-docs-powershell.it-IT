---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
ms.openlocfilehash: 733f473ed09807c33355ac6bc22491a160e5481a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192270"
---
# <span data-ttu-id="4bf36-101">Update-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="4bf36-101">Update-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="4bf36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bf36-102">SYNOPSIS</span></span>
<span data-ttu-id="4bf36-103">Aggiorna le proprietà di una risorsa del piano di impegno esistente.</span><span class="sxs-lookup"><span data-stu-id="4bf36-103">Updates properties of an existing commitment plan resource.</span></span>

## <span data-ttu-id="4bf36-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4bf36-104">SYNTAX</span></span>

```
Update-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bf36-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4bf36-105">DESCRIPTION</span></span>
<span data-ttu-id="4bf36-106">Aggiorna una risorsa del piano di impegno esistente.</span><span class="sxs-lookup"><span data-stu-id="4bf36-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="4bf36-107">Si noti che la maggior parte delle proprietà del piano di impegno non è modificabile e non può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="4bf36-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="4bf36-108">Le proprietà che possono essere modificate includono SKU (che consente di eseguire la migrazione del piano di impegno da uno SKU a un altro) e Tag.</span><span class="sxs-lookup"><span data-stu-id="4bf36-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="4bf36-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4bf36-109">EXAMPLES</span></span>

### <span data-ttu-id="4bf36-110">Esempio 1: Aggiornare un piano di impegno</span><span class="sxs-lookup"><span data-stu-id="4bf36-110">Example 1: Update a commitment plan</span></span>
```
Update-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="4bf36-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bf36-111">PARAMETERS</span></span>

### <span data-ttu-id="4bf36-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bf36-112">-DefaultProfile</span></span>
<span data-ttu-id="4bf36-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="4bf36-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4bf36-114">-Force</span><span class="sxs-lookup"><span data-stu-id="4bf36-114">-Force</span></span>
<span data-ttu-id="4bf36-115">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="4bf36-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4bf36-116">-Name</span><span class="sxs-lookup"><span data-stu-id="4bf36-116">-Name</span></span>
<span data-ttu-id="4bf36-117">Nome del piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="4bf36-117">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="4bf36-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bf36-118">-ResourceGroupName</span></span>
<span data-ttu-id="4bf36-119">Nome del gruppo di risorse per il piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="4bf36-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="4bf36-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="4bf36-120">-SkuCapacity</span></span>
<span data-ttu-id="4bf36-121">Capacità dello SKU da usare durante l'aggiornamento del piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="4bf36-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="4bf36-122">-SKUName</span><span class="sxs-lookup"><span data-stu-id="4bf36-122">-SkuName</span></span>
<span data-ttu-id="4bf36-123">Nome dello SKU da usare per l'aggiornamento del piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="4bf36-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="4bf36-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="4bf36-124">-SkuTier</span></span>
<span data-ttu-id="4bf36-125">Livello dello SKU da usare per l'aggiornamento del piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="4bf36-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="4bf36-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="4bf36-126">-Tag</span></span>
<span data-ttu-id="4bf36-127">Tag per la risorsa del piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="4bf36-127">Tags for the commitment plan resource.</span></span>

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

### <span data-ttu-id="4bf36-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4bf36-128">-Confirm</span></span>
<span data-ttu-id="4bf36-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bf36-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bf36-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bf36-130">-WhatIf</span></span>
<span data-ttu-id="4bf36-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4bf36-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4bf36-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4bf36-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bf36-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bf36-133">CommonParameters</span></span>
<span data-ttu-id="4bf36-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bf36-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bf36-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bf36-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bf36-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="4bf36-136">INPUTS</span></span>

### <span data-ttu-id="4bf36-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4bf36-137">None</span></span>

## <span data-ttu-id="4bf36-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4bf36-138">OUTPUTS</span></span>

### <span data-ttu-id="4bf36-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="4bf36-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="4bf36-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="4bf36-140">NOTES</span></span>
<span data-ttu-id="4bf36-141">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, computer, apprendimento automatico, azureml</span><span class="sxs-lookup"><span data-stu-id="4bf36-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="4bf36-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4bf36-142">RELATED LINKS</span></span>
