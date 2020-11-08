---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 60A5ACF7-2637-4BDC-BF41-80E81B23F4CD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0308c3ff5bee358a82d74d452784f42c69bc7c32
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023382"
---
# <span data-ttu-id="e3996-101">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e3996-101">Start-AzureHDInsightJob</span></span>

## <span data-ttu-id="e3996-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3996-102">SYNOPSIS</span></span>
<span data-ttu-id="e3996-103">Avvia un processo di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e3996-103">Starts an HDInsight job.</span></span>

## <span data-ttu-id="e3996-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3996-104">SYNTAX</span></span>

### <span data-ttu-id="e3996-105">Avviare jobDetails in un cluster HDInsight (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3996-105">Start jobDetails on an HDInsight Cluster (Default)</span></span>
```
Start-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>]
 -JobDefinition <AzureHDInsightJobDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e3996-106">Avviare jobDetails in un cluster HDInsight (con credenziali di sottoscrizione specifiche)</span><span class="sxs-lookup"><span data-stu-id="e3996-106">Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Start-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobDefinition <AzureHDInsightJobDefinition>
 [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e3996-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3996-107">DESCRIPTION</span></span>
<span data-ttu-id="e3996-108">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="e3996-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="e3996-109">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="e3996-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="e3996-110">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e3996-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="e3996-111">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="e3996-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="e3996-112">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="e3996-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="e3996-113">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e3996-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="e3996-114">Il cmdlet **Start-AzureHDInsightJob** avvia un processo di Azure HDInsight definito in un cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="e3996-114">The **Start-AzureHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="e3996-115">Il processo da avviare può essere un processo MapReduce, un processo di flusso, un processo hive o un processo di maiale.</span><span class="sxs-lookup"><span data-stu-id="e3996-115">The job to start can be a MapReduce job, a streaming job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="e3996-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3996-116">EXAMPLES</span></span>

### <span data-ttu-id="e3996-117">Esempio 1: avviare un processo di HDInsight</span><span class="sxs-lookup"><span data-stu-id="e3996-117">Example 1: Start an HDInsight job</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "Cluster01" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="e3996-118">Il primo comando ottiene l'ID corrente della sottoscrizione e lo archivia nella variabile $SubId.</span><span class="sxs-lookup"><span data-stu-id="e3996-118">The first command gets the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="e3996-119">Il secondo comando assegna il nome Cluster01 alla variabile $ClusterName.</span><span class="sxs-lookup"><span data-stu-id="e3996-119">The second command assigns the name Cluster01 to the $ClusterName variable.</span></span>

<span data-ttu-id="e3996-120">Il terzo comando usa il cmdlet **New-AzureHDInsightMapReduceJobDefinition** per creare una definizione di processo MapReduce e quindi la archivia nella variabile $WordCountJob.</span><span class="sxs-lookup"><span data-stu-id="e3996-120">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>

<span data-ttu-id="e3996-121">Il comando finale usa l'operatore pipeline per passare la $WordCountJob al cmdlet **Start-AzureHDInsightJob** per avviare il processo.</span><span class="sxs-lookup"><span data-stu-id="e3996-121">The final command uses the pipeline operator to pass the $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span>
<span data-ttu-id="e3996-122">Dopo l'avvio del processo, viene passato al cmdlet **wait-AzureHDInsightJob** , che attende il completamento del processo prima di passarlo al cmdlet **Get-AzureHDInsightJobOutput** per ottenere l'output del processo.</span><span class="sxs-lookup"><span data-stu-id="e3996-122">After the job starts, it is passed to the **Wait-AzureHDInsightJob** cmdlet, which waits for the job to complete before passing it to the **Get-AzureHDInsightJobOutput** cmdlet to get the job output.</span></span>

## <span data-ttu-id="e3996-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3996-123">PARAMETERS</span></span>

### <span data-ttu-id="e3996-124">-Certificato</span><span class="sxs-lookup"><span data-stu-id="e3996-124">-Certificate</span></span>
<span data-ttu-id="e3996-125">Specifica il certificato di gestione per un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="e3996-125">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3996-126">-Cluster</span><span class="sxs-lookup"><span data-stu-id="e3996-126">-Cluster</span></span>
<span data-ttu-id="e3996-127">Specifica un cluster.</span><span class="sxs-lookup"><span data-stu-id="e3996-127">Specifies a cluster.</span></span>
<span data-ttu-id="e3996-128">Questo cmdlet avvia un processo nel cluster specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e3996-128">This cmdlet starts a job on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3996-129">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="e3996-129">-Credential</span></span>
<span data-ttu-id="e3996-130">Specifica le credenziali del cluster per l'accesso HTTP diretto a un cluster.</span><span class="sxs-lookup"><span data-stu-id="e3996-130">Specifies cluster credentials for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="e3996-131">Puoi specificare questo parametro anziché il parametro *Subscription* per autenticare l'accesso a un cluster.</span><span class="sxs-lookup"><span data-stu-id="e3996-131">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Start jobDetails on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3996-132">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="e3996-132">-Endpoint</span></span>
<span data-ttu-id="e3996-133">Specifica l'endpoint da usare per la connessione a Azure.</span><span class="sxs-lookup"><span data-stu-id="e3996-133">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="e3996-134">Se non specifichi questo parametro, questo cmdlet usa l'endpoint predefinito.</span><span class="sxs-lookup"><span data-stu-id="e3996-134">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3996-135">-HostedService</span><span class="sxs-lookup"><span data-stu-id="e3996-135">-HostedService</span></span>
<span data-ttu-id="e3996-136">Specifica lo spazio dei nomi di un servizio HDInsight se non si vuole usare lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="e3996-136">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3996-137">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="e3996-137">-IgnoreSslErrors</span></span>
<span data-ttu-id="e3996-138">Indica se gli errori SSL (Secure Sockets Layer) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="e3996-138">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3996-139">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="e3996-139">-JobDefinition</span></span>
<span data-ttu-id="e3996-140">Specifica l'endpoint da usare per la connessione a Microsoft Azure se l'endpoint è diverso da quello predefinito.</span><span class="sxs-lookup"><span data-stu-id="e3996-140">Specifies the endpoint to use when connecting to Microsoft Azure if the endpoint is different from the default.</span></span>

```yaml
Type: AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: jobDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3996-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="e3996-141">-Profile</span></span>
<span data-ttu-id="e3996-142">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3996-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e3996-143">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="e3996-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e3996-144">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="e3996-144">-Subscription</span></span>
<span data-ttu-id="e3996-145">Specifica un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="e3996-145">Specifies a subscription.</span></span>
<span data-ttu-id="e3996-146">Questo cmdlet avvia un processo per l'abbonamento specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e3996-146">This cmdlet starts a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3996-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3996-147">CommonParameters</span></span>
<span data-ttu-id="e3996-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3996-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3996-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3996-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3996-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3996-150">INPUTS</span></span>

## <span data-ttu-id="e3996-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3996-151">OUTPUTS</span></span>

## <span data-ttu-id="e3996-152">Note</span><span class="sxs-lookup"><span data-stu-id="e3996-152">NOTES</span></span>

## <span data-ttu-id="e3996-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3996-153">RELATED LINKS</span></span>

[<span data-ttu-id="e3996-154">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e3996-154">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="e3996-155">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="e3996-155">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="e3996-156">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e3996-156">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="e3996-157">Stop-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e3996-157">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)

[<span data-ttu-id="e3996-158">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e3996-158">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


