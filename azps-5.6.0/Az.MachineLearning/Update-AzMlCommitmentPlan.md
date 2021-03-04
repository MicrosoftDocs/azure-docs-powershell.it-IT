---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/update-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
ms.openlocfilehash: 6bd60ced20e9c5b8ce9c3be01d419af55281aca9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956125"
---
# <span data-ttu-id="dd787-101">Update-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="dd787-101">Update-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="dd787-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd787-102">SYNOPSIS</span></span>
<span data-ttu-id="dd787-103">Aggiorna le proprietà di una risorsa del piano di impegno esistente.</span><span class="sxs-lookup"><span data-stu-id="dd787-103">Updates properties of an existing commitment plan resource.</span></span>

## <span data-ttu-id="dd787-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd787-104">SYNTAX</span></span>

```
Update-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd787-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dd787-105">DESCRIPTION</span></span>
<span data-ttu-id="dd787-106">Aggiorna una risorsa del piano di impegno esistente.</span><span class="sxs-lookup"><span data-stu-id="dd787-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="dd787-107">Si noti che la maggior parte delle proprietà del piano di impegno non è modificabile e non può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="dd787-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="dd787-108">Le proprietà che possono essere modificate includono SKU (che consente di eseguire la migrazione del piano di impegno da uno SKU a un altro) e Tag.</span><span class="sxs-lookup"><span data-stu-id="dd787-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="dd787-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd787-109">EXAMPLES</span></span>

### <span data-ttu-id="dd787-110">Esempio 1: Aggiornare un piano di impegno</span><span class="sxs-lookup"><span data-stu-id="dd787-110">Example 1: Update a commitment plan</span></span>
```
Update-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="dd787-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd787-111">PARAMETERS</span></span>

### <span data-ttu-id="dd787-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd787-112">-DefaultProfile</span></span>
<span data-ttu-id="dd787-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="dd787-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd787-114">-Force</span><span class="sxs-lookup"><span data-stu-id="dd787-114">-Force</span></span>
<span data-ttu-id="dd787-115">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="dd787-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="dd787-116">-Name</span><span class="sxs-lookup"><span data-stu-id="dd787-116">-Name</span></span>
<span data-ttu-id="dd787-117">Nome del piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="dd787-117">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dd787-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd787-118">-ResourceGroupName</span></span>
<span data-ttu-id="dd787-119">Nome del gruppo di risorse per il piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="dd787-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dd787-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="dd787-120">-SkuCapacity</span></span>
<span data-ttu-id="dd787-121">Capacità dello SKU da usare durante l'aggiornamento del piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="dd787-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dd787-122">-SKUName</span><span class="sxs-lookup"><span data-stu-id="dd787-122">-SkuName</span></span>
<span data-ttu-id="dd787-123">Nome dello SKU da usare per l'aggiornamento del piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="dd787-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dd787-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="dd787-124">-SkuTier</span></span>
<span data-ttu-id="dd787-125">Livello dello SKU da usare per l'aggiornamento del piano di impegno di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="dd787-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dd787-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="dd787-126">-Tag</span></span>
<span data-ttu-id="dd787-127">Tag per la risorsa del piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="dd787-127">Tags for the commitment plan resource.</span></span>

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

### <span data-ttu-id="dd787-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd787-128">-Confirm</span></span>
<span data-ttu-id="dd787-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd787-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd787-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd787-130">-WhatIf</span></span>
<span data-ttu-id="dd787-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd787-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd787-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd787-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd787-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd787-133">CommonParameters</span></span>
<span data-ttu-id="dd787-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd787-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd787-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd787-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd787-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="dd787-136">INPUTS</span></span>

### <span data-ttu-id="dd787-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="dd787-137">None</span></span>

## <span data-ttu-id="dd787-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd787-138">OUTPUTS</span></span>

### <span data-ttu-id="dd787-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="dd787-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="dd787-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="dd787-140">NOTES</span></span>
<span data-ttu-id="dd787-141">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, computer, apprendimento automatico, azureml</span><span class="sxs-lookup"><span data-stu-id="dd787-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="dd787-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd787-142">RELATED LINKS</span></span>
