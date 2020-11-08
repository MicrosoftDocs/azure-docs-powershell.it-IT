---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
ms.openlocfilehash: 4fadb8a48b9886fe1c5a7c916d8f810abd8de6cc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202455"
---
# <span data-ttu-id="6dcce-101">New-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="6dcce-101">New-AzKustoDataConnection</span></span>

## <span data-ttu-id="6dcce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6dcce-102">SYNOPSIS</span></span>
<span data-ttu-id="6dcce-103">Crea o aggiorna una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="6dcce-103">Creates or updates a data connection.</span></span>

## <span data-ttu-id="6dcce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6dcce-104">SYNTAX</span></span>

### <span data-ttu-id="6dcce-105">CreateExpandedEventHub (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6dcce-105">CreateExpandedEventHub (Default)</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6dcce-106">CreateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="6dcce-106">CreateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6dcce-107">CreateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="6dcce-107">CreateExpandedIotHub</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6dcce-108">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="6dcce-108">UpdateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6dcce-109">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="6dcce-109">UpdateViaIdentityExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6dcce-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6dcce-110">DESCRIPTION</span></span>
<span data-ttu-id="6dcce-111">Crea o aggiorna una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="6dcce-111">Creates or updates a data connection.</span></span>

## <span data-ttu-id="6dcce-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6dcce-112">EXAMPLES</span></span>

### <span data-ttu-id="6dcce-113">Esempio 1: creare una nuova connessione dati EventHub</span><span class="sxs-lookup"><span data-stu-id="6dcce-113">Example 1: Create a new EventHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "EventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="6dcce-114">Il comando precedente crea una nuova connessione dati EventHub denominata "myeventhubdc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="6dcce-114">The above command creates a new EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="6dcce-115">Esempio 2: creare una nuova connessione dati EventGrid</span><span class="sxs-lookup"><span data-stu-id="6dcce-115">Example 2: Create a new EventGrid data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping" -IgnoreFirstRecord "false" -BlobStorageEventType "Microsoft.Storage.BlobRenamed"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="6dcce-116">Il comando precedente crea una nuova connessione dati EventGrid denominata "myeventgriddc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="6dcce-116">The above command creates a new EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="6dcce-117">Esempio 3: creare una nuova connessione dati IotHub</span><span class="sxs-lookup"><span data-stu-id="6dcce-117">Example 3: Create a new IotHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="6dcce-118">Il comando precedente crea una nuova connessione dati IotHub denominata "myiothubdc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="6dcce-118">The above command creates a new IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="6dcce-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6dcce-119">PARAMETERS</span></span>

### <span data-ttu-id="6dcce-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6dcce-120">-AsJob</span></span>
<span data-ttu-id="6dcce-121">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="6dcce-121">Run the command as a job</span></span>

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

### <span data-ttu-id="6dcce-122">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="6dcce-122">-BlobStorageEventType</span></span>
<span data-ttu-id="6dcce-123">Nome del tipo di evento di archiviazione BLOB da elaborare.</span><span class="sxs-lookup"><span data-stu-id="6dcce-123">The name of blob storage event type to process.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.BlobStorageEventType
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dcce-124">-Clustername</span><span class="sxs-lookup"><span data-stu-id="6dcce-124">-ClusterName</span></span>
<span data-ttu-id="6dcce-125">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="6dcce-125">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="6dcce-126">-Compressione</span><span class="sxs-lookup"><span data-stu-id="6dcce-126">-Compression</span></span>
<span data-ttu-id="6dcce-127">Tipo di compressione messaggi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="6dcce-127">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: CreateExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dcce-128">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="6dcce-128">-ConsumerGroup</span></span>
<span data-ttu-id="6dcce-129">Gruppo Consumer Hub eventi/molto.</span><span class="sxs-lookup"><span data-stu-id="6dcce-129">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="6dcce-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6dcce-130">-DatabaseName</span></span>
<span data-ttu-id="6dcce-131">Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="6dcce-131">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="6dcce-132">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="6dcce-132">-DataFormat</span></span>
<span data-ttu-id="6dcce-133">Formato dati del messaggio.</span><span class="sxs-lookup"><span data-stu-id="6dcce-133">The data format of the message.</span></span>
<span data-ttu-id="6dcce-134">Facoltativamente, è possibile aggiungere il formato dati a ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="6dcce-134">Optionally the data format can be added to each message.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EventGridDataFormat
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dcce-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dcce-135">-DefaultProfile</span></span>
<span data-ttu-id="6dcce-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6dcce-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dcce-137">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="6dcce-137">-EventHubResourceId</span></span>
<span data-ttu-id="6dcce-138">L'ID risorsa dell'hub eventi da usare per creare una griglia di connessione dati/evento è configurato per l'invio di eventi.</span><span class="sxs-lookup"><span data-stu-id="6dcce-138">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedEventGrid, CreateExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dcce-139">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="6dcce-139">-EventSystemProperty</span></span>
<span data-ttu-id="6dcce-140">Proprietà di sistema dell'hub dell'evento/sacco.</span><span class="sxs-lookup"><span data-stu-id="6dcce-140">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpandedEventHub, CreateExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dcce-141">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="6dcce-141">-IgnoreFirstRecord</span></span>
<span data-ttu-id="6dcce-142">Se impostato su true, indica che l'ingestione deve ignorare il primo record di ogni file.</span><span class="sxs-lookup"><span data-stu-id="6dcce-142">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dcce-143">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="6dcce-143">-IotHubResourceId</span></span>
<span data-ttu-id="6dcce-144">ID risorsa dell'hub molto da usare per creare una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="6dcce-144">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dcce-145">-Tipo</span><span class="sxs-lookup"><span data-stu-id="6dcce-145">-Kind</span></span>
<span data-ttu-id="6dcce-146">Tipo di endpoint per la connessione dati</span><span class="sxs-lookup"><span data-stu-id="6dcce-146">Kind of the endpoint for the data connection</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dcce-147">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6dcce-147">-Location</span></span>
<span data-ttu-id="6dcce-148">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="6dcce-148">Resource location.</span></span>

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

### <span data-ttu-id="6dcce-149">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="6dcce-149">-MappingRuleName</span></span>
<span data-ttu-id="6dcce-150">Regola di mapping da usare per l'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="6dcce-150">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="6dcce-151">Facoltativamente, le informazioni di mapping possono essere aggiunte a ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="6dcce-151">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="6dcce-152">-Nome</span><span class="sxs-lookup"><span data-stu-id="6dcce-152">-Name</span></span>
<span data-ttu-id="6dcce-153">Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="6dcce-153">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dcce-154">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="6dcce-154">-NoWait</span></span>
<span data-ttu-id="6dcce-155">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="6dcce-155">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6dcce-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dcce-156">-ResourceGroupName</span></span>
<span data-ttu-id="6dcce-157">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="6dcce-157">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="6dcce-158">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="6dcce-158">-SharedAccessPolicyName</span></span>
<span data-ttu-id="6dcce-159">Nome del criterio di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="6dcce-159">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dcce-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="6dcce-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="6dcce-161">ID risorsa dell'account di archiviazione in cui si trovano i dati.</span><span class="sxs-lookup"><span data-stu-id="6dcce-161">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dcce-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6dcce-162">-SubscriptionId</span></span>
<span data-ttu-id="6dcce-163">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6dcce-163">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6dcce-164">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="6dcce-164">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6dcce-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="6dcce-165">-TableName</span></span>
<span data-ttu-id="6dcce-166">Tabella in cui devono essere ingeriti i dati.</span><span class="sxs-lookup"><span data-stu-id="6dcce-166">The table where the data should be ingested.</span></span>
<span data-ttu-id="6dcce-167">Facoltativamente, le informazioni sulla tabella possono essere aggiunte a ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="6dcce-167">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="6dcce-168">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6dcce-168">-Confirm</span></span>
<span data-ttu-id="6dcce-169">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dcce-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dcce-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dcce-170">-WhatIf</span></span>
<span data-ttu-id="6dcce-171">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6dcce-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dcce-172">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6dcce-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dcce-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dcce-173">CommonParameters</span></span>
<span data-ttu-id="6dcce-174">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dcce-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dcce-175">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6dcce-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dcce-176">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6dcce-176">INPUTS</span></span>

## <span data-ttu-id="6dcce-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6dcce-177">OUTPUTS</span></span>

### <span data-ttu-id="6dcce-178">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. IDataConnection</span><span class="sxs-lookup"><span data-stu-id="6dcce-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="6dcce-179">Note</span><span class="sxs-lookup"><span data-stu-id="6dcce-179">NOTES</span></span>

<span data-ttu-id="6dcce-180">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6dcce-180">ALIASES</span></span>

## <span data-ttu-id="6dcce-181">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6dcce-181">RELATED LINKS</span></span>

