---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 4581cfea88982eee4144730b92662374ec0a5790
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676445"
---
# <span data-ttu-id="07038-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="07038-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="07038-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07038-102">SYNOPSIS</span></span>
<span data-ttu-id="07038-103">Questo comando crea un nuovo endpoint server in un server registrato.</span><span class="sxs-lookup"><span data-stu-id="07038-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="07038-104">Questo consente al percorso specificato sul server di avviare la sincronizzazione dei file con altri endpoint nel gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="07038-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="07038-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07038-105">SYNTAX</span></span>

### <span data-ttu-id="07038-106">ObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="07038-106">ObjectParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07038-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="07038-107">StringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07038-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="07038-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07038-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07038-109">DESCRIPTION</span></span>
<span data-ttu-id="07038-110">Questo comando crea un nuovo endpoint server in un server registrato.</span><span class="sxs-lookup"><span data-stu-id="07038-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="07038-111">Questo consente al percorso specificato sul server di avviare la sincronizzazione dei file con altri endpoint nel gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="07038-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="07038-112">Se sono già presenti file in altri endpoint nel gruppo di sincronizzazione e questa posizione appena aggiunta contiene anche i file, un processo di riconciliazione tenterà di determinare se i file sono in realtà gli stessi nelle stesse cartelle di altri endpoint.</span><span class="sxs-lookup"><span data-stu-id="07038-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="07038-113">Gli spazi dei nomi verranno Uniti e la riconciliazione aiuta a prevenire i file di conflitto.</span><span class="sxs-lookup"><span data-stu-id="07038-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="07038-114">Se sono presenti file in altri endpoint del server, spesso è preferibile iniziare con una posizione vuota su questo server, in modo che i file dal cloud scendano nel server in un processo automatico denominato Fast Disaster Recovery.</span><span class="sxs-lookup"><span data-stu-id="07038-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="07038-115">I metadati dello spazio dei nomi verranno sincronizzati prima di tutto, quindi viene scaricato il flusso di dati di ogni file.</span><span class="sxs-lookup"><span data-stu-id="07038-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="07038-116">Se un file è richiesto da un utente o da un'applicazione fuori dall'ordine di download, il file verrà richiamato con priorità per soddisfare la richiesta di accesso.</span><span class="sxs-lookup"><span data-stu-id="07038-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="07038-117">Puoi facoltativamente usare il livello cloud su questo endpoint server per determinare se questo endpoint dovrebbe diventare una cache del set completo di file dal cloud.</span><span class="sxs-lookup"><span data-stu-id="07038-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="07038-118">Se viene usato il livello cloud, il download del contenuto del file verrà fermato nel punto definito dai criteri di livello cloud che è possibile impostare.</span><span class="sxs-lookup"><span data-stu-id="07038-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="07038-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07038-119">EXAMPLES</span></span>

### <span data-ttu-id="07038-120">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="07038-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="07038-121">Questo comando crea un nuovo endpoint server in un server registrato e lo inserisce in un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="07038-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="07038-122">In questo modo, fa parte di una topologia di altri endpoint e i metadati dei file e il contenuto inizieranno immediatamente la sincronizzazione tra tutte le posizioni a cui si fa riferimento come endpoint nel gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="07038-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="07038-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07038-123">PARAMETERS</span></span>

### <span data-ttu-id="07038-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07038-124">-AsJob</span></span>
<span data-ttu-id="07038-125">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="07038-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07038-126">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="07038-126">-OfflineDataTransfer</span></span>
<span data-ttu-id="07038-127">Parametro data seeded cloud</span><span class="sxs-lookup"><span data-stu-id="07038-127">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="07038-128">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="07038-128">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="07038-129">Parametro URI di condivisione file di dati con seeding cloud</span><span class="sxs-lookup"><span data-stu-id="07038-129">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="07038-130">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="07038-130">-CloudTiering</span></span>
<span data-ttu-id="07038-131">Parametro di livello cloud</span><span class="sxs-lookup"><span data-stu-id="07038-131">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="07038-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07038-132">-DefaultProfile</span></span>
<span data-ttu-id="07038-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07038-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07038-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="07038-134">-Name</span></span>
<span data-ttu-id="07038-135">Nome della ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="07038-135">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07038-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="07038-136">-ParentObject</span></span>
<span data-ttu-id="07038-137">Oggetto SyncGroup, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="07038-137">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07038-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="07038-138">-ParentResourceId</span></span>
<span data-ttu-id="07038-139">ID risorsa padre di SyncGroup</span><span class="sxs-lookup"><span data-stu-id="07038-139">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07038-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07038-140">-ResourceGroupName</span></span>
<span data-ttu-id="07038-141">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="07038-141">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07038-142">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="07038-142">-ServerLocalPath</span></span>
<span data-ttu-id="07038-143">Parametro percorso locale del server</span><span class="sxs-lookup"><span data-stu-id="07038-143">Server Local Path Parameter</span></span>

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

### <span data-ttu-id="07038-144">-ServerResourceId</span><span class="sxs-lookup"><span data-stu-id="07038-144">-ServerResourceId</span></span>
<span data-ttu-id="07038-145">ID risorsa RegisteredServer</span><span class="sxs-lookup"><span data-stu-id="07038-145">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="07038-146">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="07038-146">-StorageSyncServiceName</span></span>
<span data-ttu-id="07038-147">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="07038-147">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07038-148">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="07038-148">-SyncGroupName</span></span>
<span data-ttu-id="07038-149">Nome della SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="07038-149">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07038-150">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="07038-150">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="07038-151">I file di livello antecedente al parametro Days</span><span class="sxs-lookup"><span data-stu-id="07038-151">Tier Files Older Than Days Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07038-152">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="07038-152">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="07038-153">Parametro percentuale di spazio libero del volume</span><span class="sxs-lookup"><span data-stu-id="07038-153">Volume Free Space Percent Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07038-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07038-154">CommonParameters</span></span>
<span data-ttu-id="07038-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07038-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07038-156">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07038-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07038-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07038-157">INPUTS</span></span>

### <span data-ttu-id="07038-158">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="07038-158">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="07038-159">System. String</span><span class="sxs-lookup"><span data-stu-id="07038-159">System.String</span></span>

## <span data-ttu-id="07038-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07038-160">OUTPUTS</span></span>

### <span data-ttu-id="07038-161">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="07038-161">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="07038-162">Note</span><span class="sxs-lookup"><span data-stu-id="07038-162">NOTES</span></span>

## <span data-ttu-id="07038-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07038-163">RELATED LINKS</span></span>
