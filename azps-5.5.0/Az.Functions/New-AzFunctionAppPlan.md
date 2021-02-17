---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 934c8ed95a31f4b953096da40b5ac480020dbc1f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196278"
---
# <span data-ttu-id="468ef-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="468ef-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="468ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="468ef-102">SYNOPSIS</span></span>
<span data-ttu-id="468ef-103">Crea un piano di servizio app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="468ef-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="468ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="468ef-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="468ef-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="468ef-105">DESCRIPTION</span></span>
<span data-ttu-id="468ef-106">Crea un piano di servizio app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="468ef-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="468ef-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="468ef-107">EXAMPLES</span></span>

### <span data-ttu-id="468ef-108">Esempio 1: Creare un piano di app Windows Premium nell'Europa occidentale con capacità a scatto esploso fino a 10 istanze.</span><span class="sxs-lookup"><span data-stu-id="468ef-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="468ef-109">Questo comando crea un piano di app Premium di Windows nell'Europa occidentale con capacità a comparsa fino a 10 istanze.</span><span class="sxs-lookup"><span data-stu-id="468ef-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="468ef-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="468ef-110">PARAMETERS</span></span>

### <span data-ttu-id="468ef-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="468ef-111">-AsJob</span></span>
<span data-ttu-id="468ef-112">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="468ef-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="468ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="468ef-113">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="468ef-114">-Location</span><span class="sxs-lookup"><span data-stu-id="468ef-114">-Location</span></span>
<span data-ttu-id="468ef-115">Posizione del piano di consumo.</span><span class="sxs-lookup"><span data-stu-id="468ef-115">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="468ef-116">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="468ef-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="468ef-117">Il numero massimo di persone per il piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="468ef-117">The maximum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="468ef-118">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="468ef-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="468ef-119">Il numero minimo di persone per il piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="468ef-119">The minimum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="468ef-120">-Name</span><span class="sxs-lookup"><span data-stu-id="468ef-120">-Name</span></span>
<span data-ttu-id="468ef-121">Nome del piano di servizio dell'app.</span><span class="sxs-lookup"><span data-stu-id="468ef-121">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="468ef-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="468ef-122">-NoWait</span></span>
<span data-ttu-id="468ef-123">Eseguire il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="468ef-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="468ef-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="468ef-124">-ResourceGroupName</span></span>
<span data-ttu-id="468ef-125">Nome del gruppo di risorse a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="468ef-125">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="468ef-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="468ef-126">-Sku</span></span>
<span data-ttu-id="468ef-127">SKU del piano.</span><span class="sxs-lookup"><span data-stu-id="468ef-127">The plan sku.</span></span>
<span data-ttu-id="468ef-128">Gli input validi sono: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="468ef-128">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="468ef-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="468ef-129">-SubscriptionId</span></span>
<span data-ttu-id="468ef-130">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="468ef-130">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="468ef-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="468ef-131">-Tag</span></span>
<span data-ttu-id="468ef-132">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="468ef-132">Resource tags.</span></span>

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

### <span data-ttu-id="468ef-133">-WorkerType</span><span class="sxs-lookup"><span data-stu-id="468ef-133">-WorkerType</span></span>
<span data-ttu-id="468ef-134">Tipo di utente per il piano.</span><span class="sxs-lookup"><span data-stu-id="468ef-134">The worker type for the plan.</span></span>
<span data-ttu-id="468ef-135">Gli input validi sono: Windows o Linux.</span><span class="sxs-lookup"><span data-stu-id="468ef-135">Valid inputs are: Windows or Linux.</span></span>

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

### <span data-ttu-id="468ef-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="468ef-136">-Confirm</span></span>
<span data-ttu-id="468ef-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="468ef-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="468ef-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="468ef-138">-WhatIf</span></span>
<span data-ttu-id="468ef-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="468ef-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="468ef-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="468ef-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="468ef-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="468ef-141">CommonParameters</span></span>
<span data-ttu-id="468ef-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="468ef-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="468ef-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="468ef-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="468ef-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="468ef-144">INPUTS</span></span>

## <span data-ttu-id="468ef-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="468ef-145">OUTPUTS</span></span>

### <span data-ttu-id="468ef-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="468ef-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="468ef-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="468ef-147">NOTES</span></span>

<span data-ttu-id="468ef-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="468ef-148">ALIASES</span></span>

## <span data-ttu-id="468ef-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="468ef-149">RELATED LINKS</span></span>

