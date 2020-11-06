---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/submit-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: fc09560bca0d825cc65d8a4f964119cd50898190
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509899"
---
# <span data-ttu-id="f4fcf-101">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f4fcf-101">Submit-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="f4fcf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="f4fcf-103">Invia un processo.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-103">Submits a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4fcf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4fcf-104">SYNTAX</span></span>

### <span data-ttu-id="f4fcf-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="f4fcf-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4fcf-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="f4fcf-106">SubmitUSqlJob</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4fcf-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="f4fcf-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4fcf-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="f4fcf-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4fcf-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="f4fcf-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 -PipelineId <Guid> [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4fcf-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="f4fcf-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 -PipelineId <Guid> [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4fcf-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4fcf-111">DESCRIPTION</span></span>
<span data-ttu-id="f4fcf-112">Il cmdlet **Submit-AzureRmDataLakeAnalyticsJob** Invia un processo di analisi del Lago di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-112">The **Submit-AzureRmDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="f4fcf-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4fcf-113">EXAMPLES</span></span>

### <span data-ttu-id="f4fcf-114">Esempio 1: inviare un processo</span><span class="sxs-lookup"><span data-stu-id="f4fcf-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="f4fcf-115">Questo comando Invia un processo di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="f4fcf-116">Esempio 2: inviare un processo con i parametri di script</span><span class="sxs-lookup"><span data-stu-id="f4fcf-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="f4fcf-117">I parametri di script U-SQL sono preceduto sopra il contenuto dello script principale, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="f4fcf-117">U-SQL script parameters are prepended above the main script contents, e.g.:</span></span>

<span data-ttu-id="f4fcf-118">DECLARE @Department String = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = New DateTime (2017, 12, 6, 0, 0, 0, 0);</span><span class="sxs-lookup"><span data-stu-id="f4fcf-118">DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="f4fcf-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4fcf-119">PARAMETERS</span></span>

### <span data-ttu-id="f4fcf-120">-Account</span><span class="sxs-lookup"><span data-stu-id="f4fcf-120">-Account</span></span>
<span data-ttu-id="f4fcf-121">Nome dell'account di analisi del lago dati in base al quale verrà inviato il processo.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-121">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fcf-122">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="f4fcf-122">-CompileMode</span></span>
<span data-ttu-id="f4fcf-123">Tipo di compilazione da eseguire in questo processo.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-123">The type of compilation to be done on this job.</span></span> <span data-ttu-id="f4fcf-124">Valori validi:</span><span class="sxs-lookup"><span data-stu-id="f4fcf-124">Valid values:</span></span> 

- <span data-ttu-id="f4fcf-125">Semantic (esegue solo controlli semantici e controlli di integrità necessari)</span><span class="sxs-lookup"><span data-stu-id="f4fcf-125">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="f4fcf-126">Completo (compilazione completa)</span><span class="sxs-lookup"><span data-stu-id="f4fcf-126">Full (Full compilation)</span></span>
- <span data-ttu-id="f4fcf-127">SingleBox (compilazione completa eseguita localmente)</span><span class="sxs-lookup"><span data-stu-id="f4fcf-127">SingleBox (Full compilation performed locally)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Semantic, Full, SingleBox

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fcf-128">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="f4fcf-128">-CompileOnly</span></span>
<span data-ttu-id="f4fcf-129">Indica che l'invio deve compilare il processo e non eseguirlo se impostato su true.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-129">Indicates that the submission should only build the job and not execute if set to true.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fcf-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4fcf-130">-DefaultProfile</span></span>
<span data-ttu-id="f4fcf-131">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f4fcf-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4fcf-132">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="f4fcf-132">-AnalyticsUnits</span></span>
<span data-ttu-id="f4fcf-133">Unità di analisi da usare per questo processo.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-133">The analytics units to use for this job.</span></span> <span data-ttu-id="f4fcf-134">In genere, più unità di analisi dedicate a uno script determinano tempi di esecuzione degli script più veloci.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-134">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: DegreeOfParallelism

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fcf-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4fcf-135">-Name</span></span>
<span data-ttu-id="f4fcf-136">Nome descrittivo del processo da inviare.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-136">The friendly name of the job to submit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fcf-137">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="f4fcf-137">-PipelineId</span></span>
<span data-ttu-id="f4fcf-138">Un ID che indica che l'invio di questo processo fa parte di un set di processi ricorrenti e anche associato a una pipeline dei processi.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-138">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fcf-139">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="f4fcf-139">-PipelineName</span></span>
<span data-ttu-id="f4fcf-140">Nome descrittivo facoltativo per la pipeline associata al processo.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-140">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fcf-141">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="f4fcf-141">-PipelineUri</span></span>
<span data-ttu-id="f4fcf-142">URI facoltativo che si collega al servizio di origine associato a questa pipeline.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-142">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fcf-143">-Priorità</span><span class="sxs-lookup"><span data-stu-id="f4fcf-143">-Priority</span></span>
<span data-ttu-id="f4fcf-144">Priorità del processo.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-144">The priority of the job.</span></span> <span data-ttu-id="f4fcf-145">Se non specificato, la priorità è 1000.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-145">If not specified, the priority is 1000.</span></span> <span data-ttu-id="f4fcf-146">Un numero inferiore indica una priorità di lavoro più elevata.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-146">A lower number indicates a higher job priority.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fcf-147">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="f4fcf-147">-RecurrenceId</span></span>
<span data-ttu-id="f4fcf-148">Un ID che indica che l'invio di questo processo fa parte di un set di processi ricorrenti con lo stesso ID ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-148">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fcf-149">-Reiterazionname</span><span class="sxs-lookup"><span data-stu-id="f4fcf-149">-RecurrenceName</span></span>
<span data-ttu-id="f4fcf-150">Nome descrittivo facoltativo per la correlazione della ricorrenza tra i processi.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-150">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fcf-151">-RunId</span><span class="sxs-lookup"><span data-stu-id="f4fcf-151">-RunId</span></span>
<span data-ttu-id="f4fcf-152">ID che identifica questa iterazione di esecuzione specifica della pipeline.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-152">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fcf-153">-Runtime</span><span class="sxs-lookup"><span data-stu-id="f4fcf-153">-Runtime</span></span>
<span data-ttu-id="f4fcf-154">Facoltativamente, imposta la versione del runtime da usare per il processo.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-154">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="f4fcf-155">Se non è impostata a sinistra, viene usato il runtime predefinito.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-155">If left unset, the default runtime is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fcf-156">-Script</span><span class="sxs-lookup"><span data-stu-id="f4fcf-156">-Script</span></span>
<span data-ttu-id="f4fcf-157">Script da eseguire (scritto in linea).</span><span class="sxs-lookup"><span data-stu-id="f4fcf-157">Script to execute (written inline).</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJob, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fcf-158">-ParametroScript</span><span class="sxs-lookup"><span data-stu-id="f4fcf-158">-ScriptParameter</span></span>
<span data-ttu-id="f4fcf-159">Parametri di script per questo processo, come dizionario di nomi di parametri (stringa) ai valori (qualsiasi combinazione di byte, SByte, int, uint (o UInt32), Long, ulong (o UInt64), float, Double, Decimal, short (o Int16), ushort (o UInt16), Char, String, DateTime, bool, GUID o byte []).</span><span class="sxs-lookup"><span data-stu-id="f4fcf-159">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fcf-160">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="f4fcf-160">-ScriptPath</span></span>
<span data-ttu-id="f4fcf-161">Percorso del file di script da inviare.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-161">Path to the script file to submit.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPath, SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithScriptPathAndPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fcf-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4fcf-162">CommonParameters</span></span>
<span data-ttu-id="f4fcf-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4fcf-164">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4fcf-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4fcf-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4fcf-165">INPUTS</span></span>

### <span data-ttu-id="f4fcf-166">Stringa</span><span class="sxs-lookup"><span data-stu-id="f4fcf-166">String</span></span>
<span data-ttu-id="f4fcf-167">Il parametro "script" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f4fcf-167">Parameter 'Script' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="f4fcf-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4fcf-168">OUTPUTS</span></span>

### <span data-ttu-id="f4fcf-169">JobInformation</span><span class="sxs-lookup"><span data-stu-id="f4fcf-169">JobInformation</span></span>
<span data-ttu-id="f4fcf-170">I dettagli del processo iniziale per il processo inviato.</span><span class="sxs-lookup"><span data-stu-id="f4fcf-170">The initial job details for the submitted job.</span></span>

## <span data-ttu-id="f4fcf-171">Note</span><span class="sxs-lookup"><span data-stu-id="f4fcf-171">NOTES</span></span>

## <span data-ttu-id="f4fcf-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4fcf-172">RELATED LINKS</span></span>

[<span data-ttu-id="f4fcf-173">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f4fcf-173">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="f4fcf-174">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f4fcf-174">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="f4fcf-175">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f4fcf-175">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


