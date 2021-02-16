---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/submit-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
ms.openlocfilehash: c8e710db383aae6698278ac4fb5ad7eb4344641b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208955"
---
# <span data-ttu-id="4ea33-101">Submit-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="4ea33-101">Submit-AzSynapseSparkJob</span></span>

## <span data-ttu-id="4ea33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ea33-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea33-103">Invia un processo Spark di Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="4ea33-103">Submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="4ea33-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ea33-104">SYNTAX</span></span>

### <span data-ttu-id="4ea33-105">RunSparkJobParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4ea33-105">RunSparkJobParameterSetName (Default)</span></span>
```
Submit-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ea33-106">RunSparkJobByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ea33-106">RunSparkJobByParentObjectParameterSet</span></span>
```
Submit-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ea33-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4ea33-107">DESCRIPTION</span></span>
<span data-ttu-id="4ea33-108">Il cmdlet **Submit-AzSynapseSparkJob** invia un processo Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="4ea33-108">The **Submit-AzSynapseSparkJob** cmdlet submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="4ea33-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ea33-109">EXAMPLES</span></span>

### <span data-ttu-id="4ea33-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4ea33-110">Example 1</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language Spark -Name WordCount_Java -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/wordcount.jar -MainClassName WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="4ea33-111">Questo comando invia un processo spark di Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="4ea33-111">This command submits a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="4ea33-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4ea33-112">Example 2</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language SparkDotNet -Name WordCount_Dotnet -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/wordcount.zip -MainExecutableFile WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/result -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="4ea33-113">Questo comando invia un processo di Synapse Analytics Spark .NET.</span><span class="sxs-lookup"><span data-stu-id="4ea33-113">This command submits a Synapse Analytics Spark .NET job.</span></span>

### <span data-ttu-id="4ea33-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="4ea33-114">Example 3</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language PySpark -Name WordCount_Python -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/wordcount.py -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="4ea33-115">Questo comando invia un processo di Synapse Analytics PySpark.</span><span class="sxs-lookup"><span data-stu-id="4ea33-115">This command submits a Synapse Analytics PySpark job.</span></span>

## <span data-ttu-id="4ea33-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ea33-116">PARAMETERS</span></span>

### <span data-ttu-id="4ea33-117">-CommandLine Argument</span><span class="sxs-lookup"><span data-stu-id="4ea33-117">-CommandLineArgument</span></span>
<span data-ttu-id="4ea33-118">Argomenti facoltativi per il processo.</span><span class="sxs-lookup"><span data-stu-id="4ea33-118">Optional arguments to the job.</span></span> <span data-ttu-id="4ea33-119">ad esempio "--iterazione 10000 --timeout 20s"</span><span class="sxs-lookup"><span data-stu-id="4ea33-119">e.g. "--iteration 10000 --timeout 20s"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea33-120">-Configuration</span><span class="sxs-lookup"><span data-stu-id="4ea33-120">-Configuration</span></span>
<span data-ttu-id="4ea33-121">Proprietà di configurazione Spark.</span><span class="sxs-lookup"><span data-stu-id="4ea33-121">Spark configuration properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea33-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea33-122">-DefaultProfile</span></span>
<span data-ttu-id="4ea33-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea33-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ea33-124">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="4ea33-124">-ExecutorCount</span></span>
<span data-ttu-id="4ea33-125">Numero di esecutori da allocare nel pool spark specificato per il processo.</span><span class="sxs-lookup"><span data-stu-id="4ea33-125">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea33-126">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="4ea33-126">-ExecutorSize</span></span>
<span data-ttu-id="4ea33-127">Numero di core e memoria da usare per gli esecutori allocati nel pool Spark specificato per il processo.</span><span class="sxs-lookup"><span data-stu-id="4ea33-127">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea33-128">-Lingua</span><span class="sxs-lookup"><span data-stu-id="4ea33-128">-Language</span></span>
<span data-ttu-id="4ea33-129">Lingua del processo da inviare.</span><span class="sxs-lookup"><span data-stu-id="4ea33-129">Language of the job to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea33-130">-MainClassName</span><span class="sxs-lookup"><span data-stu-id="4ea33-130">-MainClassName</span></span>
<span data-ttu-id="4ea33-131">L'identificatore completo o la classe principale nel file di definizione principale.</span><span class="sxs-lookup"><span data-stu-id="4ea33-131">The fully-qualified identifier or the main class that is in the main definition file.</span></span>
<span data-ttu-id="4ea33-132">Obbligatorio per il processo Spark e .NET Spark.</span><span class="sxs-lookup"><span data-stu-id="4ea33-132">Required for Spark and .NET Spark job.</span></span>
<span data-ttu-id="4ea33-133">ad esempio "org.apache.spark.examples.SparkPi"</span><span class="sxs-lookup"><span data-stu-id="4ea33-133">e.g. "org.apache.spark.examples.SparkPi"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MainExecutableFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea33-134">-MainDefinitionFile</span><span class="sxs-lookup"><span data-stu-id="4ea33-134">-MainDefinitionFile</span></span>
<span data-ttu-id="4ea33-135">Il file principale usato per il processo.</span><span class="sxs-lookup"><span data-stu-id="4ea33-135">The main file used for the job.</span></span>
<span data-ttu-id="4ea33-136">ad esempio " abfss://filesystem@account.dfs.core.windows.net/mySpark.jar "</span><span class="sxs-lookup"><span data-stu-id="4ea33-136">e.g. "abfss://filesystem@account.dfs.core.windows.net/mySpark.jar"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea33-137">-Name</span><span class="sxs-lookup"><span data-stu-id="4ea33-137">-Name</span></span>
<span data-ttu-id="4ea33-138">Nome del processo Spark.</span><span class="sxs-lookup"><span data-stu-id="4ea33-138">Name of Spark job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea33-139">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="4ea33-139">-ReferenceFile</span></span>
<span data-ttu-id="4ea33-140">File aggiuntivi usati per riferimento nel file di definizione principale.</span><span class="sxs-lookup"><span data-stu-id="4ea33-140">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="4ea33-141">Elenco di URI di archiviazione con valori delimitati da virgole.</span><span class="sxs-lookup"><span data-stu-id="4ea33-141">Comma-separated storage URI list.</span></span> <span data-ttu-id="4ea33-142">ad esempio " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="4ea33-142">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea33-143">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="4ea33-143">-SparkPoolName</span></span>
<span data-ttu-id="4ea33-144">Nome del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="4ea33-144">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkJobParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea33-145">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="4ea33-145">-SparkPoolObject</span></span>
<span data-ttu-id="4ea33-146">Oggetto di input del pool spark, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="4ea33-146">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: RunSparkJobByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea33-147">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4ea33-147">-WorkspaceName</span></span>
<span data-ttu-id="4ea33-148">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="4ea33-148">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkJobParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea33-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ea33-149">-Confirm</span></span>
<span data-ttu-id="4ea33-150">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ea33-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea33-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ea33-151">-WhatIf</span></span>
<span data-ttu-id="4ea33-152">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ea33-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ea33-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ea33-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea33-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea33-154">CommonParameters</span></span>
<span data-ttu-id="4ea33-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ea33-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea33-156">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4ea33-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea33-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="4ea33-157">INPUTS</span></span>

### <span data-ttu-id="4ea33-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="4ea33-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="4ea33-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ea33-159">OUTPUTS</span></span>

### <span data-ttu-id="4ea33-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="4ea33-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="4ea33-161">NOTE</span><span class="sxs-lookup"><span data-stu-id="4ea33-161">NOTES</span></span>

## <span data-ttu-id="4ea33-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ea33-162">RELATED LINKS</span></span>
