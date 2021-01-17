---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: fe976ed4e5d34e4b10fb8bba0a5e5397173417b8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474107"
---
# <span data-ttu-id="1a500-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="1a500-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="1a500-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a500-102">SYNOPSIS</span></span>
<span data-ttu-id="1a500-103">Crea o aggiorna un database.</span><span class="sxs-lookup"><span data-stu-id="1a500-103">Creates or updates a database.</span></span>

## <span data-ttu-id="1a500-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a500-104">SYNTAX</span></span>

```
New-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-Location <String>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1a500-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a500-105">DESCRIPTION</span></span>
<span data-ttu-id="1a500-106">Crea o aggiorna un database.</span><span class="sxs-lookup"><span data-stu-id="1a500-106">Creates or updates a database.</span></span>

## <span data-ttu-id="1a500-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a500-107">EXAMPLES</span></span>

### <span data-ttu-id="1a500-108">Esempio 1: creare un nuovo database di Kusto per nome</span><span class="sxs-lookup"><span data-stu-id="1a500-108">Example 1: Create a new Kusto database by name</span></span>
```powershell
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="1a500-109">Il comando precedente crea un nuovo database di Kusto denominato "mykustodatabase" nel cluster esistente "testnewkustocluster" disponibile nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="1a500-109">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="1a500-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a500-110">PARAMETERS</span></span>

### <span data-ttu-id="1a500-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a500-111">-AsJob</span></span>
<span data-ttu-id="1a500-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="1a500-112">Run the command as a job</span></span>

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

### <span data-ttu-id="1a500-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="1a500-113">-ClusterName</span></span>
<span data-ttu-id="1a500-114">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="1a500-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="1a500-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a500-115">-DefaultProfile</span></span>
<span data-ttu-id="1a500-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a500-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a500-117">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="1a500-117">-HotCachePeriod</span></span>
<span data-ttu-id="1a500-118">Data e ora in cui i dati devono essere conservati nella cache per le query veloci in TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="1a500-118">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

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

### <span data-ttu-id="1a500-119">-Tipo</span><span class="sxs-lookup"><span data-stu-id="1a500-119">-Kind</span></span>
<span data-ttu-id="1a500-120">Tipo di database</span><span class="sxs-lookup"><span data-stu-id="1a500-120">Kind of the database</span></span>

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

### <span data-ttu-id="1a500-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1a500-121">-Location</span></span>
<span data-ttu-id="1a500-122">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="1a500-122">Resource location.</span></span>

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

### <span data-ttu-id="1a500-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a500-123">-Name</span></span>
<span data-ttu-id="1a500-124">Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="1a500-124">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="1a500-125">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="1a500-125">-NoWait</span></span>
<span data-ttu-id="1a500-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="1a500-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1a500-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a500-127">-ResourceGroupName</span></span>
<span data-ttu-id="1a500-128">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="1a500-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="1a500-129">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="1a500-129">-SoftDeletePeriod</span></span>
<span data-ttu-id="1a500-130">Il tempo di permanenza dei dati prima che venga impedito l'accessibilità alle query in TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="1a500-130">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

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

### <span data-ttu-id="1a500-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1a500-131">-SubscriptionId</span></span>
<span data-ttu-id="1a500-132">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1a500-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1a500-133">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="1a500-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1a500-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1a500-134">-Confirm</span></span>
<span data-ttu-id="1a500-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a500-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a500-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a500-136">-WhatIf</span></span>
<span data-ttu-id="1a500-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a500-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a500-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a500-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a500-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a500-139">CommonParameters</span></span>
<span data-ttu-id="1a500-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a500-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a500-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a500-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a500-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a500-142">INPUTS</span></span>

## <span data-ttu-id="1a500-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a500-143">OUTPUTS</span></span>

### <span data-ttu-id="1a500-144">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200918. IDatabase</span><span class="sxs-lookup"><span data-stu-id="1a500-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="1a500-145">Note</span><span class="sxs-lookup"><span data-stu-id="1a500-145">NOTES</span></span>

<span data-ttu-id="1a500-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1a500-146">ALIASES</span></span>

## <span data-ttu-id="1a500-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a500-147">RELATED LINKS</span></span>

