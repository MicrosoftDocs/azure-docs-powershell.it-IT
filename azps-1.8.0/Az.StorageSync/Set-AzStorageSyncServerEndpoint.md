---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 03b4ea18bc40f8ddd3a2dc2605427013c45d7506
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676428"
---
# <span data-ttu-id="12f1d-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="12f1d-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="12f1d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="12f1d-103">Questo comando consente di modificare i parametri regolabili di un endpoint server.</span><span class="sxs-lookup"><span data-stu-id="12f1d-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="12f1d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12f1d-104">SYNTAX</span></span>

### <span data-ttu-id="12f1d-105">ObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="12f1d-105">ObjectParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12f1d-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="12f1d-106">StringParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12f1d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12f1d-107">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12f1d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12f1d-108">DESCRIPTION</span></span>
<span data-ttu-id="12f1d-109">Questo comando consente di modificare i parametri regolabili di un endpoint server.</span><span class="sxs-lookup"><span data-stu-id="12f1d-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="12f1d-110">Per i criteri di tiering cloud di esempio e di livelli cloud, è possibile modificarli in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="12f1d-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="12f1d-111">Diversi aspetti di un endpoint server, ad esempio il percorso locale, non possono essere modificati dopo la creazione dell'endpoint del server.</span><span class="sxs-lookup"><span data-stu-id="12f1d-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="12f1d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12f1d-112">EXAMPLES</span></span>

### <span data-ttu-id="12f1d-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="12f1d-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="12f1d-114">Questo esempio esegue due azioni, imposta un nuovo criterio di livello cloud nell'endpoint server specificato, che indica al server di eseguire il Tier di tutti i file a cui non è stato eseguito l'accesso negli ultimi 30 giorni e disabilita anche la modalità di trasferimento dei dati offline, che inizialmente è stata abilitata nell'endpoint del server durante la creazione.</span><span class="sxs-lookup"><span data-stu-id="12f1d-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="12f1d-115">Il trasferimento dei dati offline viene usato come parte dell'interoperabilità con i servizi di migrazione in blocco, ad esempio Azure Data Box.</span><span class="sxs-lookup"><span data-stu-id="12f1d-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="12f1d-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12f1d-116">PARAMETERS</span></span>

### <span data-ttu-id="12f1d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12f1d-117">-AsJob</span></span>
<span data-ttu-id="12f1d-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="12f1d-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12f1d-119">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="12f1d-119">-OfflineDataTransfer</span></span>
<span data-ttu-id="12f1d-120">Parametro data seeded cloud</span><span class="sxs-lookup"><span data-stu-id="12f1d-120">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="12f1d-121">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="12f1d-121">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="12f1d-122">Parametro URI di condivisione file di dati con seeding cloud</span><span class="sxs-lookup"><span data-stu-id="12f1d-122">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="12f1d-123">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="12f1d-123">-CloudTiering</span></span>
<span data-ttu-id="12f1d-124">Parametro di livello cloud</span><span class="sxs-lookup"><span data-stu-id="12f1d-124">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="12f1d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12f1d-125">-DefaultProfile</span></span>
<span data-ttu-id="12f1d-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12f1d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12f1d-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12f1d-127">-InputObject</span></span>
<span data-ttu-id="12f1d-128">Oggetto SyncGroup, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="12f1d-128">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="12f1d-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="12f1d-129">-Name</span></span>
<span data-ttu-id="12f1d-130">Nome della ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="12f1d-130">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="12f1d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12f1d-131">-ResourceGroupName</span></span>
<span data-ttu-id="12f1d-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="12f1d-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="12f1d-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12f1d-133">-ResourceId</span></span>
<span data-ttu-id="12f1d-134">ID risorsa ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="12f1d-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="12f1d-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="12f1d-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="12f1d-136">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="12f1d-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="12f1d-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="12f1d-137">-SyncGroupName</span></span>
<span data-ttu-id="12f1d-138">Nome della SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="12f1d-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="12f1d-139">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="12f1d-139">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="12f1d-140">I file di livello antecedente al parametro Days</span><span class="sxs-lookup"><span data-stu-id="12f1d-140">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="12f1d-141">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="12f1d-141">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="12f1d-142">Parametro percentuale di spazio libero del volume</span><span class="sxs-lookup"><span data-stu-id="12f1d-142">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="12f1d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12f1d-143">CommonParameters</span></span>
<span data-ttu-id="12f1d-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12f1d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12f1d-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12f1d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12f1d-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12f1d-146">INPUTS</span></span>

### <span data-ttu-id="12f1d-147">System. String</span><span class="sxs-lookup"><span data-stu-id="12f1d-147">System.String</span></span>

### <span data-ttu-id="12f1d-148">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="12f1d-148">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="12f1d-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12f1d-149">OUTPUTS</span></span>

### <span data-ttu-id="12f1d-150">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="12f1d-150">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="12f1d-151">Note</span><span class="sxs-lookup"><span data-stu-id="12f1d-151">NOTES</span></span>

## <span data-ttu-id="12f1d-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12f1d-152">RELATED LINKS</span></span>
