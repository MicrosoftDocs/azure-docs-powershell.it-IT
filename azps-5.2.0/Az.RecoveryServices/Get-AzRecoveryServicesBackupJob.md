---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 623acc7d96fc6c3dc4f1496f42a53bf276f8e778
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356056"
---
# <span data-ttu-id="fd208-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="fd208-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="fd208-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd208-102">SYNOPSIS</span></span>

<span data-ttu-id="fd208-103">Ottiene i processi di backup.</span><span class="sxs-lookup"><span data-stu-id="fd208-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="fd208-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd208-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd208-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd208-105">DESCRIPTION</span></span>

<span data-ttu-id="fd208-106">Il cmdlet **Get-AzRecoveryServicesBackupJob** ottiene i processi di backup di Azure per un Vault specifico.</span><span class="sxs-lookup"><span data-stu-id="fd208-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="fd208-107">Imposta il contesto del Vault usando il parametro-VaultId.</span><span class="sxs-lookup"><span data-stu-id="fd208-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="fd208-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd208-108">EXAMPLES</span></span>

### <span data-ttu-id="fd208-109">Esempio 1: ottenere tutti i processi in corso</span><span class="sxs-lookup"><span data-stu-id="fd208-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="fd208-110">Il primo comando ottiene lo stato di un processo in corso come matrice e lo archivia nella variabile $Joblist.</span><span class="sxs-lookup"><span data-stu-id="fd208-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="fd208-111">Il secondo comando Visualizza il primo elemento nella matrice $Joblist.</span><span class="sxs-lookup"><span data-stu-id="fd208-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="fd208-112">Esempio 2: ottenere tutti i processi non riusciti negli ultimi 7 giorni</span><span class="sxs-lookup"><span data-stu-id="fd208-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="fd208-113">Questo comando restituisce i processi non riusciti dell'ultima settimana nel Vault.</span><span class="sxs-lookup"><span data-stu-id="fd208-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="fd208-114">Il parametro *from* specifica un tempo di sette giorni nel passato specificato in UTC.</span><span class="sxs-lookup"><span data-stu-id="fd208-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="fd208-115">Il comando non specifica un valore per il parametro *to* .</span><span class="sxs-lookup"><span data-stu-id="fd208-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="fd208-116">Di conseguenza, usa il valore predefinito dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="fd208-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="fd208-117">Esempio 3: ottenere un processo in corso e attendere il completamento</span><span class="sxs-lookup"><span data-stu-id="fd208-117">Example 3: Get an in-progress job and wait for completion</span></span>

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

<span data-ttu-id="fd208-118">Questo script esegue il polling del primo processo che è attualmente in corso fino al completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="fd208-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="fd208-119">Nota: è possibile usare il cmdlet **wait-AzRecoveryServicesBackupJob** per attendere il completamento di un processo di backup di Azure invece del ciclo while.</span><span class="sxs-lookup"><span data-stu-id="fd208-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

### <span data-ttu-id="fd208-120">Esempio 4: ottenere tutti i processi di AzureVM negli ultimi 2 giorni che sono stati completati correttamente</span><span class="sxs-lookup"><span data-stu-id="fd208-120">Example 4: Get all AzureVM jobs in last 2 days which finished successfully</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
<span data-ttu-id="fd208-121">Il primo cmdlet recupera l'oggetto Vault.</span><span class="sxs-lookup"><span data-stu-id="fd208-121">First cmdlet fetches the vault object.</span></span> <span data-ttu-id="fd208-122">Il secondo cmdlet archivia tutti i processi di AzureVM nella volta specificata, che sono stati completati negli ultimi 2 giorni per $jobs.</span><span class="sxs-lookup"><span data-stu-id="fd208-122">Second cmdlet stores all the AzureVM jobs in the given vault which completed in last 2 days to $jobs.</span></span> <span data-ttu-id="fd208-123">Cambiare il valore del parametro BackupManagementType in MAB per recuperare i processi di agente MAB.</span><span class="sxs-lookup"><span data-stu-id="fd208-123">Change the value of BackupManagementType parameter to MAB in order to fetch MAB agent jobs.</span></span>

## <span data-ttu-id="fd208-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd208-124">PARAMETERS</span></span>

### <span data-ttu-id="fd208-125">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="fd208-125">-BackupManagementType</span></span>

<span data-ttu-id="fd208-126">Classe di risorse protette.</span><span class="sxs-lookup"><span data-stu-id="fd208-126">The class of resources being protected.</span></span> <span data-ttu-id="fd208-127">Attualmente i valori supportati per questo cmdlet sono AzureVM, AzureStorage, AzureWorkload, MAB.</span><span class="sxs-lookup"><span data-stu-id="fd208-127">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload, MAB.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload, MAB

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd208-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd208-128">-DefaultProfile</span></span>

<span data-ttu-id="fd208-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd208-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd208-130">-Da</span><span class="sxs-lookup"><span data-stu-id="fd208-130">-From</span></span>

<span data-ttu-id="fd208-131">Specifica l'inizio, come oggetto **DateTime** , di un intervallo di tempo per i processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd208-131">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="fd208-132">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="fd208-132">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="fd208-133">Per altre informazioni sugli oggetti **DateTime** , digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="fd208-133">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="fd208-134">Usare il formato UTC per le date.</span><span class="sxs-lookup"><span data-stu-id="fd208-134">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="fd208-135">-Job</span><span class="sxs-lookup"><span data-stu-id="fd208-135">-Job</span></span>

<span data-ttu-id="fd208-136">Specifica il processo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="fd208-136">Specifies the job to get.</span></span>

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

### <span data-ttu-id="fd208-137">-JobId</span><span class="sxs-lookup"><span data-stu-id="fd208-137">-JobId</span></span>

<span data-ttu-id="fd208-138">Specifica l'ID di un processo ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd208-138">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="fd208-139">L'ID è la proprietà JobId di un oggetto **Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase** .</span><span class="sxs-lookup"><span data-stu-id="fd208-139">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="fd208-140">-Operazione</span><span class="sxs-lookup"><span data-stu-id="fd208-140">-Operation</span></span>

<span data-ttu-id="fd208-141">Specifica un'operazione dei processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd208-141">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="fd208-142">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="fd208-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fd208-143">Backup</span><span class="sxs-lookup"><span data-stu-id="fd208-143">Backup</span></span>
- <span data-ttu-id="fd208-144">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="fd208-144">ConfigureBackup</span></span>
- <span data-ttu-id="fd208-145">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="fd208-145">DeleteBackupData</span></span>
- <span data-ttu-id="fd208-146">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="fd208-146">DisableBackup</span></span>
- <span data-ttu-id="fd208-147">Ripristinare</span><span class="sxs-lookup"><span data-stu-id="fd208-147">Restore</span></span>
- <span data-ttu-id="fd208-148">BackupDataMove</span><span class="sxs-lookup"><span data-stu-id="fd208-148">BackupDataMove</span></span>

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

### <span data-ttu-id="fd208-149">-Stato</span><span class="sxs-lookup"><span data-stu-id="fd208-149">-Status</span></span>

<span data-ttu-id="fd208-150">Specifica lo stato dei processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd208-150">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="fd208-151">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="fd208-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fd208-152">InProgress</span><span class="sxs-lookup"><span data-stu-id="fd208-152">InProgress</span></span>
- <span data-ttu-id="fd208-153">Fallito</span><span class="sxs-lookup"><span data-stu-id="fd208-153">Failed</span></span>
- <span data-ttu-id="fd208-154">Annullata</span><span class="sxs-lookup"><span data-stu-id="fd208-154">Cancelled</span></span>
- <span data-ttu-id="fd208-155">Annullamento</span><span class="sxs-lookup"><span data-stu-id="fd208-155">Cancelling</span></span>
- <span data-ttu-id="fd208-156">Completato</span><span class="sxs-lookup"><span data-stu-id="fd208-156">Completed</span></span>
- <span data-ttu-id="fd208-157">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="fd208-157">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="fd208-158">-To</span><span class="sxs-lookup"><span data-stu-id="fd208-158">-To</span></span>

<span data-ttu-id="fd208-159">Specifica la fine, come oggetto **DateTime** , di un intervallo di tempo per i processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd208-159">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="fd208-160">Il valore predefinito è l'ora di sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="fd208-160">The default value is the current system time.</span></span>
<span data-ttu-id="fd208-161">Se specifichi questo parametro, devi anche specificare il parametro **-from** .</span><span class="sxs-lookup"><span data-stu-id="fd208-161">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="fd208-162">Usare il formato UTC per le date.</span><span class="sxs-lookup"><span data-stu-id="fd208-162">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="fd208-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="fd208-163">-VaultId</span></span>

<span data-ttu-id="fd208-164">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="fd208-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="fd208-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd208-165">CommonParameters</span></span>
<span data-ttu-id="fd208-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd208-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd208-167">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd208-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd208-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd208-168">INPUTS</span></span>

### <span data-ttu-id="fd208-169">System. String</span><span class="sxs-lookup"><span data-stu-id="fd208-169">System.String</span></span>

## <span data-ttu-id="fd208-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd208-170">OUTPUTS</span></span>

### <span data-ttu-id="fd208-171">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="fd208-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="fd208-172">Note</span><span class="sxs-lookup"><span data-stu-id="fd208-172">NOTES</span></span>

## <span data-ttu-id="fd208-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd208-173">RELATED LINKS</span></span>

[<span data-ttu-id="fd208-174">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="fd208-174">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="fd208-175">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="fd208-175">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="fd208-176">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="fd208-176">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
