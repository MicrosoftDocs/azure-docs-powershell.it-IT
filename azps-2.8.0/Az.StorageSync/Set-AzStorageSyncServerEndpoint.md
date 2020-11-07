---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 23aab4561e8127c67be4d9f751b250bc3fb6d1a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855034"
---
# <span data-ttu-id="4fd1d-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4fd1d-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="4fd1d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4fd1d-102">SYNOPSIS</span></span>
<span data-ttu-id="4fd1d-103">Questo comando consente di modificare i parametri regolabili di un endpoint server.</span><span class="sxs-lookup"><span data-stu-id="4fd1d-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="4fd1d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4fd1d-104">SYNTAX</span></span>

### <span data-ttu-id="4fd1d-105">StringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4fd1d-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fd1d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fd1d-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fd1d-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fd1d-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fd1d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fd1d-108">DESCRIPTION</span></span>
<span data-ttu-id="4fd1d-109">Questo comando consente di modificare i parametri regolabili di un endpoint server.</span><span class="sxs-lookup"><span data-stu-id="4fd1d-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="4fd1d-110">Per i criteri di tiering cloud di esempio e di livelli cloud, è possibile modificarli in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="4fd1d-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="4fd1d-111">Diversi aspetti di un endpoint server, ad esempio il percorso locale, non possono essere modificati dopo la creazione dell'endpoint del server.</span><span class="sxs-lookup"><span data-stu-id="4fd1d-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="4fd1d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4fd1d-112">EXAMPLES</span></span>

### <span data-ttu-id="4fd1d-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4fd1d-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="4fd1d-114">Questo esempio esegue due azioni, imposta un nuovo criterio di livello cloud nell'endpoint server specificato, che indica al server di eseguire il Tier di tutti i file a cui non è stato eseguito l'accesso negli ultimi 30 giorni e disabilita anche la modalità di trasferimento dei dati offline, che inizialmente è stata abilitata nell'endpoint del server durante la creazione.</span><span class="sxs-lookup"><span data-stu-id="4fd1d-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="4fd1d-115">Il trasferimento dei dati offline viene usato come parte dell'interoperabilità con i servizi di migrazione in blocco, ad esempio Azure Data Box.</span><span class="sxs-lookup"><span data-stu-id="4fd1d-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="4fd1d-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4fd1d-116">PARAMETERS</span></span>

### <span data-ttu-id="4fd1d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fd1d-117">-AsJob</span></span>
<span data-ttu-id="4fd1d-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4fd1d-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4fd1d-119">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="4fd1d-119">-CloudTiering</span></span>
<span data-ttu-id="4fd1d-120">Parametro di livello cloud</span><span class="sxs-lookup"><span data-stu-id="4fd1d-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="4fd1d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fd1d-121">-DefaultProfile</span></span>
<span data-ttu-id="4fd1d-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4fd1d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fd1d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fd1d-123">-InputObject</span></span>
<span data-ttu-id="4fd1d-124">Oggetto SyncGroup, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="4fd1d-124">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="4fd1d-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="4fd1d-125">-Name</span></span>
<span data-ttu-id="4fd1d-126">Nome della ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4fd1d-126">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="4fd1d-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="4fd1d-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="4fd1d-128">Parametro data seeded cloud</span><span class="sxs-lookup"><span data-stu-id="4fd1d-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="4fd1d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fd1d-129">-ResourceGroupName</span></span>
<span data-ttu-id="4fd1d-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4fd1d-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="4fd1d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fd1d-131">-ResourceId</span></span>
<span data-ttu-id="4fd1d-132">ID risorsa ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4fd1d-132">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="4fd1d-133">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="4fd1d-133">-StorageSyncServiceName</span></span>
<span data-ttu-id="4fd1d-134">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="4fd1d-134">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="4fd1d-135">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4fd1d-135">-SyncGroupName</span></span>
<span data-ttu-id="4fd1d-136">Nome della SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="4fd1d-136">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="4fd1d-137">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="4fd1d-137">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="4fd1d-138">I file di livello antecedente al parametro Days</span><span class="sxs-lookup"><span data-stu-id="4fd1d-138">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="4fd1d-139">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="4fd1d-139">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="4fd1d-140">Parametro percentuale di spazio libero del volume</span><span class="sxs-lookup"><span data-stu-id="4fd1d-140">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="4fd1d-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4fd1d-141">-Confirm</span></span>
<span data-ttu-id="4fd1d-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fd1d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fd1d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fd1d-143">-WhatIf</span></span>
<span data-ttu-id="4fd1d-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4fd1d-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4fd1d-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4fd1d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fd1d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fd1d-146">CommonParameters</span></span>
<span data-ttu-id="4fd1d-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fd1d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fd1d-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fd1d-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fd1d-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4fd1d-149">INPUTS</span></span>

### <span data-ttu-id="4fd1d-150">System. String</span><span class="sxs-lookup"><span data-stu-id="4fd1d-150">System.String</span></span>

### <span data-ttu-id="4fd1d-151">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4fd1d-151">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="4fd1d-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4fd1d-152">OUTPUTS</span></span>

### <span data-ttu-id="4fd1d-153">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4fd1d-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="4fd1d-154">Note</span><span class="sxs-lookup"><span data-stu-id="4fd1d-154">NOTES</span></span>

## <span data-ttu-id="4fd1d-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4fd1d-155">RELATED LINKS</span></span>
