---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: cbdb60fb4ec139b1dae92b7dd8e2e54675ae1f90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513940"
---
# <span data-ttu-id="ecc3a-101">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="ecc3a-101">Get-AzureRmBackupJob</span></span>

## <span data-ttu-id="ecc3a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ecc3a-102">SYNOPSIS</span></span>
<span data-ttu-id="ecc3a-103">Ottiene i processi di backup.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecc3a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecc3a-104">SYNTAX</span></span>

### <span data-ttu-id="ecc3a-105">FiltersSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ecc3a-105">FiltersSet (Default)</span></span>
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ecc3a-106">JobsListFilter</span><span class="sxs-lookup"><span data-stu-id="ecc3a-106">JobsListFilter</span></span>
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecc3a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ecc3a-107">DESCRIPTION</span></span>
<span data-ttu-id="ecc3a-108">Il cmdlet **Get-AzureRmBackupJob** ottiene i processi di backup di Azure per un Vault specifico.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-108">The **Get-AzureRmBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

## <span data-ttu-id="ecc3a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecc3a-109">EXAMPLES</span></span>

### <span data-ttu-id="ecc3a-110">Esempio 1: ottenere tutti i processi in un caveau di backup</span><span class="sxs-lookup"><span data-stu-id="ecc3a-110">Example 1: Get all jobs in a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="ecc3a-111">Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="ecc3a-111">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="ecc3a-112">Il comando Archivia l'oggetto nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-112">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="ecc3a-113">Il secondo comando consente di ottenere tutti i processi per il Vault in $Vault.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-113">The second command gets all the jobs for the vault in $Vault.</span></span>

### <span data-ttu-id="ecc3a-114">Esempio 2: ottenere processi completati</span><span class="sxs-lookup"><span data-stu-id="ecc3a-114">Example 2: Get completed jobs</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="ecc3a-115">Questo comando ottiene i processi completati dal Vault in $Vault.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-115">This command gets completed jobs from the vault in $Vault.</span></span>

### <span data-ttu-id="ecc3a-116">Esempio 3: ottenere processi non riusciti per l'ultima settimana</span><span class="sxs-lookup"><span data-stu-id="ecc3a-116">Example 3: Get failed jobs for the last week</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

<span data-ttu-id="ecc3a-117">Questo comando restituisce i processi non riusciti dell'ultima settimana dal Vault in $Vault.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-117">This command gets failed jobs from the last week from the vault in $Vault.</span></span>
<span data-ttu-id="ecc3a-118">Il parametro *from* specifica un periodo di sette giorni nel passato.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-118">The *From* parameter specifies a time seven days in the past.</span></span>
<span data-ttu-id="ecc3a-119">Il comando non specifica un valore per il parametro *to* .</span><span class="sxs-lookup"><span data-stu-id="ecc3a-119">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="ecc3a-120">Di conseguenza, usa il valore predefinito dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-120">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="ecc3a-121">Esempio 4: backup del sondaggio per un processo in corso che termina</span><span class="sxs-lookup"><span data-stu-id="ecc3a-121">Example 4: Poll Backup for an in progress job that finishes</span></span>
```
PS C:\>$Jobs = Get-AzureRmBackupJob -Vault $Vault -Status InProgress
$Job = $Jobs[0] 
while ( $Job.Status -ne Completed ) 
{
   Write-Host "Waiting for completion..." 
   Start-Sleep -Seconds 10
   $job = Get-AzureRmBackupJob -Vault $Vault -Job $Job
}
Write-Host "Done!"
Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

<span data-ttu-id="ecc3a-122">Questo script esegue il polling del primo processo che è attualmente in corso fino al completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-122">This script polls the first job that is currently in progress until the job has completed.</span></span>
<span data-ttu-id="ecc3a-123">La prima riga dello script consente di ottenere tutti i processi in $Vault in corso e quindi di archiviarli nella variabile di matrice $Jobs.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-123">The first line of the script gets all the jobs in $Vault that are in progress, and then stores those jobs in the $Jobs array variable.</span></span>
<span data-ttu-id="ecc3a-124">La seconda riga archivia il primo processo dalla matrice $Jobs nella variabile $Job.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-124">The second line stores the first job from the $Jobs array in the $Job variable.</span></span>
<span data-ttu-id="ecc3a-125">La terza riga avvia un ciclo **while** che controlla lo stato corrente del processo fino al completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-125">The third line starts a **while** loop that checks the current status of the job until the job is completed.</span></span>
<span data-ttu-id="ecc3a-126">Per informazioni sulla parola chiave **while** , digitare `Get-Help about_While` .</span><span class="sxs-lookup"><span data-stu-id="ecc3a-126">For information about the **while** keyword, type `Get-Help about_While`.</span></span>
<span data-ttu-id="ecc3a-127">Il ciclo **while** scrive un messaggio nella console, dorme per dieci secondi e quindi aggiorna la variabile $job.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-127">The **while** loop writes a message to the console, sleeps for ten seconds, and then updates the $Job variable.</span></span>
<span data-ttu-id="ecc3a-128">Lo script aggiorna la variabile $Job usando il valore esistente di $Job e il cmdlet corrente per ottenere lo stato corrente del processo.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-128">The script updates the $Job variable by using existing value of $Job and the current cmdlet to get the current status of the job.</span></span>
<span data-ttu-id="ecc3a-129">Per informazioni sui cmdlet di Windows PowerShell, digitare `Get-Help Write-Host` e `Get-Help Start-Sleep` .</span><span class="sxs-lookup"><span data-stu-id="ecc3a-129">For information about the Windows PowerShell cmdlets, type `Get-Help Write-Host` and `Get-Help Start-Sleep`.</span></span>
<span data-ttu-id="ecc3a-130">La riga finale dello script indica che lo script è terminato.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-130">The final line of the script tells you that the script has finished.</span></span>

## <span data-ttu-id="ecc3a-131">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ecc3a-131">PARAMETERS</span></span>

### <span data-ttu-id="ecc3a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecc3a-132">-DefaultProfile</span></span>
<span data-ttu-id="ecc3a-133">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ecc3a-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecc3a-134">-Da</span><span class="sxs-lookup"><span data-stu-id="ecc3a-134">-From</span></span>
<span data-ttu-id="ecc3a-135">Specifica l'inizio, come oggetto **DateTime** , di un intervallo di tempo per i processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-135">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ecc3a-136">Per ottenere un oggetto **DateTime** , usare il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-136">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="ecc3a-137">Per altre informazioni sugli oggetti **DateTime** , digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="ecc3a-137">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecc3a-138">-Job</span><span class="sxs-lookup"><span data-stu-id="ecc3a-138">-Job</span></span>
<span data-ttu-id="ecc3a-139">Specifica un processo ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-139">Specifies a job that this cmdlet gets.</span></span>
<span data-ttu-id="ecc3a-140">Per ottenere un oggetto **AzureRmBackupJob** , usa il cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-140">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecc3a-141">-JobId</span><span class="sxs-lookup"><span data-stu-id="ecc3a-141">-JobId</span></span>
<span data-ttu-id="ecc3a-142">Specifica l'ID di un processo ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-142">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="ecc3a-143">L'ID è la proprietà **InstanceID** di un oggetto **AzureRmBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="ecc3a-143">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="ecc3a-144">Per ottenere un oggetto **AzureRmBackupJob** , USA Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-144">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecc3a-145">-Operazione</span><span class="sxs-lookup"><span data-stu-id="ecc3a-145">-Operation</span></span>
<span data-ttu-id="ecc3a-146">Specifica un'operazione dei processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-146">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ecc3a-147">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecc3a-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ecc3a-148">Backup</span><span class="sxs-lookup"><span data-stu-id="ecc3a-148">Backup</span></span> 
- <span data-ttu-id="ecc3a-149">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="ecc3a-149">ConfigureBackup</span></span> 
- <span data-ttu-id="ecc3a-150">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="ecc3a-150">DeleteBackupData</span></span> 
- <span data-ttu-id="ecc3a-151">Registrare</span><span class="sxs-lookup"><span data-stu-id="ecc3a-151">Register</span></span> 
- <span data-ttu-id="ecc3a-152">Ripristinare</span><span class="sxs-lookup"><span data-stu-id="ecc3a-152">Restore</span></span> 
- <span data-ttu-id="ecc3a-153">Rimuovi protezione</span><span class="sxs-lookup"><span data-stu-id="ecc3a-153">UnProtect</span></span> 
- <span data-ttu-id="ecc3a-154">Unregister</span><span class="sxs-lookup"><span data-stu-id="ecc3a-154">Unregister</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecc3a-155">-Stato</span><span class="sxs-lookup"><span data-stu-id="ecc3a-155">-Status</span></span>
<span data-ttu-id="ecc3a-156">Specifica lo stato dei processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-156">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ecc3a-157">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecc3a-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ecc3a-158">InProgress</span><span class="sxs-lookup"><span data-stu-id="ecc3a-158">InProgress</span></span>
- <span data-ttu-id="ecc3a-159">Fallito</span><span class="sxs-lookup"><span data-stu-id="ecc3a-159">Failed</span></span>
- <span data-ttu-id="ecc3a-160">Annullata</span><span class="sxs-lookup"><span data-stu-id="ecc3a-160">Cancelled</span></span>
- <span data-ttu-id="ecc3a-161">Annullamento</span><span class="sxs-lookup"><span data-stu-id="ecc3a-161">Cancelling</span></span>
- <span data-ttu-id="ecc3a-162">Completato</span><span class="sxs-lookup"><span data-stu-id="ecc3a-162">Completed</span></span>
- <span data-ttu-id="ecc3a-163">CompletedWithWarnings è possibile specificare questo parametro per trovare tutti i processi in corso o tutti i processi non riusciti.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-163">CompletedWithWarnings You can specify this parameter to find all in progress jobs or all failed jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecc3a-164">-To</span><span class="sxs-lookup"><span data-stu-id="ecc3a-164">-To</span></span>
<span data-ttu-id="ecc3a-165">Specifica la fine, come oggetto **DateTime** , di un intervallo di tempo per i processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-165">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ecc3a-166">Il valore predefinito è l'ora di sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-166">The default value is the current system time.</span></span>
<span data-ttu-id="ecc3a-167">Se specifichi questo parametro, devi anche specificare il parametro *from* .</span><span class="sxs-lookup"><span data-stu-id="ecc3a-167">If you specify this parameter, you must also specify the *From* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecc3a-168">-Digitare</span><span class="sxs-lookup"><span data-stu-id="ecc3a-168">-Type</span></span>
<span data-ttu-id="ecc3a-169">Specifica il tipo di contenitore per cui questo cmdlet ottiene i processi di backup.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-169">Specifies the type of container for which this cmdlet gets backup jobs.</span></span>
<span data-ttu-id="ecc3a-170">Attualmente, l'unico valore supportato è AzureVM.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-170">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecc3a-171">-Vault</span><span class="sxs-lookup"><span data-stu-id="ecc3a-171">-Vault</span></span>
<span data-ttu-id="ecc3a-172">Specifica il Vault di backup per cui questo cmdlet ottiene i processi.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-172">Specifies the Backup vault for which this cmdlet gets jobs.</span></span>
<span data-ttu-id="ecc3a-173">Per ottenere un oggetto **AzureRmBackupVault** , usa il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-173">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecc3a-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecc3a-174">CommonParameters</span></span>
<span data-ttu-id="ecc3a-175">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecc3a-176">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecc3a-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecc3a-177">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ecc3a-177">INPUTS</span></span>

### <span data-ttu-id="ecc3a-178">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="ecc3a-178">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="ecc3a-179">Parameters: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ecc3a-179">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="ecc3a-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecc3a-180">OUTPUTS</span></span>

### <span data-ttu-id="ecc3a-181">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="ecc3a-181">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="ecc3a-182">Note</span><span class="sxs-lookup"><span data-stu-id="ecc3a-182">NOTES</span></span>
* <span data-ttu-id="ecc3a-183">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ecc3a-183">None</span></span>

## <span data-ttu-id="ecc3a-184">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecc3a-184">RELATED LINKS</span></span>

[<span data-ttu-id="ecc3a-185">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ecc3a-185">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="ecc3a-186">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="ecc3a-186">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)

[<span data-ttu-id="ecc3a-187">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="ecc3a-187">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


