---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EE2ADA86-B2A3-4F6F-96EF-BB61D6DC550F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 338bef67e771bf211c063bf054e13e3844497850
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023722"
---
# <span data-ttu-id="596d7-101">Stop-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="596d7-101">Stop-AzureHDInsightJob</span></span>

## <span data-ttu-id="596d7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="596d7-102">SYNOPSIS</span></span>
<span data-ttu-id="596d7-103">Interrompe un processo di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="596d7-103">Stops an HDInsight job.</span></span>

## <span data-ttu-id="596d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="596d7-104">SYNTAX</span></span>

### <span data-ttu-id="596d7-105">Avviare jobDetails in un cluster HDInsight (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="596d7-105">Start jobDetails on an HDInsight Cluster (Default)</span></span>
```
Stop-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="596d7-106">Avviare jobDetails in un cluster HDInsight (con credenziali di sottoscrizione specifiche)</span><span class="sxs-lookup"><span data-stu-id="596d7-106">Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Stop-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="596d7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="596d7-107">DESCRIPTION</span></span>
<span data-ttu-id="596d7-108">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="596d7-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="596d7-109">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="596d7-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="596d7-110">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="596d7-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="596d7-111">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="596d7-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="596d7-112">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="596d7-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="596d7-113">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="596d7-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="596d7-114">Il cmdlet **Stop-AzureHDInsightJob** arresta un processo di Azure HDInsight nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="596d7-114">The **Stop-AzureHDInsightJob** cmdlet stops an Azure HDInsight job on the specified cluster.</span></span>

## <span data-ttu-id="596d7-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="596d7-115">EXAMPLES</span></span>

## <span data-ttu-id="596d7-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="596d7-116">PARAMETERS</span></span>

### <span data-ttu-id="596d7-117">-Certificato</span><span class="sxs-lookup"><span data-stu-id="596d7-117">-Certificate</span></span>
<span data-ttu-id="596d7-118">Specifica il certificato di gestione per un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="596d7-118">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="596d7-119">-Cluster</span><span class="sxs-lookup"><span data-stu-id="596d7-119">-Cluster</span></span>
<span data-ttu-id="596d7-120">Specifica un cluster.</span><span class="sxs-lookup"><span data-stu-id="596d7-120">Specifies a cluster.</span></span>
<span data-ttu-id="596d7-121">Questo cmdlet arresta un processo che viene eseguito nel cluster specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="596d7-121">This cmdlet stops a job that runs on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="596d7-122">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="596d7-122">-Credential</span></span>
<span data-ttu-id="596d7-123">Specifica le credenziali da usare per l'accesso diretto tramite HTTP a un cluster.</span><span class="sxs-lookup"><span data-stu-id="596d7-123">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="596d7-124">Puoi specificare questo parametro anziché il parametro *Subscription* per autenticare l'accesso a un cluster.</span><span class="sxs-lookup"><span data-stu-id="596d7-124">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

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

### <span data-ttu-id="596d7-125">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="596d7-125">-Endpoint</span></span>
<span data-ttu-id="596d7-126">Specifica l'endpoint da usare per la connessione a Azure.</span><span class="sxs-lookup"><span data-stu-id="596d7-126">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="596d7-127">Se non specifichi questo parametro, questo cmdlet usa l'endpoint predefinito.</span><span class="sxs-lookup"><span data-stu-id="596d7-127">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="596d7-128">-HostedService</span><span class="sxs-lookup"><span data-stu-id="596d7-128">-HostedService</span></span>
<span data-ttu-id="596d7-129">Specifica lo spazio dei nomi di un servizio HDInsight se non si vuole usare lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="596d7-129">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="596d7-130">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="596d7-130">-IgnoreSslErrors</span></span>
<span data-ttu-id="596d7-131">Indica se gli errori SSL (Secure Sockets Layer) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="596d7-131">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="596d7-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="596d7-132">-JobId</span></span>
<span data-ttu-id="596d7-133">Specifica l'ID del processo HDInsight da interrompere.</span><span class="sxs-lookup"><span data-stu-id="596d7-133">Specifies the ID of the HDInsight job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="596d7-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="596d7-134">-Profile</span></span>
<span data-ttu-id="596d7-135">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="596d7-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="596d7-136">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="596d7-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="596d7-137">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="596d7-137">-Subscription</span></span>
<span data-ttu-id="596d7-138">Specifica un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="596d7-138">Specifies a subscription.</span></span>
<span data-ttu-id="596d7-139">Questo cmdlet arresta un processo per l'abbonamento specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="596d7-139">This cmdlet stops a job for the subscription that this parameter specifies.</span></span>

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

### <span data-ttu-id="596d7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="596d7-140">CommonParameters</span></span>
<span data-ttu-id="596d7-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="596d7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="596d7-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="596d7-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="596d7-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="596d7-143">INPUTS</span></span>

## <span data-ttu-id="596d7-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="596d7-144">OUTPUTS</span></span>

## <span data-ttu-id="596d7-145">Note</span><span class="sxs-lookup"><span data-stu-id="596d7-145">NOTES</span></span>

## <span data-ttu-id="596d7-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="596d7-146">RELATED LINKS</span></span>

[<span data-ttu-id="596d7-147">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="596d7-147">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="596d7-148">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="596d7-148">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="596d7-149">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="596d7-149">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


