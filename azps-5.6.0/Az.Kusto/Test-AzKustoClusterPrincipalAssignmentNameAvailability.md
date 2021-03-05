---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: f1c96909421dcc21d2b1f318a923ef7f9b804bf8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015133"
---
# <span data-ttu-id="9c8eb-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="9c8eb-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="9c8eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c8eb-102">SYNOPSIS</span></span>
<span data-ttu-id="9c8eb-103">Verifica che il nome dell'assegnazione dell'entità sia valido e che non sia già in uso.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="9c8eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c8eb-104">SYNTAX</span></span>

### <span data-ttu-id="9c8eb-105">CheckExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9c8eb-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9c8eb-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9c8eb-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9c8eb-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9c8eb-107">DESCRIPTION</span></span>
<span data-ttu-id="9c8eb-108">Verifica che il nome dell'assegnazione dell'entità sia valido e che non sia già in uso.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="9c8eb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c8eb-109">EXAMPLES</span></span>

### <span data-ttu-id="9c8eb-110">Esempio 1: Controllare la disponibilità di un nome di entità principale di un cluster che è in uso</span><span class="sxs-lookup"><span data-stu-id="9c8eb-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="9c8eb-111">Il comando precedente restituisce se un principalAssignment denominato "myprincipal" esiste nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="9c8eb-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="9c8eb-112">Esempio 2: Controllare la disponibilità di un nome di entità principale di un cluster che non è in uso</span><span class="sxs-lookup"><span data-stu-id="9c8eb-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="9c8eb-113">Il comando precedente restituisce se un principalAssignment denominato "newprincipal" esiste nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="9c8eb-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="9c8eb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c8eb-114">PARAMETERS</span></span>

### <span data-ttu-id="9c8eb-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9c8eb-115">-ClusterName</span></span>
<span data-ttu-id="9c8eb-116">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="9c8eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c8eb-117">-DefaultProfile</span></span>
<span data-ttu-id="9c8eb-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c8eb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c8eb-119">-InputObject</span></span>
<span data-ttu-id="9c8eb-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9c8eb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9c8eb-121">-Name</span></span>
<span data-ttu-id="9c8eb-122">Principal Assignment resource name.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-122">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="9c8eb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c8eb-123">-ResourceGroupName</span></span>
<span data-ttu-id="9c8eb-124">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="9c8eb-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c8eb-125">-SubscriptionId</span></span>
<span data-ttu-id="9c8eb-126">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9c8eb-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9c8eb-128">-Type</span><span class="sxs-lookup"><span data-stu-id="9c8eb-128">-Type</span></span>
<span data-ttu-id="9c8eb-129">Tipo di risorsa, Microsoft.Kusto/Clusters/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

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

### <span data-ttu-id="9c8eb-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c8eb-130">-Confirm</span></span>
<span data-ttu-id="9c8eb-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c8eb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c8eb-132">-WhatIf</span></span>
<span data-ttu-id="9c8eb-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c8eb-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c8eb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c8eb-135">CommonParameters</span></span>
<span data-ttu-id="9c8eb-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c8eb-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c8eb-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="9c8eb-138">INPUTS</span></span>

### <span data-ttu-id="9c8eb-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="9c8eb-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="9c8eb-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c8eb-140">OUTPUTS</span></span>

### <span data-ttu-id="9c8eb-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="9c8eb-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="9c8eb-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="9c8eb-142">NOTES</span></span>

<span data-ttu-id="9c8eb-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9c8eb-143">ALIASES</span></span>

<span data-ttu-id="9c8eb-144">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="9c8eb-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9c8eb-145">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9c8eb-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9c8eb-147">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="9c8eb-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9c8eb-148">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="9c8eb-149">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="9c8eb-150">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="9c8eb-151">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="9c8eb-152">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="9c8eb-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9c8eb-153">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="9c8eb-154">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="9c8eb-155">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="9c8eb-156">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9c8eb-157">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="9c8eb-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9c8eb-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c8eb-158">RELATED LINKS</span></span>

