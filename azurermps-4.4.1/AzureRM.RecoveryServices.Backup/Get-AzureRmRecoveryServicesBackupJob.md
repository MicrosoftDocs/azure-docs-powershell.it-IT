---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 3fb6b89f5708c951731c45e0d32e0f7a379cf754
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521561"
---
# <span data-ttu-id="ef529-101">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="ef529-101">Get-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="ef529-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ef529-102">SYNOPSIS</span></span>
<span data-ttu-id="ef529-103">Ottiene i processi di backup.</span><span class="sxs-lookup"><span data-stu-id="ef529-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef529-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef529-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef529-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef529-105">DESCRIPTION</span></span>
<span data-ttu-id="ef529-106">Il cmdlet **Get-AzureRmRecoveryServicesBackupJob** ottiene i processi di backup di Azure per un Vault specifico.</span><span class="sxs-lookup"><span data-stu-id="ef529-106">The **Get-AzureRmRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

<span data-ttu-id="ef529-107">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="ef529-107">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ef529-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef529-108">EXAMPLES</span></span>

### <span data-ttu-id="ef529-109">Esempio 1: ottenere tutti i processi in corso</span><span class="sxs-lookup"><span data-stu-id="ef529-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzureRMRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="ef529-110">Il primo comando ottiene lo stato di un processo in corso come matrice e lo archivia nella variabile $Joblist.</span><span class="sxs-lookup"><span data-stu-id="ef529-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>

<span data-ttu-id="ef529-111">Il secondo comando Visualizza il primo elemento nella matrice $Joblist.</span><span class="sxs-lookup"><span data-stu-id="ef529-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="ef529-112">Esempio 2: ottenere tutti i processi non riusciti negli ultimi 7 giorni</span><span class="sxs-lookup"><span data-stu-id="ef529-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="ef529-113">Questo comando restituisce i processi non riusciti dell'ultima settimana nel Vault.</span><span class="sxs-lookup"><span data-stu-id="ef529-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="ef529-114">Il parametro *from* specifica un tempo di sette giorni nel passato specificato in UTC.</span><span class="sxs-lookup"><span data-stu-id="ef529-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="ef529-115">Il comando non specifica un valore per il parametro *to* .</span><span class="sxs-lookup"><span data-stu-id="ef529-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="ef529-116">Di conseguenza, usa il valore predefinito dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="ef529-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="ef529-117">Esempio 3: ottenere un processo in corso e attendere il completamento</span><span class="sxs-lookup"><span data-stu-id="ef529-117">Example 3: Get an in-progress job and wait for completion</span></span>
```
PS C:\> 
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="ef529-118">Questo script esegue il polling del primo processo che è attualmente in corso fino al completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="ef529-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="ef529-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ef529-119">PARAMETERS</span></span>

### <span data-ttu-id="ef529-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="ef529-120">-BackupManagementType</span></span>
<span data-ttu-id="ef529-121">Specifica il tipo di gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="ef529-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="ef529-122">Attualmente è supportato solo AzureVM.</span><span class="sxs-lookup"><span data-stu-id="ef529-122">Currently, only AzureVM is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef529-123">-Da</span><span class="sxs-lookup"><span data-stu-id="ef529-123">-From</span></span>
<span data-ttu-id="ef529-124">Specifica l'inizio, come oggetto **DateTime** , di un intervallo di tempo per i processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef529-124">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ef529-125">Per ottenere un oggetto **DateTime** , usare il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="ef529-125">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="ef529-126">Per altre informazioni sugli oggetti **DateTime** , digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="ef529-126">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="ef529-127">Usare il formato UTC per le date.</span><span class="sxs-lookup"><span data-stu-id="ef529-127">Use UTC format for dates.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef529-128">-Job</span><span class="sxs-lookup"><span data-stu-id="ef529-128">-Job</span></span>
<span data-ttu-id="ef529-129">Specifica il nome del processo di backup da ottenere.</span><span class="sxs-lookup"><span data-stu-id="ef529-129">Specifies the name of the Backup job to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef529-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="ef529-130">-JobId</span></span>
<span data-ttu-id="ef529-131">Specifica l'ID di un processo ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef529-131">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="ef529-132">L'ID è la proprietà InstanceId di un oggetto **AzureRmRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="ef529-132">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="ef529-133">Per ottenere un oggetto **AzureRmRecoveryServicesBackupJob** , USA Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="ef529-133">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef529-134">-Operazione</span><span class="sxs-lookup"><span data-stu-id="ef529-134">-Operation</span></span>
<span data-ttu-id="ef529-135">Specifica un'operazione dei processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef529-135">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ef529-136">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ef529-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ef529-137">Backup</span><span class="sxs-lookup"><span data-stu-id="ef529-137">Backup</span></span>
- <span data-ttu-id="ef529-138">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="ef529-138">ConfigureBackup</span></span>
- <span data-ttu-id="ef529-139">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="ef529-139">DeleteBackupData</span></span>
- <span data-ttu-id="ef529-140">Registrare</span><span class="sxs-lookup"><span data-stu-id="ef529-140">Register</span></span>
- <span data-ttu-id="ef529-141">Ripristinare</span><span class="sxs-lookup"><span data-stu-id="ef529-141">Restore</span></span>
- <span data-ttu-id="ef529-142">Rimuovi protezione</span><span class="sxs-lookup"><span data-stu-id="ef529-142">UnProtect</span></span>
- <span data-ttu-id="ef529-143">Unregister</span><span class="sxs-lookup"><span data-stu-id="ef529-143">Unregister</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobOperation]
Parameter Sets: (All)
Aliases: 
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef529-144">-Stato</span><span class="sxs-lookup"><span data-stu-id="ef529-144">-Status</span></span>
<span data-ttu-id="ef529-145">Specifica lo stato dei processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef529-145">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ef529-146">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ef529-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ef529-147">InProgress</span><span class="sxs-lookup"><span data-stu-id="ef529-147">InProgress</span></span>
- <span data-ttu-id="ef529-148">Fallito</span><span class="sxs-lookup"><span data-stu-id="ef529-148">Failed</span></span>
- <span data-ttu-id="ef529-149">Annullata</span><span class="sxs-lookup"><span data-stu-id="ef529-149">Cancelled</span></span>
- <span data-ttu-id="ef529-150">Annullamento</span><span class="sxs-lookup"><span data-stu-id="ef529-150">Cancelling</span></span>
- <span data-ttu-id="ef529-151">Completato</span><span class="sxs-lookup"><span data-stu-id="ef529-151">Completed</span></span>
- <span data-ttu-id="ef529-152">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="ef529-152">CompletedWithWarnings</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobStatus]
Parameter Sets: (All)
Aliases: 
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef529-153">-To</span><span class="sxs-lookup"><span data-stu-id="ef529-153">-To</span></span>
<span data-ttu-id="ef529-154">Specifica la fine, come oggetto **DateTime** , di un intervallo di tempo per i processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef529-154">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ef529-155">Il valore predefinito è l'ora di sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="ef529-155">The default value is the current system time.</span></span>
<span data-ttu-id="ef529-156">Se specifichi questo parametro, devi anche specificare il parametro *from* .</span><span class="sxs-lookup"><span data-stu-id="ef529-156">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="ef529-157">Usare il formato UTC per le date.</span><span class="sxs-lookup"><span data-stu-id="ef529-157">Use UTC format for dates.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef529-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef529-158">-DefaultProfile</span></span>
<span data-ttu-id="ef529-159">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ef529-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef529-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef529-160">CommonParameters</span></span>
<span data-ttu-id="ef529-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef529-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef529-162">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef529-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef529-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ef529-163">INPUTS</span></span>

## <span data-ttu-id="ef529-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef529-164">OUTPUTS</span></span>

### <span data-ttu-id="ef529-165">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="ef529-165">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

### <span data-ttu-id="ef529-166">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase]</span><span class="sxs-lookup"><span data-stu-id="ef529-166">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="ef529-167">Note</span><span class="sxs-lookup"><span data-stu-id="ef529-167">NOTES</span></span>

## <span data-ttu-id="ef529-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef529-168">RELATED LINKS</span></span>

[<span data-ttu-id="ef529-169">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="ef529-169">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>](./Get-AzureRmRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="ef529-170">Stop-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="ef529-170">Stop-AzureRmRecoveryServicesBackupJob</span></span>](./Stop-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="ef529-171">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="ef529-171">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


