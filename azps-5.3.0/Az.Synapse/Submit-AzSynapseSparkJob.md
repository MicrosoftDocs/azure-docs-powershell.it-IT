---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/submit-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
ms.openlocfilehash: c8e710db383aae6698278ac4fb5ad7eb4344641b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476550"
---
# <span data-ttu-id="e449f-101">Submit-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="e449f-101">Submit-AzSynapseSparkJob</span></span>

## <span data-ttu-id="e449f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e449f-102">SYNOPSIS</span></span>
<span data-ttu-id="e449f-103">Invia un processo Spark analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="e449f-103">Submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="e449f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e449f-104">SYNTAX</span></span>

### <span data-ttu-id="e449f-105">RunSparkJobParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e449f-105">RunSparkJobParameterSetName (Default)</span></span>
```
Submit-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e449f-106">RunSparkJobByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e449f-106">RunSparkJobByParentObjectParameterSet</span></span>
```
Submit-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e449f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e449f-107">DESCRIPTION</span></span>
<span data-ttu-id="e449f-108">Il cmdlet **Submit-AzSynapseSparkJob** Invia un processo Spark analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="e449f-108">The **Submit-AzSynapseSparkJob** cmdlet submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="e449f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e449f-109">EXAMPLES</span></span>

### <span data-ttu-id="e449f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e449f-110">Example 1</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language Spark -Name WordCount_Java -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/wordcount.jar -MainClassName WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="e449f-111">Questo comando Invia un processo Spark analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="e449f-111">This command submits a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="e449f-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e449f-112">Example 2</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language SparkDotNet -Name WordCount_Dotnet -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/wordcount.zip -MainExecutableFile WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/result -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="e449f-113">Questo comando Invia un processo di Spark .NET di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="e449f-113">This command submits a Synapse Analytics Spark .NET job.</span></span>

### <span data-ttu-id="e449f-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="e449f-114">Example 3</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language PySpark -Name WordCount_Python -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/wordcount.py -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="e449f-115">Questo comando Invia un processo di analisi di PySpark di sinapsi.</span><span class="sxs-lookup"><span data-stu-id="e449f-115">This command submits a Synapse Analytics PySpark job.</span></span>

## <span data-ttu-id="e449f-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e449f-116">PARAMETERS</span></span>

### <span data-ttu-id="e449f-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="e449f-117">-CommandLineArgument</span></span>
<span data-ttu-id="e449f-118">Argomenti facoltativi per il processo.</span><span class="sxs-lookup"><span data-stu-id="e449f-118">Optional arguments to the job.</span></span> <span data-ttu-id="e449f-119">ad esempio, "--iterazione 10000--timeout 20s"</span><span class="sxs-lookup"><span data-stu-id="e449f-119">e.g. "--iteration 10000 --timeout 20s"</span></span>

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

### <span data-ttu-id="e449f-120">-Configurazione</span><span class="sxs-lookup"><span data-stu-id="e449f-120">-Configuration</span></span>
<span data-ttu-id="e449f-121">Proprietà di configurazione Spark.</span><span class="sxs-lookup"><span data-stu-id="e449f-121">Spark configuration properties.</span></span>

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

### <span data-ttu-id="e449f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e449f-122">-DefaultProfile</span></span>
<span data-ttu-id="e449f-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e449f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e449f-124">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="e449f-124">-ExecutorCount</span></span>
<span data-ttu-id="e449f-125">Numero di esecutori da allocare nel pool di scintille specificato per il processo.</span><span class="sxs-lookup"><span data-stu-id="e449f-125">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="e449f-126">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="e449f-126">-ExecutorSize</span></span>
<span data-ttu-id="e449f-127">Numero di core e memoria da usare per gli esecutori assegnati nel pool di scintille specificato per il processo.</span><span class="sxs-lookup"><span data-stu-id="e449f-127">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="e449f-128">-Lingua</span><span class="sxs-lookup"><span data-stu-id="e449f-128">-Language</span></span>
<span data-ttu-id="e449f-129">Lingua del processo da inviare.</span><span class="sxs-lookup"><span data-stu-id="e449f-129">Language of the job to submit.</span></span>

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

### <span data-ttu-id="e449f-130">-MainClassName</span><span class="sxs-lookup"><span data-stu-id="e449f-130">-MainClassName</span></span>
<span data-ttu-id="e449f-131">L'identificatore completo o la classe Main che si trova nel file di definizione principale.</span><span class="sxs-lookup"><span data-stu-id="e449f-131">The fully-qualified identifier or the main class that is in the main definition file.</span></span>
<span data-ttu-id="e449f-132">Obbligatorio per il processo Spark e Spark di .NET.</span><span class="sxs-lookup"><span data-stu-id="e449f-132">Required for Spark and .NET Spark job.</span></span>
<span data-ttu-id="e449f-133">ad esempio, "org. Apache. Spark. examples. SparkPi"</span><span class="sxs-lookup"><span data-stu-id="e449f-133">e.g. "org.apache.spark.examples.SparkPi"</span></span>

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

### <span data-ttu-id="e449f-134">-MainDefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e449f-134">-MainDefinitionFile</span></span>
<span data-ttu-id="e449f-135">File principale usato per il processo.</span><span class="sxs-lookup"><span data-stu-id="e449f-135">The main file used for the job.</span></span>
<span data-ttu-id="e449f-136">ad esempio " abfss://filesystem@account.dfs.core.windows.net/mySpark.jar "</span><span class="sxs-lookup"><span data-stu-id="e449f-136">e.g. "abfss://filesystem@account.dfs.core.windows.net/mySpark.jar"</span></span>

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

### <span data-ttu-id="e449f-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="e449f-137">-Name</span></span>
<span data-ttu-id="e449f-138">Nome del processo Spark.</span><span class="sxs-lookup"><span data-stu-id="e449f-138">Name of Spark job.</span></span>

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

### <span data-ttu-id="e449f-139">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="e449f-139">-ReferenceFile</span></span>
<span data-ttu-id="e449f-140">File aggiuntivi usati per riferimento nel file di definizione principale.</span><span class="sxs-lookup"><span data-stu-id="e449f-140">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="e449f-141">Elenco URI di archiviazione delimitato da virgole.</span><span class="sxs-lookup"><span data-stu-id="e449f-141">Comma-separated storage URI list.</span></span> <span data-ttu-id="e449f-142">ad esempio abfss://filesystem@account.dfs.core.windows.net/file1.txt , ", abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="e449f-142">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="e449f-143">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="e449f-143">-SparkPoolName</span></span>
<span data-ttu-id="e449f-144">Nome del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="e449f-144">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="e449f-145">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="e449f-145">-SparkPoolObject</span></span>
<span data-ttu-id="e449f-146">Oggetto di input del pool di Spark, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="e449f-146">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e449f-147">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e449f-147">-WorkspaceName</span></span>
<span data-ttu-id="e449f-148">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="e449f-148">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e449f-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e449f-149">-Confirm</span></span>
<span data-ttu-id="e449f-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e449f-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e449f-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e449f-151">-WhatIf</span></span>
<span data-ttu-id="e449f-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e449f-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e449f-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e449f-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e449f-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e449f-154">CommonParameters</span></span>
<span data-ttu-id="e449f-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e449f-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e449f-156">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e449f-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e449f-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e449f-157">INPUTS</span></span>

### <span data-ttu-id="e449f-158">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="e449f-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="e449f-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e449f-159">OUTPUTS</span></span>

### <span data-ttu-id="e449f-160">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="e449f-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="e449f-161">Note</span><span class="sxs-lookup"><span data-stu-id="e449f-161">NOTES</span></span>

## <span data-ttu-id="e449f-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e449f-162">RELATED LINKS</span></span>
