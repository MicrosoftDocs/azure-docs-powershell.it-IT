---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 934c8ed95a31f4b953096da40b5ac480020dbc1f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190183"
---
# <span data-ttu-id="19266-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="19266-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="19266-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19266-102">SYNOPSIS</span></span>
<span data-ttu-id="19266-103">Crea un piano di servizio App funzione.</span><span class="sxs-lookup"><span data-stu-id="19266-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="19266-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19266-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="19266-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19266-105">DESCRIPTION</span></span>
<span data-ttu-id="19266-106">Crea un piano di servizio App funzione.</span><span class="sxs-lookup"><span data-stu-id="19266-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="19266-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19266-107">EXAMPLES</span></span>

### <span data-ttu-id="19266-108">Esempio 1: creare un piano di app Windows Premium in Europa occidentale con una capacità di uscita fino a 10 istanze.</span><span class="sxs-lookup"><span data-stu-id="19266-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="19266-109">Questo comando crea un piano per l'app Windows Premium in Europa occidentale con una capacità massima di 10 istanze.</span><span class="sxs-lookup"><span data-stu-id="19266-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="19266-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19266-110">PARAMETERS</span></span>

### <span data-ttu-id="19266-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19266-111">-AsJob</span></span>
<span data-ttu-id="19266-112">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="19266-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="19266-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19266-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="19266-114">-Posizione</span><span class="sxs-lookup"><span data-stu-id="19266-114">-Location</span></span>
<span data-ttu-id="19266-115">Posizione per il piano di consumo.</span><span class="sxs-lookup"><span data-stu-id="19266-115">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="19266-116">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="19266-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="19266-117">Numero massimo di dipendenti per il piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="19266-117">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="19266-118">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="19266-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="19266-119">Il numero minimo di lavoratori per il piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="19266-119">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="19266-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="19266-120">-Name</span></span>
<span data-ttu-id="19266-121">Nome del piano del servizio app.</span><span class="sxs-lookup"><span data-stu-id="19266-121">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="19266-122">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="19266-122">-NoWait</span></span>
<span data-ttu-id="19266-123">Esegui il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="19266-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="19266-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19266-124">-ResourceGroupName</span></span>
<span data-ttu-id="19266-125">Nome del gruppo di risorse a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="19266-125">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="19266-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="19266-126">-Sku</span></span>
<span data-ttu-id="19266-127">SKU piano.</span><span class="sxs-lookup"><span data-stu-id="19266-127">The plan sku.</span></span>
<span data-ttu-id="19266-128">Gli input validi sono: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="19266-128">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="19266-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19266-129">-SubscriptionId</span></span>
<span data-ttu-id="19266-130">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="19266-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="19266-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="19266-131">-Tag</span></span>
<span data-ttu-id="19266-132">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="19266-132">Resource tags.</span></span>

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

### <span data-ttu-id="19266-133">-WorkerType</span><span class="sxs-lookup"><span data-stu-id="19266-133">-WorkerType</span></span>
<span data-ttu-id="19266-134">Tipo di lavoro per il piano.</span><span class="sxs-lookup"><span data-stu-id="19266-134">The worker type for the plan.</span></span>
<span data-ttu-id="19266-135">Gli input validi sono: Windows o Linux.</span><span class="sxs-lookup"><span data-stu-id="19266-135">Valid inputs are: Windows or Linux.</span></span>

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

### <span data-ttu-id="19266-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="19266-136">-Confirm</span></span>
<span data-ttu-id="19266-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19266-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19266-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19266-138">-WhatIf</span></span>
<span data-ttu-id="19266-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19266-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19266-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19266-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19266-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19266-141">CommonParameters</span></span>
<span data-ttu-id="19266-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19266-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19266-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19266-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19266-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19266-144">INPUTS</span></span>

## <span data-ttu-id="19266-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19266-145">OUTPUTS</span></span>

### <span data-ttu-id="19266-146">Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="19266-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="19266-147">Note</span><span class="sxs-lookup"><span data-stu-id="19266-147">NOTES</span></span>

<span data-ttu-id="19266-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="19266-148">ALIASES</span></span>

## <span data-ttu-id="19266-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19266-149">RELATED LINKS</span></span>
