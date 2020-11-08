---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodataconnectionvalidation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
ms.openlocfilehash: 9eb3ff31873b23fc97f53fffecdbbb38367ac2b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189812"
---
# <span data-ttu-id="8a2a1-101">Invoke-AzKustoDataConnectionValidation</span><span class="sxs-lookup"><span data-stu-id="8a2a1-101">Invoke-AzKustoDataConnectionValidation</span></span>

## <span data-ttu-id="8a2a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a2a1-102">SYNOPSIS</span></span>
<span data-ttu-id="8a2a1-103">Verifica che i parametri di connessione dati siano validi.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-103">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="8a2a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a2a1-104">SYNTAX</span></span>

### <span data-ttu-id="8a2a1-105">DataExpandedEventHub (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8a2a1-105">DataExpandedEventHub (Default)</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8a2a1-106">DataExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="8a2a1-106">DataExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8a2a1-107">DataExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="8a2a1-107">DataExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8a2a1-108">DataViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="8a2a1-108">DataViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 -StorageAccountResourceId <String> [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8a2a1-109">DataViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="8a2a1-109">DataViaIdentityExpandedEventHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 [-Compression <Compression>] [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8a2a1-110">DataViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="8a2a1-110">DataViaIdentityExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -IotHubResourceId <String> -Kind <Kind> -Location <String>
 -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8a2a1-111">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="8a2a1-111">UpdateExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8a2a1-112">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="8a2a1-112">UpdateViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8a2a1-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a2a1-113">DESCRIPTION</span></span>
<span data-ttu-id="8a2a1-114">Verifica che i parametri di connessione dati siano validi.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-114">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="8a2a1-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a2a1-115">EXAMPLES</span></span>

### <span data-ttu-id="8a2a1-116">Esempio 1: convalidare i parametri di connessione dati EventHub</span><span class="sxs-lookup"><span data-stu-id="8a2a1-116">Example 1: Validate EventHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="8a2a1-117">Il comando precedente convalida la connessione dati di EventHub denominata "myeventhubdc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="8a2a1-117">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="8a2a1-118">Esempio 2: convalidare i parametri di connessione dati EventGrid</span><span class="sxs-lookup"><span data-stu-id="8a2a1-118">Example 2: Validate EventGrid data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="8a2a1-119">Il comando precedente convalida la connessione dati di EventGrid denominata "myeventgriddc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="8a2a1-119">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="8a2a1-120">Esempio 3: convalidare i parametri di connessione dati IotHub</span><span class="sxs-lookup"><span data-stu-id="8a2a1-120">Example 3: Validate IotHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="8a2a1-121">Il comando precedente convalida la connessione dati di IotHub denominata "myiothubdc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="8a2a1-121">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="8a2a1-122">Esempio 4: convalidare i parametri di connessione dati EventHub tramite identità</span><span class="sxs-lookup"><span data-stu-id="8a2a1-122">Example 4: Validate EventHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="8a2a1-123">Il comando precedente convalida la connessione dati di EventHub denominata "myeventhubdc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="8a2a1-123">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="8a2a1-124">Esempio 5: convalidare i parametri di connessione dati EventGrid tramite identità</span><span class="sxs-lookup"><span data-stu-id="8a2a1-124">Example 5: Validate EventGrid data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="8a2a1-125">Il comando precedente convalida la connessione dati di EventGrid denominata "myeventgriddc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="8a2a1-125">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="8a2a1-126">Esempio 6: convalidare i parametri di connessione dati IotHub tramite identità</span><span class="sxs-lookup"><span data-stu-id="8a2a1-126">Example 6: Validate IotHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="8a2a1-127">Il comando precedente convalida la connessione dati di IotHub denominata "myiothubdc" per il database "mykustodatabase" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="8a2a1-127">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="8a2a1-128">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a2a1-128">PARAMETERS</span></span>

### <span data-ttu-id="8a2a1-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="8a2a1-129">-BlobStorageEventType</span></span>
<span data-ttu-id="8a2a1-130">Nome del tipo di evento di archiviazione BLOB da elaborare.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="8a2a1-131">-Clustername</span><span class="sxs-lookup"><span data-stu-id="8a2a1-131">-ClusterName</span></span>
<span data-ttu-id="8a2a1-132">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-132">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="8a2a1-133">-Compressione</span><span class="sxs-lookup"><span data-stu-id="8a2a1-133">-Compression</span></span>
<span data-ttu-id="8a2a1-134">Tipo di compressione messaggi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-134">The event hub messages compression type.</span></span>

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

### <span data-ttu-id="8a2a1-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="8a2a1-135">-ConsumerGroup</span></span>
<span data-ttu-id="8a2a1-136">Gruppo Consumer Hub eventi/molto.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="8a2a1-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8a2a1-137">-DatabaseName</span></span>
<span data-ttu-id="8a2a1-138">Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-138">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="8a2a1-139">-Dataconnectname</span><span class="sxs-lookup"><span data-stu-id="8a2a1-139">-DataConnectionName</span></span>
<span data-ttu-id="8a2a1-140">Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-140">The name of the data connection.</span></span>

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

### <span data-ttu-id="8a2a1-141">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="8a2a1-141">-DataFormat</span></span>
<span data-ttu-id="8a2a1-142">Formato dati del messaggio.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-142">The data format of the message.</span></span>
<span data-ttu-id="8a2a1-143">Facoltativamente, è possibile aggiungere il formato dati a ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-143">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="8a2a1-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a2a1-144">-DefaultProfile</span></span>
<span data-ttu-id="8a2a1-145">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a2a1-146">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="8a2a1-146">-EventHubResourceId</span></span>
<span data-ttu-id="8a2a1-147">L'ID risorsa dell'hub eventi da usare per creare una griglia di connessione dati/evento è configurato per l'invio di eventi.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-147">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

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

### <span data-ttu-id="8a2a1-148">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="8a2a1-148">-EventSystemProperty</span></span>
<span data-ttu-id="8a2a1-149">Proprietà di sistema dell'hub dell'evento/sacco.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-149">System properties of the event/iot hub.</span></span>

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

### <span data-ttu-id="8a2a1-150">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="8a2a1-150">-IgnoreFirstRecord</span></span>
<span data-ttu-id="8a2a1-151">Se impostato su true, indica che l'ingestione deve ignorare il primo record di ogni file.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-151">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="8a2a1-152">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a2a1-152">-InputObject</span></span>
<span data-ttu-id="8a2a1-153">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-153">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8a2a1-154">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="8a2a1-154">-IotHubResourceId</span></span>
<span data-ttu-id="8a2a1-155">ID risorsa dell'hub molto da usare per creare una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-155">The resource ID of the Iot hub to be used to create a data connection.</span></span>

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

### <span data-ttu-id="8a2a1-156">-Tipo</span><span class="sxs-lookup"><span data-stu-id="8a2a1-156">-Kind</span></span>
<span data-ttu-id="8a2a1-157">Tipo di endpoint per la connessione dati</span><span class="sxs-lookup"><span data-stu-id="8a2a1-157">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="8a2a1-158">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8a2a1-158">-Location</span></span>
<span data-ttu-id="8a2a1-159">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-159">Resource location.</span></span>

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

### <span data-ttu-id="8a2a1-160">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="8a2a1-160">-MappingRuleName</span></span>
<span data-ttu-id="8a2a1-161">Regola di mapping da usare per l'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-161">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="8a2a1-162">Facoltativamente, le informazioni di mapping possono essere aggiunte a ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-162">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="8a2a1-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a2a1-163">-ResourceGroupName</span></span>
<span data-ttu-id="8a2a1-164">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-164">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="8a2a1-165">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="8a2a1-165">-SharedAccessPolicyName</span></span>
<span data-ttu-id="8a2a1-166">Nome del criterio di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-166">The name of the share access policy.</span></span>

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

### <span data-ttu-id="8a2a1-167">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="8a2a1-167">-StorageAccountResourceId</span></span>
<span data-ttu-id="8a2a1-168">ID risorsa dell'account di archiviazione in cui si trovano i dati.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-168">The resource ID of the storage account where the data resides.</span></span>

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

### <span data-ttu-id="8a2a1-169">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a2a1-169">-SubscriptionId</span></span>
<span data-ttu-id="8a2a1-170">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-170">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8a2a1-171">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-171">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8a2a1-172">-TableName</span><span class="sxs-lookup"><span data-stu-id="8a2a1-172">-TableName</span></span>
<span data-ttu-id="8a2a1-173">Tabella in cui devono essere ingeriti i dati.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-173">The table where the data should be ingested.</span></span>
<span data-ttu-id="8a2a1-174">Facoltativamente, le informazioni sulla tabella possono essere aggiunte a ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-174">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="8a2a1-175">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8a2a1-175">-Confirm</span></span>
<span data-ttu-id="8a2a1-176">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a2a1-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a2a1-177">-WhatIf</span></span>
<span data-ttu-id="8a2a1-178">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a2a1-179">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a2a1-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a2a1-180">CommonParameters</span></span>
<span data-ttu-id="8a2a1-181">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a2a1-182">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a2a1-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a2a1-183">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a2a1-183">INPUTS</span></span>

### <span data-ttu-id="8a2a1-184">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="8a2a1-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="8a2a1-185">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a2a1-185">OUTPUTS</span></span>

### <span data-ttu-id="8a2a1-186">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. IDataConnectionValidationResult</span><span class="sxs-lookup"><span data-stu-id="8a2a1-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnectionValidationResult</span></span>

## <span data-ttu-id="8a2a1-187">Note</span><span class="sxs-lookup"><span data-stu-id="8a2a1-187">NOTES</span></span>

<span data-ttu-id="8a2a1-188">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8a2a1-188">ALIASES</span></span>

<span data-ttu-id="8a2a1-189">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a2a1-189">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8a2a1-190">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-190">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a2a1-191">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8a2a1-192">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="8a2a1-192">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8a2a1-193">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-193">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="8a2a1-194">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-194">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="8a2a1-195">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-195">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="8a2a1-196">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-196">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="8a2a1-197">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="8a2a1-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8a2a1-198">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-198">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="8a2a1-199">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-199">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="8a2a1-200">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-200">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="8a2a1-201">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-201">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8a2a1-202">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="8a2a1-202">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8a2a1-203">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a2a1-203">RELATED LINKS</span></span>
