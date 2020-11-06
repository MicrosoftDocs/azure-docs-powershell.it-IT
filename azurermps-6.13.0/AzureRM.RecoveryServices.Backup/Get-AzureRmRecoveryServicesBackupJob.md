---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 0ed0ed82c1f2c030ab10fc6a96d1582fdb34b7d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520154"
---
# <span data-ttu-id="9d8b4-101">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="9d8b4-101">Get-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="9d8b4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d8b4-102">SYNOPSIS</span></span>
<span data-ttu-id="9d8b4-103">Ottiene i processi di backup.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d8b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d8b4-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d8b4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d8b4-105">DESCRIPTION</span></span>
<span data-ttu-id="9d8b4-106">Il cmdlet **Get-AzureRmRecoveryServicesBackupJob** ottiene i processi di backup di Azure per un Vault specifico.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-106">The **Get-AzureRmRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="9d8b4-107">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-107">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="9d8b4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d8b4-108">EXAMPLES</span></span>

### <span data-ttu-id="9d8b4-109">Esempio 1: ottenere tutti i processi in corso</span><span class="sxs-lookup"><span data-stu-id="9d8b4-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzureRMRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="9d8b4-110">Il primo comando ottiene lo stato di un processo in corso come matrice e lo archivia nella variabile $Joblist.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="9d8b4-111">Il secondo comando Visualizza il primo elemento nella matrice $Joblist.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="9d8b4-112">Esempio 2: ottenere tutti i processi non riusciti negli ultimi 7 giorni</span><span class="sxs-lookup"><span data-stu-id="9d8b4-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="9d8b4-113">Questo comando restituisce i processi non riusciti dell'ultima settimana nel Vault.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="9d8b4-114">Il parametro *from* specifica un tempo di sette giorni nel passato specificato in UTC.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="9d8b4-115">Il comando non specifica un valore per il parametro *to* .</span><span class="sxs-lookup"><span data-stu-id="9d8b4-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="9d8b4-116">Di conseguenza, usa il valore predefinito dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="9d8b4-117">Esempio 3: ottenere un processo in corso e attendere il completamento</span><span class="sxs-lookup"><span data-stu-id="9d8b4-117">Example 3: Get an in-progress job and wait for completion</span></span>
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

<span data-ttu-id="9d8b4-118">Questo script esegue il polling del primo processo che è attualmente in corso fino al completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="9d8b4-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d8b4-119">PARAMETERS</span></span>

### <span data-ttu-id="9d8b4-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="9d8b4-120">-BackupManagementType</span></span>
<span data-ttu-id="9d8b4-121">Specifica il tipo di gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="9d8b4-122">Attualmente è supportato solo AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-122">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d8b4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d8b4-123">-DefaultProfile</span></span>
<span data-ttu-id="9d8b4-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d8b4-125">-Da</span><span class="sxs-lookup"><span data-stu-id="9d8b4-125">-From</span></span>
<span data-ttu-id="9d8b4-126">Specifica l'inizio, come oggetto **DateTime** , di un intervallo di tempo per i processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9d8b4-127">Per ottenere un oggetto **DateTime** , usare il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="9d8b4-128">Per altre informazioni sugli oggetti **DateTime** , digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9d8b4-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="9d8b4-129">Usare il formato UTC per le date.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-129">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="9d8b4-130">-Job</span><span class="sxs-lookup"><span data-stu-id="9d8b4-130">-Job</span></span>
<span data-ttu-id="9d8b4-131">Specifica il nome del processo di backup da ottenere.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-131">Specifies the name of the Backup job to get.</span></span>

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

### <span data-ttu-id="9d8b4-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="9d8b4-132">-JobId</span></span>
<span data-ttu-id="9d8b4-133">Specifica l'ID di un processo ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="9d8b4-134">L'ID è la proprietà InstanceId di un oggetto **AzureRmRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="9d8b4-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="9d8b4-135">Per ottenere un oggetto **AzureRmRecoveryServicesBackupJob** , USA Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="9d8b4-136">-Operazione</span><span class="sxs-lookup"><span data-stu-id="9d8b4-136">-Operation</span></span>
<span data-ttu-id="9d8b4-137">Specifica un'operazione dei processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9d8b4-138">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9d8b4-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d8b4-139">Backup</span><span class="sxs-lookup"><span data-stu-id="9d8b4-139">Backup</span></span>
- <span data-ttu-id="9d8b4-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="9d8b4-140">ConfigureBackup</span></span>
- <span data-ttu-id="9d8b4-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="9d8b4-141">DeleteBackupData</span></span>
- <span data-ttu-id="9d8b4-142">Registrare</span><span class="sxs-lookup"><span data-stu-id="9d8b4-142">Register</span></span>
- <span data-ttu-id="9d8b4-143">Ripristinare</span><span class="sxs-lookup"><span data-stu-id="9d8b4-143">Restore</span></span>
- <span data-ttu-id="9d8b4-144">Rimuovi protezione</span><span class="sxs-lookup"><span data-stu-id="9d8b4-144">UnProtect</span></span>
- <span data-ttu-id="9d8b4-145">Unregister</span><span class="sxs-lookup"><span data-stu-id="9d8b4-145">Unregister</span></span>

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

### <span data-ttu-id="9d8b4-146">-Stato</span><span class="sxs-lookup"><span data-stu-id="9d8b4-146">-Status</span></span>
<span data-ttu-id="9d8b4-147">Specifica lo stato dei processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9d8b4-148">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9d8b4-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d8b4-149">InProgress</span><span class="sxs-lookup"><span data-stu-id="9d8b4-149">InProgress</span></span>
- <span data-ttu-id="9d8b4-150">Fallito</span><span class="sxs-lookup"><span data-stu-id="9d8b4-150">Failed</span></span>
- <span data-ttu-id="9d8b4-151">Annullata</span><span class="sxs-lookup"><span data-stu-id="9d8b4-151">Cancelled</span></span>
- <span data-ttu-id="9d8b4-152">Annullamento</span><span class="sxs-lookup"><span data-stu-id="9d8b4-152">Cancelling</span></span>
- <span data-ttu-id="9d8b4-153">Completato</span><span class="sxs-lookup"><span data-stu-id="9d8b4-153">Completed</span></span>
- <span data-ttu-id="9d8b4-154">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="9d8b4-154">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="9d8b4-155">-To</span><span class="sxs-lookup"><span data-stu-id="9d8b4-155">-To</span></span>
<span data-ttu-id="9d8b4-156">Specifica la fine, come oggetto **DateTime** , di un intervallo di tempo per i processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9d8b4-157">Il valore predefinito è l'ora di sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-157">The default value is the current system time.</span></span>
<span data-ttu-id="9d8b4-158">Se specifichi questo parametro, devi anche specificare il parametro *from* .</span><span class="sxs-lookup"><span data-stu-id="9d8b4-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="9d8b4-159">Usare il formato UTC per le date.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-159">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="9d8b4-160">-VaultId</span><span class="sxs-lookup"><span data-stu-id="9d8b4-160">-VaultId</span></span>
<span data-ttu-id="9d8b4-161">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-161">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9d8b4-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d8b4-162">CommonParameters</span></span>
<span data-ttu-id="9d8b4-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d8b4-164">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d8b4-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d8b4-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d8b4-165">INPUTS</span></span>

### <span data-ttu-id="9d8b4-166">System. String</span><span class="sxs-lookup"><span data-stu-id="9d8b4-166">System.String</span></span>
<span data-ttu-id="9d8b4-167">Parametri: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9d8b4-167">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="9d8b4-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d8b4-168">OUTPUTS</span></span>

### <span data-ttu-id="9d8b4-169">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="9d8b4-169">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="9d8b4-170">Note</span><span class="sxs-lookup"><span data-stu-id="9d8b4-170">NOTES</span></span>

## <span data-ttu-id="9d8b4-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d8b4-171">RELATED LINKS</span></span>

[<span data-ttu-id="9d8b4-172">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="9d8b4-172">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>](./Get-AzureRmRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="9d8b4-173">Stop-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="9d8b4-173">Stop-AzureRmRecoveryServicesBackupJob</span></span>](./Stop-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="9d8b4-174">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="9d8b4-174">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


