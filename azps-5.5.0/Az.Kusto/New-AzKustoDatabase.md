---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: fe976ed4e5d34e4b10fb8bba0a5e5397173417b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203779"
---
# <span data-ttu-id="b36a4-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="b36a4-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="b36a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b36a4-102">SYNOPSIS</span></span>
<span data-ttu-id="b36a4-103">Crea o aggiorna un database.</span><span class="sxs-lookup"><span data-stu-id="b36a4-103">Creates or updates a database.</span></span>

## <span data-ttu-id="b36a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b36a4-104">SYNTAX</span></span>

```
New-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-Location <String>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b36a4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b36a4-105">DESCRIPTION</span></span>
<span data-ttu-id="b36a4-106">Crea o aggiorna un database.</span><span class="sxs-lookup"><span data-stu-id="b36a4-106">Creates or updates a database.</span></span>

## <span data-ttu-id="b36a4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b36a4-107">EXAMPLES</span></span>

### <span data-ttu-id="b36a4-108">Esempio 1: Creare un nuovo database Kusto in base al nome</span><span class="sxs-lookup"><span data-stu-id="b36a4-108">Example 1: Create a new Kusto database by name</span></span>
```powershell
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="b36a4-109">Il comando precedente crea un nuovo database Kusto denominato "mykustodatabase" nel cluster esistente "testnewkustocluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="b36a4-109">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="b36a4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b36a4-110">PARAMETERS</span></span>

### <span data-ttu-id="b36a4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b36a4-111">-AsJob</span></span>
<span data-ttu-id="b36a4-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="b36a4-112">Run the command as a job</span></span>

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

### <span data-ttu-id="b36a4-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b36a4-113">-ClusterName</span></span>
<span data-ttu-id="b36a4-114">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="b36a4-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="b36a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b36a4-115">-DefaultProfile</span></span>
<span data-ttu-id="b36a4-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b36a4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b36a4-117">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="b36a4-117">-HotCachePeriod</span></span>
<span data-ttu-id="b36a4-118">Ora in cui i dati devono essere mantenuti nella cache per le query veloci in TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="b36a4-118">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

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

### <span data-ttu-id="b36a4-119">-Kind</span><span class="sxs-lookup"><span data-stu-id="b36a4-119">-Kind</span></span>
<span data-ttu-id="b36a4-120">Tipo di database</span><span class="sxs-lookup"><span data-stu-id="b36a4-120">Kind of the database</span></span>

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

### <span data-ttu-id="b36a4-121">-Location</span><span class="sxs-lookup"><span data-stu-id="b36a4-121">-Location</span></span>
<span data-ttu-id="b36a4-122">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b36a4-122">Resource location.</span></span>

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

### <span data-ttu-id="b36a4-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b36a4-123">-Name</span></span>
<span data-ttu-id="b36a4-124">Nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="b36a4-124">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="b36a4-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b36a4-125">-NoWait</span></span>
<span data-ttu-id="b36a4-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="b36a4-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b36a4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b36a4-127">-ResourceGroupName</span></span>
<span data-ttu-id="b36a4-128">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="b36a4-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="b36a4-129">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="b36a4-129">-SoftDeletePeriod</span></span>
<span data-ttu-id="b36a4-130">Il tempo che i dati devono mantenere prima di non essere più accessibili alle query nell'intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="b36a4-130">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

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

### <span data-ttu-id="b36a4-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b36a4-131">-SubscriptionId</span></span>
<span data-ttu-id="b36a4-132">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b36a4-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b36a4-133">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b36a4-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b36a4-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b36a4-134">-Confirm</span></span>
<span data-ttu-id="b36a4-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b36a4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b36a4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b36a4-136">-WhatIf</span></span>
<span data-ttu-id="b36a4-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b36a4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b36a4-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b36a4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b36a4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b36a4-139">CommonParameters</span></span>
<span data-ttu-id="b36a4-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b36a4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b36a4-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b36a4-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b36a4-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="b36a4-142">INPUTS</span></span>

## <span data-ttu-id="b36a4-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b36a4-143">OUTPUTS</span></span>

### <span data-ttu-id="b36a4-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="b36a4-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="b36a4-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="b36a4-145">NOTES</span></span>

<span data-ttu-id="b36a4-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b36a4-146">ALIASES</span></span>

## <span data-ttu-id="b36a4-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b36a4-147">RELATED LINKS</span></span>

