---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabasenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
ms.openlocfilehash: ab15d7a9da10e7e7a024d3af332f449cd011a290
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201184"
---
# <span data-ttu-id="67ab4-101">Test-AzKustoDatabaseNameAvailability</span><span class="sxs-lookup"><span data-stu-id="67ab4-101">Test-AzKustoDatabaseNameAvailability</span></span>

## <span data-ttu-id="67ab4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67ab4-102">SYNOPSIS</span></span>
<span data-ttu-id="67ab4-103">Verifica che il nome del database sia valido e non sia già in uso.</span><span class="sxs-lookup"><span data-stu-id="67ab4-103">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="67ab4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67ab4-104">SYNTAX</span></span>

### <span data-ttu-id="67ab4-105">CheckExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67ab4-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabaseNameAvailability -ClusterName <String> -ResourceGroupName <String> -Name <String>
 -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="67ab4-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="67ab4-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabaseNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="67ab4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67ab4-107">DESCRIPTION</span></span>
<span data-ttu-id="67ab4-108">Verifica che il nome del database sia valido e non sia già in uso.</span><span class="sxs-lookup"><span data-stu-id="67ab4-108">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="67ab4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67ab4-109">EXAMPLES</span></span>

### <span data-ttu-id="67ab4-110">Esempio 1: verificare la disponibilità di un nome di database kusto in uso</span><span class="sxs-lookup"><span data-stu-id="67ab4-110">Example 1: Check the availability of a Kusto database name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Type Microsoft.Kusto/Clusters/Databases

Message                                                                                                          Name            NameAvailable Reason
-------                                                                                                          ----            ------------- ------
Database mykustodatabase already exists in cluster testnewkustocluster. Please select a different database name. mykustodatabase False
```

<span data-ttu-id="67ab4-111">Il comando precedente restituisce o meno un database di Kusto denominato "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="67ab4-111">The above command returns whether or not a Kusto database named "mykustodatabase" exists in the "testnewkustocluster" cluster.</span></span>

### <span data-ttu-id="67ab4-112">Esempio 2: verificare la disponibilità di un nome di database kusto non in uso</span><span class="sxs-lookup"><span data-stu-id="67ab4-112">Example 2: Check the availability of a Kusto database name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase2 -Type Microsoft.Kusto/Clusters/Databases

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mykustodatabase2 True
```

<span data-ttu-id="67ab4-113">Il comando precedente restituisce o meno un database di Kusto denominato "mykustodatabase2" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="67ab4-113">The above command returns whether or not a Kusto database named "mykustodatabase2" exists in the "testnewkustocluster" cluster.</span></span>

## <span data-ttu-id="67ab4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67ab4-114">PARAMETERS</span></span>

### <span data-ttu-id="67ab4-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="67ab4-115">-ClusterName</span></span>
<span data-ttu-id="67ab4-116">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="67ab4-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="67ab4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ab4-117">-DefaultProfile</span></span>
<span data-ttu-id="67ab4-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67ab4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67ab4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67ab4-119">-InputObject</span></span>
<span data-ttu-id="67ab4-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="67ab4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="67ab4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="67ab4-121">-Name</span></span>
<span data-ttu-id="67ab4-122">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="67ab4-122">Resource name.</span></span>

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

### <span data-ttu-id="67ab4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67ab4-123">-ResourceGroupName</span></span>
<span data-ttu-id="67ab4-124">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="67ab4-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="67ab4-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67ab4-125">-SubscriptionId</span></span>
<span data-ttu-id="67ab4-126">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="67ab4-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="67ab4-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="67ab4-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="67ab4-128">-Digitare</span><span class="sxs-lookup"><span data-stu-id="67ab4-128">-Type</span></span>
<span data-ttu-id="67ab4-129">Tipo di risorsa, ad esempio Microsoft. kusto/Clusters/databases.</span><span class="sxs-lookup"><span data-stu-id="67ab4-129">The type of resource, for instance Microsoft.Kusto/Clusters/databases.</span></span>

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

### <span data-ttu-id="67ab4-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="67ab4-130">-Confirm</span></span>
<span data-ttu-id="67ab4-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67ab4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67ab4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67ab4-132">-WhatIf</span></span>
<span data-ttu-id="67ab4-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67ab4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67ab4-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67ab4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67ab4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ab4-135">CommonParameters</span></span>
<span data-ttu-id="67ab4-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67ab4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ab4-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67ab4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ab4-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67ab4-138">INPUTS</span></span>

### <span data-ttu-id="67ab4-139">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="67ab4-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="67ab4-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67ab4-140">OUTPUTS</span></span>

### <span data-ttu-id="67ab4-141">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="67ab4-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="67ab4-142">Note</span><span class="sxs-lookup"><span data-stu-id="67ab4-142">NOTES</span></span>

<span data-ttu-id="67ab4-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="67ab4-143">ALIASES</span></span>

<span data-ttu-id="67ab4-144">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67ab4-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="67ab4-145">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="67ab4-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="67ab4-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="67ab4-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="67ab4-147">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="67ab4-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="67ab4-148">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="67ab4-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="67ab4-149">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="67ab4-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="67ab4-150">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="67ab4-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="67ab4-151">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="67ab4-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="67ab4-152">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="67ab4-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="67ab4-153">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="67ab4-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="67ab4-154">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="67ab4-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="67ab4-155">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="67ab4-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="67ab4-156">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="67ab4-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="67ab4-157">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="67ab4-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="67ab4-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67ab4-158">RELATED LINKS</span></span>

