---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: 0fbffb0effff782c154e4b6c38d6eb296b89ffb9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180430"
---
# <span data-ttu-id="f66dc-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="f66dc-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="f66dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f66dc-102">SYNOPSIS</span></span>
<span data-ttu-id="f66dc-103">Controlla che il nome dell'assegnazione dell'entità sia valido e che non sia già in uso.</span><span class="sxs-lookup"><span data-stu-id="f66dc-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="f66dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f66dc-104">SYNTAX</span></span>

### <span data-ttu-id="f66dc-105">CheckExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f66dc-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f66dc-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f66dc-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f66dc-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f66dc-107">DESCRIPTION</span></span>
<span data-ttu-id="f66dc-108">Controlla che il nome dell'assegnazione dell'entità sia valido e che non sia già in uso.</span><span class="sxs-lookup"><span data-stu-id="f66dc-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="f66dc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f66dc-109">EXAMPLES</span></span>

### <span data-ttu-id="f66dc-110">Esempio 1: Controllare la disponibilità di un nome di entità principale di un cluster che è in uso</span><span class="sxs-lookup"><span data-stu-id="f66dc-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="f66dc-111">Il comando precedente restituisce se un principalAssignment denominato "myprincipal" esiste nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="f66dc-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="f66dc-112">Esempio 2: Controllare la disponibilità di un nome di entità principale di un cluster che non è in uso</span><span class="sxs-lookup"><span data-stu-id="f66dc-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="f66dc-113">Il comando precedente restituisce se un principalAssignment denominato "newprincipal" esiste nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="f66dc-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="f66dc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f66dc-114">PARAMETERS</span></span>

### <span data-ttu-id="f66dc-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f66dc-115">-ClusterName</span></span>
<span data-ttu-id="f66dc-116">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f66dc-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f66dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f66dc-117">-DefaultProfile</span></span>
<span data-ttu-id="f66dc-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f66dc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f66dc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f66dc-119">-InputObject</span></span>
<span data-ttu-id="f66dc-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f66dc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f66dc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f66dc-121">-Name</span></span>
<span data-ttu-id="f66dc-122">Principal Assignment resource name.</span><span class="sxs-lookup"><span data-stu-id="f66dc-122">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="f66dc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f66dc-123">-ResourceGroupName</span></span>
<span data-ttu-id="f66dc-124">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f66dc-124">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f66dc-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f66dc-125">-SubscriptionId</span></span>
<span data-ttu-id="f66dc-126">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f66dc-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f66dc-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="f66dc-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f66dc-128">-Type</span><span class="sxs-lookup"><span data-stu-id="f66dc-128">-Type</span></span>
<span data-ttu-id="f66dc-129">Tipo di risorsa, Microsoft.Kusto/Clusters/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="f66dc-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f66dc-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f66dc-130">-Confirm</span></span>
<span data-ttu-id="f66dc-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f66dc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f66dc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f66dc-132">-WhatIf</span></span>
<span data-ttu-id="f66dc-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f66dc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f66dc-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f66dc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f66dc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f66dc-135">CommonParameters</span></span>
<span data-ttu-id="f66dc-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f66dc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f66dc-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f66dc-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f66dc-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="f66dc-138">INPUTS</span></span>

### <span data-ttu-id="f66dc-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f66dc-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f66dc-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f66dc-140">OUTPUTS</span></span>

### <span data-ttu-id="f66dc-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="f66dc-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="f66dc-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="f66dc-142">NOTES</span></span>

<span data-ttu-id="f66dc-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f66dc-143">ALIASES</span></span>

<span data-ttu-id="f66dc-144">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="f66dc-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f66dc-145">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="f66dc-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f66dc-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f66dc-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f66dc-147">INPUTOBJECT <IKustoIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="f66dc-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f66dc-148">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="f66dc-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f66dc-149">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f66dc-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f66dc-150">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="f66dc-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f66dc-151">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f66dc-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f66dc-152">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="f66dc-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f66dc-153">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f66dc-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f66dc-154">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f66dc-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f66dc-155">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f66dc-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f66dc-156">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f66dc-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f66dc-157">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="f66dc-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f66dc-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f66dc-158">RELATED LINKS</span></span>

