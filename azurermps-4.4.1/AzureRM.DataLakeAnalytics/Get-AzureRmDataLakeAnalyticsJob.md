---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 6a172de918e8b0675abaf01edf2ec198dae75b5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521700"
---
# <span data-ttu-id="d9e84-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d9e84-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="d9e84-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9e84-102">SYNOPSIS</span></span>
<span data-ttu-id="d9e84-103">Ottiene un processo di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="d9e84-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9e84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9e84-104">SYNTAX</span></span>

### <span data-ttu-id="d9e84-105">Tutti in gruppo risorse e account (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d9e84-105">All In Resource Group and Account (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9e84-106">JobInformation specifico</span><span class="sxs-lookup"><span data-stu-id="d9e84-106">Specific JobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9e84-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9e84-107">DESCRIPTION</span></span>
<span data-ttu-id="d9e84-108">Il cmdlet **Get-AzureRmDataLakeAnalyticsJob** ottiene un processo di analisi del Lago di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="d9e84-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="d9e84-109">Se non specifichi un processo, questo cmdlet ottiene tutti i processi.</span><span class="sxs-lookup"><span data-stu-id="d9e84-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="d9e84-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9e84-110">EXAMPLES</span></span>

### <span data-ttu-id="d9e84-111">Esempio 1: ottenere un processo specificato</span><span class="sxs-lookup"><span data-stu-id="d9e84-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="d9e84-112">Questo comando ottiene il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="d9e84-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="d9e84-113">Esempio 2: ottenere processi inviati nell'ultima settimana</span><span class="sxs-lookup"><span data-stu-id="d9e84-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="d9e84-114">Questo comando consente di ottenere i processi inviati nell'ultima settimana.</span><span class="sxs-lookup"><span data-stu-id="d9e84-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="d9e84-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9e84-115">PARAMETERS</span></span>

### <span data-ttu-id="d9e84-116">-Account</span><span class="sxs-lookup"><span data-stu-id="d9e84-116">-Account</span></span>
<span data-ttu-id="d9e84-117">Specifica il nome di un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="d9e84-117">Specifies the name of a Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e84-118">-Includi</span><span class="sxs-lookup"><span data-stu-id="d9e84-118">-Include</span></span>
<span data-ttu-id="d9e84-119">Specifica le opzioni che indicano il tipo di informazioni aggiuntive da recuperare sul processo.</span><span class="sxs-lookup"><span data-stu-id="d9e84-119">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="d9e84-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d9e84-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d9e84-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d9e84-121">None</span></span>
- <span data-ttu-id="d9e84-122">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="d9e84-122">DebugInfo</span></span>
- <span data-ttu-id="d9e84-123">Statistiche</span><span class="sxs-lookup"><span data-stu-id="d9e84-123">Statistics</span></span>
- <span data-ttu-id="d9e84-124">Tutti</span><span class="sxs-lookup"><span data-stu-id="d9e84-124">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: Specific JobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e84-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="d9e84-125">-JobId</span></span>
<span data-ttu-id="d9e84-126">Specifica l'ID del processo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="d9e84-126">Specifies the ID of the job to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Specific JobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e84-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9e84-127">-Name</span></span>
<span data-ttu-id="d9e84-128">Specifica un nome da usare per filtrare i risultati dell'elenco processi.</span><span class="sxs-lookup"><span data-stu-id="d9e84-128">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="d9e84-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d9e84-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d9e84-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d9e84-130">None</span></span>
- <span data-ttu-id="d9e84-131">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="d9e84-131">DebugInfo</span></span>
- <span data-ttu-id="d9e84-132">Statistiche</span><span class="sxs-lookup"><span data-stu-id="d9e84-132">Statistics</span></span>
- <span data-ttu-id="d9e84-133">Tutti</span><span class="sxs-lookup"><span data-stu-id="d9e84-133">All</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e84-134">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="d9e84-134">-PipelineId</span></span>
<span data-ttu-id="d9e84-135">Un ID facoltativo che indica solo i processi parte della pipeline specificata deve essere restituito.</span><span class="sxs-lookup"><span data-stu-id="d9e84-135">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e84-136">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="d9e84-136">-RecurrenceId</span></span>
<span data-ttu-id="d9e84-137">Un ID facoltativo che indica solo i processi parte della ricorrenza specificata deve essere restituito.</span><span class="sxs-lookup"><span data-stu-id="d9e84-137">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e84-138">-Risultato</span><span class="sxs-lookup"><span data-stu-id="d9e84-138">-Result</span></span>
<span data-ttu-id="d9e84-139">Specifica un filtro di risultato per i risultati del processo.</span><span class="sxs-lookup"><span data-stu-id="d9e84-139">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="d9e84-140">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d9e84-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d9e84-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d9e84-141">None</span></span>
- <span data-ttu-id="d9e84-142">Annullata</span><span class="sxs-lookup"><span data-stu-id="d9e84-142">Cancelled</span></span>
- <span data-ttu-id="d9e84-143">Fallito</span><span class="sxs-lookup"><span data-stu-id="d9e84-143">Failed</span></span>
- <span data-ttu-id="d9e84-144">Succeeded</span><span class="sxs-lookup"><span data-stu-id="d9e84-144">Succeeded</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e84-145">-Stato</span><span class="sxs-lookup"><span data-stu-id="d9e84-145">-State</span></span>
<span data-ttu-id="d9e84-146">Specifica un filtro di stato per i risultati del processo.</span><span class="sxs-lookup"><span data-stu-id="d9e84-146">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="d9e84-147">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d9e84-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d9e84-148">Accettato</span><span class="sxs-lookup"><span data-stu-id="d9e84-148">Accepted</span></span>
- <span data-ttu-id="d9e84-149">Nuovo</span><span class="sxs-lookup"><span data-stu-id="d9e84-149">New</span></span>
- <span data-ttu-id="d9e84-150">Compilazione</span><span class="sxs-lookup"><span data-stu-id="d9e84-150">Compiling</span></span>
- <span data-ttu-id="d9e84-151">Pianificazione</span><span class="sxs-lookup"><span data-stu-id="d9e84-151">Scheduling</span></span>
- <span data-ttu-id="d9e84-152">Accodati</span><span class="sxs-lookup"><span data-stu-id="d9e84-152">Queued</span></span>
- <span data-ttu-id="d9e84-153">Iniziale</span><span class="sxs-lookup"><span data-stu-id="d9e84-153">Starting</span></span>
- <span data-ttu-id="d9e84-154">In pausa</span><span class="sxs-lookup"><span data-stu-id="d9e84-154">Paused</span></span>
- <span data-ttu-id="d9e84-155">Esecuzione</span><span class="sxs-lookup"><span data-stu-id="d9e84-155">Running</span></span>
- <span data-ttu-id="d9e84-156">Terminato</span><span class="sxs-lookup"><span data-stu-id="d9e84-156">Ended</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e84-157">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="d9e84-157">-SubmittedAfter</span></span>
<span data-ttu-id="d9e84-158">Specifica un filtro data.</span><span class="sxs-lookup"><span data-stu-id="d9e84-158">Specifies a date filter.</span></span>
<span data-ttu-id="d9e84-159">Usa questo parametro per filtrare il risultato dell'elenco processi in processi inviati dopo la data specificata.</span><span class="sxs-lookup"><span data-stu-id="d9e84-159">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e84-160">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="d9e84-160">-SubmittedBefore</span></span>
<span data-ttu-id="d9e84-161">Specifica un filtro data.</span><span class="sxs-lookup"><span data-stu-id="d9e84-161">Specifies a date filter.</span></span>
<span data-ttu-id="d9e84-162">Usa questo parametro per filtrare il risultato dell'elenco processi in processi inviati prima della data specificata.</span><span class="sxs-lookup"><span data-stu-id="d9e84-162">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e84-163">-Mittente</span><span class="sxs-lookup"><span data-stu-id="d9e84-163">-Submitter</span></span>
<span data-ttu-id="d9e84-164">Specifica l'indirizzo di posta elettronica di un utente.</span><span class="sxs-lookup"><span data-stu-id="d9e84-164">Specifies the email address of a user.</span></span>
<span data-ttu-id="d9e84-165">Usa questo parametro per filtrare i risultati dell'elenco processi in processi inviati da un utente specificato.</span><span class="sxs-lookup"><span data-stu-id="d9e84-165">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e84-166">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="d9e84-166">-Top</span></span>
<span data-ttu-id="d9e84-167">Un valore facoltativo che indica il numero di processi da restituire.</span><span class="sxs-lookup"><span data-stu-id="d9e84-167">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="d9e84-168">Il valore predefinito è 500</span><span class="sxs-lookup"><span data-stu-id="d9e84-168">Default value is 500</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e84-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9e84-169">-DefaultProfile</span></span>
<span data-ttu-id="d9e84-170">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9e84-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9e84-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9e84-171">CommonParameters</span></span>
<span data-ttu-id="d9e84-172">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9e84-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9e84-173">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9e84-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9e84-174">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9e84-174">INPUTS</span></span>

### <span data-ttu-id="d9e84-175">GUID</span><span class="sxs-lookup"><span data-stu-id="d9e84-175">Guid</span></span>
<span data-ttu-id="d9e84-176">Il parametro "JobId" accetta il valore di tipo "GUID" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d9e84-176">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="d9e84-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9e84-177">OUTPUTS</span></span>

### <span data-ttu-id="d9e84-178">JobInformation</span><span class="sxs-lookup"><span data-stu-id="d9e84-178">JobInformation</span></span>
<span data-ttu-id="d9e84-179">Dettagli delle informazioni sui processi specificati</span><span class="sxs-lookup"><span data-stu-id="d9e84-179">The specified job information details</span></span>

### <span data-ttu-id="d9e84-180">Elenco<JobInformation></span><span class="sxs-lookup"><span data-stu-id="d9e84-180">List<JobInformation></span></span>
<span data-ttu-id="d9e84-181">L'elenco dei processi nell'account di analisi dei dati del lago specificato.</span><span class="sxs-lookup"><span data-stu-id="d9e84-181">The list of jobs in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="d9e84-182">Note</span><span class="sxs-lookup"><span data-stu-id="d9e84-182">NOTES</span></span>

## <span data-ttu-id="d9e84-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9e84-183">RELATED LINKS</span></span>

[<span data-ttu-id="d9e84-184">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d9e84-184">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="d9e84-185">Invia-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d9e84-185">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="d9e84-186">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d9e84-186">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


