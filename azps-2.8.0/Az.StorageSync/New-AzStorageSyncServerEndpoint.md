---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 524e9334b3e706dc51a2dfd4efc5d6f3cce710c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858333"
---
# <span data-ttu-id="f0537-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f0537-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="f0537-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f0537-102">SYNOPSIS</span></span>
<span data-ttu-id="f0537-103">Questo comando crea un nuovo endpoint server in un server registrato.</span><span class="sxs-lookup"><span data-stu-id="f0537-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="f0537-104">Questo consente al percorso specificato sul server di avviare la sincronizzazione dei file con altri endpoint nel gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="f0537-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="f0537-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0537-105">SYNTAX</span></span>

### <span data-ttu-id="f0537-106">StringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f0537-106">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0537-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0537-107">ObjectParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0537-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0537-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0537-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0537-109">DESCRIPTION</span></span>
<span data-ttu-id="f0537-110">Questo comando crea un nuovo endpoint server in un server registrato.</span><span class="sxs-lookup"><span data-stu-id="f0537-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="f0537-111">Questo consente al percorso specificato sul server di avviare la sincronizzazione dei file con altri endpoint nel gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="f0537-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="f0537-112">Se sono già presenti file in altri endpoint nel gruppo di sincronizzazione e questa posizione appena aggiunta contiene anche i file, un processo di riconciliazione tenterà di determinare se i file sono in realtà gli stessi nelle stesse cartelle di altri endpoint.</span><span class="sxs-lookup"><span data-stu-id="f0537-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="f0537-113">Gli spazi dei nomi verranno Uniti e la riconciliazione aiuta a prevenire i file di conflitto.</span><span class="sxs-lookup"><span data-stu-id="f0537-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="f0537-114">Se sono presenti file in altri endpoint del server, spesso è preferibile iniziare con una posizione vuota su questo server, in modo che i file dal cloud scendano nel server in un processo automatico denominato Fast Disaster Recovery.</span><span class="sxs-lookup"><span data-stu-id="f0537-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="f0537-115">I metadati dello spazio dei nomi verranno sincronizzati prima di tutto, quindi viene scaricato il flusso di dati di ogni file.</span><span class="sxs-lookup"><span data-stu-id="f0537-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="f0537-116">Se un file è richiesto da un utente o da un'applicazione fuori dall'ordine di download, il file verrà richiamato con priorità per soddisfare la richiesta di accesso.</span><span class="sxs-lookup"><span data-stu-id="f0537-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="f0537-117">Puoi facoltativamente usare il livello cloud su questo endpoint server per determinare se questo endpoint dovrebbe diventare una cache del set completo di file dal cloud.</span><span class="sxs-lookup"><span data-stu-id="f0537-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="f0537-118">Se viene usato il livello cloud, il download del contenuto del file verrà fermato nel punto definito dai criteri di livello cloud che è possibile impostare.</span><span class="sxs-lookup"><span data-stu-id="f0537-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="f0537-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0537-119">EXAMPLES</span></span>

### <span data-ttu-id="f0537-120">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f0537-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="f0537-121">Questo comando crea un nuovo endpoint server in un server registrato e lo inserisce in un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="f0537-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="f0537-122">In questo modo, fa parte di una topologia di altri endpoint e i metadati dei file e il contenuto inizieranno immediatamente la sincronizzazione tra tutte le posizioni a cui si fa riferimento come endpoint nel gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="f0537-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="f0537-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f0537-123">PARAMETERS</span></span>

### <span data-ttu-id="f0537-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0537-124">-AsJob</span></span>
<span data-ttu-id="f0537-125">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f0537-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0537-126">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="f0537-126">-CloudTiering</span></span>
<span data-ttu-id="f0537-127">Parametro di livello cloud</span><span class="sxs-lookup"><span data-stu-id="f0537-127">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="f0537-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0537-128">-DefaultProfile</span></span>
<span data-ttu-id="f0537-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f0537-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0537-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0537-130">-Name</span></span>
<span data-ttu-id="f0537-131">Nome della ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f0537-131">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="f0537-132">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="f0537-132">-OfflineDataTransfer</span></span>
<span data-ttu-id="f0537-133">Parametro data seeded cloud</span><span class="sxs-lookup"><span data-stu-id="f0537-133">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="f0537-134">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="f0537-134">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="f0537-135">Parametro URI di condivisione file di dati con seeding cloud</span><span class="sxs-lookup"><span data-stu-id="f0537-135">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="f0537-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f0537-136">-ParentObject</span></span>
<span data-ttu-id="f0537-137">Oggetto SyncGroup, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="f0537-137">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="f0537-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f0537-138">-ParentResourceId</span></span>
<span data-ttu-id="f0537-139">ID risorsa padre di SyncGroup</span><span class="sxs-lookup"><span data-stu-id="f0537-139">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="f0537-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0537-140">-ResourceGroupName</span></span>
<span data-ttu-id="f0537-141">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f0537-141">Resource Group Name.</span></span>

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

### <span data-ttu-id="f0537-142">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="f0537-142">-ServerLocalPath</span></span>
<span data-ttu-id="f0537-143">Parametro percorso locale del server</span><span class="sxs-lookup"><span data-stu-id="f0537-143">Server Local Path Parameter</span></span>

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

### <span data-ttu-id="f0537-144">-ServerResourceId</span><span class="sxs-lookup"><span data-stu-id="f0537-144">-ServerResourceId</span></span>
<span data-ttu-id="f0537-145">ID risorsa RegisteredServer</span><span class="sxs-lookup"><span data-stu-id="f0537-145">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="f0537-146">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="f0537-146">-StorageSyncServiceName</span></span>
<span data-ttu-id="f0537-147">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="f0537-147">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="f0537-148">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="f0537-148">-SyncGroupName</span></span>
<span data-ttu-id="f0537-149">Nome della SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="f0537-149">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="f0537-150">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="f0537-150">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="f0537-151">I file di livello antecedente al parametro Days</span><span class="sxs-lookup"><span data-stu-id="f0537-151">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="f0537-152">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="f0537-152">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="f0537-153">Parametro percentuale di spazio libero del volume</span><span class="sxs-lookup"><span data-stu-id="f0537-153">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="f0537-154">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f0537-154">-Confirm</span></span>
<span data-ttu-id="f0537-155">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0537-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0537-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0537-156">-WhatIf</span></span>
<span data-ttu-id="f0537-157">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0537-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0537-158">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0537-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0537-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0537-159">CommonParameters</span></span>
<span data-ttu-id="f0537-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0537-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0537-161">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0537-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0537-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f0537-162">INPUTS</span></span>

### <span data-ttu-id="f0537-163">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f0537-163">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="f0537-164">System. String</span><span class="sxs-lookup"><span data-stu-id="f0537-164">System.String</span></span>

## <span data-ttu-id="f0537-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0537-165">OUTPUTS</span></span>

### <span data-ttu-id="f0537-166">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f0537-166">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="f0537-167">Note</span><span class="sxs-lookup"><span data-stu-id="f0537-167">NOTES</span></span>

## <span data-ttu-id="f0537-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0537-168">RELATED LINKS</span></span>
