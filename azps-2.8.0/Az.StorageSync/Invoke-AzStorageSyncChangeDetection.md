---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: c266b6623463165f14e01e55f0fec4d2d59a581f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858306"
---
# <span data-ttu-id="a0f80-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="a0f80-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="a0f80-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0f80-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f80-103">Questo comando può essere usato per avviare manualmente il rilevamento delle modifiche agli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a0f80-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="a0f80-104">Può essere destinata all'intera condivisione, sottocartella o set di file.</span><span class="sxs-lookup"><span data-stu-id="a0f80-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="a0f80-105">Può essere rilevato un massimo di 10.000 modifiche.</span><span class="sxs-lookup"><span data-stu-id="a0f80-105">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="a0f80-106">Se l'ambito delle modifiche è noto, limitare l'esecuzione di questo comando alle parti dello spazio dei nomi, in modo che il rilevamento della modifica possa terminare rapidamente e all'interno di un limite di modifiche di 10.000.</span><span class="sxs-lookup"><span data-stu-id="a0f80-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="a0f80-107">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0f80-107">SYNTAX</span></span>

### <span data-ttu-id="a0f80-108">StringAndDirectoryParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a0f80-108">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0f80-109">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0f80-109">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0f80-110">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0f80-110">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0f80-111">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0f80-111">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0f80-112">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0f80-112">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0f80-113">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0f80-113">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0f80-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0f80-114">DESCRIPTION</span></span>
<span data-ttu-id="a0f80-115">Periodicamente, in Azure file Sync viene controllato lo spazio dei nomi all'interno di una condivisione file di Azure di sincronizzazione per le modifiche apportate alla condivisione file con altri mezzi rispetto alla sincronizzazione. L'obiettivo è identificare queste modifiche e infine sincronizzarle con i server connessi.</span><span class="sxs-lookup"><span data-stu-id="a0f80-115">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="a0f80-116">Questo comando può essere usato per avviare manualmente il rilevamento delle modifiche agli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a0f80-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="a0f80-117">Può essere destinata all'intera condivisione, sottocartella o set di file.</span><span class="sxs-lookup"><span data-stu-id="a0f80-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="a0f80-118">Se l'ambito delle modifiche è noto, limitare l'esecuzione di questo comando alle parti dello spazio dei nomi, in modo che il rilevamento della modifica possa terminare rapidamente e all'interno di un limite di modifiche di 10.000.</span><span class="sxs-lookup"><span data-stu-id="a0f80-118">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="a0f80-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0f80-119">EXAMPLES</span></span>

### <span data-ttu-id="a0f80-120">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a0f80-120">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="a0f80-121">In questo esempio, il rilevamento delle modifiche viene eseguito nelle directory "data" e "Reporting\Templates" di una condivisione file di Azure di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="a0f80-121">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="a0f80-122">Tutti i percorsi sono relativi alla radice dello spazio dei nomi di condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="a0f80-122">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="a0f80-123">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a0f80-123">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="a0f80-124">In questo esempio, il rilevamento delle modifiche viene eseguito per un set di file noti al chiamante del comando per essere stati modificati.</span><span class="sxs-lookup"><span data-stu-id="a0f80-124">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="a0f80-125">L'obiettivo è quello di rilevare e sincronizzare anche le modifiche di Azure file Sync.</span><span class="sxs-lookup"><span data-stu-id="a0f80-125">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="a0f80-126">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a0f80-126">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="a0f80-127">In questo esempio viene eseguito il rilevamento delle modifiche per la directory "examples" e verranno rilevate le modifiche ricorsive nelle sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="a0f80-127">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="a0f80-128">Tieni presente che questo comando consente di rilevare fino a 10.000 modifiche prima che vengano interrotte automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a0f80-128">Keep in mind that this command can detect up to 10,000 changes before it is automatically aborted.</span></span> <span data-ttu-id="a0f80-129">Se si sospetta che si verifichino più di 10.000 modifiche, eseguire il comando in sezioni secondarie dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a0f80-129">If you suspect more than 10,000 changes to have occurred, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="a0f80-130">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0f80-130">PARAMETERS</span></span>

### <span data-ttu-id="a0f80-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0f80-131">-AsJob</span></span>
<span data-ttu-id="a0f80-132">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a0f80-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0f80-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f80-133">-DefaultProfile</span></span>
<span data-ttu-id="a0f80-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0f80-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0f80-135">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="a0f80-135">-DirectoryPath</span></span>
<span data-ttu-id="a0f80-136">Directory in cui verrà eseguito il rilevamento delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="a0f80-136">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="a0f80-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0f80-137">-InputObject</span></span>
<span data-ttu-id="a0f80-138">Oggetto CloudEndpoint, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="a0f80-138">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="a0f80-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0f80-139">-Name</span></span>
<span data-ttu-id="a0f80-140">Nome della CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a0f80-140">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="a0f80-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0f80-141">-PassThru</span></span>
<span data-ttu-id="a0f80-142">In esecuzione normale, questo cmdlet non restituisce alcun valore per l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a0f80-142">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="a0f80-143">Se fornisci il parametro PassThru, il cmdlet scriverà un valore nella pipeline dopo l'esecuzione corretta.</span><span class="sxs-lookup"><span data-stu-id="a0f80-143">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="a0f80-144">-Path</span><span class="sxs-lookup"><span data-stu-id="a0f80-144">-Path</span></span>
<span data-ttu-id="a0f80-145">Percorso in cui verrà eseguito il rilevamento delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="a0f80-145">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="a0f80-146">-Ricorsiva</span><span class="sxs-lookup"><span data-stu-id="a0f80-146">-Recursive</span></span>
<span data-ttu-id="a0f80-147">Indica se il rilevamento delle modifiche della directory è ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="a0f80-147">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="a0f80-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0f80-148">-ResourceGroupName</span></span>
<span data-ttu-id="a0f80-149">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a0f80-149">Resource Group Name.</span></span>

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

### <span data-ttu-id="a0f80-150">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0f80-150">-ResourceId</span></span>
<span data-ttu-id="a0f80-151">ID risorsa CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="a0f80-151">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="a0f80-152">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="a0f80-152">-StorageSyncServiceName</span></span>
<span data-ttu-id="a0f80-153">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="a0f80-153">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="a0f80-154">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a0f80-154">-SyncGroupName</span></span>
<span data-ttu-id="a0f80-155">Nome della SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="a0f80-155">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="a0f80-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a0f80-156">-Confirm</span></span>
<span data-ttu-id="a0f80-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0f80-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0f80-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0f80-158">-WhatIf</span></span>
<span data-ttu-id="a0f80-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0f80-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0f80-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0f80-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0f80-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f80-161">CommonParameters</span></span>
<span data-ttu-id="a0f80-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0f80-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f80-163">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0f80-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f80-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0f80-164">INPUTS</span></span>

### <span data-ttu-id="a0f80-165">System. String</span><span class="sxs-lookup"><span data-stu-id="a0f80-165">System.String</span></span>

### <span data-ttu-id="a0f80-166">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a0f80-166">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="a0f80-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0f80-167">OUTPUTS</span></span>

### <span data-ttu-id="a0f80-168">System. void</span><span class="sxs-lookup"><span data-stu-id="a0f80-168">System.Void</span></span>

## <span data-ttu-id="a0f80-169">Note</span><span class="sxs-lookup"><span data-stu-id="a0f80-169">NOTES</span></span>

## <span data-ttu-id="a0f80-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0f80-170">RELATED LINKS</span></span>
