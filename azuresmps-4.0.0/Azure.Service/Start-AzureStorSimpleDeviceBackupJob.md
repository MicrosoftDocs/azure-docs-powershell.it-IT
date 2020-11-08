---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 76826524-480F-458E-A996-A9DBACB8BA9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa220334c75d3e6832698ec10fbad71896473d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029489"
---
# <span data-ttu-id="b7e8e-101">Start-AzureStorSimpleDeviceBackupJob</span><span class="sxs-lookup"><span data-stu-id="b7e8e-101">Start-AzureStorSimpleDeviceBackupJob</span></span>

## <span data-ttu-id="b7e8e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="b7e8e-103">Avvia un nuovo processo che crea un backup da un criterio di backup esistente.</span><span class="sxs-lookup"><span data-stu-id="b7e8e-103">Starts a new job that creates a backup from an existing backup policy.</span></span>

## <span data-ttu-id="b7e8e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7e8e-104">SYNTAX</span></span>

### <span data-ttu-id="b7e8e-105">Empty (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b7e8e-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b7e8e-106">BackupTypeGiven</span><span class="sxs-lookup"><span data-stu-id="b7e8e-106">BackupTypeGiven</span></span>
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> -BackupType <String>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b7e8e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7e8e-107">DESCRIPTION</span></span>
<span data-ttu-id="b7e8e-108">Il cmdlet **Start-AzureStorSimpleDeviceBackupJob** avvia un nuovo processo che crea un backup da un criterio di backup esistente in un dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="b7e8e-108">The **Start-AzureStorSimpleDeviceBackupJob** cmdlet starts a new job that creates a backup from an existing backup policy on a StorSimple device.</span></span>
<span data-ttu-id="b7e8e-109">Per impostazione predefinita, questo cmdlet crea un backup dello snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="b7e8e-109">By default, this cmdlet creates a local snapshot backup.</span></span>
<span data-ttu-id="b7e8e-110">Per creare un backup cloud, specificare un valore di CloudSnapshot per il parametro *BackupType* .</span><span class="sxs-lookup"><span data-stu-id="b7e8e-110">To create a cloud backup, specify a value of CloudSnapshot for the *BackupType* parameter.</span></span>

## <span data-ttu-id="b7e8e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7e8e-111">EXAMPLES</span></span>

### <span data-ttu-id="b7e8e-112">Esempio 1: creare un backup dello snapshot locale</span><span class="sxs-lookup"><span data-stu-id="b7e8e-112">Example 1: Create a local snapshot backup</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f"
JobId                                                                StatusCode RequestId
-----                                                                ---------- ---------
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08                                 Accepted   456cf6bafd427103b71c07145e26d35c

VERBOSE: Your backup operation has been submitted for processing. Use commandlet "Get-AzureStorSimpleJob -JobId
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08" to track status.
```

<span data-ttu-id="b7e8e-113">Questo comando crea un backup dello snapshot locale per l'ID dei criteri specificato.</span><span class="sxs-lookup"><span data-stu-id="b7e8e-113">This command creates a local snapshot backup for the specified policy ID.</span></span>
<span data-ttu-id="b7e8e-114">Questo comando avvia il processo e quindi restituisce un oggetto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="b7e8e-114">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="b7e8e-115">Per visualizzare lo stato del processo, usare il cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="b7e8e-115">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="b7e8e-116">Esempio 2: creare un backup snapshot del cloud e attendere la fine</span><span class="sxs-lookup"><span data-stu-id="b7e8e-116">Example 2: Create a cloud snapshot backup and wait to finish</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -BackupType CloudSnapshot -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f28ecf6cf75a7f128ca18e6ae14f9003
```

<span data-ttu-id="b7e8e-117">Questo comando crea un backup snapshot del cloud per l'ID dei criteri specificato.</span><span class="sxs-lookup"><span data-stu-id="b7e8e-117">This command creates a cloud snapshot backup for the specified policy ID.</span></span>
<span data-ttu-id="b7e8e-118">Questo comando specifica il parametro *WaitForComplete* , quindi il comando completa l'attività e quindi restituisce un oggetto **TaskStatusInfo** per il processo.</span><span class="sxs-lookup"><span data-stu-id="b7e8e-118">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the job.</span></span>

## <span data-ttu-id="b7e8e-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7e8e-119">PARAMETERS</span></span>

### <span data-ttu-id="b7e8e-120">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="b7e8e-120">-BackupPolicyId</span></span>
<span data-ttu-id="b7e8e-121">Specifica l'ID dei criteri di backup da usare per creare il backup.</span><span class="sxs-lookup"><span data-stu-id="b7e8e-121">Specifies the ID of the backup policy to use to create the backup.</span></span>

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

### <span data-ttu-id="b7e8e-122">-BackupType</span><span class="sxs-lookup"><span data-stu-id="b7e8e-122">-BackupType</span></span>
<span data-ttu-id="b7e8e-123">Specifica il tipo di backup.</span><span class="sxs-lookup"><span data-stu-id="b7e8e-123">Specifies the backup type.</span></span>
<span data-ttu-id="b7e8e-124">I valori validi sono: LocalSnapshot e CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="b7e8e-124">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

```yaml
Type: String
Parameter Sets: BackupTypeGiven
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7e8e-125">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b7e8e-125">-DeviceName</span></span>
<span data-ttu-id="b7e8e-126">Specifica il nome del dispositivo StorSimple in cui avviare il processo di backup.</span><span class="sxs-lookup"><span data-stu-id="b7e8e-126">Specifies the name of the StorSimple device on which to start the backup job.</span></span>

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

### <span data-ttu-id="b7e8e-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="b7e8e-127">-Profile</span></span>
<span data-ttu-id="b7e8e-128">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="b7e8e-128">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="b7e8e-129">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="b7e8e-129">-WaitForComplete</span></span>
<span data-ttu-id="b7e8e-130">Indica che questo cmdlet attende che l'operazione venga completata prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b7e8e-130">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="b7e8e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7e8e-131">CommonParameters</span></span>
<span data-ttu-id="b7e8e-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7e8e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7e8e-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7e8e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7e8e-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7e8e-134">INPUTS</span></span>

### <span data-ttu-id="b7e8e-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b7e8e-135">None</span></span>

## <span data-ttu-id="b7e8e-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7e8e-136">OUTPUTS</span></span>

### <span data-ttu-id="b7e8e-137">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="b7e8e-137">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="b7e8e-138">Questo cmdlet restituisce un oggetto **TaskStatusInfo** se specifichi il parametro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="b7e8e-138">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="b7e8e-139">Se non specifichi tale parametro, restituisce un oggetto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="b7e8e-139">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="b7e8e-140">Note</span><span class="sxs-lookup"><span data-stu-id="b7e8e-140">NOTES</span></span>

## <span data-ttu-id="b7e8e-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7e8e-141">RELATED LINKS</span></span>

[<span data-ttu-id="b7e8e-142">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="b7e8e-142">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="b7e8e-143">Start-AzureStorSimpleDeviceBackupRestoreJob</span><span class="sxs-lookup"><span data-stu-id="b7e8e-143">Start-AzureStorSimpleDeviceBackupRestoreJob</span></span>](./Start-AzureStorSimpleDeviceBackupRestoreJob.md)


