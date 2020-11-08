---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: b8adfd7c069c4215ec8f26d259ed9d1bc39be2d9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033616"
---
# <span data-ttu-id="added-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="added-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="added-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="added-102">SYNOPSIS</span></span>
<span data-ttu-id="added-103">Questo comando consente di modificare i parametri regolabili di un endpoint server.</span><span class="sxs-lookup"><span data-stu-id="added-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="added-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="added-104">SYNTAX</span></span>

### <span data-ttu-id="added-105">StringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="added-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="added-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="added-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="added-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="added-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="added-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="added-108">DESCRIPTION</span></span>
<span data-ttu-id="added-109">Questo comando consente di modificare i parametri regolabili di un endpoint server.</span><span class="sxs-lookup"><span data-stu-id="added-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="added-110">Per i criteri di tiering cloud di esempio e di livelli cloud, è possibile modificarli in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="added-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="added-111">Diversi aspetti di un endpoint server, ad esempio il percorso locale, non possono essere modificati dopo la creazione dell'endpoint del server.</span><span class="sxs-lookup"><span data-stu-id="added-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="added-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="added-112">EXAMPLES</span></span>

### <span data-ttu-id="added-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="added-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="added-114">Questo esempio esegue due azioni, imposta un nuovo criterio di livello cloud nell'endpoint server specificato, che indica al server di eseguire il Tier di tutti i file a cui non è stato eseguito l'accesso negli ultimi 30 giorni e disabilita anche la modalità di trasferimento dei dati offline, che inizialmente è stata abilitata nell'endpoint del server durante la creazione.</span><span class="sxs-lookup"><span data-stu-id="added-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="added-115">Il trasferimento dei dati offline viene usato come parte dell'interoperabilità con i servizi di migrazione in blocco, ad esempio Azure Data Box.</span><span class="sxs-lookup"><span data-stu-id="added-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="added-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="added-116">PARAMETERS</span></span>

### <span data-ttu-id="added-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="added-117">-AsJob</span></span>
<span data-ttu-id="added-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="added-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="added-119">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="added-119">-CloudTiering</span></span>
<span data-ttu-id="added-120">Parametro di livello cloud</span><span class="sxs-lookup"><span data-stu-id="added-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="added-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="added-121">-DefaultProfile</span></span>
<span data-ttu-id="added-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="added-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="added-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="added-123">-InputObject</span></span>
<span data-ttu-id="added-124">Oggetto SyncGroup, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="added-124">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="added-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="added-125">-Name</span></span>
<span data-ttu-id="added-126">Nome della ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="added-126">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="added-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="added-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="added-128">Parametro data seeded cloud</span><span class="sxs-lookup"><span data-stu-id="added-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="added-129">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="added-129">-localCacheMode</span></span>
<span data-ttu-id="added-130">Parametro della modalità cache locale</span><span class="sxs-lookup"><span data-stu-id="added-130">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="added-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="added-131">-ResourceGroupName</span></span>
<span data-ttu-id="added-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="added-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="added-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="added-133">-ResourceId</span></span>
<span data-ttu-id="added-134">ID risorsa ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="added-134">ServerEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="added-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="added-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="added-136">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="added-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="added-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="added-137">-SyncGroupName</span></span>
<span data-ttu-id="added-138">Nome della SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="added-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="added-139">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="added-139">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="added-140">I file di livello antecedente al parametro Days</span><span class="sxs-lookup"><span data-stu-id="added-140">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="added-141">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="added-141">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="added-142">Parametro percentuale di spazio libero del volume</span><span class="sxs-lookup"><span data-stu-id="added-142">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="added-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="added-143">-Confirm</span></span>
<span data-ttu-id="added-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="added-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="added-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="added-145">-WhatIf</span></span>
<span data-ttu-id="added-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="added-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="added-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="added-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="added-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="added-148">CommonParameters</span></span>
<span data-ttu-id="added-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="added-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="added-150">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="added-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="added-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="added-151">INPUTS</span></span>

### <span data-ttu-id="added-152">System. String</span><span class="sxs-lookup"><span data-stu-id="added-152">System.String</span></span>

### <span data-ttu-id="added-153">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="added-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="added-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="added-154">OUTPUTS</span></span>

### <span data-ttu-id="added-155">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="added-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="added-156">Note</span><span class="sxs-lookup"><span data-stu-id="added-156">NOTES</span></span>

## <span data-ttu-id="added-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="added-157">RELATED LINKS</span></span>
