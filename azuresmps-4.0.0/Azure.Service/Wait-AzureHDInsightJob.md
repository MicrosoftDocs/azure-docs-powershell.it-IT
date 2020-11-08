---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 2EA36090-1A45-4F77-9222-9C0E9C07656C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea1247fd2b91f173b8125ad61c0bf2b57f408d18
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023790"
---
# <span data-ttu-id="054fc-101">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="054fc-101">Wait-AzureHDInsightJob</span></span>

## <span data-ttu-id="054fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="054fc-102">SYNOPSIS</span></span>
<span data-ttu-id="054fc-103">Attende il completamento o l'errore di un processo di HDInsight e visualizza lo stato di avanzamento del processo.</span><span class="sxs-lookup"><span data-stu-id="054fc-103">Awaits the completion or failure of an HDInsight job and displays the progress of the job.</span></span>

## <span data-ttu-id="054fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="054fc-104">SYNTAX</span></span>

### <span data-ttu-id="054fc-105">Ottenere la cronologia jobDetails di un cluster HDInsight (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="054fc-105">Get jobDetails History of a HDInsight Cluster (Default)</span></span>
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="054fc-106">Ottenere la cronologia jobDetails di un cluster HDInsight (con credenziali di sottoscrizione specifiche)</span><span class="sxs-lookup"><span data-stu-id="054fc-106">Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Wait-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Job <AzureHDInsightJob> -Subscription <String> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="054fc-107">Lavoro di attesa con JobId in un cluster HDInsight</span><span class="sxs-lookup"><span data-stu-id="054fc-107">Wait Job with JobId on an HDInsight Cluster</span></span>
```
Wait-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-WaitTimeoutInSeconds <Double>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="054fc-108">Lavoro di attesa con processo in un cluster HDInsight</span><span class="sxs-lookup"><span data-stu-id="054fc-108">Wait Job with Job on an HDInsight Cluster</span></span>
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] -Job <AzureHDInsightJob> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="054fc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="054fc-109">DESCRIPTION</span></span>
<span data-ttu-id="054fc-110">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="054fc-110">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="054fc-111">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="054fc-111">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="054fc-112">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="054fc-112">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="054fc-113">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="054fc-113">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="054fc-114">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="054fc-114">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="054fc-115">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="054fc-115">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="054fc-116">Il cmdlet **wait-AzureHDInsightJob** attende il completamento o l'errore di un processo di Azure HDInsight e visualizza lo stato di avanzamento del processo.</span><span class="sxs-lookup"><span data-stu-id="054fc-116">The **Wait-AzureHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job and displays the progress of the job.</span></span>

## <span data-ttu-id="054fc-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="054fc-117">EXAMPLES</span></span>

### <span data-ttu-id="054fc-118">Esempio 1: eseguire un processo e attenderne il completamento</span><span class="sxs-lookup"><span data-stu-id="054fc-118">Example 1: Run a job and wait for it to complete</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:>\ $ClusterName = "MyCluster"
PS C:>\ $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:>\ $WordCountJob | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="054fc-119">Il primo comando ottiene l'ID di abbonamento di Azure corrente e lo archivia nella variabile $SubId.</span><span class="sxs-lookup"><span data-stu-id="054fc-119">The first command gets the current Azure subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="054fc-120">Il secondo comando ottiene il cluster specificato e lo archivia nella variabile $ClusterName.</span><span class="sxs-lookup"><span data-stu-id="054fc-120">The second command gets the specified cluster, and then stores it in the $ClusterName variable.</span></span>

<span data-ttu-id="054fc-121">Il terzo comando usa il cmdlet **New-AzureHDInsightMapReduceJobDefinition** per creare una definizione di processo MapReduce e quindi la archivia nella variabile $WordCountJob.</span><span class="sxs-lookup"><span data-stu-id="054fc-121">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>

<span data-ttu-id="054fc-122">Il quarto comando usa diversi cmdlet in sequenza:</span><span class="sxs-lookup"><span data-stu-id="054fc-122">The fourth command uses several cmdlets in sequence:</span></span> 

- <span data-ttu-id="054fc-123">Usa l'operatore pipeline per passare $WordCountJob al cmdlet **Start-AzureHDInsightJob** per avviare il processo.</span><span class="sxs-lookup"><span data-stu-id="054fc-123">It uses the pipeline operator to pass $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span> 
- <span data-ttu-id="054fc-124">Il processo viene passato al cmdlet **wait-AzureHDInsightJob** per attendere 3600 secondi per completare il processo.</span><span class="sxs-lookup"><span data-stu-id="054fc-124">The job is passed to the **Wait-AzureHDInsightJob** cmdlet to wait 3600 seconds for the job to complete.</span></span> 
- <span data-ttu-id="054fc-125">Se il processo viene completato, il comando usa il cmdlet **Get-AzureHDInsightJobOutput** per ottenere l'output del processo.</span><span class="sxs-lookup"><span data-stu-id="054fc-125">If the job completes, the command uses the **Get-AzureHDInsightJobOutput** cmdlet to get the job output.</span></span>

## <span data-ttu-id="054fc-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="054fc-126">PARAMETERS</span></span>

### <span data-ttu-id="054fc-127">-Certificato</span><span class="sxs-lookup"><span data-stu-id="054fc-127">-Certificate</span></span>
<span data-ttu-id="054fc-128">Specifica il certificato di gestione per un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="054fc-128">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="054fc-129">-Cluster</span><span class="sxs-lookup"><span data-stu-id="054fc-129">-Cluster</span></span>
<span data-ttu-id="054fc-130">Specifica un cluster.</span><span class="sxs-lookup"><span data-stu-id="054fc-130">Specifies a cluster.</span></span>
<span data-ttu-id="054fc-131">Questo cmdlet attende un processo nel cluster specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="054fc-131">This cmdlet waits for a job on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="054fc-132">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="054fc-132">-Credential</span></span>
<span data-ttu-id="054fc-133">Specifica le credenziali da usare per l'accesso diretto tramite HTTP a un cluster.</span><span class="sxs-lookup"><span data-stu-id="054fc-133">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="054fc-134">Puoi specificare questo parametro anziché il parametro *Subscription* per autenticare l'accesso a un cluster.</span><span class="sxs-lookup"><span data-stu-id="054fc-134">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Get jobDetails History of a HDInsight Cluster, Wait Job with JobId on an HDInsight Cluster, Wait Job with Job on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="054fc-135">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="054fc-135">-Endpoint</span></span>
<span data-ttu-id="054fc-136">Specifica l'endpoint da usare per la connessione a Azure.</span><span class="sxs-lookup"><span data-stu-id="054fc-136">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="054fc-137">Se non specifichi questo parametro, questo cmdlet usa l'endpoint predefinito.</span><span class="sxs-lookup"><span data-stu-id="054fc-137">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="054fc-138">-HostedService</span><span class="sxs-lookup"><span data-stu-id="054fc-138">-HostedService</span></span>
<span data-ttu-id="054fc-139">Specifica lo spazio dei nomi di un servizio HDInsight.</span><span class="sxs-lookup"><span data-stu-id="054fc-139">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="054fc-140">Se non specifichi questo parametro, viene usato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="054fc-140">If you do not specify this parameter, the default namespace is used.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="054fc-141">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="054fc-141">-IgnoreSslErrors</span></span>
<span data-ttu-id="054fc-142">Indica se gli errori SSL (Secure Sockets Layer) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="054fc-142">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="054fc-143">-Job</span><span class="sxs-lookup"><span data-stu-id="054fc-143">-Job</span></span>
<span data-ttu-id="054fc-144">Specifica un processo di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="054fc-144">Specifies an Azure HDInsight job.</span></span>

```yaml
Type: AzureHDInsightJob
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential), Wait Job with Job on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="054fc-145">-JobId</span><span class="sxs-lookup"><span data-stu-id="054fc-145">-JobId</span></span>
<span data-ttu-id="054fc-146">Specifica l'ID del processo da attendere.</span><span class="sxs-lookup"><span data-stu-id="054fc-146">Specifies the ID of the job to wait for.</span></span>

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="054fc-147">-Profile</span><span class="sxs-lookup"><span data-stu-id="054fc-147">-Profile</span></span>
<span data-ttu-id="054fc-148">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="054fc-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="054fc-149">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="054fc-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="054fc-150">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="054fc-150">-Subscription</span></span>
<span data-ttu-id="054fc-151">Specifica un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="054fc-151">Specifies a subscription.</span></span>
<span data-ttu-id="054fc-152">Questo cmdlet attende un processo per l'abbonamento specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="054fc-152">This cmdlet waits for a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="054fc-153">-WaitTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="054fc-153">-WaitTimeoutInSeconds</span></span>
<span data-ttu-id="054fc-154">Specifica il timeout, in secondi, per l'operazione di attesa.</span><span class="sxs-lookup"><span data-stu-id="054fc-154">Specifies the time-out, in seconds, for the wait operation.</span></span>
<span data-ttu-id="054fc-155">Se il timeout scade prima del completamento del processo, il cmdlet cessa di essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="054fc-155">If the time-out expires before the job completes, the cmdlet ceases to run.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="054fc-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="054fc-156">CommonParameters</span></span>
<span data-ttu-id="054fc-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="054fc-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="054fc-158">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="054fc-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="054fc-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="054fc-159">INPUTS</span></span>

## <span data-ttu-id="054fc-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="054fc-160">OUTPUTS</span></span>

## <span data-ttu-id="054fc-161">Note</span><span class="sxs-lookup"><span data-stu-id="054fc-161">NOTES</span></span>

## <span data-ttu-id="054fc-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="054fc-162">RELATED LINKS</span></span>

[<span data-ttu-id="054fc-163">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="054fc-163">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="054fc-164">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="054fc-164">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="054fc-165">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="054fc-165">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="054fc-166">Stop-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="054fc-166">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)


