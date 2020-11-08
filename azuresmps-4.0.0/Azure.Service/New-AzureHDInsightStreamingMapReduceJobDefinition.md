---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 824F6302-6285-4AEC-A63C-E2519DE4C7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2597d66e87de682bbf5702085612f7338d75deac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029471"
---
# <span data-ttu-id="f9039-101">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f9039-101">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="f9039-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f9039-102">SYNOPSIS</span></span>
<span data-ttu-id="f9039-103">Definisce un nuovo processo di flusso di MapReduce.</span><span class="sxs-lookup"><span data-stu-id="f9039-103">Defines a new streaming MapReduce job.</span></span>

## <span data-ttu-id="f9039-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9039-104">SYNTAX</span></span>

```
New-AzureHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-CmdEnv <String[]>]
 [-Combiner <String>] [-Defines <Hashtable>] [-Files <String[]>] [-InputPath <String>] [-JobName <String>]
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f9039-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9039-105">DESCRIPTION</span></span>
<span data-ttu-id="f9039-106">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="f9039-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="f9039-107">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="f9039-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="f9039-108">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f9039-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="f9039-109">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="f9039-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="f9039-110">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="f9039-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="f9039-111">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f9039-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="f9039-112">Il cmdlet **New-AzureHDInsightStreamingMapReduceJobDefinition** definisce un nuovo oggetto definizione processo che rappresenta i parametri di un processo di flusso di Hadoop.</span><span class="sxs-lookup"><span data-stu-id="f9039-112">The **New-AzureHDInsightStreamingMapReduceJobDefinition** cmdlet defines a new job definition object that represents the parameters of a Hadoop streaming job.</span></span>

## <span data-ttu-id="f9039-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9039-113">EXAMPLES</span></span>

### <span data-ttu-id="f9039-114">Esempio 1: creare una definizione di processo di flusso MapReduce</span><span class="sxs-lookup"><span data-stu-id="f9039-114">Example 1: Create a streaming MapReduce job definition</span></span>
```
PS C:\>$StreamingWordCount = New-AzureHDInsightStreamingMapReduceJobDefinition -Files "/Example/Apps/WordCount.exe", "/Example/Apps/Cat.exe" -InputPath "/Example/Data/Gutenberg/Davinci.txt" -OutputPath "/Example/Data/StreamingOutput/WordCount.txt" -Mapper "Cat.exe" -Reducer "WordCount.exe"
```

<span data-ttu-id="f9039-115">Questo comando crea la definizione del processo di flusso MapReduce specificato e la archivia nella variabile $StreamingWordCount.</span><span class="sxs-lookup"><span data-stu-id="f9039-115">This command creates the specified streaming MapReduce job definition, and then stores it in the $StreamingWordCount variable.</span></span>

## <span data-ttu-id="f9039-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f9039-116">PARAMETERS</span></span>

### <span data-ttu-id="f9039-117">-Argomenti</span><span class="sxs-lookup"><span data-stu-id="f9039-117">-Arguments</span></span>
<span data-ttu-id="f9039-118">Specifica una matrice di argomenti per un processo di Hadoop.</span><span class="sxs-lookup"><span data-stu-id="f9039-118">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="f9039-119">Gli argomenti vengono passati come argomenti della riga di comando per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="f9039-119">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Args

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9039-120">-CmdEnv</span><span class="sxs-lookup"><span data-stu-id="f9039-120">-CmdEnv</span></span>
<span data-ttu-id="f9039-121">Specifica una matrice di variabili di ambiente della riga di comando da impostare quando un processo viene eseguito su nodi dati.</span><span class="sxs-lookup"><span data-stu-id="f9039-121">Specifies an array of command-line environment variables to set when a job runs on data nodes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9039-122">-Combiner</span><span class="sxs-lookup"><span data-stu-id="f9039-122">-Combiner</span></span>
<span data-ttu-id="f9039-123">Specifica un nome di file combinatore.</span><span class="sxs-lookup"><span data-stu-id="f9039-123">Specifies a Combiner file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9039-124">-Definisce</span><span class="sxs-lookup"><span data-stu-id="f9039-124">-Defines</span></span>
<span data-ttu-id="f9039-125">Specifica i valori di configurazione di Hadoop da impostare quando il processo viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9039-125">Specifies Hadoop configuration values to set when the job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Params

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9039-126">-File</span><span class="sxs-lookup"><span data-stu-id="f9039-126">-Files</span></span>
<span data-ttu-id="f9039-127">Specifica una matrice di file necessari per un processo.</span><span class="sxs-lookup"><span data-stu-id="f9039-127">Specifies an array of files that are required for a job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9039-128">-InputPath</span><span class="sxs-lookup"><span data-stu-id="f9039-128">-InputPath</span></span>
<span data-ttu-id="f9039-129">Specifica il percorso di WASB per i file di input.</span><span class="sxs-lookup"><span data-stu-id="f9039-129">Specifies the WASB path to the input files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Input

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9039-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="f9039-130">-JobName</span></span>
<span data-ttu-id="f9039-131">Specifica il nome della nuova definizione di processo MapReduce.</span><span class="sxs-lookup"><span data-stu-id="f9039-131">Specifies the name of the new MapReduce job definition.</span></span>
<span data-ttu-id="f9039-132">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f9039-132">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9039-133">-Mapper</span><span class="sxs-lookup"><span data-stu-id="f9039-133">-Mapper</span></span>
<span data-ttu-id="f9039-134">Specifica un nome di file di Mapper.</span><span class="sxs-lookup"><span data-stu-id="f9039-134">Specifies a Mapper file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9039-135">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="f9039-135">-OutputPath</span></span>
<span data-ttu-id="f9039-136">Specifica il percorso di WASB per l'output del processo.</span><span class="sxs-lookup"><span data-stu-id="f9039-136">Specifies the WASB path for the job output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Output

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9039-137">-Profile</span><span class="sxs-lookup"><span data-stu-id="f9039-137">-Profile</span></span>
<span data-ttu-id="f9039-138">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9039-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f9039-139">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="f9039-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9039-140">-Riduttore</span><span class="sxs-lookup"><span data-stu-id="f9039-140">-Reducer</span></span>
<span data-ttu-id="f9039-141">Specifica un nome di file del riduttore.</span><span class="sxs-lookup"><span data-stu-id="f9039-141">Specifies a Reducer file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9039-142">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="f9039-142">-StatusFolder</span></span>
<span data-ttu-id="f9039-143">Specifica la cartella che contiene gli output standard e gli output degli errori per il processo, inclusi il codice di uscita e i registri delle attività.</span><span class="sxs-lookup"><span data-stu-id="f9039-143">Specifies the folder that contains the standard outputs and error outputs for the job, including its exit code and task logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9039-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9039-144">CommonParameters</span></span>
<span data-ttu-id="f9039-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9039-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9039-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9039-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9039-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f9039-147">INPUTS</span></span>

## <span data-ttu-id="f9039-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9039-148">OUTPUTS</span></span>

## <span data-ttu-id="f9039-149">Note</span><span class="sxs-lookup"><span data-stu-id="f9039-149">NOTES</span></span>

## <span data-ttu-id="f9039-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9039-150">RELATED LINKS</span></span>

[<span data-ttu-id="f9039-151">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f9039-151">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="f9039-152">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f9039-152">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="f9039-153">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f9039-153">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="f9039-154">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f9039-154">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)


