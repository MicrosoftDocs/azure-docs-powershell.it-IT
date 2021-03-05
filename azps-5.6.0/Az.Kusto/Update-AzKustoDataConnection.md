---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/update-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
ms.openlocfilehash: 94a0764b61b32ce55ff4d9aca06a22d67b1edc96
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008989"
---
# <span data-ttu-id="1e2cd-101">Update-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="1e2cd-101">Update-AzKustoDataConnection</span></span>

## <span data-ttu-id="1e2cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e2cd-102">SYNOPSIS</span></span>
<span data-ttu-id="1e2cd-103">Aggiorna una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-103">Updates a data connection.</span></span>

## <span data-ttu-id="1e2cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e2cd-104">SYNTAX</span></span>

### <span data-ttu-id="1e2cd-105">UpdateExpandedEventHub (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1e2cd-105">UpdateExpandedEventHub (Default)</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1e2cd-106">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="1e2cd-106">UpdateExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1e2cd-107">UpdateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="1e2cd-107">UpdateExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1e2cd-108">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="1e2cd-108">UpdateViaIdentityExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> -StorageAccountResourceId <String>
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1e2cd-109">UpdateViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="1e2cd-109">UpdateViaIdentityExpandedEventHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1e2cd-110">UpdateViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="1e2cd-110">UpdateViaIdentityExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>]
 [-EventSystemProperty <String[]>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1e2cd-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1e2cd-111">DESCRIPTION</span></span>
<span data-ttu-id="1e2cd-112">Aggiorna una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-112">Updates a data connection.</span></span>

## <span data-ttu-id="1e2cd-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e2cd-113">EXAMPLES</span></span>

### <span data-ttu-id="1e2cd-114">Esempio 1: Aggiornare una connessione dati di EventHub esistente</span><span class="sxs-lookup"><span data-stu-id="1e2cd-114">Example 1: Update an existing EventHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="1e2cd-115">Il comando precedente aggiorna la connessione dati Esistente di EventHub denominata "myeventhubdc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="1e2cd-115">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="1e2cd-116">Esempio 2: Aggiornare una connessione dati EventGrid esistente</span><span class="sxs-lookup"><span data-stu-id="1e2cd-116">Example 2: Update an existing EventGrid data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="1e2cd-117">Il comando precedente aggiorna la connessione dati EventGrid esistente denominata "myeventgriddc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="1e2cd-117">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="1e2cd-118">Esempio 3: Aggiornare una connessione dati IotHub esistente</span><span class="sxs-lookup"><span data-stu-id="1e2cd-118">Example 3: Update an existing IotHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="1e2cd-119">Il comando precedente aggiorna la connessione dati IotHub esistente denominata "myiothubdc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="1e2cd-119">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="1e2cd-120">Esempio 4: Aggiornare una connessione dati di EventHub esistente tramite identità</span><span class="sxs-lookup"><span data-stu-id="1e2cd-120">Example 4: Update an existing EventHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="1e2cd-121">Il comando precedente aggiorna la connessione dati Esistente di EventHub denominata "myeventhubdc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="1e2cd-121">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="1e2cd-122">Esempio 5: Aggiornare una connessione dati EventGrid esistente tramite l'identità</span><span class="sxs-lookup"><span data-stu-id="1e2cd-122">Example 5: Update an existing EventGrid data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="1e2cd-123">Il comando precedente aggiorna la connessione dati EventGrid esistente denominata "myeventgriddc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="1e2cd-123">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="1e2cd-124">Esempio 6: Aggiornare una connessione dati IotHub esistente tramite un'identità</span><span class="sxs-lookup"><span data-stu-id="1e2cd-124">Example 6: Update an existing IotHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="1e2cd-125">Il comando precedente aggiorna la connessione dati IotHub esistente denominata "myiothubdc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="1e2cd-125">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="1e2cd-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e2cd-126">PARAMETERS</span></span>

### <span data-ttu-id="1e2cd-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e2cd-127">-AsJob</span></span>
<span data-ttu-id="1e2cd-128">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="1e2cd-128">Run the command as a job</span></span>

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

### <span data-ttu-id="1e2cd-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="1e2cd-129">-BlobStorageEventType</span></span>
<span data-ttu-id="1e2cd-130">Nome del tipo di evento di archiviazione BLOB da elaborare.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="1e2cd-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1e2cd-131">-ClusterName</span></span>
<span data-ttu-id="1e2cd-132">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-132">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="1e2cd-133">-Compression</span><span class="sxs-lookup"><span data-stu-id="1e2cd-133">-Compression</span></span>
<span data-ttu-id="1e2cd-134">Tipo di compressione dei messaggi dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-134">The event hub messages compression type.</span></span>

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

### <span data-ttu-id="1e2cd-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="1e2cd-135">-ConsumerGroup</span></span>
<span data-ttu-id="1e2cd-136">Gruppo consumer hub evento/iot.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="1e2cd-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1e2cd-137">-DatabaseName</span></span>
<span data-ttu-id="1e2cd-138">Nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-138">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="1e2cd-139">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="1e2cd-139">-DataFormat</span></span>
<span data-ttu-id="1e2cd-140">Formato dati del messaggio.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-140">The data format of the message.</span></span>
<span data-ttu-id="1e2cd-141">Facoltativamente, è possibile aggiungere il formato dati a ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-141">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="1e2cd-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e2cd-142">-DefaultProfile</span></span>
<span data-ttu-id="1e2cd-143">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e2cd-144">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="1e2cd-144">-EventHubResourceId</span></span>
<span data-ttu-id="1e2cd-145">L'ID risorsa dell'hub eventi da usare per creare una connessione dati/griglia eventi è configurato per l'invio di eventi.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-145">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

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

### <span data-ttu-id="1e2cd-146">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="1e2cd-146">-EventSystemProperty</span></span>
<span data-ttu-id="1e2cd-147">Proprietà di sistema dell'hub evento/iot.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-147">System properties of the event/iot hub.</span></span>

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

### <span data-ttu-id="1e2cd-148">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="1e2cd-148">-IgnoreFirstRecord</span></span>
<span data-ttu-id="1e2cd-149">Se impostato su true, indica che l'inserimento deve ignorare il primo record di ogni file.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-149">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="1e2cd-150">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e2cd-150">-InputObject</span></span>
<span data-ttu-id="1e2cd-151">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-151">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1e2cd-152">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="1e2cd-152">-IotHubResourceId</span></span>
<span data-ttu-id="1e2cd-153">ID risorsa dell'hub Iot da usare per creare una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-153">The resource ID of the Iot hub to be used to create a data connection.</span></span>

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

### <span data-ttu-id="1e2cd-154">-Kind</span><span class="sxs-lookup"><span data-stu-id="1e2cd-154">-Kind</span></span>
<span data-ttu-id="1e2cd-155">Tipo dell'endpoint per la connessione dati</span><span class="sxs-lookup"><span data-stu-id="1e2cd-155">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="1e2cd-156">-Location</span><span class="sxs-lookup"><span data-stu-id="1e2cd-156">-Location</span></span>
<span data-ttu-id="1e2cd-157">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-157">Resource location.</span></span>

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

### <span data-ttu-id="1e2cd-158">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="1e2cd-158">-MappingRuleName</span></span>
<span data-ttu-id="1e2cd-159">Regola di mapping da usare per inserire i dati.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-159">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="1e2cd-160">Facoltativamente, è possibile aggiungere informazioni di mapping a ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-160">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="1e2cd-161">-Name</span><span class="sxs-lookup"><span data-stu-id="1e2cd-161">-Name</span></span>
<span data-ttu-id="1e2cd-162">Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-162">The name of the data connection.</span></span>

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

### <span data-ttu-id="1e2cd-163">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1e2cd-163">-NoWait</span></span>
<span data-ttu-id="1e2cd-164">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="1e2cd-164">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1e2cd-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e2cd-165">-ResourceGroupName</span></span>
<span data-ttu-id="1e2cd-166">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-166">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="1e2cd-167">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="1e2cd-167">-SharedAccessPolicyName</span></span>
<span data-ttu-id="1e2cd-168">Nome dei criteri di accesso alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-168">The name of the share access policy.</span></span>

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

### <span data-ttu-id="1e2cd-169">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="1e2cd-169">-StorageAccountResourceId</span></span>
<span data-ttu-id="1e2cd-170">ID risorsa dell'account di archiviazione in cui risiedono i dati.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-170">The resource ID of the storage account where the data resides.</span></span>

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

### <span data-ttu-id="1e2cd-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e2cd-171">-SubscriptionId</span></span>
<span data-ttu-id="1e2cd-172">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1e2cd-173">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-173">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1e2cd-174">-TableName</span><span class="sxs-lookup"><span data-stu-id="1e2cd-174">-TableName</span></span>
<span data-ttu-id="1e2cd-175">Tabella in cui devono essere inseriti i dati.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-175">The table where the data should be ingested.</span></span>
<span data-ttu-id="1e2cd-176">Facoltativamente, le informazioni della tabella possono essere aggiunte a ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-176">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="1e2cd-177">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e2cd-177">-Confirm</span></span>
<span data-ttu-id="1e2cd-178">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e2cd-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e2cd-179">-WhatIf</span></span>
<span data-ttu-id="1e2cd-180">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e2cd-181">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e2cd-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e2cd-182">CommonParameters</span></span>
<span data-ttu-id="1e2cd-183">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e2cd-184">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e2cd-185">INPUT</span><span class="sxs-lookup"><span data-stu-id="1e2cd-185">INPUTS</span></span>

### <span data-ttu-id="1e2cd-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="1e2cd-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="1e2cd-187">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e2cd-187">OUTPUTS</span></span>

### <span data-ttu-id="1e2cd-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="1e2cd-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="1e2cd-189">NOTE</span><span class="sxs-lookup"><span data-stu-id="1e2cd-189">NOTES</span></span>

<span data-ttu-id="1e2cd-190">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1e2cd-190">ALIASES</span></span>

<span data-ttu-id="1e2cd-191">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="1e2cd-191">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1e2cd-192">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-192">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1e2cd-193">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-193">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1e2cd-194">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="1e2cd-194">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1e2cd-195">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-195">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="1e2cd-196">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-196">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="1e2cd-197">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-197">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="1e2cd-198">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-198">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="1e2cd-199">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="1e2cd-199">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1e2cd-200">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-200">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="1e2cd-201">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-201">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="1e2cd-202">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-202">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="1e2cd-203">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-203">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1e2cd-204">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="1e2cd-204">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1e2cd-205">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e2cd-205">RELATED LINKS</span></span>

