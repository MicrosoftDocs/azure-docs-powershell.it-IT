---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: 48c1a3c3b7422f76bfbea0fbff8c3df541764606
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510752"
---
# <span data-ttu-id="96e7c-101">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="96e7c-101">Get-AzureRmBackupJob</span></span>

## <span data-ttu-id="96e7c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="96e7c-103">Ottiene i processi di backup.</span><span class="sxs-lookup"><span data-stu-id="96e7c-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96e7c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96e7c-104">SYNTAX</span></span>

### <span data-ttu-id="96e7c-105">FiltersSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="96e7c-105">FiltersSet (Default)</span></span>
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="96e7c-106">JobsListFilter</span><span class="sxs-lookup"><span data-stu-id="96e7c-106">JobsListFilter</span></span>
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96e7c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96e7c-107">DESCRIPTION</span></span>
<span data-ttu-id="96e7c-108">Il cmdlet **Get-AzureRmBackupJob** ottiene i processi di backup di Azure per un Vault specifico.</span><span class="sxs-lookup"><span data-stu-id="96e7c-108">The **Get-AzureRmBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

## <span data-ttu-id="96e7c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96e7c-109">EXAMPLES</span></span>

### <span data-ttu-id="96e7c-110">Esempio 1: ottenere tutti i processi in un caveau di backup</span><span class="sxs-lookup"><span data-stu-id="96e7c-110">Example 1: Get all jobs in a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="96e7c-111">Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="96e7c-111">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="96e7c-112">Il comando Archivia l'oggetto nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="96e7c-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="96e7c-113">Il secondo comando consente di ottenere tutti i processi per il Vault in $Vault.</span><span class="sxs-lookup"><span data-stu-id="96e7c-113">The second command gets all the jobs for the vault in $Vault.</span></span>

### <span data-ttu-id="96e7c-114">Esempio 2: ottenere processi completati</span><span class="sxs-lookup"><span data-stu-id="96e7c-114">Example 2: Get completed jobs</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="96e7c-115">Questo comando ottiene i processi completati dal Vault in $Vault.</span><span class="sxs-lookup"><span data-stu-id="96e7c-115">This command gets completed jobs from the vault in $Vault.</span></span>

### <span data-ttu-id="96e7c-116">Esempio 3: ottenere processi non riusciti per l'ultima settimana</span><span class="sxs-lookup"><span data-stu-id="96e7c-116">Example 3: Get failed jobs for the last week</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

<span data-ttu-id="96e7c-117">Questo comando restituisce i processi non riusciti dell'ultima settimana dal Vault in $Vault.</span><span class="sxs-lookup"><span data-stu-id="96e7c-117">This command gets failed jobs from the last week from the vault in $Vault.</span></span>
<span data-ttu-id="96e7c-118">Il parametro *from* specifica un periodo di sette giorni nel passato.</span><span class="sxs-lookup"><span data-stu-id="96e7c-118">The *From* parameter specifies a time seven days in the past.</span></span>
<span data-ttu-id="96e7c-119">Il comando non specifica un valore per il parametro *to* .</span><span class="sxs-lookup"><span data-stu-id="96e7c-119">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="96e7c-120">Di conseguenza, usa il valore predefinito dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="96e7c-120">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="96e7c-121">Esempio 4: backup del sondaggio per un processo in corso che termina</span><span class="sxs-lookup"><span data-stu-id="96e7c-121">Example 4: Poll Backup for an in progress job that finishes</span></span>
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

<span data-ttu-id="96e7c-122">Questo script esegue il polling del primo processo che è attualmente in corso fino al completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="96e7c-122">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="96e7c-123">La prima riga dello script consente di ottenere tutti i processi in $Vault in corso e quindi di archiviarli nella variabile di matrice $Jobs.</span><span class="sxs-lookup"><span data-stu-id="96e7c-123">The first line of the script gets all the jobs in $Vault that are in progress, and then stores those jobs in the $Jobs array variable.</span></span>

<span data-ttu-id="96e7c-124">La seconda riga archivia il primo processo dalla matrice $Jobs nella variabile $Job.</span><span class="sxs-lookup"><span data-stu-id="96e7c-124">The second line stores the first job from the $Jobs array in the $Job variable.</span></span>

<span data-ttu-id="96e7c-125">La terza riga avvia un ciclo **while** che controlla lo stato corrente del processo fino al completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="96e7c-125">The third line starts a **while** loop that checks the current status of the job until the job is completed.</span></span>
<span data-ttu-id="96e7c-126">Per informazioni sulla parola chiave **while** , digitare `Get-Help about_While` .</span><span class="sxs-lookup"><span data-stu-id="96e7c-126">For information about the **while** keyword, type `Get-Help about_While`.</span></span>

<span data-ttu-id="96e7c-127">Il ciclo **while** scrive un messaggio nella console, dorme per dieci secondi e quindi aggiorna la variabile $job.</span><span class="sxs-lookup"><span data-stu-id="96e7c-127">The **while** loop writes a message to the console, sleeps for ten seconds, and then updates the $Job variable.</span></span>
<span data-ttu-id="96e7c-128">Lo script aggiorna la variabile $Job usando il valore esistente di $Job e il cmdlet corrente per ottenere lo stato corrente del processo.</span><span class="sxs-lookup"><span data-stu-id="96e7c-128">The script updates the $Job variable by using existing value of $Job and the current cmdlet to get the current status of the job.</span></span>
<span data-ttu-id="96e7c-129">Per informazioni sui cmdlet di Windows PowerShell, digitare `Get-Help Write-Host` e `Get-Help Start-Sleep` .</span><span class="sxs-lookup"><span data-stu-id="96e7c-129">For information about the Windows PowerShell cmdlets, type `Get-Help Write-Host` and `Get-Help Start-Sleep`.</span></span>

<span data-ttu-id="96e7c-130">La riga finale dello script indica che lo script è terminato.</span><span class="sxs-lookup"><span data-stu-id="96e7c-130">The final line of the script tells you that the script has finished.</span></span>

## <span data-ttu-id="96e7c-131">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96e7c-131">PARAMETERS</span></span>

### <span data-ttu-id="96e7c-132">-Da</span><span class="sxs-lookup"><span data-stu-id="96e7c-132">-From</span></span>
<span data-ttu-id="96e7c-133">Specifica l'inizio, come oggetto **DateTime** , di un intervallo di tempo per i processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96e7c-133">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="96e7c-134">Per ottenere un oggetto **DateTime** , usare il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="96e7c-134">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="96e7c-135">Per altre informazioni sugli oggetti **DateTime** , digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="96e7c-135">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="96e7c-136">-Job</span><span class="sxs-lookup"><span data-stu-id="96e7c-136">-Job</span></span>
<span data-ttu-id="96e7c-137">Specifica un processo ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96e7c-137">Specifies a job that this cmdlet gets.</span></span>
<span data-ttu-id="96e7c-138">Per ottenere un oggetto **AzureRmBackupJob** , usa il cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="96e7c-138">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="96e7c-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="96e7c-139">-JobId</span></span>
<span data-ttu-id="96e7c-140">Specifica l'ID di un processo ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96e7c-140">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="96e7c-141">L'ID è la proprietà **InstanceID** di un oggetto **AzureRmBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="96e7c-141">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="96e7c-142">Per ottenere un oggetto **AzureRmBackupJob** , USA Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="96e7c-142">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

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

### <span data-ttu-id="96e7c-143">-Operazione</span><span class="sxs-lookup"><span data-stu-id="96e7c-143">-Operation</span></span>
<span data-ttu-id="96e7c-144">Specifica un'operazione dei processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96e7c-144">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="96e7c-145">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="96e7c-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="96e7c-146">Backup</span><span class="sxs-lookup"><span data-stu-id="96e7c-146">Backup</span></span> 
- <span data-ttu-id="96e7c-147">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="96e7c-147">ConfigureBackup</span></span> 
- <span data-ttu-id="96e7c-148">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="96e7c-148">DeleteBackupData</span></span> 
- <span data-ttu-id="96e7c-149">Registrare</span><span class="sxs-lookup"><span data-stu-id="96e7c-149">Register</span></span> 
- <span data-ttu-id="96e7c-150">Ripristinare</span><span class="sxs-lookup"><span data-stu-id="96e7c-150">Restore</span></span> 
- <span data-ttu-id="96e7c-151">Rimuovi protezione</span><span class="sxs-lookup"><span data-stu-id="96e7c-151">UnProtect</span></span> 
- <span data-ttu-id="96e7c-152">Unregister</span><span class="sxs-lookup"><span data-stu-id="96e7c-152">Unregister</span></span>

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

### <span data-ttu-id="96e7c-153">-Stato</span><span class="sxs-lookup"><span data-stu-id="96e7c-153">-Status</span></span>
<span data-ttu-id="96e7c-154">Specifica lo stato dei processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96e7c-154">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="96e7c-155">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="96e7c-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="96e7c-156">InProgress</span><span class="sxs-lookup"><span data-stu-id="96e7c-156">InProgress</span></span>
- <span data-ttu-id="96e7c-157">Fallito</span><span class="sxs-lookup"><span data-stu-id="96e7c-157">Failed</span></span>
- <span data-ttu-id="96e7c-158">Annullata</span><span class="sxs-lookup"><span data-stu-id="96e7c-158">Cancelled</span></span>
- <span data-ttu-id="96e7c-159">Annullamento</span><span class="sxs-lookup"><span data-stu-id="96e7c-159">Cancelling</span></span>
- <span data-ttu-id="96e7c-160">Completato</span><span class="sxs-lookup"><span data-stu-id="96e7c-160">Completed</span></span>
- <span data-ttu-id="96e7c-161">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="96e7c-161">CompletedWithWarnings</span></span> 

<span data-ttu-id="96e7c-162">Puoi specificare questo parametro per trovare tutti i processi in corso o tutti i processi non riusciti.</span><span class="sxs-lookup"><span data-stu-id="96e7c-162">You can specify this parameter to find all in progress jobs or all failed jobs.</span></span>

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

### <span data-ttu-id="96e7c-163">-To</span><span class="sxs-lookup"><span data-stu-id="96e7c-163">-To</span></span>
<span data-ttu-id="96e7c-164">Specifica la fine, come oggetto **DateTime** , di un intervallo di tempo per i processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96e7c-164">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="96e7c-165">Il valore predefinito è l'ora di sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="96e7c-165">The default value is the current system time.</span></span>
<span data-ttu-id="96e7c-166">Se specifichi questo parametro, devi anche specificare il parametro *from* .</span><span class="sxs-lookup"><span data-stu-id="96e7c-166">If you specify this parameter, you must also specify the *From* parameter.</span></span>

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

### <span data-ttu-id="96e7c-167">-Digitare</span><span class="sxs-lookup"><span data-stu-id="96e7c-167">-Type</span></span>
<span data-ttu-id="96e7c-168">Specifica il tipo di contenitore per cui questo cmdlet ottiene i processi di backup.</span><span class="sxs-lookup"><span data-stu-id="96e7c-168">Specifies the type of container for which this cmdlet gets backup jobs.</span></span>
<span data-ttu-id="96e7c-169">Attualmente, l'unico valore supportato è AzureVM.</span><span class="sxs-lookup"><span data-stu-id="96e7c-169">Currently, the only supported value is AzureVM.</span></span>

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

### <span data-ttu-id="96e7c-170">-Vault</span><span class="sxs-lookup"><span data-stu-id="96e7c-170">-Vault</span></span>
<span data-ttu-id="96e7c-171">Specifica il Vault di backup per cui questo cmdlet ottiene i processi.</span><span class="sxs-lookup"><span data-stu-id="96e7c-171">Specifies the Backup vault for which this cmdlet gets jobs.</span></span>
<span data-ttu-id="96e7c-172">Per ottenere un oggetto **AzureRmBackupVault** , usa il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="96e7c-172">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="96e7c-173">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96e7c-173">-DefaultProfile</span></span>
<span data-ttu-id="96e7c-174">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96e7c-174">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96e7c-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96e7c-175">CommonParameters</span></span>
<span data-ttu-id="96e7c-176">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96e7c-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96e7c-177">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96e7c-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96e7c-178">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96e7c-178">INPUTS</span></span>

### <span data-ttu-id="96e7c-179">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="96e7c-179">AzureRmBackupVault</span></span>

## <span data-ttu-id="96e7c-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96e7c-180">OUTPUTS</span></span>

### <span data-ttu-id="96e7c-181">AzureRmBackupJob[]</span><span class="sxs-lookup"><span data-stu-id="96e7c-181">AzureRmBackupJob[]</span></span>
<span data-ttu-id="96e7c-182">Questo cmdlet restituisce uno o più processi di backup.</span><span class="sxs-lookup"><span data-stu-id="96e7c-182">This cmdlet returns one or more Backup jobs.</span></span>

## <span data-ttu-id="96e7c-183">Note</span><span class="sxs-lookup"><span data-stu-id="96e7c-183">NOTES</span></span>
* <span data-ttu-id="96e7c-184">Nessuno</span><span class="sxs-lookup"><span data-stu-id="96e7c-184">None</span></span>

## <span data-ttu-id="96e7c-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96e7c-185">RELATED LINKS</span></span>

[<span data-ttu-id="96e7c-186">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="96e7c-186">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="96e7c-187">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="96e7c-187">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)

[<span data-ttu-id="96e7c-188">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="96e7c-188">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


