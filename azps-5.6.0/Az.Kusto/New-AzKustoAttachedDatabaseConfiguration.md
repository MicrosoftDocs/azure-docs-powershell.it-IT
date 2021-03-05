---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 6b540b82ed07e42a6789a2603299508c21c7c3aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983485"
---
# <span data-ttu-id="ba95a-101">New-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba95a-101">New-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="ba95a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba95a-102">SYNOPSIS</span></span>
<span data-ttu-id="ba95a-103">Crea o aggiorna una configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="ba95a-103">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="ba95a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba95a-104">SYNTAX</span></span>

```
New-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterResourceId <String>] [-DatabaseName <String>]
 [-DefaultPrincipalsModificationKind <DefaultPrincipalsModificationKind>] [-Location <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ba95a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ba95a-105">DESCRIPTION</span></span>
<span data-ttu-id="ba95a-106">Crea o aggiorna una configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="ba95a-106">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="ba95a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba95a-107">EXAMPLES</span></span>

### <span data-ttu-id="ba95a-108">Esempio 1: Creare una nuova configurazione AttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba95a-108">Example 1: Create a new AttachedDatabaseConfiguration</span></span>
```powershell
PS C:\> New-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" -Location "East US" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustocluster" -DatabaseName "mykustodatabase" -DefaultPrincipalsModificationKind "Union"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="ba95a-109">Il comando precedente crea un database ReadOnly "mykustodatabase" nel cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="ba95a-109">The above command creates a ReadOnly database "mykustodatabase" in cluster "testnewkustoclusterf".</span></span>
<span data-ttu-id="ba95a-110">Segue il database "mykustodatabase" del cluster "testnewkustocluster"</span><span class="sxs-lookup"><span data-stu-id="ba95a-110">It follows the database "mykustodatabase" from cluster "testnewkustocluster"</span></span>

## <span data-ttu-id="ba95a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba95a-111">PARAMETERS</span></span>

### <span data-ttu-id="ba95a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba95a-112">-AsJob</span></span>
<span data-ttu-id="ba95a-113">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="ba95a-113">Run the command as a job</span></span>

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

### <span data-ttu-id="ba95a-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ba95a-114">-ClusterName</span></span>
<span data-ttu-id="ba95a-115">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ba95a-115">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ba95a-116">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="ba95a-116">-ClusterResourceId</span></span>
<span data-ttu-id="ba95a-117">ID risorsa del cluster in cui risiedono i database da collegare.</span><span class="sxs-lookup"><span data-stu-id="ba95a-117">The resource id of the cluster where the databases you would like to attach reside.</span></span>

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

### <span data-ttu-id="ba95a-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ba95a-118">-DatabaseName</span></span>
<span data-ttu-id="ba95a-119">Il nome del database che si vuole collegare, usare \* se si vogliono seguire tutti i database attuali e futuri.</span><span class="sxs-lookup"><span data-stu-id="ba95a-119">The name of the database which you would like to attach, use \* if you want to follow all current and future databases.</span></span>

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

### <span data-ttu-id="ba95a-120">-DefaultPrincipalsModificationPrincipalsModificationPrincipal</span><span class="sxs-lookup"><span data-stu-id="ba95a-120">-DefaultPrincipalsModificationKind</span></span>
<span data-ttu-id="ba95a-121">Tipo di modifica delle entità predefinite</span><span class="sxs-lookup"><span data-stu-id="ba95a-121">The default principals modification kind</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DefaultPrincipalsModificationKind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba95a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba95a-122">-DefaultProfile</span></span>
<span data-ttu-id="ba95a-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba95a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba95a-124">-Location</span><span class="sxs-lookup"><span data-stu-id="ba95a-124">-Location</span></span>
<span data-ttu-id="ba95a-125">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ba95a-125">Resource location.</span></span>

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

### <span data-ttu-id="ba95a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ba95a-126">-Name</span></span>
<span data-ttu-id="ba95a-127">Nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="ba95a-127">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba95a-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ba95a-128">-NoWait</span></span>
<span data-ttu-id="ba95a-129">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="ba95a-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ba95a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba95a-130">-ResourceGroupName</span></span>
<span data-ttu-id="ba95a-131">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ba95a-131">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ba95a-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba95a-132">-SubscriptionId</span></span>
<span data-ttu-id="ba95a-133">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ba95a-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ba95a-134">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ba95a-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ba95a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba95a-135">-Confirm</span></span>
<span data-ttu-id="ba95a-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba95a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba95a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba95a-137">-WhatIf</span></span>
<span data-ttu-id="ba95a-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba95a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba95a-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba95a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba95a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba95a-140">CommonParameters</span></span>
<span data-ttu-id="ba95a-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba95a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba95a-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ba95a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba95a-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="ba95a-143">INPUTS</span></span>

## <span data-ttu-id="ba95a-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba95a-144">OUTPUTS</span></span>

### <span data-ttu-id="ba95a-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba95a-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="ba95a-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="ba95a-146">NOTES</span></span>

<span data-ttu-id="ba95a-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ba95a-147">ALIASES</span></span>

## <span data-ttu-id="ba95a-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba95a-148">RELATED LINKS</span></span>

