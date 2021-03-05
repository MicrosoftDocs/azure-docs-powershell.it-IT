---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/test-azkustodatabaseprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
ms.openlocfilehash: 6a151119552ab4b0e42d247641248dd110af4994
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972814"
---
# <span data-ttu-id="1c0a9-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="1c0a9-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="1c0a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c0a9-102">SYNOPSIS</span></span>
<span data-ttu-id="1c0a9-103">Verifica che l'assegnazione dell'entità database sia valida e che non sia già in uso.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-103">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="1c0a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c0a9-104">SYNTAX</span></span>

### <span data-ttu-id="1c0a9-105">CheckExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1c0a9-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1c0a9-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1c0a9-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1c0a9-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1c0a9-107">DESCRIPTION</span></span>
<span data-ttu-id="1c0a9-108">Verifica che l'assegnazione dell'entità database sia valida e che non sia già in uso.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-108">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="1c0a9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c0a9-109">EXAMPLES</span></span>

### <span data-ttu-id="1c0a9-110">Esempio 1: Verificare la disponibilità di un nome di entità principale di database in uso</span><span class="sxs-lookup"><span data-stu-id="1c0a9-110">Example 1: Check the availability of a database principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "myprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments" 

Message                                                                                                                                   Name            NameAvailable Reason
-------                                                                                                                                    ----            ------------- ------
Database principal assignment myprincipal already exists in database mykustodatabase. Please select a different principal assignment name. myprincipal   False
```

<span data-ttu-id="1c0a9-111">Il comando precedente restituisce se un principalAssignment denominato "myprincipal" esiste nel database "mykustodatabase" del cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="1c0a9-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="1c0a9-112">Esempio 2: Verificare la disponibilità di un nome di entità principale di database che non è in uso</span><span class="sxs-lookup"><span data-stu-id="1c0a9-112">Example 2: Check the availability of a database principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "newprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="1c0a9-113">Il comando precedente restituisce se un principalAssignment denominato "myprincipal" esiste nel database "mykustodatabase" del cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="1c0a9-113">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster" .</span></span>

## <span data-ttu-id="1c0a9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c0a9-114">PARAMETERS</span></span>

### <span data-ttu-id="1c0a9-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1c0a9-115">-ClusterName</span></span>
<span data-ttu-id="1c0a9-116">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="1c0a9-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1c0a9-117">-DatabaseName</span></span>
<span data-ttu-id="1c0a9-118">Nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="1c0a9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c0a9-119">-DefaultProfile</span></span>
<span data-ttu-id="1c0a9-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c0a9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c0a9-121">-InputObject</span></span>
<span data-ttu-id="1c0a9-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1c0a9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1c0a9-123">-Name</span></span>
<span data-ttu-id="1c0a9-124">Principal Assignment resource name.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-124">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="1c0a9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c0a9-125">-ResourceGroupName</span></span>
<span data-ttu-id="1c0a9-126">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="1c0a9-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1c0a9-127">-SubscriptionId</span></span>
<span data-ttu-id="1c0a9-128">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1c0a9-129">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1c0a9-130">-Type</span><span class="sxs-lookup"><span data-stu-id="1c0a9-130">-Type</span></span>
<span data-ttu-id="1c0a9-131">Tipo di risorsa, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-131">The type of resource, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span></span>

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

### <span data-ttu-id="1c0a9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c0a9-132">-Confirm</span></span>
<span data-ttu-id="1c0a9-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c0a9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c0a9-134">-WhatIf</span></span>
<span data-ttu-id="1c0a9-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c0a9-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c0a9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c0a9-137">CommonParameters</span></span>
<span data-ttu-id="1c0a9-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c0a9-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c0a9-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="1c0a9-140">INPUTS</span></span>

### <span data-ttu-id="1c0a9-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="1c0a9-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="1c0a9-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c0a9-142">OUTPUTS</span></span>

### <span data-ttu-id="1c0a9-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="1c0a9-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="1c0a9-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="1c0a9-144">NOTES</span></span>

<span data-ttu-id="1c0a9-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1c0a9-145">ALIASES</span></span>

<span data-ttu-id="1c0a9-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="1c0a9-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1c0a9-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1c0a9-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1c0a9-149">INPUTOBJECT <IKustoIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="1c0a9-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1c0a9-150">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="1c0a9-151">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="1c0a9-152">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="1c0a9-153">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="1c0a9-154">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="1c0a9-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1c0a9-155">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="1c0a9-156">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="1c0a9-157">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="1c0a9-158">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1c0a9-159">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="1c0a9-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1c0a9-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c0a9-160">RELATED LINKS</span></span>

