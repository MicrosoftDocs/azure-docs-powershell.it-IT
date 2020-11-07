---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/submit-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 23c8f8baa2753382ef2ee91f62199966a4fb9c2d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836355"
---
# <span data-ttu-id="3c1bf-101">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3c1bf-101">Submit-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="3c1bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c1bf-102">SYNOPSIS</span></span>
<span data-ttu-id="3c1bf-103">Invia un processo.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-103">Submits a job.</span></span>

## <span data-ttu-id="3c1bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c1bf-104">SYNTAX</span></span>

### <span data-ttu-id="3c1bf-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="3c1bf-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c1bf-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="3c1bf-106">SubmitUSqlJob</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c1bf-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="3c1bf-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c1bf-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="3c1bf-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c1bf-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="3c1bf-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c1bf-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="3c1bf-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c1bf-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c1bf-111">DESCRIPTION</span></span>
<span data-ttu-id="3c1bf-112">Il cmdlet **Submit-AzDataLakeAnalyticsJob** Invia un processo di analisi del Lago di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-112">The **Submit-AzDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="3c1bf-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c1bf-113">EXAMPLES</span></span>

### <span data-ttu-id="3c1bf-114">Esempio 1: inviare un processo</span><span class="sxs-lookup"><span data-stu-id="3c1bf-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="3c1bf-115">Questo comando Invia un processo di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="3c1bf-116">Esempio 2: inviare un processo con i parametri di script</span><span class="sxs-lookup"><span data-stu-id="3c1bf-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="3c1bf-117">I parametri di script U-SQL sono preceduto sopra il contenuto dello script principale, ad esempio: DECLARE @Department String = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = New DateTime (2017, 12, 6, 0, 0, 0, 0);</span><span class="sxs-lookup"><span data-stu-id="3c1bf-117">U-SQL script parameters are prepended above the main script contents, e.g.: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="3c1bf-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c1bf-118">PARAMETERS</span></span>

### <span data-ttu-id="3c1bf-119">-Account</span><span class="sxs-lookup"><span data-stu-id="3c1bf-119">-Account</span></span>
<span data-ttu-id="3c1bf-120">Nome dell'account di analisi del lago dati in base al quale verrà inviato il processo.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-120">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="3c1bf-121">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="3c1bf-121">-AnalyticsUnits</span></span>
<span data-ttu-id="3c1bf-122">Unità di analisi da usare per questo processo.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-122">The analytics units to use for this job.</span></span> <span data-ttu-id="3c1bf-123">In genere, più unità di analisi dedicate a uno script determinano tempi di esecuzione degli script più veloci.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-123">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: DegreeOfParallelism

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c1bf-124">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="3c1bf-124">-CompileMode</span></span>
<span data-ttu-id="3c1bf-125">Tipo di compilazione da eseguire in questo processo.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-125">The type of compilation to be done on this job.</span></span> <span data-ttu-id="3c1bf-126">Valori validi:</span><span class="sxs-lookup"><span data-stu-id="3c1bf-126">Valid values:</span></span> 
- <span data-ttu-id="3c1bf-127">Semantic (esegue solo controlli semantici e controlli di integrità necessari)</span><span class="sxs-lookup"><span data-stu-id="3c1bf-127">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="3c1bf-128">Completo (compilazione completa)</span><span class="sxs-lookup"><span data-stu-id="3c1bf-128">Full (Full compilation)</span></span>
- <span data-ttu-id="3c1bf-129">SingleBox (compilazione completa eseguita localmente)</span><span class="sxs-lookup"><span data-stu-id="3c1bf-129">SingleBox (Full compilation performed locally)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Semantic, Full, SingleBox

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c1bf-130">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="3c1bf-130">-CompileOnly</span></span>
<span data-ttu-id="3c1bf-131">Indica che l'invio deve compilare il processo e non eseguirlo se impostato su true.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-131">Indicates that the submission should only build the job and not execute if set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c1bf-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c1bf-132">-DefaultProfile</span></span>
<span data-ttu-id="3c1bf-133">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3c1bf-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c1bf-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c1bf-134">-Name</span></span>
<span data-ttu-id="3c1bf-135">Nome descrittivo del processo da inviare.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-135">The friendly name of the job to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c1bf-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="3c1bf-136">-PipelineId</span></span>
<span data-ttu-id="3c1bf-137">Un ID che indica che l'invio di questo processo fa parte di un set di processi ricorrenti e anche associato a una pipeline dei processi.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-137">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c1bf-138">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="3c1bf-138">-PipelineName</span></span>
<span data-ttu-id="3c1bf-139">Nome descrittivo facoltativo per la pipeline associata al processo.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-139">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c1bf-140">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="3c1bf-140">-PipelineUri</span></span>
<span data-ttu-id="3c1bf-141">URI facoltativo che si collega al servizio di origine associato a questa pipeline.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-141">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c1bf-142">-Priorità</span><span class="sxs-lookup"><span data-stu-id="3c1bf-142">-Priority</span></span>
<span data-ttu-id="3c1bf-143">Priorità del processo.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-143">The priority of the job.</span></span> <span data-ttu-id="3c1bf-144">Se non specificato, la priorità è 1000.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-144">If not specified, the priority is 1000.</span></span> <span data-ttu-id="3c1bf-145">Un numero inferiore indica una priorità di lavoro più elevata.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-145">A lower number indicates a higher job priority.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c1bf-146">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="3c1bf-146">-RecurrenceId</span></span>
<span data-ttu-id="3c1bf-147">Un ID che indica che l'invio di questo processo fa parte di un set di processi ricorrenti con lo stesso ID ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-147">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c1bf-148">-Reiterazionname</span><span class="sxs-lookup"><span data-stu-id="3c1bf-148">-RecurrenceName</span></span>
<span data-ttu-id="3c1bf-149">Nome descrittivo facoltativo per la correlazione della ricorrenza tra i processi.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-149">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c1bf-150">-RunId</span><span class="sxs-lookup"><span data-stu-id="3c1bf-150">-RunId</span></span>
<span data-ttu-id="3c1bf-151">ID che identifica questa iterazione di esecuzione specifica della pipeline.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-151">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c1bf-152">-Runtime</span><span class="sxs-lookup"><span data-stu-id="3c1bf-152">-Runtime</span></span>
<span data-ttu-id="3c1bf-153">Facoltativamente, imposta la versione del runtime da usare per il processo.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-153">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="3c1bf-154">Se non è impostata a sinistra, viene usato il runtime predefinito.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-154">If left unset, the default runtime is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c1bf-155">-Script</span><span class="sxs-lookup"><span data-stu-id="3c1bf-155">-Script</span></span>
<span data-ttu-id="3c1bf-156">Script da eseguire (scritto in linea).</span><span class="sxs-lookup"><span data-stu-id="3c1bf-156">Script to execute (written inline).</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJob, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c1bf-157">-ParametroScript</span><span class="sxs-lookup"><span data-stu-id="3c1bf-157">-ScriptParameter</span></span>
<span data-ttu-id="3c1bf-158">Parametri di script per questo processo, come dizionario di nomi di parametri (stringa) ai valori (qualsiasi combinazione di byte, SByte, int, uint (o UInt32), Long, ulong (o UInt64), float, Double, Decimal, short (o Int16), ushort (o UInt16), Char, String, DateTime, bool, GUID o byte []).</span><span class="sxs-lookup"><span data-stu-id="3c1bf-158">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c1bf-159">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="3c1bf-159">-ScriptPath</span></span>
<span data-ttu-id="3c1bf-160">Percorso del file di script da inviare.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-160">Path to the script file to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPath, SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithScriptPathAndPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c1bf-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c1bf-161">CommonParameters</span></span>
<span data-ttu-id="3c1bf-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c1bf-163">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c1bf-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c1bf-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c1bf-164">INPUTS</span></span>

### <span data-ttu-id="3c1bf-165">System. String</span><span class="sxs-lookup"><span data-stu-id="3c1bf-165">System.String</span></span>

### <span data-ttu-id="3c1bf-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3c1bf-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="3c1bf-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3c1bf-167">System.Int32</span></span>

### <span data-ttu-id="3c1bf-168">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="3c1bf-168">System.Collections.IDictionary</span></span>

### <span data-ttu-id="3c1bf-169">System. Guid</span><span class="sxs-lookup"><span data-stu-id="3c1bf-169">System.Guid</span></span>

### <span data-ttu-id="3c1bf-170">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3c1bf-170">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3c1bf-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c1bf-171">OUTPUTS</span></span>

### <span data-ttu-id="3c1bf-172">Microsoft. Azure. Management. datalake. Analytics. Models. JobInformation</span><span class="sxs-lookup"><span data-stu-id="3c1bf-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="3c1bf-173">Note</span><span class="sxs-lookup"><span data-stu-id="3c1bf-173">NOTES</span></span>

## <span data-ttu-id="3c1bf-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c1bf-174">RELATED LINKS</span></span>

[<span data-ttu-id="3c1bf-175">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3c1bf-175">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="3c1bf-176">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3c1bf-176">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="3c1bf-177">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3c1bf-177">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


