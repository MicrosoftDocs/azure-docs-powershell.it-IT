---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: d55ffe30554c70b9d7b8fa1ed90380c6a5b181cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011422"
---
# <span data-ttu-id="00854-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="00854-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="00854-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00854-102">SYNOPSIS</span></span>
<span data-ttu-id="00854-103">Questo comando può essere usato per avviare manualmente il rilevamento delle modifiche agli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="00854-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="00854-104">Può essere indirizzato all'intera condivisione, sottocartella o set di file.</span><span class="sxs-lookup"><span data-stu-id="00854-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="00854-105">È possibile trovare un massimo di 10.000 elementi.</span><span class="sxs-lookup"><span data-stu-id="00854-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="00854-106">Se si conosce l'ambito delle modifiche, limitare l'esecuzione di questo comando a parti dello spazio dei nomi, in modo che il rilevamento delle modifiche finisca rapidamente e entro il limite di 10.000 elementi.</span><span class="sxs-lookup"><span data-stu-id="00854-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="00854-107">Il cmdlet Invoke-AzStorageSyncChangeDetection non rileva le modifiche seguenti nella condivisione file di Azure:</span><span class="sxs-lookup"><span data-stu-id="00854-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect the following changes in the Azure file share:</span></span>
> - <span data-ttu-id="00854-108">File eliminati.</span><span class="sxs-lookup"><span data-stu-id="00854-108">Files that are deleted.</span></span> 
> - <span data-ttu-id="00854-109">File spostati dalla condivisione.</span><span class="sxs-lookup"><span data-stu-id="00854-109">Files that are moved out of the share.</span></span>
> - <span data-ttu-id="00854-110">File eliminati e creati con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="00854-110">Files that are deleted and created with the same name.</span></span>  
> 
>  <span data-ttu-id="00854-111">Queste modifiche verranno rilevate durante [l'esecuzione del processo di rilevamento delle](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) modifiche.</span><span class="sxs-lookup"><span data-stu-id="00854-111">These changes will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) runs.</span></span>

## <span data-ttu-id="00854-112">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00854-112">SYNTAX</span></span>

### <span data-ttu-id="00854-113">StringAndDirectoryParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="00854-113">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00854-114">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="00854-114">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00854-115">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="00854-115">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00854-116">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="00854-116">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00854-117">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="00854-117">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00854-118">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="00854-118">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00854-119">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="00854-119">DESCRIPTION</span></span>
<span data-ttu-id="00854-120">Periodicamente, Azure File Sync controlla lo spazio dei nomi all'interno di una condivisione file di Azure sincronizzata per verificare la presenza di modifiche apportate alla condivisione file con altri mezzi rispetto alla sincronizzazione. L'obiettivo è identificare queste modifiche e in ultima analisi sincronizzarle con i server connessi.</span><span class="sxs-lookup"><span data-stu-id="00854-120">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="00854-121">Questo comando può essere usato per avviare manualmente il rilevamento delle modifiche agli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="00854-121">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="00854-122">Può essere indirizzato all'intera condivisione, sottocartella o set di file.</span><span class="sxs-lookup"><span data-stu-id="00854-122">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="00854-123">Se si conosce l'ambito delle modifiche, limitare l'esecuzione di questo comando a parti dello spazio dei nomi, in modo che il rilevamento delle modifiche finisca rapidamente e entro il limite di 10.000 elementi.</span><span class="sxs-lookup"><span data-stu-id="00854-123">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 items limit.</span></span>

## <span data-ttu-id="00854-124">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00854-124">EXAMPLES</span></span>

### <span data-ttu-id="00854-125">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="00854-125">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="00854-126">In questo esempio il rilevamento delle modifiche viene eseguito nelle directory "Dati" e "Report\Modelli" di una condivisione file di Azure sincronizzata.</span><span class="sxs-lookup"><span data-stu-id="00854-126">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="00854-127">Tutti i percorsi sono relativi alla radice dello spazio dei nomi di condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="00854-127">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="00854-128">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="00854-128">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="00854-129">In questo esempio, il rilevamento delle modifiche viene eseguito per un set di file che sono noti al chiamante del comando per essere stati modificati.</span><span class="sxs-lookup"><span data-stu-id="00854-129">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="00854-130">L'obiettivo è fare in modo che Azure File Sync rilevi e sincronii anche queste modifiche.</span><span class="sxs-lookup"><span data-stu-id="00854-130">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="00854-131">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="00854-131">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="00854-132">In questo esempio viene eseguito il rilevamento delle modifiche per la directory "Examples" e vengono rilevate in modo ricorsivo le modifiche nelle sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="00854-132">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="00854-133">Tenere presente che se il percorso contiene più di 10.000 elementi, il cmdlet avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="00854-133">Keep in mind the cmdlet will fail if the path contains more than 10,000 items.</span></span> <span data-ttu-id="00854-134">Se il percorso contiene più di 10.000 elementi, eseguire il comando nelle parti secondarie dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="00854-134">If the path contains more than 10,000 items, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="00854-135">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00854-135">PARAMETERS</span></span>

### <span data-ttu-id="00854-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00854-136">-AsJob</span></span>
<span data-ttu-id="00854-137">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="00854-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00854-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00854-138">-DefaultProfile</span></span>
<span data-ttu-id="00854-139">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="00854-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00854-140">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="00854-140">-DirectoryPath</span></span>
<span data-ttu-id="00854-141">Directory in cui verrà eseguito il rilevamento delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="00854-141">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="00854-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00854-142">-InputObject</span></span>
<span data-ttu-id="00854-143">Oggetto CloudEndpoint, in genere passato attraverso il parametro.</span><span class="sxs-lookup"><span data-stu-id="00854-143">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="00854-144">-Name</span><span class="sxs-lookup"><span data-stu-id="00854-144">-Name</span></span>
<span data-ttu-id="00854-145">Nome di CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="00854-145">Name of the CloudEndpoint.</span></span> <span data-ttu-id="00854-146">Il nome è un GUID, non il nome descrittivo visualizzato nel portale.</span><span class="sxs-lookup"><span data-stu-id="00854-146">The name is a GUID, not the friendly name that's displayed in the portal.</span></span> <span data-ttu-id="00854-147">Per ottenere CloudEndpointName, usare il cmdlet Get-AzStorageSyncCloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="00854-147">To get the CloudEndpointName, use the Get-AzStorageSyncCloudEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="00854-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00854-148">-PassThru</span></span>
<span data-ttu-id="00854-149">Nella normale esecuzione, questo cmdlet non restituisce alcun valore in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="00854-149">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="00854-150">Se si fornisce il parametro PassThru, il cmdlet scriverà un valore nella pipeline dopo l'esecuzione corretta.</span><span class="sxs-lookup"><span data-stu-id="00854-150">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="00854-151">-Path</span><span class="sxs-lookup"><span data-stu-id="00854-151">-Path</span></span>
<span data-ttu-id="00854-152">Percorso in cui verrà eseguito il rilevamento delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="00854-152">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="00854-153">-Ricorsivo</span><span class="sxs-lookup"><span data-stu-id="00854-153">-Recursive</span></span>
<span data-ttu-id="00854-154">Indicazione se il rilevamento delle modifiche alla directory è ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="00854-154">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="00854-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00854-155">-ResourceGroupName</span></span>
<span data-ttu-id="00854-156">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="00854-156">Resource Group Name.</span></span>

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

### <span data-ttu-id="00854-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00854-157">-ResourceId</span></span>
<span data-ttu-id="00854-158">ID risorsa CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="00854-158">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="00854-159">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="00854-159">-StorageSyncServiceName</span></span>
<span data-ttu-id="00854-160">Nome di StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="00854-160">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="00854-161">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="00854-161">-SyncGroupName</span></span>
<span data-ttu-id="00854-162">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="00854-162">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="00854-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00854-163">-Confirm</span></span>
<span data-ttu-id="00854-164">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00854-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00854-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00854-165">-WhatIf</span></span>
<span data-ttu-id="00854-166">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00854-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00854-167">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00854-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00854-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00854-168">CommonParameters</span></span>
<span data-ttu-id="00854-169">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00854-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00854-170">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00854-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00854-171">INPUT</span><span class="sxs-lookup"><span data-stu-id="00854-171">INPUTS</span></span>

### <span data-ttu-id="00854-172">System.String</span><span class="sxs-lookup"><span data-stu-id="00854-172">System.String</span></span>

### <span data-ttu-id="00854-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="00854-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="00854-174">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00854-174">OUTPUTS</span></span>

### <span data-ttu-id="00854-175">System.Void</span><span class="sxs-lookup"><span data-stu-id="00854-175">System.Void</span></span>

## <span data-ttu-id="00854-176">NOTE</span><span class="sxs-lookup"><span data-stu-id="00854-176">NOTES</span></span>

## <span data-ttu-id="00854-177">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00854-177">RELATED LINKS</span></span>
