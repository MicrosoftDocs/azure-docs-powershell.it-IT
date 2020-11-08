---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0B194605-F6B2-4FBC-ABF8-E49876EC7CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b215cfa95c20a2e8d13cfefa9e2ef0b3794a6727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023598"
---
# <span data-ttu-id="54a9e-101">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="54a9e-101">Get-AzureHDInsightJobOutput</span></span>

## <span data-ttu-id="54a9e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="54a9e-102">SYNOPSIS</span></span>
<span data-ttu-id="54a9e-103">Ottiene l'output del log per un processo.</span><span class="sxs-lookup"><span data-stu-id="54a9e-103">Gets the log output for a job.</span></span>

## <span data-ttu-id="54a9e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="54a9e-104">SYNTAX</span></span>

```
Get-AzureHDInsightJobOutput [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-DownloadTaskLogs] [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-StandardError]
 [-StandardOutput] [-Subscription <String>] [-TaskLogsDirectory <String>] [-TaskSummary]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="54a9e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54a9e-105">DESCRIPTION</span></span>
<span data-ttu-id="54a9e-106">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="54a9e-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="54a9e-107">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="54a9e-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="54a9e-108">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="54a9e-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="54a9e-109">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere creare cluster basati su Linux in [HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span><span class="sxs-lookup"><span data-stu-id="54a9e-109">For information about how to use the new HDInsight to create a cluster, see Create Linux-based clusters in [HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="54a9e-110">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span><span class="sxs-lookup"><span data-stu-id="54a9e-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="54a9e-111">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span><span class="sxs-lookup"><span data-stu-id="54a9e-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="54a9e-112">Il cmdlet **Get-AzureHDInsightJobOutput** Ottiene l'output del log per un processo dall'account di archiviazione associato a un cluster.</span><span class="sxs-lookup"><span data-stu-id="54a9e-112">The **Get-AzureHDInsightJobOutput** cmdlet gets the log output for a job from the storage account associated with a cluster.</span></span>
<span data-ttu-id="54a9e-113">È possibile ottenere vari tipi di log dei processi, tra cui output standard, errore standard, registri delle attività e riepilogo dei registri delle attività.</span><span class="sxs-lookup"><span data-stu-id="54a9e-113">You can get various types of job logs including standard output, standard error, task logs, and a summary of the task logs.</span></span>

## <span data-ttu-id="54a9e-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="54a9e-114">EXAMPLES</span></span>

### <span data-ttu-id="54a9e-115">Esempio 1: ottenere l'output del processo</span><span class="sxs-lookup"><span data-stu-id="54a9e-115">Example 1: Get job output</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster"
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" $WordCountJob
    | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -StandardError
```

<span data-ttu-id="54a9e-116">Il primo comando ottiene l'ID della sottoscrizione corrente e lo archivia nella variabile $SubId.</span><span class="sxs-lookup"><span data-stu-id="54a9e-116">The first command gets the ID of the current subscription, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="54a9e-117">Il secondo comando Archivia il nome cluster nella variabile $Clustername.</span><span class="sxs-lookup"><span data-stu-id="54a9e-117">The second command stores the name MyCluster in the $Clustername variable.</span></span>

<span data-ttu-id="54a9e-118">Il terzo comando crea una definizione di processo MapReduce e la archivia nella variabile $WordCountJob.</span><span class="sxs-lookup"><span data-stu-id="54a9e-118">The third command creates a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>
<span data-ttu-id="54a9e-119">Il comando passa il processo in $WordCountJob al cmdlet **Start-AzureHDInsightJob** per avviare il processo.</span><span class="sxs-lookup"><span data-stu-id="54a9e-119">The command passes the job in $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span>
<span data-ttu-id="54a9e-120">Passa inoltre $WordCountJob al cmdlet **wait-AzureHDInsightJob** per attendere il completamento del processo e quindi usa **Get-AzureHDInsightJobOutput** per ottenere l'output del processo.</span><span class="sxs-lookup"><span data-stu-id="54a9e-120">It also passes $WordCountJob to the **Wait-AzureHDInsightJob** cmdlet to wait for the job to finish, and then it uses **Get-AzureHDInsightJobOutput** to get the job output.</span></span>

## <span data-ttu-id="54a9e-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="54a9e-121">PARAMETERS</span></span>

### <span data-ttu-id="54a9e-122">-Certificato</span><span class="sxs-lookup"><span data-stu-id="54a9e-122">-Certificate</span></span>
<span data-ttu-id="54a9e-123">Specifica il certificato di gestione per un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="54a9e-123">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a9e-124">-Cluster</span><span class="sxs-lookup"><span data-stu-id="54a9e-124">-Cluster</span></span>
<span data-ttu-id="54a9e-125">Specifica un cluster.</span><span class="sxs-lookup"><span data-stu-id="54a9e-125">Specifies a cluster.</span></span>
<span data-ttu-id="54a9e-126">Questo cmdlet consente di ottenere i log dei processi dal cluster specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="54a9e-126">This cmdlet gets job logs from the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54a9e-127">-DownloadTaskLogs</span><span class="sxs-lookup"><span data-stu-id="54a9e-127">-DownloadTaskLogs</span></span>
<span data-ttu-id="54a9e-128">Indica che questo cmdlet ottiene i registri delle attività per un processo.</span><span class="sxs-lookup"><span data-stu-id="54a9e-128">Indicates that this cmdlet gets the task logs for a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a9e-129">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="54a9e-129">-Endpoint</span></span>
<span data-ttu-id="54a9e-130">Specifica l'endpoint da usare per la connessione a Azure.</span><span class="sxs-lookup"><span data-stu-id="54a9e-130">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="54a9e-131">Se non specifichi questo parametro, questo cmdlet usa l'endpoint predefinito.</span><span class="sxs-lookup"><span data-stu-id="54a9e-131">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a9e-132">-HostedService</span><span class="sxs-lookup"><span data-stu-id="54a9e-132">-HostedService</span></span>
<span data-ttu-id="54a9e-133">Specifica lo spazio dei nomi di un servizio HDInsight se non si vuole usare lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="54a9e-133">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a9e-134">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="54a9e-134">-IgnoreSslErrors</span></span>
<span data-ttu-id="54a9e-135">Indica se gli errori SSL (Secure Sockets Layer) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="54a9e-135">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a9e-136">-JobId</span><span class="sxs-lookup"><span data-stu-id="54a9e-136">-JobId</span></span>
<span data-ttu-id="54a9e-137">Specifica l'ID del processo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="54a9e-137">Specifies the ID of the job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54a9e-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="54a9e-138">-Profile</span></span>
<span data-ttu-id="54a9e-139">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54a9e-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54a9e-140">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="54a9e-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="54a9e-141">-StandardError</span><span class="sxs-lookup"><span data-stu-id="54a9e-141">-StandardError</span></span>
<span data-ttu-id="54a9e-142">Indica che questo cmdlet ottiene l'output StdErr di un processo.</span><span class="sxs-lookup"><span data-stu-id="54a9e-142">Indicates that this cmdlet gets the StdErr output of a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a9e-143">-StandardOutput</span><span class="sxs-lookup"><span data-stu-id="54a9e-143">-StandardOutput</span></span>
<span data-ttu-id="54a9e-144">Indica che questo cmdlet ottiene l'output SdtOut di un processo.</span><span class="sxs-lookup"><span data-stu-id="54a9e-144">Indicates that this cmdlet gets the SdtOut output of a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a9e-145">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="54a9e-145">-Subscription</span></span>
<span data-ttu-id="54a9e-146">Specifica l'abbonamento che contiene il cluster HDInsight per ottenere.</span><span class="sxs-lookup"><span data-stu-id="54a9e-146">Specifies the subscription that contains the HDInsight cluster to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a9e-147">-TaskLogsDirectory</span><span class="sxs-lookup"><span data-stu-id="54a9e-147">-TaskLogsDirectory</span></span>
<span data-ttu-id="54a9e-148">Specifica una cartella locale in cui archiviare i registri delle attività.</span><span class="sxs-lookup"><span data-stu-id="54a9e-148">Specifies a local folder in which to store tasks logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LogsDir

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a9e-149">-TaskSummary</span><span class="sxs-lookup"><span data-stu-id="54a9e-149">-TaskSummary</span></span>
<span data-ttu-id="54a9e-150">Indica che questo cmdlet ottiene il riepilogo del log attività.</span><span class="sxs-lookup"><span data-stu-id="54a9e-150">Indicates that this cmdlets gets the task log summary.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a9e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54a9e-151">CommonParameters</span></span>
<span data-ttu-id="54a9e-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54a9e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54a9e-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54a9e-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54a9e-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="54a9e-154">INPUTS</span></span>

## <span data-ttu-id="54a9e-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="54a9e-155">OUTPUTS</span></span>

## <span data-ttu-id="54a9e-156">Note</span><span class="sxs-lookup"><span data-stu-id="54a9e-156">NOTES</span></span>

## <span data-ttu-id="54a9e-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="54a9e-157">RELATED LINKS</span></span>

[<span data-ttu-id="54a9e-158">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="54a9e-158">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="54a9e-159">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="54a9e-159">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="54a9e-160">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="54a9e-160">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)
