---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
ms.openlocfilehash: 70862dee30fd03430d93de88e1e63f0f5acf5e6c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362526"
---
# <span data-ttu-id="12f2e-101">Update-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="12f2e-101">Update-AzKustoDataConnection</span></span>

## <span data-ttu-id="12f2e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12f2e-102">SYNOPSIS</span></span>
<span data-ttu-id="12f2e-103">Aggiorna una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="12f2e-103">Updates a data connection.</span></span>

## <span data-ttu-id="12f2e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12f2e-104">SYNTAX</span></span>

### <span data-ttu-id="12f2e-105">UpdateExpandedEventHub (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="12f2e-105">UpdateExpandedEventHub (Default)</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="12f2e-106">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="12f2e-106">UpdateExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="12f2e-107">UpdateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="12f2e-107">UpdateExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="12f2e-108">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="12f2e-108">UpdateViaIdentityExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> -StorageAccountResourceId <String>
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="12f2e-109">UpdateViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="12f2e-109">UpdateViaIdentityExpandedEventHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="12f2e-110">UpdateViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="12f2e-110">UpdateViaIdentityExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>]
 [-EventSystemProperty <String[]>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="12f2e-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12f2e-111">DESCRIPTION</span></span>
<span data-ttu-id="12f2e-112">Aggiorna una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="12f2e-112">Updates a data connection.</span></span>

## <span data-ttu-id="12f2e-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12f2e-113">EXAMPLES</span></span>

### <span data-ttu-id="12f2e-114">Esempio 1: aggiornare una connessione dati EventHub esistente</span><span class="sxs-lookup"><span data-stu-id="12f2e-114">Example 1: Update an existing EventHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="12f2e-115">Il comando precedente aggiorna la connessione dati EventHub esistente denominata "myeventhubdc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="12f2e-115">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="12f2e-116">Esempio 2: aggiornare una connessione dati EventGrid esistente</span><span class="sxs-lookup"><span data-stu-id="12f2e-116">Example 2: Update an existing EventGrid data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="12f2e-117">Il comando precedente aggiorna la connessione dati EventGrid esistente denominata "myeventgriddc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="12f2e-117">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="12f2e-118">Esempio 3: aggiornare una connessione dati IotHub esistente</span><span class="sxs-lookup"><span data-stu-id="12f2e-118">Example 3: Update an existing IotHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="12f2e-119">Il comando precedente aggiorna la connessione dati IotHub esistente denominata "myiothubdc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="12f2e-119">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="12f2e-120">Esempio 4: aggiornare una connessione dati di EventHub esistente tramite l'identità</span><span class="sxs-lookup"><span data-stu-id="12f2e-120">Example 4: Update an existing EventHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="12f2e-121">Il comando precedente aggiorna la connessione dati EventHub esistente denominata "myeventhubdc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="12f2e-121">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="12f2e-122">Esempio 5: aggiornare una connessione dati di EventGrid esistente tramite l'identità</span><span class="sxs-lookup"><span data-stu-id="12f2e-122">Example 5: Update an existing EventGrid data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="12f2e-123">Il comando precedente aggiorna la connessione dati EventGrid esistente denominata "myeventgriddc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="12f2e-123">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="12f2e-124">Esempio 6: aggiornare una connessione dati di IotHub esistente tramite l'identità</span><span class="sxs-lookup"><span data-stu-id="12f2e-124">Example 6: Update an existing IotHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="12f2e-125">Il comando precedente aggiorna la connessione dati IotHub esistente denominata "myiothubdc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="12f2e-125">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="12f2e-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12f2e-126">PARAMETERS</span></span>

### <span data-ttu-id="12f2e-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12f2e-127">-AsJob</span></span>
<span data-ttu-id="12f2e-128">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="12f2e-128">Run the command as a job</span></span>

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

### <span data-ttu-id="12f2e-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="12f2e-129">-BlobStorageEventType</span></span>
<span data-ttu-id="12f2e-130">Nome del tipo di evento di archiviazione BLOB da elaborare.</span><span class="sxs-lookup"><span data-stu-id="12f2e-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="12f2e-131">-Clustername</span><span class="sxs-lookup"><span data-stu-id="12f2e-131">-ClusterName</span></span>
<span data-ttu-id="12f2e-132">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="12f2e-132">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12f2e-133">-Compressione</span><span class="sxs-lookup"><span data-stu-id="12f2e-133">-Compression</span></span>
<span data-ttu-id="12f2e-134">Tipo di compressione messaggi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="12f2e-134">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: UpdateExpandedEventHub, UpdateViaIdentityExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12f2e-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="12f2e-135">-ConsumerGroup</span></span>
<span data-ttu-id="12f2e-136">Gruppo Consumer Hub eventi/molto.</span><span class="sxs-lookup"><span data-stu-id="12f2e-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="12f2e-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="12f2e-137">-DatabaseName</span></span>
<span data-ttu-id="12f2e-138">Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="12f2e-138">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12f2e-139">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="12f2e-139">-DataFormat</span></span>
<span data-ttu-id="12f2e-140">Formato dati del messaggio.</span><span class="sxs-lookup"><span data-stu-id="12f2e-140">The data format of the message.</span></span>
<span data-ttu-id="12f2e-141">Facoltativamente, è possibile aggiungere il formato dati a ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="12f2e-141">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="12f2e-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12f2e-142">-DefaultProfile</span></span>
<span data-ttu-id="12f2e-143">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12f2e-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12f2e-144">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="12f2e-144">-EventHubResourceId</span></span>
<span data-ttu-id="12f2e-145">L'ID risorsa dell'hub eventi da usare per creare una griglia di connessione dati/evento è configurato per l'invio di eventi.</span><span class="sxs-lookup"><span data-stu-id="12f2e-145">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateViaIdentityExpandedEventGrid, UpdateViaIdentityExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12f2e-146">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="12f2e-146">-EventSystemProperty</span></span>
<span data-ttu-id="12f2e-147">Proprietà di sistema dell'hub dell'evento/sacco.</span><span class="sxs-lookup"><span data-stu-id="12f2e-147">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpandedEventHub, UpdateExpandedIotHub, UpdateViaIdentityExpandedEventHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12f2e-148">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="12f2e-148">-IgnoreFirstRecord</span></span>
<span data-ttu-id="12f2e-149">Se impostato su true, indica che l'ingestione deve ignorare il primo record di ogni file.</span><span class="sxs-lookup"><span data-stu-id="12f2e-149">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="12f2e-150">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12f2e-150">-InputObject</span></span>
<span data-ttu-id="12f2e-151">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="12f2e-151">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpandedEventGrid, UpdateViaIdentityExpandedEventHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12f2e-152">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="12f2e-152">-IotHubResourceId</span></span>
<span data-ttu-id="12f2e-153">ID risorsa dell'hub molto da usare per creare una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="12f2e-153">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedIotHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12f2e-154">-Tipo</span><span class="sxs-lookup"><span data-stu-id="12f2e-154">-Kind</span></span>
<span data-ttu-id="12f2e-155">Tipo di endpoint per la connessione dati</span><span class="sxs-lookup"><span data-stu-id="12f2e-155">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="12f2e-156">-Posizione</span><span class="sxs-lookup"><span data-stu-id="12f2e-156">-Location</span></span>
<span data-ttu-id="12f2e-157">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="12f2e-157">Resource location.</span></span>

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

### <span data-ttu-id="12f2e-158">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="12f2e-158">-MappingRuleName</span></span>
<span data-ttu-id="12f2e-159">Regola di mapping da usare per l'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="12f2e-159">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="12f2e-160">Facoltativamente, le informazioni di mapping possono essere aggiunte a ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="12f2e-160">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="12f2e-161">-Nome</span><span class="sxs-lookup"><span data-stu-id="12f2e-161">-Name</span></span>
<span data-ttu-id="12f2e-162">Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="12f2e-162">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12f2e-163">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="12f2e-163">-NoWait</span></span>
<span data-ttu-id="12f2e-164">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="12f2e-164">Run the command asynchronously</span></span>

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

### <span data-ttu-id="12f2e-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12f2e-165">-ResourceGroupName</span></span>
<span data-ttu-id="12f2e-166">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="12f2e-166">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12f2e-167">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="12f2e-167">-SharedAccessPolicyName</span></span>
<span data-ttu-id="12f2e-168">Nome del criterio di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="12f2e-168">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedIotHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12f2e-169">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="12f2e-169">-StorageAccountResourceId</span></span>
<span data-ttu-id="12f2e-170">ID risorsa dell'account di archiviazione in cui si trovano i dati.</span><span class="sxs-lookup"><span data-stu-id="12f2e-170">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12f2e-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12f2e-171">-SubscriptionId</span></span>
<span data-ttu-id="12f2e-172">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="12f2e-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="12f2e-173">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="12f2e-173">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12f2e-174">-TableName</span><span class="sxs-lookup"><span data-stu-id="12f2e-174">-TableName</span></span>
<span data-ttu-id="12f2e-175">Tabella in cui devono essere ingeriti i dati.</span><span class="sxs-lookup"><span data-stu-id="12f2e-175">The table where the data should be ingested.</span></span>
<span data-ttu-id="12f2e-176">Facoltativamente, le informazioni sulla tabella possono essere aggiunte a ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="12f2e-176">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="12f2e-177">-Confermare</span><span class="sxs-lookup"><span data-stu-id="12f2e-177">-Confirm</span></span>
<span data-ttu-id="12f2e-178">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12f2e-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12f2e-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12f2e-179">-WhatIf</span></span>
<span data-ttu-id="12f2e-180">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12f2e-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12f2e-181">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12f2e-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12f2e-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12f2e-182">CommonParameters</span></span>
<span data-ttu-id="12f2e-183">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12f2e-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12f2e-184">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12f2e-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12f2e-185">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12f2e-185">INPUTS</span></span>

### <span data-ttu-id="12f2e-186">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="12f2e-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="12f2e-187">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12f2e-187">OUTPUTS</span></span>

### <span data-ttu-id="12f2e-188">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. IDataConnection</span><span class="sxs-lookup"><span data-stu-id="12f2e-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="12f2e-189">Note</span><span class="sxs-lookup"><span data-stu-id="12f2e-189">NOTES</span></span>

<span data-ttu-id="12f2e-190">ALIAS</span><span class="sxs-lookup"><span data-stu-id="12f2e-190">ALIASES</span></span>

<span data-ttu-id="12f2e-191">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12f2e-191">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="12f2e-192">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="12f2e-192">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="12f2e-193">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="12f2e-193">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="12f2e-194">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="12f2e-194">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="12f2e-195">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="12f2e-195">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="12f2e-196">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="12f2e-196">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="12f2e-197">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="12f2e-197">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="12f2e-198">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="12f2e-198">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="12f2e-199">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="12f2e-199">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="12f2e-200">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="12f2e-200">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="12f2e-201">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="12f2e-201">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="12f2e-202">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="12f2e-202">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="12f2e-203">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="12f2e-203">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="12f2e-204">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="12f2e-204">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="12f2e-205">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12f2e-205">RELATED LINKS</span></span>

