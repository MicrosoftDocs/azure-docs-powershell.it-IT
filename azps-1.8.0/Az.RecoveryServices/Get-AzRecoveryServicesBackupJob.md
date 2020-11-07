---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 21498e13490b22b58621e2100dcc885442db7607
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677664"
---
# <span data-ttu-id="e1eb2-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="e1eb2-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="e1eb2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e1eb2-102">SYNOPSIS</span></span>
<span data-ttu-id="e1eb2-103">Ottiene i processi di backup.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="e1eb2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1eb2-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1eb2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1eb2-105">DESCRIPTION</span></span>
<span data-ttu-id="e1eb2-106">Il cmdlet **Get-AzRecoveryServicesBackupJob** ottiene i processi di backup di Azure per un Vault specifico.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="e1eb2-107">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="e1eb2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1eb2-108">EXAMPLES</span></span>

### <span data-ttu-id="e1eb2-109">Esempio 1: ottenere tutti i processi in corso</span><span class="sxs-lookup"><span data-stu-id="e1eb2-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="e1eb2-110">Il primo comando ottiene lo stato di un processo in corso come matrice e lo archivia nella variabile $Joblist.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="e1eb2-111">Il secondo comando Visualizza il primo elemento nella matrice $Joblist.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="e1eb2-112">Esempio 2: ottenere tutti i processi non riusciti negli ultimi 7 giorni</span><span class="sxs-lookup"><span data-stu-id="e1eb2-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="e1eb2-113">Questo comando restituisce i processi non riusciti dell'ultima settimana nel Vault.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="e1eb2-114">Il parametro *from* specifica un tempo di sette giorni nel passato specificato in UTC.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="e1eb2-115">Il comando non specifica un valore per il parametro *to* .</span><span class="sxs-lookup"><span data-stu-id="e1eb2-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="e1eb2-116">Di conseguenza, usa il valore predefinito dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="e1eb2-117">Esempio 3: ottenere un processo in corso e attendere il completamento</span><span class="sxs-lookup"><span data-stu-id="e1eb2-117">Example 3: Get an in-progress job and wait for completion</span></span>
```
PS C:\> 
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="e1eb2-118">Questo script esegue il polling del primo processo che è attualmente in corso fino al completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="e1eb2-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e1eb2-119">PARAMETERS</span></span>

### <span data-ttu-id="e1eb2-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="e1eb2-120">-BackupManagementType</span></span>
<span data-ttu-id="e1eb2-121">Specifica il tipo di gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="e1eb2-122">Attualmente è supportato solo AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-122">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1eb2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1eb2-123">-DefaultProfile</span></span>
<span data-ttu-id="e1eb2-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1eb2-125">-Da</span><span class="sxs-lookup"><span data-stu-id="e1eb2-125">-From</span></span>
<span data-ttu-id="e1eb2-126">Specifica l'inizio, come oggetto **DateTime** , di un intervallo di tempo per i processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="e1eb2-127">Per ottenere un oggetto **DateTime** , usare il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="e1eb2-128">Per altre informazioni sugli oggetti **DateTime** , digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="e1eb2-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="e1eb2-129">Usare il formato UTC per le date.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-129">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="e1eb2-130">-Job</span><span class="sxs-lookup"><span data-stu-id="e1eb2-130">-Job</span></span>
<span data-ttu-id="e1eb2-131">Specifica il nome del processo di backup da ottenere.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-131">Specifies the name of the Backup job to get.</span></span>

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

### <span data-ttu-id="e1eb2-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="e1eb2-132">-JobId</span></span>
<span data-ttu-id="e1eb2-133">Specifica l'ID di un processo ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="e1eb2-134">L'ID è la proprietà InstanceId di un oggetto **AzureRmRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="e1eb2-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="e1eb2-135">Per ottenere un oggetto **AzureRmRecoveryServicesBackupJob** , USA Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="e1eb2-136">-Operazione</span><span class="sxs-lookup"><span data-stu-id="e1eb2-136">-Operation</span></span>
<span data-ttu-id="e1eb2-137">Specifica un'operazione dei processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="e1eb2-138">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e1eb2-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e1eb2-139">Backup</span><span class="sxs-lookup"><span data-stu-id="e1eb2-139">Backup</span></span>
- <span data-ttu-id="e1eb2-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="e1eb2-140">ConfigureBackup</span></span>
- <span data-ttu-id="e1eb2-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="e1eb2-141">DeleteBackupData</span></span>
- <span data-ttu-id="e1eb2-142">Registrare</span><span class="sxs-lookup"><span data-stu-id="e1eb2-142">Register</span></span>
- <span data-ttu-id="e1eb2-143">Ripristinare</span><span class="sxs-lookup"><span data-stu-id="e1eb2-143">Restore</span></span>
- <span data-ttu-id="e1eb2-144">Rimuovi protezione</span><span class="sxs-lookup"><span data-stu-id="e1eb2-144">UnProtect</span></span>
- <span data-ttu-id="e1eb2-145">Unregister</span><span class="sxs-lookup"><span data-stu-id="e1eb2-145">Unregister</span></span>

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

### <span data-ttu-id="e1eb2-146">-Stato</span><span class="sxs-lookup"><span data-stu-id="e1eb2-146">-Status</span></span>
<span data-ttu-id="e1eb2-147">Specifica lo stato dei processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="e1eb2-148">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e1eb2-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e1eb2-149">InProgress</span><span class="sxs-lookup"><span data-stu-id="e1eb2-149">InProgress</span></span>
- <span data-ttu-id="e1eb2-150">Fallito</span><span class="sxs-lookup"><span data-stu-id="e1eb2-150">Failed</span></span>
- <span data-ttu-id="e1eb2-151">Annullata</span><span class="sxs-lookup"><span data-stu-id="e1eb2-151">Cancelled</span></span>
- <span data-ttu-id="e1eb2-152">Annullamento</span><span class="sxs-lookup"><span data-stu-id="e1eb2-152">Cancelling</span></span>
- <span data-ttu-id="e1eb2-153">Completato</span><span class="sxs-lookup"><span data-stu-id="e1eb2-153">Completed</span></span>
- <span data-ttu-id="e1eb2-154">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="e1eb2-154">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="e1eb2-155">-To</span><span class="sxs-lookup"><span data-stu-id="e1eb2-155">-To</span></span>
<span data-ttu-id="e1eb2-156">Specifica la fine, come oggetto **DateTime** , di un intervallo di tempo per i processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="e1eb2-157">Il valore predefinito è l'ora di sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-157">The default value is the current system time.</span></span>
<span data-ttu-id="e1eb2-158">Se specifichi questo parametro, devi anche specificare il parametro *from* .</span><span class="sxs-lookup"><span data-stu-id="e1eb2-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="e1eb2-159">Usare il formato UTC per le date.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-159">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="e1eb2-160">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e1eb2-160">-VaultId</span></span>
<span data-ttu-id="e1eb2-161">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-161">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1eb2-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1eb2-162">CommonParameters</span></span>
<span data-ttu-id="e1eb2-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1eb2-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1eb2-164">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1eb2-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1eb2-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e1eb2-165">INPUTS</span></span>

### <span data-ttu-id="e1eb2-166">System. String</span><span class="sxs-lookup"><span data-stu-id="e1eb2-166">System.String</span></span>

## <span data-ttu-id="e1eb2-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1eb2-167">OUTPUTS</span></span>

### <span data-ttu-id="e1eb2-168">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="e1eb2-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="e1eb2-169">Note</span><span class="sxs-lookup"><span data-stu-id="e1eb2-169">NOTES</span></span>

## <span data-ttu-id="e1eb2-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1eb2-170">RELATED LINKS</span></span>

[<span data-ttu-id="e1eb2-171">Get-AzRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="e1eb2-171">Get-AzRecoveryServicesBackupJobDetails</span></span>](./Get-AzRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="e1eb2-172">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="e1eb2-172">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="e1eb2-173">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="e1eb2-173">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


