---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/invoke-azkustodataconnectionvalidation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
ms.openlocfilehash: c12c38227c4d0a3d0a6b58685c1b8b5233c161ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959629"
---
# <span data-ttu-id="f2168-101">Invoke-AzKustoDataConnectionValidation</span><span class="sxs-lookup"><span data-stu-id="f2168-101">Invoke-AzKustoDataConnectionValidation</span></span>

## <span data-ttu-id="f2168-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2168-102">SYNOPSIS</span></span>
<span data-ttu-id="f2168-103">Controlla che i parametri di connessione dati siano validi.</span><span class="sxs-lookup"><span data-stu-id="f2168-103">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="f2168-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2168-104">SYNTAX</span></span>

### <span data-ttu-id="f2168-105">DataExpandedEventHub (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f2168-105">DataExpandedEventHub (Default)</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f2168-106">DataExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="f2168-106">DataExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f2168-107">DataExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="f2168-107">DataExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f2168-108">DataViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="f2168-108">DataViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 -StorageAccountResourceId <String> [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f2168-109">DataViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="f2168-109">DataViaIdentityExpandedEventHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 [-Compression <Compression>] [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f2168-110">DataViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="f2168-110">DataViaIdentityExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -IotHubResourceId <String> -Kind <Kind> -Location <String>
 -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f2168-111">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="f2168-111">UpdateExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f2168-112">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="f2168-112">UpdateViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f2168-113">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f2168-113">DESCRIPTION</span></span>
<span data-ttu-id="f2168-114">Controlla che i parametri di connessione dati siano validi.</span><span class="sxs-lookup"><span data-stu-id="f2168-114">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="f2168-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2168-115">EXAMPLES</span></span>

### <span data-ttu-id="f2168-116">Esempio 1: Convalidare i parametri di connessione dati di EventHub</span><span class="sxs-lookup"><span data-stu-id="f2168-116">Example 1: Validate EventHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="f2168-117">Il comando precedente convalida la connessione dati di EventHub denominata "myeventhubdc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="f2168-117">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="f2168-118">Esempio 2: Convalidare i parametri di connessione dati EventGrid</span><span class="sxs-lookup"><span data-stu-id="f2168-118">Example 2: Validate EventGrid data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="f2168-119">Il comando precedente convalida la connessione dati EventGrid denominata "myeventgriddc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="f2168-119">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="f2168-120">Esempio 3: Convalidare i parametri di connessione dati di IotHub</span><span class="sxs-lookup"><span data-stu-id="f2168-120">Example 3: Validate IotHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="f2168-121">Il comando precedente convalida la connessione dati IotHub denominata "myiothubdc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="f2168-121">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="f2168-122">Esempio 4: Convalidare i parametri di connessione dati di EventHub tramite identità</span><span class="sxs-lookup"><span data-stu-id="f2168-122">Example 4: Validate EventHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="f2168-123">Il comando precedente convalida la connessione dati di EventHub denominata "myeventhubdc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="f2168-123">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="f2168-124">Esempio 5: Convalidare i parametri di connessione dati EventGrid tramite l'identità</span><span class="sxs-lookup"><span data-stu-id="f2168-124">Example 5: Validate EventGrid data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="f2168-125">Il comando precedente convalida la connessione dati EventGrid denominata "myeventgriddc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="f2168-125">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="f2168-126">Esempio 6: Convalidare i parametri di connessione dati di IotHub tramite identità</span><span class="sxs-lookup"><span data-stu-id="f2168-126">Example 6: Validate IotHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="f2168-127">Il comando precedente convalida la connessione dati IotHub denominata "myiothubdc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="f2168-127">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="f2168-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2168-128">PARAMETERS</span></span>

### <span data-ttu-id="f2168-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="f2168-129">-BlobStorageEventType</span></span>
<span data-ttu-id="f2168-130">Nome del tipo di evento di archiviazione BLOB da elaborare.</span><span class="sxs-lookup"><span data-stu-id="f2168-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="f2168-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f2168-131">-ClusterName</span></span>
<span data-ttu-id="f2168-132">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f2168-132">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2168-133">-Compression</span><span class="sxs-lookup"><span data-stu-id="f2168-133">-Compression</span></span>
<span data-ttu-id="f2168-134">Tipo di compressione dei messaggi dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="f2168-134">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: DataExpandedEventHub, DataViaIdentityExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2168-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="f2168-135">-ConsumerGroup</span></span>
<span data-ttu-id="f2168-136">Gruppo consumer hub evento/iot.</span><span class="sxs-lookup"><span data-stu-id="f2168-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="f2168-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f2168-137">-DatabaseName</span></span>
<span data-ttu-id="f2168-138">Nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f2168-138">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2168-139">-DataConnectionName</span><span class="sxs-lookup"><span data-stu-id="f2168-139">-DataConnectionName</span></span>
<span data-ttu-id="f2168-140">Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="f2168-140">The name of the data connection.</span></span>

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

### <span data-ttu-id="f2168-141">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="f2168-141">-DataFormat</span></span>
<span data-ttu-id="f2168-142">Formato dati del messaggio.</span><span class="sxs-lookup"><span data-stu-id="f2168-142">The data format of the message.</span></span>
<span data-ttu-id="f2168-143">Facoltativamente, è possibile aggiungere il formato dati a ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="f2168-143">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="f2168-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2168-144">-DefaultProfile</span></span>
<span data-ttu-id="f2168-145">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2168-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2168-146">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="f2168-146">-EventHubResourceId</span></span>
<span data-ttu-id="f2168-147">L'ID risorsa dell'hub eventi da usare per creare una connessione dati/griglia eventi è configurato per l'invio di eventi.</span><span class="sxs-lookup"><span data-stu-id="f2168-147">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2168-148">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="f2168-148">-EventSystemProperty</span></span>
<span data-ttu-id="f2168-149">Proprietà di sistema dell'hub evento/iot.</span><span class="sxs-lookup"><span data-stu-id="f2168-149">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: DataExpandedEventHub, DataExpandedIotHub, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2168-150">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="f2168-150">-IgnoreFirstRecord</span></span>
<span data-ttu-id="f2168-151">Se impostato su true, indica che l'inserimento deve ignorare il primo record di ogni file.</span><span class="sxs-lookup"><span data-stu-id="f2168-151">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="f2168-152">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2168-152">-InputObject</span></span>
<span data-ttu-id="f2168-153">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f2168-153">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2168-154">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="f2168-154">-IotHubResourceId</span></span>
<span data-ttu-id="f2168-155">ID risorsa dell'hub Iot da usare per creare una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="f2168-155">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2168-156">-Kind</span><span class="sxs-lookup"><span data-stu-id="f2168-156">-Kind</span></span>
<span data-ttu-id="f2168-157">Tipo dell'endpoint per la connessione dati</span><span class="sxs-lookup"><span data-stu-id="f2168-157">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="f2168-158">-Location</span><span class="sxs-lookup"><span data-stu-id="f2168-158">-Location</span></span>
<span data-ttu-id="f2168-159">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f2168-159">Resource location.</span></span>

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

### <span data-ttu-id="f2168-160">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="f2168-160">-MappingRuleName</span></span>
<span data-ttu-id="f2168-161">Regola di mapping da usare per inserire i dati.</span><span class="sxs-lookup"><span data-stu-id="f2168-161">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="f2168-162">Facoltativamente, è possibile aggiungere informazioni di mapping a ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="f2168-162">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="f2168-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2168-163">-ResourceGroupName</span></span>
<span data-ttu-id="f2168-164">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f2168-164">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2168-165">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="f2168-165">-SharedAccessPolicyName</span></span>
<span data-ttu-id="f2168-166">Nome dei criteri di accesso alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="f2168-166">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2168-167">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="f2168-167">-StorageAccountResourceId</span></span>
<span data-ttu-id="f2168-168">ID risorsa dell'account di archiviazione in cui risiedono i dati.</span><span class="sxs-lookup"><span data-stu-id="f2168-168">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataViaIdentityExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2168-169">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2168-169">-SubscriptionId</span></span>
<span data-ttu-id="f2168-170">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f2168-170">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f2168-171">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="f2168-171">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2168-172">-TableName</span><span class="sxs-lookup"><span data-stu-id="f2168-172">-TableName</span></span>
<span data-ttu-id="f2168-173">Tabella in cui devono essere inseriti i dati.</span><span class="sxs-lookup"><span data-stu-id="f2168-173">The table where the data should be ingested.</span></span>
<span data-ttu-id="f2168-174">Facoltativamente, le informazioni della tabella possono essere aggiunte a ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="f2168-174">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="f2168-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2168-175">-Confirm</span></span>
<span data-ttu-id="f2168-176">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2168-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2168-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2168-177">-WhatIf</span></span>
<span data-ttu-id="f2168-178">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2168-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2168-179">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2168-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2168-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2168-180">CommonParameters</span></span>
<span data-ttu-id="f2168-181">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2168-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2168-182">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f2168-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2168-183">INPUT</span><span class="sxs-lookup"><span data-stu-id="f2168-183">INPUTS</span></span>

### <span data-ttu-id="f2168-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f2168-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f2168-185">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2168-185">OUTPUTS</span></span>

### <span data-ttu-id="f2168-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnectionValidResult</span><span class="sxs-lookup"><span data-stu-id="f2168-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnectionValidationResult</span></span>

## <span data-ttu-id="f2168-187">NOTE</span><span class="sxs-lookup"><span data-stu-id="f2168-187">NOTES</span></span>

<span data-ttu-id="f2168-188">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f2168-188">ALIASES</span></span>

<span data-ttu-id="f2168-189">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="f2168-189">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f2168-190">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="f2168-190">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f2168-191">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f2168-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f2168-192">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="f2168-192">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f2168-193">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="f2168-193">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f2168-194">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f2168-194">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f2168-195">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="f2168-195">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f2168-196">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f2168-196">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f2168-197">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="f2168-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f2168-198">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f2168-198">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f2168-199">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f2168-199">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f2168-200">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f2168-200">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f2168-201">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f2168-201">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f2168-202">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="f2168-202">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f2168-203">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2168-203">RELATED LINKS</span></span>

