---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 53da56d932d3e2b57c2b2bbf17107918c9c1226d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195663"
---
# <span data-ttu-id="003cd-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="003cd-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="003cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="003cd-102">SYNOPSIS</span></span>
<span data-ttu-id="003cd-103">Questo comando crea un nuovo endpoint server in un server registrato.</span><span class="sxs-lookup"><span data-stu-id="003cd-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="003cd-104">In questo modo il percorso specificato nel server può avviare la sincronizzazione dei file con altri endpoint nel gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="003cd-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="003cd-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="003cd-105">SYNTAX</span></span>

### <span data-ttu-id="003cd-106">StringParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="003cd-106">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="003cd-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="003cd-107">ObjectParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="003cd-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="003cd-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="003cd-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="003cd-109">DESCRIPTION</span></span>
<span data-ttu-id="003cd-110">Questo comando crea un nuovo endpoint server in un server registrato.</span><span class="sxs-lookup"><span data-stu-id="003cd-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="003cd-111">In questo modo il percorso specificato nel server può avviare la sincronizzazione dei file con altri endpoint nel gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="003cd-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="003cd-112">Se sono già presenti file in altri endpoint nel gruppo di sincronizzazione e questa posizione appena aggiunta contiene anche file, un processo di riconciliazione tenterà di determinare se i file sono in realtà gli stessi nella stessa cartella degli altri endpoint.</span><span class="sxs-lookup"><span data-stu-id="003cd-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="003cd-113">Gli spazi dei nomi verranno uniti e la riconciliazione aiuta a prevenire i file in conflitto.</span><span class="sxs-lookup"><span data-stu-id="003cd-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="003cd-114">Se ci sono file su altri endpoint del server, spesso è meglio iniziare con una posizione vuota su questo server, in modo che i file dal cloud svolvano fino al server in un processo automatico chiamato ripristino di emergenza rapido.</span><span class="sxs-lookup"><span data-stu-id="003cd-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="003cd-115">I metadati dello spazio dei nomi verranno sincronizzati prima, quindi viene scaricato il flusso di dati di ogni file.</span><span class="sxs-lookup"><span data-stu-id="003cd-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="003cd-116">Se un file viene richiesto da un utente o un'applicazione non in ordine di download, verrà richiamato con la priorità per soddisfare la richiesta di accesso.</span><span class="sxs-lookup"><span data-stu-id="003cd-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="003cd-117">Se si desidera, è possibile usare la livelli del cloud in questo endpoint server per determinare se l'endpoint dovrebbe diventare una cache del set completo di file dal cloud.</span><span class="sxs-lookup"><span data-stu-id="003cd-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="003cd-118">Se si usa il livello del cloud, il download del contenuto dei file si interromperà in corrispondenza del punto definito dai criteri di livelli del cloud che è possibile impostare.</span><span class="sxs-lookup"><span data-stu-id="003cd-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="003cd-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="003cd-119">EXAMPLES</span></span>

### <span data-ttu-id="003cd-120">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="003cd-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="003cd-121">Questo comando crea un nuovo endpoint server in un server registrato e lo inserisce in un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="003cd-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="003cd-122">Così come fa parte di una topologia di altri endpoint, i metadati e il contenuto dei file inizieranno immediatamente a essere sincronizzati tra tutte le posizioni a cui viene fatto riferimento come endpoint nel gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="003cd-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="003cd-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="003cd-123">PARAMETERS</span></span>

### <span data-ttu-id="003cd-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="003cd-124">-AsJob</span></span>
<span data-ttu-id="003cd-125">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="003cd-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="003cd-126">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="003cd-126">-CloudTiering</span></span>
<span data-ttu-id="003cd-127">Parametro per il tiering del cloud</span><span class="sxs-lookup"><span data-stu-id="003cd-127">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="003cd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="003cd-128">-DefaultProfile</span></span>
<span data-ttu-id="003cd-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="003cd-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="003cd-130">-Name</span><span class="sxs-lookup"><span data-stu-id="003cd-130">-Name</span></span>
<span data-ttu-id="003cd-131">Nome di ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="003cd-131">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="003cd-132">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="003cd-132">-OfflineDataTransfer</span></span>
<span data-ttu-id="003cd-133">Parametro dati seeded cloud</span><span class="sxs-lookup"><span data-stu-id="003cd-133">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="003cd-134">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="003cd-134">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="003cd-135">Parametro URI condivisione file di dati seeded cloud</span><span class="sxs-lookup"><span data-stu-id="003cd-135">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="003cd-136">-initialDownloadPolicy</span><span class="sxs-lookup"><span data-stu-id="003cd-136">-initialDownloadPolicy</span></span>
<span data-ttu-id="003cd-137">Parametro della modalità cache locale</span><span class="sxs-lookup"><span data-stu-id="003cd-137">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="003cd-138">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="003cd-138">-localCacheMode</span></span>
<span data-ttu-id="003cd-139">Parametro della modalità cache locale</span><span class="sxs-lookup"><span data-stu-id="003cd-139">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="003cd-140">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="003cd-140">-ParentObject</span></span>
<span data-ttu-id="003cd-141">Oggetto SyncGroup, in genere passato attraverso il parametro.</span><span class="sxs-lookup"><span data-stu-id="003cd-141">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="003cd-142">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="003cd-142">-ParentResourceId</span></span>
<span data-ttu-id="003cd-143">ID risorsa padre SyncGroup</span><span class="sxs-lookup"><span data-stu-id="003cd-143">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="003cd-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="003cd-144">-ResourceGroupName</span></span>
<span data-ttu-id="003cd-145">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="003cd-145">Resource Group Name.</span></span>

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

### <span data-ttu-id="003cd-146">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="003cd-146">-ServerLocalPath</span></span>
<span data-ttu-id="003cd-147">Parametro del percorso locale del server</span><span class="sxs-lookup"><span data-stu-id="003cd-147">Server Local Path Parameter</span></span>

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

### <span data-ttu-id="003cd-148">-ServerResourceId</span><span class="sxs-lookup"><span data-stu-id="003cd-148">-ServerResourceId</span></span>
<span data-ttu-id="003cd-149">RegisteredServer Resource Id</span><span class="sxs-lookup"><span data-stu-id="003cd-149">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="003cd-150">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="003cd-150">-StorageSyncServiceName</span></span>
<span data-ttu-id="003cd-151">Nome di StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="003cd-151">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="003cd-152">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="003cd-152">-SyncGroupName</span></span>
<span data-ttu-id="003cd-153">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="003cd-153">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="003cd-154">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="003cd-154">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="003cd-155">Parametro per il livello dei file più vecchi dei giorni</span><span class="sxs-lookup"><span data-stu-id="003cd-155">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="003cd-156">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="003cd-156">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="003cd-157">Parametro per la percentuale di spazio libero volume</span><span class="sxs-lookup"><span data-stu-id="003cd-157">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="003cd-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="003cd-158">-Confirm</span></span>
<span data-ttu-id="003cd-159">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="003cd-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="003cd-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="003cd-160">-WhatIf</span></span>
<span data-ttu-id="003cd-161">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="003cd-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="003cd-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="003cd-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="003cd-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="003cd-163">CommonParameters</span></span>
<span data-ttu-id="003cd-164">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="003cd-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="003cd-165">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="003cd-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="003cd-166">INPUT</span><span class="sxs-lookup"><span data-stu-id="003cd-166">INPUTS</span></span>

### <span data-ttu-id="003cd-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="003cd-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="003cd-168">System.String</span><span class="sxs-lookup"><span data-stu-id="003cd-168">System.String</span></span>

## <span data-ttu-id="003cd-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="003cd-169">OUTPUTS</span></span>

### <span data-ttu-id="003cd-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="003cd-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="003cd-171">NOTE</span><span class="sxs-lookup"><span data-stu-id="003cd-171">NOTES</span></span>

## <span data-ttu-id="003cd-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="003cd-172">RELATED LINKS</span></span>
