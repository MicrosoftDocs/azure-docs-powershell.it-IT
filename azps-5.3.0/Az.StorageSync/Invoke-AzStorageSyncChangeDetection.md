---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: 9b7c539074f38b730a8ab5cd767a62fb44216ef6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474619"
---
# <span data-ttu-id="5926c-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="5926c-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="5926c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5926c-102">SYNOPSIS</span></span>
<span data-ttu-id="5926c-103">Questo comando può essere usato per avviare manualmente il rilevamento delle modifiche agli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="5926c-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="5926c-104">Può essere destinata all'intera condivisione, sottocartella o set di file.</span><span class="sxs-lookup"><span data-stu-id="5926c-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="5926c-105">Può essere rilevato un massimo di 10.000 elementi.</span><span class="sxs-lookup"><span data-stu-id="5926c-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="5926c-106">Se l'ambito delle modifiche è noto, limitare l'esecuzione di questo comando alle parti dello spazio dei nomi, in modo che il rilevamento della modifica possa terminare rapidamente e entro il limite degli elementi di 10.000.</span><span class="sxs-lookup"><span data-stu-id="5926c-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="5926c-107">Il cmdlet Invoke-AzStorageSyncChangeDetection non rileverà le modifiche seguenti nella condivisione file di Azure:</span><span class="sxs-lookup"><span data-stu-id="5926c-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect the following changes in the Azure file share:</span></span>
> - <span data-ttu-id="5926c-108">File eliminati.</span><span class="sxs-lookup"><span data-stu-id="5926c-108">Files that are deleted.</span></span> 
> - <span data-ttu-id="5926c-109">File spostati fuori dalla condivisione.</span><span class="sxs-lookup"><span data-stu-id="5926c-109">Files that are moved out of the share.</span></span>
> - <span data-ttu-id="5926c-110">File eliminati e creati con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="5926c-110">Files that are deleted and created with the same name.</span></span>  
> 
>  <span data-ttu-id="5926c-111">Queste modifiche verranno rilevate durante l'esecuzione del [processo di rilevamento delle modifiche](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) .</span><span class="sxs-lookup"><span data-stu-id="5926c-111">These changes will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) runs.</span></span>

## <span data-ttu-id="5926c-112">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5926c-112">SYNTAX</span></span>

### <span data-ttu-id="5926c-113">StringAndDirectoryParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5926c-113">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5926c-114">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="5926c-114">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5926c-115">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="5926c-115">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5926c-116">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="5926c-116">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5926c-117">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="5926c-117">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5926c-118">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="5926c-118">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5926c-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5926c-119">DESCRIPTION</span></span>
<span data-ttu-id="5926c-120">Periodicamente, in Azure file Sync viene controllato lo spazio dei nomi all'interno di una condivisione file di Azure di sincronizzazione per le modifiche apportate alla condivisione file con altri mezzi rispetto alla sincronizzazione. L'obiettivo è identificare queste modifiche e infine sincronizzarle con i server connessi.</span><span class="sxs-lookup"><span data-stu-id="5926c-120">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="5926c-121">Questo comando può essere usato per avviare manualmente il rilevamento delle modifiche agli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="5926c-121">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="5926c-122">Può essere destinata all'intera condivisione, sottocartella o set di file.</span><span class="sxs-lookup"><span data-stu-id="5926c-122">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="5926c-123">Se l'ambito delle modifiche è noto, limitare l'esecuzione di questo comando alle parti dello spazio dei nomi, in modo che il rilevamento della modifica possa terminare rapidamente e entro il limite degli elementi di 10.000.</span><span class="sxs-lookup"><span data-stu-id="5926c-123">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 items limit.</span></span>

## <span data-ttu-id="5926c-124">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5926c-124">EXAMPLES</span></span>

### <span data-ttu-id="5926c-125">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5926c-125">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="5926c-126">In questo esempio, il rilevamento delle modifiche viene eseguito nelle directory "data" e "Reporting\Templates" di una condivisione file di Azure di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="5926c-126">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="5926c-127">Tutti i percorsi sono relativi alla radice dello spazio dei nomi di condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="5926c-127">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="5926c-128">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5926c-128">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="5926c-129">In questo esempio, il rilevamento delle modifiche viene eseguito per un set di file noti al chiamante del comando per essere stati modificati.</span><span class="sxs-lookup"><span data-stu-id="5926c-129">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="5926c-130">L'obiettivo è quello di rilevare e sincronizzare anche le modifiche di Azure file Sync.</span><span class="sxs-lookup"><span data-stu-id="5926c-130">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="5926c-131">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="5926c-131">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="5926c-132">In questo esempio viene eseguito il rilevamento delle modifiche per la directory "examples" e verranno rilevate le modifiche ricorsive nelle sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="5926c-132">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="5926c-133">Tieni presente che il cmdlet avrà esito negativo se il percorso contiene più di 10.000 elementi.</span><span class="sxs-lookup"><span data-stu-id="5926c-133">Keep in mind the cmdlet will fail if the path contains more than 10,000 items.</span></span> <span data-ttu-id="5926c-134">Se il percorso contiene più di 10.000 elementi, eseguire il comando in sezioni secondarie dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="5926c-134">If the path contains more than 10,000 items, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="5926c-135">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5926c-135">PARAMETERS</span></span>

### <span data-ttu-id="5926c-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5926c-136">-AsJob</span></span>
<span data-ttu-id="5926c-137">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5926c-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5926c-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5926c-138">-DefaultProfile</span></span>
<span data-ttu-id="5926c-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5926c-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5926c-140">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="5926c-140">-DirectoryPath</span></span>
<span data-ttu-id="5926c-141">Directory in cui verrà eseguito il rilevamento delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="5926c-141">Directory where change detection will be performed.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5926c-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5926c-142">-InputObject</span></span>
<span data-ttu-id="5926c-143">Oggetto CloudEndpoint, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="5926c-143">CloudEndpoint Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: ObjectAndDirectoryParameterSet, ObjectAndPathParameterSet
Aliases: CloudEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5926c-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="5926c-144">-Name</span></span>
<span data-ttu-id="5926c-145">Nome della CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5926c-145">Name of the CloudEndpoint.</span></span> <span data-ttu-id="5926c-146">Il nome è un GUID, non il nome descrittivo visualizzato nel portale.</span><span class="sxs-lookup"><span data-stu-id="5926c-146">The name is a GUID, not the friendly name that's displayed in the portal.</span></span> <span data-ttu-id="5926c-147">Per ottenere il CloudEndpointName, usa il cmdlet Get-AzStorageSyncCloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5926c-147">To get the CloudEndpointName, use the Get-AzStorageSyncCloudEndpoint cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5926c-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5926c-148">-PassThru</span></span>
<span data-ttu-id="5926c-149">In esecuzione normale, questo cmdlet non restituisce alcun valore per l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5926c-149">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="5926c-150">Se fornisci il parametro PassThru, il cmdlet scriverà un valore nella pipeline dopo l'esecuzione corretta.</span><span class="sxs-lookup"><span data-stu-id="5926c-150">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="5926c-151">-Path</span><span class="sxs-lookup"><span data-stu-id="5926c-151">-Path</span></span>
<span data-ttu-id="5926c-152">Percorso in cui verrà eseguito il rilevamento delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="5926c-152">Path where change detection will be performed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: StringAndPathParameterSet, ResourceIdAndPathParameterSet, ObjectAndPathParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5926c-153">-Ricorsiva</span><span class="sxs-lookup"><span data-stu-id="5926c-153">-Recursive</span></span>
<span data-ttu-id="5926c-154">Indica se il rilevamento delle modifiche della directory è ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="5926c-154">Indication whether directory change detection is recursive.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5926c-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5926c-155">-ResourceGroupName</span></span>
<span data-ttu-id="5926c-156">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5926c-156">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5926c-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5926c-157">-ResourceId</span></span>
<span data-ttu-id="5926c-158">ID risorsa CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="5926c-158">CloudEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdAndDirectoryParameterSet, ResourceIdAndPathParameterSet
Aliases: CloudEndpointId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5926c-159">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="5926c-159">-StorageSyncServiceName</span></span>
<span data-ttu-id="5926c-160">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="5926c-160">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5926c-161">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="5926c-161">-SyncGroupName</span></span>
<span data-ttu-id="5926c-162">Nome della SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="5926c-162">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5926c-163">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5926c-163">-Confirm</span></span>
<span data-ttu-id="5926c-164">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5926c-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5926c-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5926c-165">-WhatIf</span></span>
<span data-ttu-id="5926c-166">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5926c-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5926c-167">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5926c-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5926c-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5926c-168">CommonParameters</span></span>
<span data-ttu-id="5926c-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5926c-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5926c-170">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5926c-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5926c-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5926c-171">INPUTS</span></span>

### <span data-ttu-id="5926c-172">System. String</span><span class="sxs-lookup"><span data-stu-id="5926c-172">System.String</span></span>

### <span data-ttu-id="5926c-173">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5926c-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="5926c-174">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5926c-174">OUTPUTS</span></span>

### <span data-ttu-id="5926c-175">System. void</span><span class="sxs-lookup"><span data-stu-id="5926c-175">System.Void</span></span>

## <span data-ttu-id="5926c-176">Note</span><span class="sxs-lookup"><span data-stu-id="5926c-176">NOTES</span></span>

## <span data-ttu-id="5926c-177">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5926c-177">RELATED LINKS</span></span>
