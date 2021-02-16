---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodataconnectionnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
ms.openlocfilehash: 14eee624f4de3129ddeefee05d402abb0cb686db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180423"
---
# <span data-ttu-id="ae1b2-101">Test-AzKustoDataConnectionNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ae1b2-101">Test-AzKustoDataConnectionNameAvailability</span></span>

## <span data-ttu-id="ae1b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae1b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ae1b2-103">Verifica che il nome della connessione dati sia valido e che non sia già in uso.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-103">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="ae1b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae1b2-104">SYNTAX</span></span>

### <span data-ttu-id="ae1b2-105">CheckExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ae1b2-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDataConnectionNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ae1b2-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ae1b2-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDataConnectionNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ae1b2-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ae1b2-107">DESCRIPTION</span></span>
<span data-ttu-id="ae1b2-108">Verifica che il nome della connessione dati sia valido e che non sia già in uso.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-108">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="ae1b2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae1b2-109">EXAMPLES</span></span>

### <span data-ttu-id="ae1b2-110">Esempio 1: Verificare la disponibilità di un nome di connessione dati in uso</span><span class="sxs-lookup"><span data-stu-id="ae1b2-110">Example 1: Check the availability of a Data Connection name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mykustodataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message                                                                                                                                                          Name                  NameAvailable Reason
-------                                                                                                                                                          ----                  ------------- ------
Data Connection mykustodataconnection already exists in database mykustodatabase in cluster testnewkustocluster. Please select a different data connection name. mykustodataconnection False         AlreadyExists
```

<span data-ttu-id="ae1b2-111">Il comando precedente restituisce se una connessione dati denominata "mykustodataconnection" è presente nel database "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="ae1b2-111">The above command returns whether or not a Data Connection named "mykustodataconnection" exists in the "mykustodatabase" database.</span></span>

### <span data-ttu-id="ae1b2-112">Esempio 2: Verificare la disponibilità di un nome di connessione dati non in uso</span><span class="sxs-lookup"><span data-stu-id="ae1b2-112">Example 2: Check the availability of a Data Connection name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mydataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mydataconnection True
```

<span data-ttu-id="ae1b2-113">Il comando precedente restituisce se una connessione dati denominata "connessionedati" è presente o meno nel database "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="ae1b2-113">The above command returns whether or not a Data Connection named "mydataconnection" exists in the "mykustodatabase" database.</span></span>

## <span data-ttu-id="ae1b2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae1b2-114">PARAMETERS</span></span>

### <span data-ttu-id="ae1b2-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ae1b2-115">-ClusterName</span></span>
<span data-ttu-id="ae1b2-116">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ae1b2-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ae1b2-117">-DatabaseName</span></span>
<span data-ttu-id="ae1b2-118">Nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="ae1b2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae1b2-119">-DefaultProfile</span></span>
<span data-ttu-id="ae1b2-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae1b2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae1b2-121">-InputObject</span></span>
<span data-ttu-id="ae1b2-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ae1b2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ae1b2-123">-Name</span></span>
<span data-ttu-id="ae1b2-124">Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-124">Data Connection name.</span></span>

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

### <span data-ttu-id="ae1b2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae1b2-125">-ResourceGroupName</span></span>
<span data-ttu-id="ae1b2-126">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ae1b2-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae1b2-127">-SubscriptionId</span></span>
<span data-ttu-id="ae1b2-128">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ae1b2-129">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ae1b2-130">-Type</span><span class="sxs-lookup"><span data-stu-id="ae1b2-130">-Type</span></span>
<span data-ttu-id="ae1b2-131">Tipo di risorsa, Microsoft.Kusto/Clusters/Databases/dataConnections.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-131">The type of resource, Microsoft.Kusto/Clusters/Databases/dataConnections.</span></span>

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

### <span data-ttu-id="ae1b2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae1b2-132">-Confirm</span></span>
<span data-ttu-id="ae1b2-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae1b2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae1b2-134">-WhatIf</span></span>
<span data-ttu-id="ae1b2-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae1b2-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae1b2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae1b2-137">CommonParameters</span></span>
<span data-ttu-id="ae1b2-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae1b2-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae1b2-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="ae1b2-140">INPUTS</span></span>

### <span data-ttu-id="ae1b2-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="ae1b2-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ae1b2-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae1b2-142">OUTPUTS</span></span>

### <span data-ttu-id="ae1b2-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="ae1b2-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="ae1b2-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="ae1b2-144">NOTES</span></span>

<span data-ttu-id="ae1b2-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ae1b2-145">ALIASES</span></span>

<span data-ttu-id="ae1b2-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="ae1b2-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ae1b2-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ae1b2-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ae1b2-149">INPUTOBJECT <IKustoIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="ae1b2-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ae1b2-150">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ae1b2-151">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ae1b2-152">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ae1b2-153">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ae1b2-154">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="ae1b2-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ae1b2-155">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ae1b2-156">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ae1b2-157">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ae1b2-158">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ae1b2-159">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ae1b2-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ae1b2-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae1b2-160">RELATED LINKS</span></span>

