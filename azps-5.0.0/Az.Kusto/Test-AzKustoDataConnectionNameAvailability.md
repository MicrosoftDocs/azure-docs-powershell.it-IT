---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodataconnectionnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
ms.openlocfilehash: 556e0a7662a91c5c82bab7727bf676adf88d45d6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203635"
---
# <span data-ttu-id="b3716-101">Test-AzKustoDataConnectionNameAvailability</span><span class="sxs-lookup"><span data-stu-id="b3716-101">Test-AzKustoDataConnectionNameAvailability</span></span>

## <span data-ttu-id="b3716-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3716-102">SYNOPSIS</span></span>
<span data-ttu-id="b3716-103">Verifica che il nome della connessione dati sia valido e non sia già in uso.</span><span class="sxs-lookup"><span data-stu-id="b3716-103">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="b3716-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3716-104">SYNTAX</span></span>

### <span data-ttu-id="b3716-105">CheckExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b3716-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDataConnectionNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b3716-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b3716-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDataConnectionNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b3716-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3716-107">DESCRIPTION</span></span>
<span data-ttu-id="b3716-108">Verifica che il nome della connessione dati sia valido e non sia già in uso.</span><span class="sxs-lookup"><span data-stu-id="b3716-108">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="b3716-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3716-109">EXAMPLES</span></span>

### <span data-ttu-id="b3716-110">Esempio 1: verificare la disponibilità di un nome di connessione dati in uso</span><span class="sxs-lookup"><span data-stu-id="b3716-110">Example 1: Check the availability of a Data Connection name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mykustodataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message                                                                                                                                                          Name                  NameAvailable Reason
-------                                                                                                                                                          ----                  ------------- ------
Data Connection mykustodataconnection already exists in database mykustodatabase in cluster testnewkustocluster. Please select a different data connection name. mykustodataconnection False         AlreadyExists
```

<span data-ttu-id="b3716-111">Il comando sopra riportato restituisce se esiste o meno una connessione dati denominata "mykustodataconnection" nel database "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="b3716-111">The above command returns whether or not a Data Connection named "mykustodataconnection" exists in the "mykustodatabase" database.</span></span>

### <span data-ttu-id="b3716-112">Esempio 2: verificare la disponibilità di un nome di connessione dati non in uso</span><span class="sxs-lookup"><span data-stu-id="b3716-112">Example 2: Check the availability of a Data Connection name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mydataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mydataconnection True
```

<span data-ttu-id="b3716-113">Il comando sopra riportato restituisce se esiste o meno una connessione dati denominata "mydataconnection" nel database "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="b3716-113">The above command returns whether or not a Data Connection named "mydataconnection" exists in the "mykustodatabase" database.</span></span>

## <span data-ttu-id="b3716-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3716-114">PARAMETERS</span></span>

### <span data-ttu-id="b3716-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="b3716-115">-ClusterName</span></span>
<span data-ttu-id="b3716-116">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="b3716-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="b3716-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b3716-117">-DatabaseName</span></span>
<span data-ttu-id="b3716-118">Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="b3716-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="b3716-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3716-119">-DefaultProfile</span></span>
<span data-ttu-id="b3716-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3716-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3716-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3716-121">-InputObject</span></span>
<span data-ttu-id="b3716-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b3716-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b3716-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3716-123">-Name</span></span>
<span data-ttu-id="b3716-124">Nome connessione dati.</span><span class="sxs-lookup"><span data-stu-id="b3716-124">Data Connection name.</span></span>

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

### <span data-ttu-id="b3716-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3716-125">-ResourceGroupName</span></span>
<span data-ttu-id="b3716-126">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="b3716-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="b3716-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3716-127">-SubscriptionId</span></span>
<span data-ttu-id="b3716-128">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b3716-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b3716-129">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b3716-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b3716-130">-Digitare</span><span class="sxs-lookup"><span data-stu-id="b3716-130">-Type</span></span>
<span data-ttu-id="b3716-131">Il tipo di risorsa, Microsoft. kusto/Clusters/database/dataconnectings.</span><span class="sxs-lookup"><span data-stu-id="b3716-131">The type of resource, Microsoft.Kusto/Clusters/Databases/dataConnections.</span></span>

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

### <span data-ttu-id="b3716-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b3716-132">-Confirm</span></span>
<span data-ttu-id="b3716-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3716-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3716-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3716-134">-WhatIf</span></span>
<span data-ttu-id="b3716-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3716-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3716-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3716-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3716-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3716-137">CommonParameters</span></span>
<span data-ttu-id="b3716-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3716-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3716-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3716-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3716-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3716-140">INPUTS</span></span>

### <span data-ttu-id="b3716-141">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="b3716-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="b3716-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3716-142">OUTPUTS</span></span>

### <span data-ttu-id="b3716-143">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="b3716-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="b3716-144">Note</span><span class="sxs-lookup"><span data-stu-id="b3716-144">NOTES</span></span>

<span data-ttu-id="b3716-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b3716-145">ALIASES</span></span>

<span data-ttu-id="b3716-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3716-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b3716-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b3716-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b3716-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b3716-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b3716-149">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="b3716-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b3716-150">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="b3716-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="b3716-151">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="b3716-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="b3716-152">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="b3716-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="b3716-153">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="b3716-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="b3716-154">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="b3716-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b3716-155">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b3716-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="b3716-156">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="b3716-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="b3716-157">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="b3716-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="b3716-158">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b3716-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b3716-159">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b3716-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b3716-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3716-160">RELATED LINKS</span></span>

