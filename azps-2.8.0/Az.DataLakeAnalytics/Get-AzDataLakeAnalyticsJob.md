---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 73a9325ea4f1bc45eaaf2fb81796d526c7b95fea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674879"
---
# <span data-ttu-id="d8114-101">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d8114-101">Get-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="d8114-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d8114-102">SYNOPSIS</span></span>
<span data-ttu-id="d8114-103">Ottiene un processo di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="d8114-103">Gets a Data Lake Analytics job.</span></span>

## <span data-ttu-id="d8114-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8114-104">SYNTAX</span></span>

### <span data-ttu-id="d8114-105">GetAllInResourceGroupAndAccount (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d8114-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8114-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="d8114-106">GetBySpecificJobInformation</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8114-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8114-107">DESCRIPTION</span></span>
<span data-ttu-id="d8114-108">Il cmdlet **Get-AzDataLakeAnalyticsJob** ottiene un processo di analisi del Lago di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="d8114-108">The **Get-AzDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="d8114-109">Se non specifichi un processo, questo cmdlet ottiene tutti i processi.</span><span class="sxs-lookup"><span data-stu-id="d8114-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="d8114-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8114-110">EXAMPLES</span></span>

### <span data-ttu-id="d8114-111">Esempio 1: ottenere un processo specificato</span><span class="sxs-lookup"><span data-stu-id="d8114-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="d8114-112">Questo comando ottiene il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="d8114-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="d8114-113">Esempio 2: ottenere processi inviati nell'ultima settimana</span><span class="sxs-lookup"><span data-stu-id="d8114-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="d8114-114">Questo comando consente di ottenere i processi inviati nell'ultima settimana.</span><span class="sxs-lookup"><span data-stu-id="d8114-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="d8114-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8114-115">PARAMETERS</span></span>

### <span data-ttu-id="d8114-116">-Account</span><span class="sxs-lookup"><span data-stu-id="d8114-116">-Account</span></span>
<span data-ttu-id="d8114-117">Specifica il nome di un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="d8114-117">Specifies the name of a Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="d8114-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8114-118">-DefaultProfile</span></span>
<span data-ttu-id="d8114-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d8114-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8114-120">-Includi</span><span class="sxs-lookup"><span data-stu-id="d8114-120">-Include</span></span>
<span data-ttu-id="d8114-121">Specifica le opzioni che indicano il tipo di informazioni aggiuntive da recuperare sul processo.</span><span class="sxs-lookup"><span data-stu-id="d8114-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="d8114-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d8114-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d8114-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d8114-123">None</span></span>
- <span data-ttu-id="d8114-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="d8114-124">DebugInfo</span></span>
- <span data-ttu-id="d8114-125">Statistiche</span><span class="sxs-lookup"><span data-stu-id="d8114-125">Statistics</span></span>
- <span data-ttu-id="d8114-126">Tutti</span><span class="sxs-lookup"><span data-stu-id="d8114-126">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases:
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8114-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="d8114-127">-JobId</span></span>
<span data-ttu-id="d8114-128">Specifica l'ID del processo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="d8114-128">Specifies the ID of the job to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobInformation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8114-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8114-129">-Name</span></span>
<span data-ttu-id="d8114-130">Specifica un nome da usare per filtrare i risultati dell'elenco processi.</span><span class="sxs-lookup"><span data-stu-id="d8114-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="d8114-131">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d8114-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d8114-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d8114-132">None</span></span>
- <span data-ttu-id="d8114-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="d8114-133">DebugInfo</span></span>
- <span data-ttu-id="d8114-134">Statistiche</span><span class="sxs-lookup"><span data-stu-id="d8114-134">Statistics</span></span>
- <span data-ttu-id="d8114-135">Tutti</span><span class="sxs-lookup"><span data-stu-id="d8114-135">All</span></span>

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8114-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="d8114-136">-PipelineId</span></span>
<span data-ttu-id="d8114-137">Un ID facoltativo che indica solo i processi parte della pipeline specificata deve essere restituito.</span><span class="sxs-lookup"><span data-stu-id="d8114-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8114-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="d8114-138">-RecurrenceId</span></span>
<span data-ttu-id="d8114-139">Un ID facoltativo che indica solo i processi parte della ricorrenza specificata deve essere restituito.</span><span class="sxs-lookup"><span data-stu-id="d8114-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8114-140">-Risultato</span><span class="sxs-lookup"><span data-stu-id="d8114-140">-Result</span></span>
<span data-ttu-id="d8114-141">Specifica un filtro di risultato per i risultati del processo.</span><span class="sxs-lookup"><span data-stu-id="d8114-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="d8114-142">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d8114-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d8114-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d8114-143">None</span></span>
- <span data-ttu-id="d8114-144">Annullata</span><span class="sxs-lookup"><span data-stu-id="d8114-144">Cancelled</span></span>
- <span data-ttu-id="d8114-145">Fallito</span><span class="sxs-lookup"><span data-stu-id="d8114-145">Failed</span></span>
- <span data-ttu-id="d8114-146">Succeeded</span><span class="sxs-lookup"><span data-stu-id="d8114-146">Succeeded</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8114-147">-Stato</span><span class="sxs-lookup"><span data-stu-id="d8114-147">-State</span></span>
<span data-ttu-id="d8114-148">Specifica un filtro di stato per i risultati del processo.</span><span class="sxs-lookup"><span data-stu-id="d8114-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="d8114-149">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d8114-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d8114-150">Accettato</span><span class="sxs-lookup"><span data-stu-id="d8114-150">Accepted</span></span>
- <span data-ttu-id="d8114-151">Nuovo</span><span class="sxs-lookup"><span data-stu-id="d8114-151">New</span></span>
- <span data-ttu-id="d8114-152">Compilazione</span><span class="sxs-lookup"><span data-stu-id="d8114-152">Compiling</span></span>
- <span data-ttu-id="d8114-153">Pianificazione</span><span class="sxs-lookup"><span data-stu-id="d8114-153">Scheduling</span></span>
- <span data-ttu-id="d8114-154">Accodati</span><span class="sxs-lookup"><span data-stu-id="d8114-154">Queued</span></span>
- <span data-ttu-id="d8114-155">Iniziale</span><span class="sxs-lookup"><span data-stu-id="d8114-155">Starting</span></span>
- <span data-ttu-id="d8114-156">In pausa</span><span class="sxs-lookup"><span data-stu-id="d8114-156">Paused</span></span>
- <span data-ttu-id="d8114-157">Esecuzione</span><span class="sxs-lookup"><span data-stu-id="d8114-157">Running</span></span>
- <span data-ttu-id="d8114-158">Terminato</span><span class="sxs-lookup"><span data-stu-id="d8114-158">Ended</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8114-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="d8114-159">-SubmittedAfter</span></span>
<span data-ttu-id="d8114-160">Specifica un filtro data.</span><span class="sxs-lookup"><span data-stu-id="d8114-160">Specifies a date filter.</span></span>
<span data-ttu-id="d8114-161">Usa questo parametro per filtrare il risultato dell'elenco processi in processi inviati dopo la data specificata.</span><span class="sxs-lookup"><span data-stu-id="d8114-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8114-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="d8114-162">-SubmittedBefore</span></span>
<span data-ttu-id="d8114-163">Specifica un filtro data.</span><span class="sxs-lookup"><span data-stu-id="d8114-163">Specifies a date filter.</span></span>
<span data-ttu-id="d8114-164">Usa questo parametro per filtrare il risultato dell'elenco processi in processi inviati prima della data specificata.</span><span class="sxs-lookup"><span data-stu-id="d8114-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8114-165">-Mittente</span><span class="sxs-lookup"><span data-stu-id="d8114-165">-Submitter</span></span>
<span data-ttu-id="d8114-166">Specifica l'indirizzo di posta elettronica di un utente.</span><span class="sxs-lookup"><span data-stu-id="d8114-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="d8114-167">Usa questo parametro per filtrare i risultati dell'elenco processi in processi inviati da un utente specificato.</span><span class="sxs-lookup"><span data-stu-id="d8114-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8114-168">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="d8114-168">-Top</span></span>
<span data-ttu-id="d8114-169">Un valore facoltativo che indica il numero di processi da restituire.</span><span class="sxs-lookup"><span data-stu-id="d8114-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="d8114-170">Il valore predefinito è 500</span><span class="sxs-lookup"><span data-stu-id="d8114-170">Default value is 500</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8114-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8114-171">CommonParameters</span></span>
<span data-ttu-id="d8114-172">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8114-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8114-173">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8114-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8114-174">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d8114-174">INPUTS</span></span>

### <span data-ttu-id="d8114-175">System. String</span><span class="sxs-lookup"><span data-stu-id="d8114-175">System.String</span></span>

### <span data-ttu-id="d8114-176">System. Guid</span><span class="sxs-lookup"><span data-stu-id="d8114-176">System.Guid</span></span>

### <span data-ttu-id="d8114-177">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + ExtendedJobData</span><span class="sxs-lookup"><span data-stu-id="d8114-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span></span>

### <span data-ttu-id="d8114-178">System. Nullable ' 1 [[System. DateTimeOffset, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d8114-178">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d8114-179">Microsoft. Azure. Management. datalake. Analytics. Models. JobState []</span><span class="sxs-lookup"><span data-stu-id="d8114-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span></span>

### <span data-ttu-id="d8114-180">Microsoft. Azure. Management. datalake. Analytics. Models. JobResult []</span><span class="sxs-lookup"><span data-stu-id="d8114-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span></span>

### <span data-ttu-id="d8114-181">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d8114-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d8114-182">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d8114-182">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d8114-183">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8114-183">OUTPUTS</span></span>

### <span data-ttu-id="d8114-184">Microsoft. Azure. Management. datalake. Analytics. Models. JobInformation</span><span class="sxs-lookup"><span data-stu-id="d8114-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="d8114-185">Note</span><span class="sxs-lookup"><span data-stu-id="d8114-185">NOTES</span></span>

## <span data-ttu-id="d8114-186">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8114-186">RELATED LINKS</span></span>

[<span data-ttu-id="d8114-187">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d8114-187">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="d8114-188">Invia-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d8114-188">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="d8114-189">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d8114-189">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)

