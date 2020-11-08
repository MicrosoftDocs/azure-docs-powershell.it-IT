---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 049201C9-590F-47EB-9030-25F80CD8DFA5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f3337556a9d7bd52e5800af5cdbd65b71ab9818
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023481"
---
# <span data-ttu-id="d0c0a-101">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="d0c0a-101">New-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="d0c0a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="d0c0a-103">Crea un volume in un contenitore di volumi specificato.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-103">Creates a volume in a specified volume container.</span></span>

## <span data-ttu-id="d0c0a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0c0a-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer> -VolumeName <String>
 -VolumeSizeInBytes <Int64>
 -AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>
 -VolumeAppType <AppType> -Online <Boolean> -EnableDefaultBackup <Boolean> -EnableMonitoring <Boolean>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d0c0a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0c0a-105">DESCRIPTION</span></span>
<span data-ttu-id="d0c0a-106">Il cmdlet **New-AzureStorSimpleDeviceVolume** crea un volume in un contenitore di volumi specificato.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-106">The **New-AzureStorSimpleDeviceVolume** cmdlet creates a volume in a specified volume container.</span></span>
<span data-ttu-id="d0c0a-107">Questo cmdlet associa ogni volume a uno o più record di controllo di Access.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-107">This cmdlet associates each volume with one or more access control records.</span></span>
<span data-ttu-id="d0c0a-108">Per ottenere oggetti **AccessControlRecord** , usa il cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="d0c0a-108">To obtain **AccessControlRecord** objects, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="d0c0a-109">Specificare un nome, una dimensione e AppType per il volume.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-109">Specify a name, size, and AppType for the volume.</span></span>
<span data-ttu-id="d0c0a-110">Specificare inoltre se creare il volume online, se abilitare il backup predefinito e se abilitare il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-110">Also, specify whether to create the volume online, whether to enable default backup, and whether to enable monitoring.</span></span>

## <span data-ttu-id="d0c0a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0c0a-111">EXAMPLES</span></span>

### <span data-ttu-id="d0c0a-112">Esempio 1: creare un volume</span><span class="sxs-lookup"><span data-stu-id="d0c0a-112">Example 1: Create a volume</span></span>
```
PS C:\>$AcrList = Get-AzureStorSimpleAccessControlRecord
PS C:\> Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer07" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Size 2000000000 -AccessControlRecords $AcrList -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False

VERBOSE: ClientRequestId: a29d1a84-1f81-4f20-9130-7adfe45e41fb_PS
VERBOSE: ClientRequestId: 8fa63df1-3f81-4029-a536-b536a70068ad_PS
VERBOSE: ClientRequestId: 964c5744-8bb1-4f70-beda-95ca4c7f3eb6_PS
VERBOSE: ClientRequestId: f09fff3a-54fa-4a0e-93db-b079260ed2dd_PS
VERBOSE: ClientRequestId: 59aa29e3-8044-411a-adae-b64a2681ffed_PS
VERBOSE: ClientRequestId: 0ffd0297-19be-40fe-a64e-6a2947d831b4_PS
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90 for tracking the task's status
VERBOSE: Volume container with name: VolumeContainer07 is found.
```

<span data-ttu-id="d0c0a-113">Il primo comando ottiene i record di controllo di Access nella configurazione del servizio di gestione di StorSimple usando il cmdlet **Get-AzureStorSimpleAccessControlRecord** e li archivia nella variabile $AcrList.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-113">The first command gets the access control records in the StorSimple Manager service configuration by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet, and then stores them in the $AcrList variable.</span></span>

<span data-ttu-id="d0c0a-114">Il secondo comando ottiene il contenitore del volume denominato VolumeContainer07 per il dispositivo denominato Contoso63-AppVm usando il cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="d0c0a-114">The second command gets the volume container named VolumeContainer07 for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="d0c0a-115">Il comando passa il contenitore al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-115">The command passes that container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d0c0a-116">Questo cmdlet crea il volume.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-116">This cmdlet creates the volume.</span></span>
<span data-ttu-id="d0c0a-117">Il comando specifica il nome per il volume, le dimensioni e i record di controllo di Access archiviati in $AcrList.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-117">The command specifies the name for the volume, the size, and the access control records stored in $AcrList.</span></span>
<span data-ttu-id="d0c0a-118">Questo comando avvia il processo e quindi restituisce un oggetto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="d0c0a-118">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="d0c0a-119">Per visualizzare lo stato del processo, usare il cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="d0c0a-119">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="d0c0a-120">Esempio 2: creare un volume senza controllo Controlaccess controllo recordsaccess di Access</span><span class="sxs-lookup"><span data-stu-id="d0c0a-120">Example 2: Create a volume without Access Controlaccess control recordsaccess control</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer01" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume22" -Size 2000000000 -AccessControlRecords @() -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False -WaitForComplete
VERBOSE: ClientRequestId: 3f359790-7e1f-48e7-acf8-ecabba850966_PS
VERBOSE: ClientRequestId: 2723ebcf-cd72-47bb-99b5-0c099d45641b_PS
VERBOSE: ClientRequestId: e605091f-dd63-42a7-bda2-24753cbc1f9a_PS
VERBOSE: ClientRequestId: b3fd08c3-67c5-4309-9591-15d92c360469_PS
VERBOSE: ClientRequestId: 15a024a3-b0c9-4f83-9c34-0ed8b95d024b_PS
VERBOSE: ClientRequestId: c13f92f9-aea1-40dd-af80-3affe273adbe_PS


TaskId       : ceef657e-390e-4f7a-aab7-669a29c29e7f
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 1d79febf-f752-4255-af2d-230d40773bc6_PS
AccessType             : NoAccess
AcrIdList              : {}
AcrList                : {}
AppType                : PrimaryVolume
DataContainer          : Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainer
DataContainerId        : 68b63d15-6aa5-4e69-9f9d-4a0bc607d6e9
InstanceId             : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd
InternalInstanceId     : 
IsBackupEnabled        : False
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
Name                   : Volume22
Online                 : True
OperationInProgress    : None
SizeInBytes            : 2000000000
VSN                    : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd

VERBOSE: Volume container with name: VolumeContainer01 is found.
```

<span data-ttu-id="d0c0a-121">Questo comando ottiene il contenitore del volume denominato VolumeContainer01 per il dispositivo denominato Contoso63-AppVm usando il cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="d0c0a-121">This command gets the volume container named VolumeContainer01 for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="d0c0a-122">Il comando passa il contenitore al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-122">The command passes that container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d0c0a-123">Questo cmdlet crea il volume.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-123">This cmdlet creates the volume.</span></span>
<span data-ttu-id="d0c0a-124">Il comando specifica il nome per il volume, le dimensioni e un valore vuoto per i record di controllo di Access.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-124">The command specifies the name for the volume, the size, and an empty value for access control records.</span></span>
<span data-ttu-id="d0c0a-125">Questo comando specifica il parametro *WaitForComplete* , quindi restituisce un **TaskStatusInfo** dopo aver creato il volume.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-125">This command specifies the *WaitForComplete* parameter, so it returns a **TaskStatusInfo** after it creates the volume.</span></span>

<span data-ttu-id="d0c0a-126">Poiché il comando specifica nessun record di controllo di accesso, non è possibile accedere a questo volume.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-126">Because the command specifies no access control records, this volume cannot be accessed.</span></span>
<span data-ttu-id="d0c0a-127">È possibile aggiungere l'accesso, in seguito, usando il cmdlet **set-AzureStorSimpleDeviceVolume** .</span><span class="sxs-lookup"><span data-stu-id="d0c0a-127">You can add access, later, by using **Set-AzureStorSimpleDeviceVolume** cmdlet.</span></span>

## <span data-ttu-id="d0c0a-128">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0c0a-128">PARAMETERS</span></span>

### <span data-ttu-id="d0c0a-129">-AccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="d0c0a-129">-AccessControlRecords</span></span>
<span data-ttu-id="d0c0a-130">Specifica un elenco di record di controllo di Access da associare al volume.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-130">Specifies a list of access control records to associate with the volume.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0c0a-131">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d0c0a-131">-DeviceName</span></span>
<span data-ttu-id="d0c0a-132">Specifica il nome del dispositivo StorSimple in cui creare il volume.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-132">Specifies the name of the StorSimple device on which to create the volume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c0a-133">-EnableDefaultBackup</span><span class="sxs-lookup"><span data-stu-id="d0c0a-133">-EnableDefaultBackup</span></span>
<span data-ttu-id="d0c0a-134">Specifica se abilitare il backup predefinito per il volume.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-134">Specifies whether to enable default backup for the volume.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c0a-135">-EnableMonitoring</span><span class="sxs-lookup"><span data-stu-id="d0c0a-135">-EnableMonitoring</span></span>
<span data-ttu-id="d0c0a-136">Specifica se abilitare il monitoraggio per il volume.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-136">Specifies whether to enable monitoring for the volume.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c0a-137">-Online</span><span class="sxs-lookup"><span data-stu-id="d0c0a-137">-Online</span></span>
<span data-ttu-id="d0c0a-138">Specifica se creare il volume online.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-138">Specifies whether to create the volume online.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c0a-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="d0c0a-139">-Profile</span></span>
<span data-ttu-id="d0c0a-140">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-140">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c0a-141">-VolumeAppType</span><span class="sxs-lookup"><span data-stu-id="d0c0a-141">-VolumeAppType</span></span>
<span data-ttu-id="d0c0a-142">Specifica se creare un volume principale o di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-142">Specifies whether to create a primary or archive volume.</span></span>
<span data-ttu-id="d0c0a-143">I valori validi sono: PrimaryVolume e ArchiveVolume.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-143">Valid values are: PrimaryVolume and ArchiveVolume.</span></span>

```yaml
Type: AppType
Parameter Sets: (All)
Aliases: AppType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c0a-144">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="d0c0a-144">-VolumeContainer</span></span>
<span data-ttu-id="d0c0a-145">Specifica il contenitore, come oggetto **DataContainer** , in cui creare il volume.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-145">Specifies the container, as a **DataContainer** object, in which to create the volume.</span></span>
<span data-ttu-id="d0c0a-146">Per ottenere un oggetto **VirtualDisk** , usa il cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="d0c0a-146">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0c0a-147">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="d0c0a-147">-VolumeName</span></span>
<span data-ttu-id="d0c0a-148">Specifica un nome per il nuovo volume.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-148">Specifies a name for the new volume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c0a-149">-VolumeSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="d0c0a-149">-VolumeSizeInBytes</span></span>
<span data-ttu-id="d0c0a-150">Specifica la dimensione del volume in byte.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-150">Specifies the volume size in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: SizeInBytes

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c0a-151">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="d0c0a-151">-WaitForComplete</span></span>
<span data-ttu-id="d0c0a-152">Indica che questo cmdlet attende che l'operazione venga completata prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-152">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c0a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0c0a-153">CommonParameters</span></span>
<span data-ttu-id="d0c0a-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0c0a-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0c0a-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0c0a-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0c0a-156">INPUTS</span></span>

### <span data-ttu-id="d0c0a-157">DataContainer, elenco\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="d0c0a-157">DataContainer, List\<AccessControlRecord\></span></span>
<span data-ttu-id="d0c0a-158">Questo cmdlet accetta un oggetto **DataContainer** e un elenco di oggetti **AccessControlRecord** per il nuovo volume.</span><span class="sxs-lookup"><span data-stu-id="d0c0a-158">This cmdlet accepts a **DataContainer** object and a list of **AccessControlRecord** objects for the new volume.</span></span>

## <span data-ttu-id="d0c0a-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0c0a-159">OUTPUTS</span></span>

### <span data-ttu-id="d0c0a-160">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="d0c0a-160">TaskStatusInfo</span></span>
<span data-ttu-id="d0c0a-161">Questo cmdlet restituisce un oggetto **TaskStatusInfo** , se specifichi il parametro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="d0c0a-161">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="d0c0a-162">Note</span><span class="sxs-lookup"><span data-stu-id="d0c0a-162">NOTES</span></span>

## <span data-ttu-id="d0c0a-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0c0a-163">RELATED LINKS</span></span>

[<span data-ttu-id="d0c0a-164">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="d0c0a-164">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="d0c0a-165">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="d0c0a-165">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="d0c0a-166">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="d0c0a-166">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="d0c0a-167">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="d0c0a-167">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="d0c0a-168">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="d0c0a-168">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="d0c0a-169">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="d0c0a-169">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


