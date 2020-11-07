---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: cc23d8535e7aaca656379811121ed09bad2f64bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855745"
---
# <span data-ttu-id="0cc95-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="0cc95-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="0cc95-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0cc95-102">SYNOPSIS</span></span>

<span data-ttu-id="0cc95-103">Ottiene i processi di backup.</span><span class="sxs-lookup"><span data-stu-id="0cc95-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="0cc95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0cc95-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cc95-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0cc95-105">DESCRIPTION</span></span>

<span data-ttu-id="0cc95-106">Il cmdlet **Get-AzRecoveryServicesBackupJob** ottiene i processi di backup di Azure per un Vault specifico.</span><span class="sxs-lookup"><span data-stu-id="0cc95-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="0cc95-107">Imposta il contesto del Vault usando il parametro-VaultId.</span><span class="sxs-lookup"><span data-stu-id="0cc95-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="0cc95-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0cc95-108">EXAMPLES</span></span>

### <span data-ttu-id="0cc95-109">Esempio 1: ottenere tutti i processi in corso</span><span class="sxs-lookup"><span data-stu-id="0cc95-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="0cc95-110">Il primo comando ottiene lo stato di un processo in corso come matrice e lo archivia nella variabile $Joblist.</span><span class="sxs-lookup"><span data-stu-id="0cc95-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="0cc95-111">Il secondo comando Visualizza il primo elemento nella matrice $Joblist.</span><span class="sxs-lookup"><span data-stu-id="0cc95-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="0cc95-112">Esempio 2: ottenere tutti i processi non riusciti negli ultimi 7 giorni</span><span class="sxs-lookup"><span data-stu-id="0cc95-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="0cc95-113">Questo comando restituisce i processi non riusciti dell'ultima settimana nel Vault.</span><span class="sxs-lookup"><span data-stu-id="0cc95-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="0cc95-114">Il parametro *from* specifica un tempo di sette giorni nel passato specificato in UTC.</span><span class="sxs-lookup"><span data-stu-id="0cc95-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="0cc95-115">Il comando non specifica un valore per il parametro *to* .</span><span class="sxs-lookup"><span data-stu-id="0cc95-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="0cc95-116">Di conseguenza, usa il valore predefinito dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="0cc95-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="0cc95-117">Esempio 3: ottenere un processo in corso e attendere il completamento</span><span class="sxs-lookup"><span data-stu-id="0cc95-117">Example 3: Get an in-progress job and wait for completion</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
$Job = $Jobs[0]
While ( $Job.Status -ne Completed ) {
    Write-Host -Object "Waiting for completion..."
    Start-Sleep -Seconds 10
    $Job = Get-AzRecoveryServicesBackupJob -Job $Job -VaultId $vault.ID
}
Write-Host -Object "Done!"

Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

<span data-ttu-id="0cc95-118">Questo script esegue il polling del primo processo che è attualmente in corso fino al completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="0cc95-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="0cc95-119">Nota: è possibile usare il cmdlet **wait-AzRecoveryServicesBackupJob** per attendere il completamento di un processo di backup di Azure invece del ciclo while.</span><span class="sxs-lookup"><span data-stu-id="0cc95-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

## <span data-ttu-id="0cc95-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0cc95-120">PARAMETERS</span></span>

### <span data-ttu-id="0cc95-121">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="0cc95-121">-BackupManagementType</span></span>

<span data-ttu-id="0cc95-122">Specifica il tipo di gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="0cc95-122">Specifies the Backup management type.</span></span>
<span data-ttu-id="0cc95-123">Attualmente è supportato solo AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="0cc95-123">Currently, only AzureVM, AzureStorage is supported.</span></span>

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

### <span data-ttu-id="0cc95-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cc95-124">-DefaultProfile</span></span>

<span data-ttu-id="0cc95-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0cc95-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cc95-126">-Da</span><span class="sxs-lookup"><span data-stu-id="0cc95-126">-From</span></span>

<span data-ttu-id="0cc95-127">Specifica l'inizio, come oggetto **DateTime** , di un intervallo di tempo per i processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cc95-127">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="0cc95-128">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="0cc95-128">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="0cc95-129">Per altre informazioni sugli oggetti **DateTime** , digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="0cc95-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="0cc95-130">Usare il formato UTC per le date.</span><span class="sxs-lookup"><span data-stu-id="0cc95-130">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="0cc95-131">-Job</span><span class="sxs-lookup"><span data-stu-id="0cc95-131">-Job</span></span>

<span data-ttu-id="0cc95-132">Specifica il processo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="0cc95-132">Specifies the job to get.</span></span>

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

### <span data-ttu-id="0cc95-133">-JobId</span><span class="sxs-lookup"><span data-stu-id="0cc95-133">-JobId</span></span>

<span data-ttu-id="0cc95-134">Specifica l'ID di un processo ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cc95-134">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="0cc95-135">L'ID è la proprietà JobId di un oggetto **Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase** .</span><span class="sxs-lookup"><span data-stu-id="0cc95-135">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="0cc95-136">-Operazione</span><span class="sxs-lookup"><span data-stu-id="0cc95-136">-Operation</span></span>

<span data-ttu-id="0cc95-137">Specifica un'operazione dei processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cc95-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="0cc95-138">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0cc95-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0cc95-139">Backup</span><span class="sxs-lookup"><span data-stu-id="0cc95-139">Backup</span></span>
- <span data-ttu-id="0cc95-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="0cc95-140">ConfigureBackup</span></span>
- <span data-ttu-id="0cc95-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="0cc95-141">DeleteBackupData</span></span>
- <span data-ttu-id="0cc95-142">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="0cc95-142">DisableBackup</span></span>
- <span data-ttu-id="0cc95-143">Ripristinare</span><span class="sxs-lookup"><span data-stu-id="0cc95-143">Restore</span></span>

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

### <span data-ttu-id="0cc95-144">-Stato</span><span class="sxs-lookup"><span data-stu-id="0cc95-144">-Status</span></span>

<span data-ttu-id="0cc95-145">Specifica lo stato dei processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cc95-145">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="0cc95-146">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0cc95-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0cc95-147">InProgress</span><span class="sxs-lookup"><span data-stu-id="0cc95-147">InProgress</span></span>
- <span data-ttu-id="0cc95-148">Fallito</span><span class="sxs-lookup"><span data-stu-id="0cc95-148">Failed</span></span>
- <span data-ttu-id="0cc95-149">Annullata</span><span class="sxs-lookup"><span data-stu-id="0cc95-149">Cancelled</span></span>
- <span data-ttu-id="0cc95-150">Annullamento</span><span class="sxs-lookup"><span data-stu-id="0cc95-150">Cancelling</span></span>
- <span data-ttu-id="0cc95-151">Completato</span><span class="sxs-lookup"><span data-stu-id="0cc95-151">Completed</span></span>
- <span data-ttu-id="0cc95-152">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="0cc95-152">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="0cc95-153">-To</span><span class="sxs-lookup"><span data-stu-id="0cc95-153">-To</span></span>

<span data-ttu-id="0cc95-154">Specifica la fine, come oggetto **DateTime** , di un intervallo di tempo per i processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cc95-154">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="0cc95-155">Il valore predefinito è l'ora di sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="0cc95-155">The default value is the current system time.</span></span>
<span data-ttu-id="0cc95-156">Se specifichi questo parametro, devi anche specificare il parametro **-from** .</span><span class="sxs-lookup"><span data-stu-id="0cc95-156">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="0cc95-157">Usare il formato UTC per le date.</span><span class="sxs-lookup"><span data-stu-id="0cc95-157">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="0cc95-158">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0cc95-158">-VaultId</span></span>

<span data-ttu-id="0cc95-159">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0cc95-159">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0cc95-160">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cc95-160">-CommonParameters</span></span>

<span data-ttu-id="0cc95-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cc95-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cc95-162">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0cc95-162">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cc95-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0cc95-163">INPUTS</span></span>

### <span data-ttu-id="0cc95-164">System. String</span><span class="sxs-lookup"><span data-stu-id="0cc95-164">System.String</span></span>

## <span data-ttu-id="0cc95-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0cc95-165">OUTPUTS</span></span>

### <span data-ttu-id="0cc95-166">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="0cc95-166">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="0cc95-167">Note</span><span class="sxs-lookup"><span data-stu-id="0cc95-167">NOTES</span></span>

## <span data-ttu-id="0cc95-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0cc95-168">RELATED LINKS</span></span>

[<span data-ttu-id="0cc95-169">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="0cc95-169">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="0cc95-170">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="0cc95-170">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="0cc95-171">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="0cc95-171">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
