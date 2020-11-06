---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: 3402dc7018f094a5f95a967385d9bae8d70c68f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512731"
---
# <span data-ttu-id="ada56-101">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="ada56-101">Get-AzureRmBackupJob</span></span>

## <span data-ttu-id="ada56-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ada56-102">SYNOPSIS</span></span>
<span data-ttu-id="ada56-103">Ottiene i processi di backup.</span><span class="sxs-lookup"><span data-stu-id="ada56-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ada56-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ada56-104">SYNTAX</span></span>

### <span data-ttu-id="ada56-105">FiltersSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ada56-105">FiltersSet (Default)</span></span>
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ada56-106">JobsListFilter</span><span class="sxs-lookup"><span data-stu-id="ada56-106">JobsListFilter</span></span>
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ada56-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ada56-107">DESCRIPTION</span></span>
<span data-ttu-id="ada56-108">Il cmdlet **Get-AzureRmBackupJob** ottiene i processi di backup di Azure per un Vault specifico.</span><span class="sxs-lookup"><span data-stu-id="ada56-108">The **Get-AzureRmBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

## <span data-ttu-id="ada56-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ada56-109">EXAMPLES</span></span>

### <span data-ttu-id="ada56-110">Esempio 1: ottenere tutti i processi in un caveau di backup</span><span class="sxs-lookup"><span data-stu-id="ada56-110">Example 1: Get all jobs in a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="ada56-111">Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="ada56-111">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="ada56-112">Il comando Archivia l'oggetto nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="ada56-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="ada56-113">Il secondo comando consente di ottenere tutti i processi per il Vault in $Vault.</span><span class="sxs-lookup"><span data-stu-id="ada56-113">The second command gets all the jobs for the vault in $Vault.</span></span>

### <span data-ttu-id="ada56-114">Esempio 2: ottenere processi completati</span><span class="sxs-lookup"><span data-stu-id="ada56-114">Example 2: Get completed jobs</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="ada56-115">Questo comando ottiene i processi completati dal Vault in $Vault.</span><span class="sxs-lookup"><span data-stu-id="ada56-115">This command gets completed jobs from the vault in $Vault.</span></span>

### <span data-ttu-id="ada56-116">Esempio 3: ottenere processi non riusciti per l'ultima settimana</span><span class="sxs-lookup"><span data-stu-id="ada56-116">Example 3: Get failed jobs for the last week</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

<span data-ttu-id="ada56-117">Questo comando restituisce i processi non riusciti dell'ultima settimana dal Vault in $Vault.</span><span class="sxs-lookup"><span data-stu-id="ada56-117">This command gets failed jobs from the last week from the vault in $Vault.</span></span>
<span data-ttu-id="ada56-118">Il parametro *from* specifica un periodo di sette giorni nel passato.</span><span class="sxs-lookup"><span data-stu-id="ada56-118">The *From* parameter specifies a time seven days in the past.</span></span>
<span data-ttu-id="ada56-119">Il comando non specifica un valore per il parametro *to* .</span><span class="sxs-lookup"><span data-stu-id="ada56-119">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="ada56-120">Di conseguenza, usa il valore predefinito dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="ada56-120">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="ada56-121">Esempio 4: backup del sondaggio per un processo in corso che termina</span><span class="sxs-lookup"><span data-stu-id="ada56-121">Example 4: Poll Backup for an in progress job that finishes</span></span>
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

<span data-ttu-id="ada56-122">Questo script esegue il polling del primo processo che è attualmente in corso fino al completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="ada56-122">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="ada56-123">La prima riga dello script consente di ottenere tutti i processi in $Vault in corso e quindi di archiviarli nella variabile di matrice $Jobs.</span><span class="sxs-lookup"><span data-stu-id="ada56-123">The first line of the script gets all the jobs in $Vault that are in progress, and then stores those jobs in the $Jobs array variable.</span></span>

<span data-ttu-id="ada56-124">La seconda riga archivia il primo processo dalla matrice $Jobs nella variabile $Job.</span><span class="sxs-lookup"><span data-stu-id="ada56-124">The second line stores the first job from the $Jobs array in the $Job variable.</span></span>

<span data-ttu-id="ada56-125">La terza riga avvia un ciclo **while** che controlla lo stato corrente del processo fino al completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="ada56-125">The third line starts a **while** loop that checks the current status of the job until the job is completed.</span></span>
<span data-ttu-id="ada56-126">Per informazioni sulla parola chiave **while** , digitare `Get-Help about_While` .</span><span class="sxs-lookup"><span data-stu-id="ada56-126">For information about the **while** keyword, type `Get-Help about_While`.</span></span>

<span data-ttu-id="ada56-127">Il ciclo **while** scrive un messaggio nella console, dorme per dieci secondi e quindi aggiorna la variabile $job.</span><span class="sxs-lookup"><span data-stu-id="ada56-127">The **while** loop writes a message to the console, sleeps for ten seconds, and then updates the $Job variable.</span></span>
<span data-ttu-id="ada56-128">Lo script aggiorna la variabile $Job usando il valore esistente di $Job e il cmdlet corrente per ottenere lo stato corrente del processo.</span><span class="sxs-lookup"><span data-stu-id="ada56-128">The script updates the $Job variable by using existing value of $Job and the current cmdlet to get the current status of the job.</span></span>
<span data-ttu-id="ada56-129">Per informazioni sui cmdlet di Windows PowerShell, digitare `Get-Help Write-Host` e `Get-Help Start-Sleep` .</span><span class="sxs-lookup"><span data-stu-id="ada56-129">For information about the Windows PowerShell cmdlets, type `Get-Help Write-Host` and `Get-Help Start-Sleep`.</span></span>

<span data-ttu-id="ada56-130">La riga finale dello script indica che lo script è terminato.</span><span class="sxs-lookup"><span data-stu-id="ada56-130">The final line of the script tells you that the script has finished.</span></span>

## <span data-ttu-id="ada56-131">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ada56-131">PARAMETERS</span></span>

### <span data-ttu-id="ada56-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada56-132">-DefaultProfile</span></span>
<span data-ttu-id="ada56-133">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ada56-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada56-134">-Da</span><span class="sxs-lookup"><span data-stu-id="ada56-134">-From</span></span>
<span data-ttu-id="ada56-135">Specifica l'inizio, come oggetto **DateTime** , di un intervallo di tempo per i processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ada56-135">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ada56-136">Per ottenere un oggetto **DateTime** , usare il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="ada56-136">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="ada56-137">Per altre informazioni sugli oggetti **DateTime** , digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="ada56-137">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada56-138">-Job</span><span class="sxs-lookup"><span data-stu-id="ada56-138">-Job</span></span>
<span data-ttu-id="ada56-139">Specifica un processo ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ada56-139">Specifies a job that this cmdlet gets.</span></span>
<span data-ttu-id="ada56-140">Per ottenere un oggetto **AzureRmBackupJob** , usa il cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="ada56-140">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada56-141">-JobId</span><span class="sxs-lookup"><span data-stu-id="ada56-141">-JobId</span></span>
<span data-ttu-id="ada56-142">Specifica l'ID di un processo ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ada56-142">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="ada56-143">L'ID è la proprietà **InstanceID** di un oggetto **AzureRmBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="ada56-143">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="ada56-144">Per ottenere un oggetto **AzureRmBackupJob** , USA Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="ada56-144">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada56-145">-Operazione</span><span class="sxs-lookup"><span data-stu-id="ada56-145">-Operation</span></span>
<span data-ttu-id="ada56-146">Specifica un'operazione dei processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ada56-146">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ada56-147">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ada56-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ada56-148">Backup</span><span class="sxs-lookup"><span data-stu-id="ada56-148">Backup</span></span> 
- <span data-ttu-id="ada56-149">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="ada56-149">ConfigureBackup</span></span> 
- <span data-ttu-id="ada56-150">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="ada56-150">DeleteBackupData</span></span> 
- <span data-ttu-id="ada56-151">Registrare</span><span class="sxs-lookup"><span data-stu-id="ada56-151">Register</span></span> 
- <span data-ttu-id="ada56-152">Ripristinare</span><span class="sxs-lookup"><span data-stu-id="ada56-152">Restore</span></span> 
- <span data-ttu-id="ada56-153">Rimuovi protezione</span><span class="sxs-lookup"><span data-stu-id="ada56-153">UnProtect</span></span> 
- <span data-ttu-id="ada56-154">Unregister</span><span class="sxs-lookup"><span data-stu-id="ada56-154">Unregister</span></span>

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada56-155">-Stato</span><span class="sxs-lookup"><span data-stu-id="ada56-155">-Status</span></span>
<span data-ttu-id="ada56-156">Specifica lo stato dei processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ada56-156">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ada56-157">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ada56-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ada56-158">InProgress</span><span class="sxs-lookup"><span data-stu-id="ada56-158">InProgress</span></span>
- <span data-ttu-id="ada56-159">Fallito</span><span class="sxs-lookup"><span data-stu-id="ada56-159">Failed</span></span>
- <span data-ttu-id="ada56-160">Annullata</span><span class="sxs-lookup"><span data-stu-id="ada56-160">Cancelled</span></span>
- <span data-ttu-id="ada56-161">Annullamento</span><span class="sxs-lookup"><span data-stu-id="ada56-161">Cancelling</span></span>
- <span data-ttu-id="ada56-162">Completato</span><span class="sxs-lookup"><span data-stu-id="ada56-162">Completed</span></span>
- <span data-ttu-id="ada56-163">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="ada56-163">CompletedWithWarnings</span></span> 

<span data-ttu-id="ada56-164">Puoi specificare questo parametro per trovare tutti i processi in corso o tutti i processi non riusciti.</span><span class="sxs-lookup"><span data-stu-id="ada56-164">You can specify this parameter to find all in progress jobs or all failed jobs.</span></span>

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada56-165">-To</span><span class="sxs-lookup"><span data-stu-id="ada56-165">-To</span></span>
<span data-ttu-id="ada56-166">Specifica la fine, come oggetto **DateTime** , di un intervallo di tempo per i processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ada56-166">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ada56-167">Il valore predefinito è l'ora di sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="ada56-167">The default value is the current system time.</span></span>
<span data-ttu-id="ada56-168">Se specifichi questo parametro, devi anche specificare il parametro *from* .</span><span class="sxs-lookup"><span data-stu-id="ada56-168">If you specify this parameter, you must also specify the *From* parameter.</span></span>

```yaml
Type: DateTime
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada56-169">-Digitare</span><span class="sxs-lookup"><span data-stu-id="ada56-169">-Type</span></span>
<span data-ttu-id="ada56-170">Specifica il tipo di contenitore per cui questo cmdlet ottiene i processi di backup.</span><span class="sxs-lookup"><span data-stu-id="ada56-170">Specifies the type of container for which this cmdlet gets backup jobs.</span></span>
<span data-ttu-id="ada56-171">Attualmente, l'unico valore supportato è AzureVM.</span><span class="sxs-lookup"><span data-stu-id="ada56-171">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada56-172">-Vault</span><span class="sxs-lookup"><span data-stu-id="ada56-172">-Vault</span></span>
<span data-ttu-id="ada56-173">Specifica il Vault di backup per cui questo cmdlet ottiene i processi.</span><span class="sxs-lookup"><span data-stu-id="ada56-173">Specifies the Backup vault for which this cmdlet gets jobs.</span></span>
<span data-ttu-id="ada56-174">Per ottenere un oggetto **AzureRmBackupVault** , usa il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="ada56-174">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ada56-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada56-175">CommonParameters</span></span>
<span data-ttu-id="ada56-176">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ada56-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada56-177">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ada56-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada56-178">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ada56-178">INPUTS</span></span>

### <span data-ttu-id="ada56-179">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ada56-179">AzureRmBackupVault</span></span>

## <span data-ttu-id="ada56-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ada56-180">OUTPUTS</span></span>

### <span data-ttu-id="ada56-181">AzureRmBackupJob[]</span><span class="sxs-lookup"><span data-stu-id="ada56-181">AzureRmBackupJob[]</span></span>
<span data-ttu-id="ada56-182">Questo cmdlet restituisce uno o più processi di backup.</span><span class="sxs-lookup"><span data-stu-id="ada56-182">This cmdlet returns one or more Backup jobs.</span></span>

## <span data-ttu-id="ada56-183">Note</span><span class="sxs-lookup"><span data-stu-id="ada56-183">NOTES</span></span>
* <span data-ttu-id="ada56-184">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ada56-184">None</span></span>

## <span data-ttu-id="ada56-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ada56-185">RELATED LINKS</span></span>

[<span data-ttu-id="ada56-186">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ada56-186">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="ada56-187">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="ada56-187">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)

[<span data-ttu-id="ada56-188">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="ada56-188">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


