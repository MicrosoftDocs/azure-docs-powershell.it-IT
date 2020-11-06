---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: bb0ad536d738facdfe50bc7983517f4505ab4ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519198"
---
# <span data-ttu-id="f1d4a-101">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f1d4a-101">Submit-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="f1d4a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f1d4a-102">SYNOPSIS</span></span>
<span data-ttu-id="f1d4a-103">Invia un processo.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-103">Submits a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1d4a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1d4a-104">SYNTAX</span></span>

### <span data-ttu-id="f1d4a-105">Inviare un processo con il percorso di script per U-SQL</span><span class="sxs-lookup"><span data-stu-id="f1d4a-105">Submit job with script path for U-SQL</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1d4a-106">Inviare il processo U-SQL</span><span class="sxs-lookup"><span data-stu-id="f1d4a-106">Submit U-SQL Job</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1d4a-107">Inviare un processo con il percorso di script per U-SQL con informazioni reucurrence</span><span class="sxs-lookup"><span data-stu-id="f1d4a-107">Submit job with script path for U-SQL with reucurrence information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1d4a-108">Inviare il processo U-SQL con le informazioni sulla ricorrenza</span><span class="sxs-lookup"><span data-stu-id="f1d4a-108">Submit U-SQL Job with recurrence information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1d4a-109">Inviare un processo con il percorso di script per U-SQL con reucurrence e le informazioni sulla pipeline</span><span class="sxs-lookup"><span data-stu-id="f1d4a-109">Submit job with script path for U-SQL with reucurrence and pipeline information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1d4a-110">Inviare il processo U-SQL con le informazioni sulla ricorrenza e sulla pipeline</span><span class="sxs-lookup"><span data-stu-id="f1d4a-110">Submit U-SQL Job with recurrence and pipeline information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1d4a-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1d4a-111">DESCRIPTION</span></span>
<span data-ttu-id="f1d4a-112">Il cmdlet **Submit-AzureRmDataLakeAnalyticsJob** Invia un processo di analisi del Lago di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-112">The **Submit-AzureRmDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="f1d4a-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1d4a-113">EXAMPLES</span></span>

### <span data-ttu-id="f1d4a-114">Esempio 1: inviare un processo</span><span class="sxs-lookup"><span data-stu-id="f1d4a-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -DegreeOfParallelism 32
```

<span data-ttu-id="f1d4a-115">Questo comando Invia un processo di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-115">This command submits a Data Lake Analytics job.</span></span>

## <span data-ttu-id="f1d4a-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f1d4a-116">PARAMETERS</span></span>

### <span data-ttu-id="f1d4a-117">-Account</span><span class="sxs-lookup"><span data-stu-id="f1d4a-117">-Account</span></span>
<span data-ttu-id="f1d4a-118">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="f1d4a-119">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="f1d4a-119">-CompileMode</span></span>
<span data-ttu-id="f1d4a-120">Specifica la modalità di compilazione del processo.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-120">Specifies the compilation mode of the job.</span></span>
<span data-ttu-id="f1d4a-121">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f1d4a-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f1d4a-122">Semantico</span><span class="sxs-lookup"><span data-stu-id="f1d4a-122">Semantic</span></span>
- <span data-ttu-id="f1d4a-123">Completo</span><span class="sxs-lookup"><span data-stu-id="f1d4a-123">Full</span></span>
- <span data-ttu-id="f1d4a-124">SingleBox</span><span class="sxs-lookup"><span data-stu-id="f1d4a-124">SingleBox</span></span>

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

### <span data-ttu-id="f1d4a-125">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="f1d4a-125">-CompileOnly</span></span>
<span data-ttu-id="f1d4a-126">Indica che questo cmdlet compila il processo senza eseguirlo.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-126">Indicates that this cmdlet compiles the job without running it.</span></span>

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

### <span data-ttu-id="f1d4a-127">-DegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="f1d4a-127">-DegreeOfParallelism</span></span>
<span data-ttu-id="f1d4a-128">Specifica le unità di analisi del Lago di dati (DLAU) del processo, che indica il parallelismo massimo consentito del processo.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-128">Specifies the Data Lake Analytics Units (DLAU) of the job, which indicates the maximum allowable parallelism of the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d4a-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1d4a-129">-Name</span></span>
<span data-ttu-id="f1d4a-130">Specifica il nome del processo.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-130">Specifies the job name.</span></span>

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

### <span data-ttu-id="f1d4a-131">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="f1d4a-131">-PipelineId</span></span>
<span data-ttu-id="f1d4a-132">Un ID che indica che l'invio di questo processo fa parte di un set di processi ricorrenti e anche associato a una pipeline dei processi.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-132">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d4a-133">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="f1d4a-133">-PipelineName</span></span>
<span data-ttu-id="f1d4a-134">Nome descrittivo facoltativo per la pipeline associata al processo.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-134">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d4a-135">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="f1d4a-135">-PipelineUri</span></span>
<span data-ttu-id="f1d4a-136">URI facoltativo che si collega al servizio di origine associato a questa pipeline.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-136">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d4a-137">-Priorità</span><span class="sxs-lookup"><span data-stu-id="f1d4a-137">-Priority</span></span>
<span data-ttu-id="f1d4a-138">Specifica la priorità del processo.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-138">Specifies the priority of the job.</span></span>
<span data-ttu-id="f1d4a-139">Se non specificato, la priorità è 1000.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-139">If not specified, the priority is 1000.</span></span>
<span data-ttu-id="f1d4a-140">Un numero basso indica una priorità di lavoro più elevata.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-140">A low number indicates a higher job priority.</span></span>

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

### <span data-ttu-id="f1d4a-141">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="f1d4a-141">-RecurrenceId</span></span>
<span data-ttu-id="f1d4a-142">Un ID che indica che l'invio di questo processo fa parte di un set di processi ricorrenti con lo stesso ID ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-142">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d4a-143">-Reiterazionname</span><span class="sxs-lookup"><span data-stu-id="f1d4a-143">-RecurrenceName</span></span>
<span data-ttu-id="f1d4a-144">Nome descrittivo facoltativo per la correlazione della ricorrenza tra i processi.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-144">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d4a-145">-RunId</span><span class="sxs-lookup"><span data-stu-id="f1d4a-145">-RunId</span></span>
<span data-ttu-id="f1d4a-146">ID che identifica questa iterazione di esecuzione specifica della pipeline.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-146">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d4a-147">-Runtime</span><span class="sxs-lookup"><span data-stu-id="f1d4a-147">-Runtime</span></span>
<span data-ttu-id="f1d4a-148">Specifica la versione di runtime del processo.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-148">Specifies the runtime version of the job.</span></span>

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

### <span data-ttu-id="f1d4a-149">-Script</span><span class="sxs-lookup"><span data-stu-id="f1d4a-149">-Script</span></span>
<span data-ttu-id="f1d4a-150">Specifica il contenuto dello script da eseguire.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-150">Specifies the contents of the script to run.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit U-SQL Job, Submit U-SQL Job with recurrence information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d4a-151">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="f1d4a-151">-ScriptPath</span></span>
<span data-ttu-id="f1d4a-152">Specifica il percorso del file locale per l'esecuzione dello script.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-152">Specifies the local file path to the script to run.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL, Submit job with script path for U-SQL with reucurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d4a-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1d4a-153">-DefaultProfile</span></span>
<span data-ttu-id="f1d4a-154">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1d4a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1d4a-155">CommonParameters</span></span>
<span data-ttu-id="f1d4a-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1d4a-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1d4a-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1d4a-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f1d4a-158">INPUTS</span></span>

### <span data-ttu-id="f1d4a-159">Stringa</span><span class="sxs-lookup"><span data-stu-id="f1d4a-159">String</span></span>
<span data-ttu-id="f1d4a-160">Il parametro "script" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f1d4a-160">Parameter 'Script' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="f1d4a-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1d4a-161">OUTPUTS</span></span>

### <span data-ttu-id="f1d4a-162">JobInformation</span><span class="sxs-lookup"><span data-stu-id="f1d4a-162">JobInformation</span></span>
<span data-ttu-id="f1d4a-163">I dettagli del processo iniziale per il processo inviato.</span><span class="sxs-lookup"><span data-stu-id="f1d4a-163">The initial job details for the submitted job.</span></span>

## <span data-ttu-id="f1d4a-164">Note</span><span class="sxs-lookup"><span data-stu-id="f1d4a-164">NOTES</span></span>

## <span data-ttu-id="f1d4a-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1d4a-165">RELATED LINKS</span></span>

[<span data-ttu-id="f1d4a-166">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f1d4a-166">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="f1d4a-167">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f1d4a-167">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="f1d4a-168">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f1d4a-168">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


