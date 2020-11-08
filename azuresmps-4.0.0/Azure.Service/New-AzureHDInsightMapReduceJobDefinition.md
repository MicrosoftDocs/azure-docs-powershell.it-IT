---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A8953045-3836-4C5A-96F8-461CB1DB6BBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58958a6bedd29cd55535fe879fab813a430ff20b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023874"
---
# <span data-ttu-id="42b9a-101">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="42b9a-101">New-AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="42b9a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="42b9a-103">Definisce un nuovo processo di MapReduce.</span><span class="sxs-lookup"><span data-stu-id="42b9a-103">Defines a new MapReduce job.</span></span>

## <span data-ttu-id="42b9a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42b9a-104">SYNTAX</span></span>

```
New-AzureHDInsightMapReduceJobDefinition [-Arguments <String[]>] -ClassName <String> [-Defines <Hashtable>]
 [-Files <String[]>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="42b9a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42b9a-105">DESCRIPTION</span></span>
<span data-ttu-id="42b9a-106">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="42b9a-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="42b9a-107">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="42b9a-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="42b9a-108">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="42b9a-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="42b9a-109">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="42b9a-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="42b9a-110">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="42b9a-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="42b9a-111">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="42b9a-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="42b9a-112">Il cmdlet **New-AzureHDInsightMapReduceJobDefinition** definisce un nuovo processo MapReduce da eseguire in un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="42b9a-112">The **New-AzureHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job to run on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="42b9a-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42b9a-113">EXAMPLES</span></span>

### <span data-ttu-id="42b9a-114">Esempio 1: definire un processo MapReduce, eseguire il processo e ottenere l'output</span><span class="sxs-lookup"><span data-stu-id="42b9a-114">Example 1: Define a MapReduce job, run the job, and get the output</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "WordCount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="42b9a-115">Il primo comando ottiene l'ID della sottoscrizione corrente e lo archivia nella variabile $SubId.</span><span class="sxs-lookup"><span data-stu-id="42b9a-115">The first command gets the ID of the current subscription, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="42b9a-116">Il secondo comando assegna il nome "cluster" alla variabile $Clustername.</span><span class="sxs-lookup"><span data-stu-id="42b9a-116">The second command assigns the name MyCluster to the $Clustername variable.</span></span>

<span data-ttu-id="42b9a-117">Il terzo comando usa il cmdlet **New-AzureHDInsightMapReduceJobDefinition** per creare una definizione di processo MapReduce e quindi archiviarla nella variabile $WordCountJob.</span><span class="sxs-lookup"><span data-stu-id="42b9a-117">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then store it in the $WordCountJob variable.</span></span>

<span data-ttu-id="42b9a-118">Il quarto comando esegue una sequenza di operazioni usando questi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="42b9a-118">The fourth command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="42b9a-119">**Start-AzureHDInsightJob** per avviare il processo in $clustername.</span><span class="sxs-lookup"><span data-stu-id="42b9a-119">**Start-AzureHDInsightJob** to start the job on $ClusterName.</span></span> 
- <span data-ttu-id="42b9a-120">**Wait-AzureHDInsightJob** aspetta che il processo finisca e visualizzi lo stato di avanzamento verso il completamento.</span><span class="sxs-lookup"><span data-stu-id="42b9a-120">**Wait-AzureHDInsightJob** to wait for the job to finish and to display the progress toward completion.</span></span>
- <span data-ttu-id="42b9a-121">**Get-AzureHDInsightJobOutput** per ottenere l'output del processo.</span><span class="sxs-lookup"><span data-stu-id="42b9a-121">**Get-AzureHDInsightJobOutput** to get the job output.</span></span>

## <span data-ttu-id="42b9a-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42b9a-122">PARAMETERS</span></span>

### <span data-ttu-id="42b9a-123">-Argomenti</span><span class="sxs-lookup"><span data-stu-id="42b9a-123">-Arguments</span></span>
<span data-ttu-id="42b9a-124">Specifica una matrice di argomenti per un processo di Hadoop.</span><span class="sxs-lookup"><span data-stu-id="42b9a-124">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="42b9a-125">Gli argomenti vengono passati come argomenti della riga di comando per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="42b9a-125">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="42b9a-126">-ClassName</span><span class="sxs-lookup"><span data-stu-id="42b9a-126">-ClassName</span></span>
<span data-ttu-id="42b9a-127">Specifica il nome della classe Job nel file Java Archive (JAR).</span><span class="sxs-lookup"><span data-stu-id="42b9a-127">Specifies the name of the job class in the Java Archive (JAR) file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Class

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b9a-128">-Definisce</span><span class="sxs-lookup"><span data-stu-id="42b9a-128">-Defines</span></span>
<span data-ttu-id="42b9a-129">Specifica i valori di configurazione di Hadoop da impostare quando il processo viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42b9a-129">Specifies Hadoop configuration values to set when the job runs.</span></span>

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

### <span data-ttu-id="42b9a-130">-File</span><span class="sxs-lookup"><span data-stu-id="42b9a-130">-Files</span></span>
<span data-ttu-id="42b9a-131">Specifica una matrice di file WASB necessari per un processo.</span><span class="sxs-lookup"><span data-stu-id="42b9a-131">Specifies an array of WASB files that are required for a job.</span></span>

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

### <span data-ttu-id="42b9a-132">-JarFile</span><span class="sxs-lookup"><span data-stu-id="42b9a-132">-JarFile</span></span>
<span data-ttu-id="42b9a-133">Specifica il nome completo di un file JAR che contiene il codice e le dipendenze di un processo di MapReduce.</span><span class="sxs-lookup"><span data-stu-id="42b9a-133">Specifies the fully qualified name of a JAR file that contains the code and dependencies of a MapReduce job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Jar

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b9a-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="42b9a-134">-JobName</span></span>
<span data-ttu-id="42b9a-135">Specifica il nome di un processo di MapReduce.</span><span class="sxs-lookup"><span data-stu-id="42b9a-135">Specifies the name of a MapReduce job.</span></span>
<span data-ttu-id="42b9a-136">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="42b9a-136">This parameter is optional.</span></span>
<span data-ttu-id="42b9a-137">Se non specifichi questo parametro, viene usato il valore del parametro *ClassName* .</span><span class="sxs-lookup"><span data-stu-id="42b9a-137">If you do not specify this parameter, the value of the *ClassName* parameter is used.</span></span>

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

### <span data-ttu-id="42b9a-138">-LibJars</span><span class="sxs-lookup"><span data-stu-id="42b9a-138">-LibJars</span></span>
<span data-ttu-id="42b9a-139">Specifica una matrice di riferimenti LibJar del processo.</span><span class="sxs-lookup"><span data-stu-id="42b9a-139">Specifies an array of LibJar references of the job.</span></span>

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

### <span data-ttu-id="42b9a-140">-Profile</span><span class="sxs-lookup"><span data-stu-id="42b9a-140">-Profile</span></span>
<span data-ttu-id="42b9a-141">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42b9a-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="42b9a-142">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="42b9a-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="42b9a-143">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="42b9a-143">-StatusFolder</span></span>
<span data-ttu-id="42b9a-144">Specifica la posizione della cartella che contiene gli output standard e gli output degli errori per un processo, inclusi il codice di uscita e i registri delle attività.</span><span class="sxs-lookup"><span data-stu-id="42b9a-144">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="42b9a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42b9a-145">CommonParameters</span></span>
<span data-ttu-id="42b9a-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42b9a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42b9a-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42b9a-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42b9a-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42b9a-148">INPUTS</span></span>

## <span data-ttu-id="42b9a-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42b9a-149">OUTPUTS</span></span>

## <span data-ttu-id="42b9a-150">Note</span><span class="sxs-lookup"><span data-stu-id="42b9a-150">NOTES</span></span>

## <span data-ttu-id="42b9a-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42b9a-151">RELATED LINKS</span></span>

[<span data-ttu-id="42b9a-152">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="42b9a-152">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="42b9a-153">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="42b9a-153">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="42b9a-154">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="42b9a-154">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="42b9a-155">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="42b9a-155">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="42b9a-156">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="42b9a-156">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="42b9a-157">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="42b9a-157">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


