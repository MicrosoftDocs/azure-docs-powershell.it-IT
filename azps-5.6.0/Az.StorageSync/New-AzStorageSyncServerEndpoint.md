---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: c76fd37e0a95c6ea5c39897c617602106979f94a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011389"
---
# <span data-ttu-id="bfcd2-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfcd2-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="bfcd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfcd2-102">SYNOPSIS</span></span>
<span data-ttu-id="bfcd2-103">Questo comando crea un nuovo endpoint server in un server registrato.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="bfcd2-104">In questo modo il percorso specificato nel server può avviare la sincronizzazione dei file con altri endpoint nel gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="bfcd2-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bfcd2-105">SYNTAX</span></span>

### <span data-ttu-id="bfcd2-106">StringParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="bfcd2-106">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfcd2-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfcd2-107">ObjectParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfcd2-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfcd2-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfcd2-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bfcd2-109">DESCRIPTION</span></span>
<span data-ttu-id="bfcd2-110">Questo comando crea un nuovo endpoint server in un server registrato.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="bfcd2-111">In questo modo il percorso specificato nel server può avviare la sincronizzazione dei file con altri endpoint nel gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="bfcd2-112">Se sono già presenti file in altri endpoint nel gruppo di sincronizzazione e questa posizione appena aggiunta contiene anche file, un processo di riconciliazione tenterà di determinare se i file sono in realtà gli stessi nella stessa cartella degli altri endpoint.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="bfcd2-113">Gli spazi dei nomi verranno uniti e la riconciliazione aiuta a prevenire i file in conflitto.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="bfcd2-114">Se ci sono file su altri endpoint del server, spesso è meglio iniziare con una posizione vuota su questo server, in modo che i file dal cloud svolvano fino al server in un processo automatico chiamato ripristino di emergenza rapido.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="bfcd2-115">I metadati dello spazio dei nomi verranno sincronizzati prima, quindi viene scaricato il flusso di dati di ogni file.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="bfcd2-116">Se un file viene richiesto da un utente o un'applicazione non in ordine di download, verrà richiamato con la priorità per soddisfare la richiesta di accesso.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="bfcd2-117">Se si desidera, è possibile usare il livello del cloud in questo endpoint server per determinare se l'endpoint dovrebbe diventare una cache del set completo di file dal cloud.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="bfcd2-118">Se si usa il livello del cloud, il download del contenuto dei file si interromperà in corrispondenza del punto definito dai criteri di livelli del cloud che è possibile impostare.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="bfcd2-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bfcd2-119">EXAMPLES</span></span>

### <span data-ttu-id="bfcd2-120">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bfcd2-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="bfcd2-121">Questo comando crea un nuovo endpoint server in un server registrato e lo inserisce in un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="bfcd2-122">Così come fa parte di una topologia di altri endpoint, i metadati e il contenuto dei file inizieranno immediatamente a essere sincronizzati tra tutte le posizioni a cui viene fatto riferimento come endpoint nel gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="bfcd2-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfcd2-123">PARAMETERS</span></span>

### <span data-ttu-id="bfcd2-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bfcd2-124">-AsJob</span></span>
<span data-ttu-id="bfcd2-125">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="bfcd2-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bfcd2-126">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="bfcd2-126">-CloudTiering</span></span>
<span data-ttu-id="bfcd2-127">Parametro per il tiering del cloud</span><span class="sxs-lookup"><span data-stu-id="bfcd2-127">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="bfcd2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfcd2-128">-DefaultProfile</span></span>
<span data-ttu-id="bfcd2-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcd2-130">-Name</span><span class="sxs-lookup"><span data-stu-id="bfcd2-130">-Name</span></span>
<span data-ttu-id="bfcd2-131">Nome di ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-131">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="bfcd2-132">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="bfcd2-132">-OfflineDataTransfer</span></span>
<span data-ttu-id="bfcd2-133">Parametro dati seeded cloud</span><span class="sxs-lookup"><span data-stu-id="bfcd2-133">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="bfcd2-134">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="bfcd2-134">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="bfcd2-135">Parametro URI condivisione file di dati seeded cloud</span><span class="sxs-lookup"><span data-stu-id="bfcd2-135">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="bfcd2-136">-initialDownloadPolicy</span><span class="sxs-lookup"><span data-stu-id="bfcd2-136">-initialDownloadPolicy</span></span>
<span data-ttu-id="bfcd2-137">Parametro della modalità cache locale</span><span class="sxs-lookup"><span data-stu-id="bfcd2-137">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="bfcd2-138">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="bfcd2-138">-localCacheMode</span></span>
<span data-ttu-id="bfcd2-139">Parametro della modalità cache locale</span><span class="sxs-lookup"><span data-stu-id="bfcd2-139">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="bfcd2-140">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bfcd2-140">-ParentObject</span></span>
<span data-ttu-id="bfcd2-141">Oggetto SyncGroup, in genere passato attraverso il parametro.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-141">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="bfcd2-142">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="bfcd2-142">-ParentResourceId</span></span>
<span data-ttu-id="bfcd2-143">ID risorsa padre SyncGroup</span><span class="sxs-lookup"><span data-stu-id="bfcd2-143">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="bfcd2-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfcd2-144">-ResourceGroupName</span></span>
<span data-ttu-id="bfcd2-145">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-145">Resource Group Name.</span></span>

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

### <span data-ttu-id="bfcd2-146">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="bfcd2-146">-ServerLocalPath</span></span>
<span data-ttu-id="bfcd2-147">Parametro del percorso locale del server</span><span class="sxs-lookup"><span data-stu-id="bfcd2-147">Server Local Path Parameter</span></span>

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

### <span data-ttu-id="bfcd2-148">-ServerResourceId</span><span class="sxs-lookup"><span data-stu-id="bfcd2-148">-ServerResourceId</span></span>
<span data-ttu-id="bfcd2-149">RegisteredServer Resource Id</span><span class="sxs-lookup"><span data-stu-id="bfcd2-149">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="bfcd2-150">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="bfcd2-150">-StorageSyncServiceName</span></span>
<span data-ttu-id="bfcd2-151">Nome di StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-151">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="bfcd2-152">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="bfcd2-152">-SyncGroupName</span></span>
<span data-ttu-id="bfcd2-153">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-153">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="bfcd2-154">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="bfcd2-154">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="bfcd2-155">Parametro livello file più vecchi di giorni</span><span class="sxs-lookup"><span data-stu-id="bfcd2-155">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="bfcd2-156">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="bfcd2-156">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="bfcd2-157">Parametro per la percentuale di spazio libero volume</span><span class="sxs-lookup"><span data-stu-id="bfcd2-157">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="bfcd2-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfcd2-158">-Confirm</span></span>
<span data-ttu-id="bfcd2-159">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfcd2-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfcd2-160">-WhatIf</span></span>
<span data-ttu-id="bfcd2-161">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bfcd2-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfcd2-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfcd2-163">CommonParameters</span></span>
<span data-ttu-id="bfcd2-164">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfcd2-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfcd2-165">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfcd2-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfcd2-166">INPUT</span><span class="sxs-lookup"><span data-stu-id="bfcd2-166">INPUTS</span></span>

### <span data-ttu-id="bfcd2-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="bfcd2-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="bfcd2-168">System.String</span><span class="sxs-lookup"><span data-stu-id="bfcd2-168">System.String</span></span>

## <span data-ttu-id="bfcd2-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bfcd2-169">OUTPUTS</span></span>

### <span data-ttu-id="bfcd2-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfcd2-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="bfcd2-171">NOTE</span><span class="sxs-lookup"><span data-stu-id="bfcd2-171">NOTES</span></span>

## <span data-ttu-id="bfcd2-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bfcd2-172">RELATED LINKS</span></span>
