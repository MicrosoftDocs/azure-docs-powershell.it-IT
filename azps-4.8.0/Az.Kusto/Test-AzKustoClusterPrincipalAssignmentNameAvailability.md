---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: cb4f375632626ee3c3428e6a990a228dacecd288
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192452"
---
# <span data-ttu-id="ddae8-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ddae8-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="ddae8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ddae8-102">SYNOPSIS</span></span>
<span data-ttu-id="ddae8-103">Verifica che il nome dell'assegnazione principale sia valido e non sia già in uso.</span><span class="sxs-lookup"><span data-stu-id="ddae8-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="ddae8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ddae8-104">SYNTAX</span></span>

### <span data-ttu-id="ddae8-105">CheckExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ddae8-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ddae8-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ddae8-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ddae8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddae8-107">DESCRIPTION</span></span>
<span data-ttu-id="ddae8-108">Verifica che il nome dell'assegnazione principale sia valido e non sia già in uso.</span><span class="sxs-lookup"><span data-stu-id="ddae8-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="ddae8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ddae8-109">EXAMPLES</span></span>

### <span data-ttu-id="ddae8-110">Esempio 1: verificare la disponibilità di un nome di principalassignment cluster in uso</span><span class="sxs-lookup"><span data-stu-id="ddae8-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="ddae8-111">Il comando precedente restituisce o meno un PrincipalAssignment denominato "Principal" esistente nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="ddae8-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ddae8-112">Esempio 2: verificare la disponibilità di un nome di cluster principalassignment non in uso</span><span class="sxs-lookup"><span data-stu-id="ddae8-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="ddae8-113">Il comando precedente restituisce o meno un PrincipalAssignment denominato "newprincipal" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="ddae8-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="ddae8-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ddae8-114">PARAMETERS</span></span>

### <span data-ttu-id="ddae8-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="ddae8-115">-ClusterName</span></span>
<span data-ttu-id="ddae8-116">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="ddae8-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ddae8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddae8-117">-DefaultProfile</span></span>
<span data-ttu-id="ddae8-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ddae8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddae8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddae8-119">-InputObject</span></span>
<span data-ttu-id="ddae8-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ddae8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ddae8-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ddae8-121">-Name</span></span>
<span data-ttu-id="ddae8-122">Nome risorsa assegnazione principale.</span><span class="sxs-lookup"><span data-stu-id="ddae8-122">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="ddae8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddae8-123">-ResourceGroupName</span></span>
<span data-ttu-id="ddae8-124">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="ddae8-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ddae8-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ddae8-125">-SubscriptionId</span></span>
<span data-ttu-id="ddae8-126">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ddae8-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ddae8-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ddae8-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ddae8-128">-Digitare</span><span class="sxs-lookup"><span data-stu-id="ddae8-128">-Type</span></span>
<span data-ttu-id="ddae8-129">Il tipo di risorsa, Microsoft. kusto/Clusters/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="ddae8-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

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

### <span data-ttu-id="ddae8-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ddae8-130">-Confirm</span></span>
<span data-ttu-id="ddae8-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddae8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddae8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddae8-132">-WhatIf</span></span>
<span data-ttu-id="ddae8-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddae8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddae8-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddae8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddae8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddae8-135">CommonParameters</span></span>
<span data-ttu-id="ddae8-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddae8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddae8-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddae8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddae8-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ddae8-138">INPUTS</span></span>

### <span data-ttu-id="ddae8-139">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="ddae8-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ddae8-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ddae8-140">OUTPUTS</span></span>

### <span data-ttu-id="ddae8-141">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="ddae8-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="ddae8-142">Note</span><span class="sxs-lookup"><span data-stu-id="ddae8-142">NOTES</span></span>

<span data-ttu-id="ddae8-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ddae8-143">ALIASES</span></span>

<span data-ttu-id="ddae8-144">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ddae8-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ddae8-145">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ddae8-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ddae8-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ddae8-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ddae8-147">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="ddae8-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ddae8-148">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="ddae8-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ddae8-149">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="ddae8-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ddae8-150">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="ddae8-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ddae8-151">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="ddae8-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ddae8-152">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="ddae8-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ddae8-153">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ddae8-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ddae8-154">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="ddae8-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ddae8-155">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="ddae8-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ddae8-156">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ddae8-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ddae8-157">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ddae8-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ddae8-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ddae8-158">RELATED LINKS</span></span>

