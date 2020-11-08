---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F9C8D0AA-ED97-43E8-ADB1-5AE1A4517666
online version: ''
schema: 2.0.0
ms.openlocfilehash: c524bb90d84df6ad3e37b552b957dac2d75b6a6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023705"
---
# <span data-ttu-id="329f5-101">Start-AzureStorSimpleDeviceBackupRestoreJob</span><span class="sxs-lookup"><span data-stu-id="329f5-101">Start-AzureStorSimpleDeviceBackupRestoreJob</span></span>

## <span data-ttu-id="329f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="329f5-102">SYNOPSIS</span></span>
<span data-ttu-id="329f5-103">Avvia un processo che ripristina un backup in un dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="329f5-103">Starts a job that restores a backup on a StorSimple device.</span></span>

## <span data-ttu-id="329f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="329f5-104">SYNTAX</span></span>

### <span data-ttu-id="329f5-105">Empty (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="329f5-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="329f5-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="329f5-106">IdentifyById</span></span>
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> -SnapshotId <String>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="329f5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="329f5-107">DESCRIPTION</span></span>
<span data-ttu-id="329f5-108">Il cmdlet **Start-AzureStorSimpleDeviceBackupRestoreJob** avvia un processo che ripristina un backup in un dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="329f5-108">The **Start-AzureStorSimpleDeviceBackupRestoreJob** cmdlet starts a job that restores a backup on a StorSimple device.</span></span>
<span data-ttu-id="329f5-109">Specificare un ID di backup e un ID snapshot facoltativo.</span><span class="sxs-lookup"><span data-stu-id="329f5-109">Specify a backup ID and an optional snapshot ID.</span></span>

## <span data-ttu-id="329f5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="329f5-110">EXAMPLES</span></span>

### <span data-ttu-id="329f5-111">Esempio 1: avviare un processo per ripristinare un backup</span><span class="sxs-lookup"><span data-stu-id="329f5-111">Example 1: Start a job to restore a backup</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -WaitForComplete
Confirm
Are you sure you want to restore the backup with backupId b3b50534-763c-4b05-9724-5ecf62bde721? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y


Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 217d0647-c001-4f43-9833-f8155a458e95
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e0aa2dcd2f197a8588c40a067fe0e519
```

<span data-ttu-id="329f5-112">Questo comando avvia un processo che ripristina l'oggetto di backup con l'ID specificato e gli snapshot associati nel dispositivo denominato Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="329f5-112">This command starts a job that restores the backup object that has the specified ID, and its associated snapshots, on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="329f5-113">Il comando specifica il parametro *WaitForComplete* , in modo che il processo finisca prima che il cmdlet restituisca il controllo alla console.</span><span class="sxs-lookup"><span data-stu-id="329f5-113">The command specifies the *WaitForComplete* parameter, so the job finishes before the cmdlet returns control to the console.</span></span>

### <span data-ttu-id="329f5-114">Esempio 2: avviare un processo per ripristinare uno snapshot specifico</span><span class="sxs-lookup"><span data-stu-id="329f5-114">Example 2: Start a job to restore a specific snapshot</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -SnapshotId "2d0cfad7-46bf-4266-8859-96549646e947_0000000000000000" -Force

The start job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 9102ed9a-078f-4648-a
721-3cffbba31336 for tracking the job status
```

<span data-ttu-id="329f5-115">Questo comando avvia un processo che ripristina lo snapshot di backup con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="329f5-115">This command starts a job that restores the backup snapshot that has the specified ID.</span></span>
<span data-ttu-id="329f5-116">Il comando specifica l'oggetto di backup in base all'ID nel dispositivo denominato Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="329f5-116">The command specifies the backup object by ID on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="329f5-117">Il comando specifica il parametro *Force* , quindi avvia il processo senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="329f5-117">The command specifies the *Force* parameter, so it starts the job without prompting you to confirm.</span></span>

## <span data-ttu-id="329f5-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="329f5-118">PARAMETERS</span></span>

### <span data-ttu-id="329f5-119">-BackupId</span><span class="sxs-lookup"><span data-stu-id="329f5-119">-BackupId</span></span>
<span data-ttu-id="329f5-120">Specifica l'ID istanza del backup da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="329f5-120">Specifies the instance ID of the backup to restore.</span></span>

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

### <span data-ttu-id="329f5-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="329f5-121">-DeviceName</span></span>
<span data-ttu-id="329f5-122">Specifica il nome del dispositivo StorSimple in cui è presente il backup.</span><span class="sxs-lookup"><span data-stu-id="329f5-122">Specifies the name of the StorSimple device on which the backup exists.</span></span>

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

### <span data-ttu-id="329f5-123">-Force</span><span class="sxs-lookup"><span data-stu-id="329f5-123">-Force</span></span>
<span data-ttu-id="329f5-124">Indica che questo cmdlet non richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="329f5-124">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="329f5-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="329f5-125">-Profile</span></span>
<span data-ttu-id="329f5-126">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="329f5-126">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="329f5-127">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="329f5-127">-SnapshotId</span></span>
<span data-ttu-id="329f5-128">Specifica l'ID istanza dello snapshot da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="329f5-128">Specifies the instance ID of the snapshot to restore.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329f5-129">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="329f5-129">-WaitForComplete</span></span>
<span data-ttu-id="329f5-130">Indica che questo cmdlet attende che l'operazione venga completata prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="329f5-130">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="329f5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="329f5-131">CommonParameters</span></span>
<span data-ttu-id="329f5-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="329f5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="329f5-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="329f5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="329f5-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="329f5-134">INPUTS</span></span>

### <span data-ttu-id="329f5-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="329f5-135">None</span></span>

## <span data-ttu-id="329f5-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="329f5-136">OUTPUTS</span></span>

### <span data-ttu-id="329f5-137">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="329f5-137">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="329f5-138">Questo cmdlet restituisce un oggetto **TaskStatusInfo** se specifichi il parametro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="329f5-138">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="329f5-139">Se non specifichi tale parametro, restituisce un oggetto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="329f5-139">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="329f5-140">Note</span><span class="sxs-lookup"><span data-stu-id="329f5-140">NOTES</span></span>

## <span data-ttu-id="329f5-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="329f5-141">RELATED LINKS</span></span>

[<span data-ttu-id="329f5-142">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="329f5-142">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="329f5-143">Start-AzureStorSimpleDeviceBackupJob</span><span class="sxs-lookup"><span data-stu-id="329f5-143">Start-AzureStorSimpleDeviceBackupJob</span></span>](./Start-AzureStorSimpleDeviceBackupJob.md)


