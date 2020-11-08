---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 47650E39-758C-4D3C-9653-B70576CA0979
online version: ''
schema: 2.0.0
ms.openlocfilehash: a93791e3184fcabacbf90caebcb2170746922b36
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029929"
---
# <span data-ttu-id="eb88d-101">Remove-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="eb88d-101">Remove-AzureStorSimpleDeviceBackup</span></span>

## <span data-ttu-id="eb88d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eb88d-102">SYNOPSIS</span></span>
<span data-ttu-id="eb88d-103">Elimina un oggetto di backup.</span><span class="sxs-lookup"><span data-stu-id="eb88d-103">Deletes a backup object.</span></span>

## <span data-ttu-id="eb88d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb88d-104">SYNTAX</span></span>

### <span data-ttu-id="eb88d-105">IdentifyById (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eb88d-105">IdentifyById (Default)</span></span>
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupId <String> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="eb88d-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="eb88d-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -Backup <Backup> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="eb88d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb88d-107">DESCRIPTION</span></span>
<span data-ttu-id="eb88d-108">Il cmdlet **Remove-AzureStorSimpleDeviceBackup** Elimina un singolo oggetto backup.</span><span class="sxs-lookup"><span data-stu-id="eb88d-108">The **Remove-AzureStorSimpleDeviceBackup** cmdlet deletes a single backup object.</span></span>
<span data-ttu-id="eb88d-109">Se si tenta di eliminare un backup già eliminato, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="eb88d-109">If you attempt to delete a backup that has already been deleted, this cmdlet returns an error.</span></span>

## <span data-ttu-id="eb88d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb88d-110">EXAMPLES</span></span>

### <span data-ttu-id="eb88d-111">Esempio 1: rimuovere un backup per un dispositivo</span><span class="sxs-lookup"><span data-stu-id="eb88d-111">Example 1: Remove a backup for a device</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId "dcb5c991-0485-400f-8d0a-03a1341ee989" -Force
The remove job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 6c73aff2-f5a1-4b5e-
9a4e-857e128dc216 for tracking the job status
```

<span data-ttu-id="eb88d-112">Questo comando rimuove il backup con l'ID specificato per il dispositivo denominato Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="eb88d-112">This command removes the backup that has the specified ID for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="eb88d-113">Il comando avvia l'operazione che rimuove l'oggetto di **backup** e quindi restituisce un oggetto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="eb88d-113">The command starts the operation that removes the **Backup** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="eb88d-114">Per visualizzare lo stato dell'attività, usa il cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="eb88d-114">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="eb88d-115">Esempio 2: rimuovere il primo backup di un dispositivo usando il relativo ID</span><span class="sxs-lookup"><span data-stu-id="eb88d-115">Example 2: Remove the first backup for a device by using its ID</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId $Backup[0].InstanceId -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 53a656c3-c082-4e1f-afb7-bff3db45c791
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f4411f38d07f68b88095682dbeedd9e9
```

<span data-ttu-id="eb88d-116">Il primo comando consente di ottenere i backup per il dispositivo denominato Contoso63-AppVm e quindi di archiviarli nella variabile $Backup.</span><span class="sxs-lookup"><span data-stu-id="eb88d-116">The first command gets the backups for the device named Contoso63-AppVm, and then stores them in the $Backup variable.</span></span>

<span data-ttu-id="eb88d-117">Il secondo comando Elimina un backup dal dispositivo denominato Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="eb88d-117">The second command deletes a backup from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="eb88d-118">Il comando usa la notazione standard del punto per fare riferimento alla proprietà **InstanceID** del primo elemento della matrice $backup.</span><span class="sxs-lookup"><span data-stu-id="eb88d-118">The command uses standard dot notation to refer to the **InstanceId** property of the first element of the $Backup array.</span></span>
<span data-ttu-id="eb88d-119">Questo comando specifica il parametro *WaitForComplete* e, di conseguenza, il comando attende fino al completamento dell'operazione e quindi restituisce un oggetto **TaskStatusInfo** .</span><span class="sxs-lookup"><span data-stu-id="eb88d-119">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="eb88d-120">Esempio 3: rimuovere il primo backup di un dispositivo usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="eb88d-120">Example 3: Remove the first backup for a device by using the pipeline</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -WaitForComplete
PS C:\> $Backup[0] | Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -Force -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 48059fd8-e355-4b91-9385-630d24f31df6
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e1753f3bf68e6e44ab719436b5111e41
```

<span data-ttu-id="eb88d-121">Il primo comando consente di ottenere i backup per il dispositivo denominato Contoso63-AppVm e quindi di archiviarli nella variabile $Backup.</span><span class="sxs-lookup"><span data-stu-id="eb88d-121">The first command gets the backups for the device named Contoso63-AppVm, and then stores them in the $Backup variable.</span></span>

<span data-ttu-id="eb88d-122">Il secondo comando passa il primo oggetto archiviato nella matrice $Backup al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="eb88d-122">The second command passes the first object stored in the $Backup array to the current cmdlet.</span></span>
<span data-ttu-id="eb88d-123">Questo cmdlet elimina il backup dal dispositivo denominato Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="eb88d-123">That cmdlet deletes that backup from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="eb88d-124">Questo comando specifica il parametro *WaitForComplete* e, di conseguenza, il comando attende fino al completamento dell'operazione e quindi restituisce un oggetto **TaskStatusInfo** .</span><span class="sxs-lookup"><span data-stu-id="eb88d-124">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

## <span data-ttu-id="eb88d-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eb88d-125">PARAMETERS</span></span>

### <span data-ttu-id="eb88d-126">-Backup</span><span class="sxs-lookup"><span data-stu-id="eb88d-126">-Backup</span></span>
<span data-ttu-id="eb88d-127">Specifica l'oggetto di **backup** da eliminare.</span><span class="sxs-lookup"><span data-stu-id="eb88d-127">Specifies the **Backup** object to delete.</span></span>
<span data-ttu-id="eb88d-128">Per ottenere un oggetto di **backup** , usare il cmdlet **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="eb88d-128">To obtain a **Backup** object, use the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>

```yaml
Type: Backup
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb88d-129">-BackupId</span><span class="sxs-lookup"><span data-stu-id="eb88d-129">-BackupId</span></span>
<span data-ttu-id="eb88d-130">Specifica l'ID istanza di un backup da eliminare.</span><span class="sxs-lookup"><span data-stu-id="eb88d-130">Specifies the instance ID of a backup to delete.</span></span>

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

### <span data-ttu-id="eb88d-131">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="eb88d-131">-DeviceName</span></span>
<span data-ttu-id="eb88d-132">Specifica il nome del dispositivo StorSimple in cui eliminare un backup.</span><span class="sxs-lookup"><span data-stu-id="eb88d-132">Specifies the name of the StorSimple device on which to delete a backup.</span></span>

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

### <span data-ttu-id="eb88d-133">-Force</span><span class="sxs-lookup"><span data-stu-id="eb88d-133">-Force</span></span>
<span data-ttu-id="eb88d-134">Indica che questo cmdlet non richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="eb88d-134">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="eb88d-135">-Profile</span><span class="sxs-lookup"><span data-stu-id="eb88d-135">-Profile</span></span>
<span data-ttu-id="eb88d-136">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="eb88d-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="eb88d-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="eb88d-137">-WaitForComplete</span></span>
<span data-ttu-id="eb88d-138">Indica che questo cmdlet attende che l'operazione venga completata prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="eb88d-138">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="eb88d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb88d-139">CommonParameters</span></span>
<span data-ttu-id="eb88d-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb88d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb88d-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb88d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb88d-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eb88d-142">INPUTS</span></span>

### <span data-ttu-id="eb88d-143">Backup</span><span class="sxs-lookup"><span data-stu-id="eb88d-143">Backup</span></span>

## <span data-ttu-id="eb88d-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb88d-144">OUTPUTS</span></span>

### <span data-ttu-id="eb88d-145">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="eb88d-145">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="eb88d-146">Questo cmdlet restituisce un oggetto **TaskStatusInfo** se specifichi il parametro *WaitForComplete* se non specifichi tale parametro, restituisce un oggetto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="eb88d-146">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="eb88d-147">Note</span><span class="sxs-lookup"><span data-stu-id="eb88d-147">NOTES</span></span>

## <span data-ttu-id="eb88d-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb88d-148">RELATED LINKS</span></span>

[<span data-ttu-id="eb88d-149">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="eb88d-149">Get-AzureStorSimpleDeviceBackup</span></span>](./Get-AzureStorSimpleDeviceBackup.md)


