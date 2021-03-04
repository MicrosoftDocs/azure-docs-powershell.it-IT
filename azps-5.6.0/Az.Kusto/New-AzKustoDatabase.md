---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: b3e6319de721d63071c730bb43e1ef7db5a46e25
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956126"
---
# <span data-ttu-id="35dc3-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="35dc3-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="35dc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35dc3-102">SYNOPSIS</span></span>
<span data-ttu-id="35dc3-103">Crea o aggiorna un database.</span><span class="sxs-lookup"><span data-stu-id="35dc3-103">Creates or updates a database.</span></span>

## <span data-ttu-id="35dc3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35dc3-104">SYNTAX</span></span>

```
New-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-Location <String>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35dc3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="35dc3-105">DESCRIPTION</span></span>
<span data-ttu-id="35dc3-106">Crea o aggiorna un database.</span><span class="sxs-lookup"><span data-stu-id="35dc3-106">Creates or updates a database.</span></span>

## <span data-ttu-id="35dc3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35dc3-107">EXAMPLES</span></span>

### <span data-ttu-id="35dc3-108">Esempio 1: Creare un nuovo database Kusto in base al nome</span><span class="sxs-lookup"><span data-stu-id="35dc3-108">Example 1: Create a new Kusto database by name</span></span>
```powershell
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="35dc3-109">Il comando precedente crea un nuovo database Kusto denominato "mykustodatabase" nel cluster esistente "testnewkustocluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="35dc3-109">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="35dc3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35dc3-110">PARAMETERS</span></span>

### <span data-ttu-id="35dc3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35dc3-111">-AsJob</span></span>
<span data-ttu-id="35dc3-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="35dc3-112">Run the command as a job</span></span>

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

### <span data-ttu-id="35dc3-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="35dc3-113">-ClusterName</span></span>
<span data-ttu-id="35dc3-114">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="35dc3-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="35dc3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35dc3-115">-DefaultProfile</span></span>
<span data-ttu-id="35dc3-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35dc3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35dc3-117">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="35dc3-117">-HotCachePeriod</span></span>
<span data-ttu-id="35dc3-118">Il tempo che i dati devono mantenere nella cache per le query veloci in TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="35dc3-118">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35dc3-119">-Kind</span><span class="sxs-lookup"><span data-stu-id="35dc3-119">-Kind</span></span>
<span data-ttu-id="35dc3-120">Tipo di database</span><span class="sxs-lookup"><span data-stu-id="35dc3-120">Kind of the database</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35dc3-121">-Location</span><span class="sxs-lookup"><span data-stu-id="35dc3-121">-Location</span></span>
<span data-ttu-id="35dc3-122">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="35dc3-122">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35dc3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="35dc3-123">-Name</span></span>
<span data-ttu-id="35dc3-124">Nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="35dc3-124">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35dc3-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="35dc3-125">-NoWait</span></span>
<span data-ttu-id="35dc3-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="35dc3-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="35dc3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35dc3-127">-ResourceGroupName</span></span>
<span data-ttu-id="35dc3-128">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="35dc3-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="35dc3-129">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="35dc3-129">-SoftDeletePeriod</span></span>
<span data-ttu-id="35dc3-130">Il tempo che i dati devono mantenere prima di non essere più accessibili alle query nell'intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="35dc3-130">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35dc3-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35dc3-131">-SubscriptionId</span></span>
<span data-ttu-id="35dc3-132">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="35dc3-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="35dc3-133">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="35dc3-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="35dc3-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35dc3-134">-Confirm</span></span>
<span data-ttu-id="35dc3-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35dc3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35dc3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35dc3-136">-WhatIf</span></span>
<span data-ttu-id="35dc3-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35dc3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35dc3-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35dc3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35dc3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35dc3-139">CommonParameters</span></span>
<span data-ttu-id="35dc3-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35dc3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35dc3-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="35dc3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35dc3-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="35dc3-142">INPUTS</span></span>

## <span data-ttu-id="35dc3-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35dc3-143">OUTPUTS</span></span>

### <span data-ttu-id="35dc3-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="35dc3-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="35dc3-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="35dc3-145">NOTES</span></span>

<span data-ttu-id="35dc3-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="35dc3-146">ALIASES</span></span>

## <span data-ttu-id="35dc3-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35dc3-147">RELATED LINKS</span></span>

