---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabaseprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
ms.openlocfilehash: b4a670046403aafb4b40740c34f27d7c81bcf8e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476896"
---
# <span data-ttu-id="1900f-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="1900f-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="1900f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1900f-102">SYNOPSIS</span></span>
<span data-ttu-id="1900f-103">Verifica che l'assegnazione dell'entità database sia valida e non sia già in uso.</span><span class="sxs-lookup"><span data-stu-id="1900f-103">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="1900f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1900f-104">SYNTAX</span></span>

### <span data-ttu-id="1900f-105">CheckExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1900f-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1900f-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1900f-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1900f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1900f-107">DESCRIPTION</span></span>
<span data-ttu-id="1900f-108">Verifica che l'assegnazione dell'entità database sia valida e non sia già in uso.</span><span class="sxs-lookup"><span data-stu-id="1900f-108">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="1900f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1900f-109">EXAMPLES</span></span>

### <span data-ttu-id="1900f-110">Esempio 1: verificare la disponibilità di un nome di database principalassignment in uso</span><span class="sxs-lookup"><span data-stu-id="1900f-110">Example 1: Check the availability of a database principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "myprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments" 

Message                                                                                                                                   Name            NameAvailable Reason
-------                                                                                                                                    ----            ------------- ------
Database principal assignment myprincipal already exists in database mykustodatabase. Please select a different principal assignment name. myprincipal   False
```

<span data-ttu-id="1900f-111">Il comando precedente restituisce se un PrincipalAssignment denominato "Principal" esiste o meno nel database "mykustodatabase" dal cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="1900f-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="1900f-112">Esempio 2: verificare la disponibilità di un nome di database principalassignment non in uso</span><span class="sxs-lookup"><span data-stu-id="1900f-112">Example 2: Check the availability of a database principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "newprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="1900f-113">Il comando precedente restituisce se un PrincipalAssignment denominato "Principal" esiste o meno nel database "mykustodatabase" dal cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="1900f-113">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster" .</span></span>

## <span data-ttu-id="1900f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1900f-114">PARAMETERS</span></span>

### <span data-ttu-id="1900f-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="1900f-115">-ClusterName</span></span>
<span data-ttu-id="1900f-116">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="1900f-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="1900f-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1900f-117">-DatabaseName</span></span>
<span data-ttu-id="1900f-118">Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="1900f-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="1900f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1900f-119">-DefaultProfile</span></span>
<span data-ttu-id="1900f-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1900f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1900f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1900f-121">-InputObject</span></span>
<span data-ttu-id="1900f-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1900f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1900f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="1900f-123">-Name</span></span>
<span data-ttu-id="1900f-124">Nome risorsa assegnazione principale.</span><span class="sxs-lookup"><span data-stu-id="1900f-124">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="1900f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1900f-125">-ResourceGroupName</span></span>
<span data-ttu-id="1900f-126">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="1900f-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="1900f-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1900f-127">-SubscriptionId</span></span>
<span data-ttu-id="1900f-128">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1900f-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1900f-129">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="1900f-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1900f-130">-Digitare</span><span class="sxs-lookup"><span data-stu-id="1900f-130">-Type</span></span>
<span data-ttu-id="1900f-131">Il tipo di risorsa, Microsoft. kusto/Clusters/databases/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="1900f-131">The type of resource, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span></span>

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

### <span data-ttu-id="1900f-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1900f-132">-Confirm</span></span>
<span data-ttu-id="1900f-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1900f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1900f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1900f-134">-WhatIf</span></span>
<span data-ttu-id="1900f-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1900f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1900f-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1900f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1900f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1900f-137">CommonParameters</span></span>
<span data-ttu-id="1900f-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1900f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1900f-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1900f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1900f-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1900f-140">INPUTS</span></span>

### <span data-ttu-id="1900f-141">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="1900f-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="1900f-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1900f-142">OUTPUTS</span></span>

### <span data-ttu-id="1900f-143">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200918. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="1900f-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="1900f-144">Note</span><span class="sxs-lookup"><span data-stu-id="1900f-144">NOTES</span></span>

<span data-ttu-id="1900f-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1900f-145">ALIASES</span></span>

<span data-ttu-id="1900f-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1900f-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1900f-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="1900f-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1900f-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1900f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1900f-149">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="1900f-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1900f-150">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="1900f-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="1900f-151">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="1900f-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="1900f-152">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="1900f-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="1900f-153">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="1900f-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="1900f-154">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="1900f-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1900f-155">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1900f-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="1900f-156">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="1900f-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="1900f-157">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="1900f-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="1900f-158">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1900f-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1900f-159">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="1900f-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1900f-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1900f-160">RELATED LINKS</span></span>

