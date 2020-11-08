---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 26da7e8b0bf3ca24edd9f4abd52f0c27aabf49e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191508"
---
# <span data-ttu-id="3edde-101">New-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="3edde-101">New-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="3edde-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3edde-102">SYNOPSIS</span></span>
<span data-ttu-id="3edde-103">Crea o aggiorna una configurazione di database allegato.</span><span class="sxs-lookup"><span data-stu-id="3edde-103">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="3edde-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3edde-104">SYNTAX</span></span>

```
New-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterResourceId <String>] [-DatabaseName <String>]
 [-DefaultPrincipalsModificationKind <DefaultPrincipalsModificationKind>] [-Location <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3edde-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3edde-105">DESCRIPTION</span></span>
<span data-ttu-id="3edde-106">Crea o aggiorna una configurazione di database allegato.</span><span class="sxs-lookup"><span data-stu-id="3edde-106">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="3edde-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3edde-107">EXAMPLES</span></span>

### <span data-ttu-id="3edde-108">Esempio 1: creare un nuovo AttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="3edde-108">Example 1: Create a new AttachedDatabaseConfiguration</span></span>
```powershell
PS C:\> New-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" -Location "East US" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustocluster" -DatabaseName "mykustodatabase" -DefaultPrincipalsModificationKind "Union"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="3edde-109">Il comando precedente crea un database ReadOnly "mykustodatabase" nel cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="3edde-109">The above command creates a ReadOnly database "mykustodatabase" in cluster "testnewkustoclusterf".</span></span>
<span data-ttu-id="3edde-110">Segue il database "mykustodatabase" dal cluster "testnewkustocluster"</span><span class="sxs-lookup"><span data-stu-id="3edde-110">It follows the database "mykustodatabase" from cluster "testnewkustocluster"</span></span>

## <span data-ttu-id="3edde-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3edde-111">PARAMETERS</span></span>

### <span data-ttu-id="3edde-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3edde-112">-AsJob</span></span>
<span data-ttu-id="3edde-113">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="3edde-113">Run the command as a job</span></span>

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

### <span data-ttu-id="3edde-114">-Clustername</span><span class="sxs-lookup"><span data-stu-id="3edde-114">-ClusterName</span></span>
<span data-ttu-id="3edde-115">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="3edde-115">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="3edde-116">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="3edde-116">-ClusterResourceId</span></span>
<span data-ttu-id="3edde-117">ID risorsa del cluster in cui risiedono i database da allegare.</span><span class="sxs-lookup"><span data-stu-id="3edde-117">The resource id of the cluster where the databases you would like to attach reside.</span></span>

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

### <span data-ttu-id="3edde-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3edde-118">-DatabaseName</span></span>
<span data-ttu-id="3edde-119">Nome del database che si desidera allegare, usare \* se si vogliono seguire tutti i database correnti e futuri.</span><span class="sxs-lookup"><span data-stu-id="3edde-119">The name of the database which you would like to attach, use \* if you want to follow all current and future databases.</span></span>

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

### <span data-ttu-id="3edde-120">-DefaultPrincipalsModificationKind</span><span class="sxs-lookup"><span data-stu-id="3edde-120">-DefaultPrincipalsModificationKind</span></span>
<span data-ttu-id="3edde-121">Tipo di modifica delle entità predefinite</span><span class="sxs-lookup"><span data-stu-id="3edde-121">The default principals modification kind</span></span>

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

### <span data-ttu-id="3edde-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3edde-122">-DefaultProfile</span></span>
<span data-ttu-id="3edde-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3edde-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3edde-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3edde-124">-Location</span></span>
<span data-ttu-id="3edde-125">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="3edde-125">Resource location.</span></span>

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

### <span data-ttu-id="3edde-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="3edde-126">-Name</span></span>
<span data-ttu-id="3edde-127">Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="3edde-127">The name of the attached database configuration.</span></span>

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

### <span data-ttu-id="3edde-128">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="3edde-128">-NoWait</span></span>
<span data-ttu-id="3edde-129">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="3edde-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3edde-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3edde-130">-ResourceGroupName</span></span>
<span data-ttu-id="3edde-131">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="3edde-131">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="3edde-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3edde-132">-SubscriptionId</span></span>
<span data-ttu-id="3edde-133">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3edde-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3edde-134">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="3edde-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3edde-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3edde-135">-Confirm</span></span>
<span data-ttu-id="3edde-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3edde-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3edde-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3edde-137">-WhatIf</span></span>
<span data-ttu-id="3edde-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3edde-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3edde-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3edde-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3edde-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3edde-140">CommonParameters</span></span>
<span data-ttu-id="3edde-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3edde-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3edde-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3edde-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3edde-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3edde-143">INPUTS</span></span>

## <span data-ttu-id="3edde-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3edde-144">OUTPUTS</span></span>

### <span data-ttu-id="3edde-145">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="3edde-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="3edde-146">Note</span><span class="sxs-lookup"><span data-stu-id="3edde-146">NOTES</span></span>

<span data-ttu-id="3edde-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3edde-147">ALIASES</span></span>

## <span data-ttu-id="3edde-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3edde-148">RELATED LINKS</span></span>

