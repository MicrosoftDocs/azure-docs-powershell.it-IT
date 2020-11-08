---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3E3C9626-7AED-4B15-93D0-0B79AD17A834
online version: ''
schema: 2.0.0
ms.openlocfilehash: de4b768dbc6c97e84bccd4c8e0ef42f6f81a5b31
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029812"
---
# <span data-ttu-id="e6e68-101">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e6e68-101">Get-AzureHDInsightJob</span></span>

## <span data-ttu-id="e6e68-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6e68-102">SYNOPSIS</span></span>
<span data-ttu-id="e6e68-103">Ottiene i processi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e6e68-103">Gets HDInsight jobs.</span></span>

## <span data-ttu-id="e6e68-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6e68-104">SYNTAX</span></span>

### <span data-ttu-id="e6e68-105">Ottenere la cronologia jobDetails di un cluster HDInsight (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e6e68-105">Get jobDetails History of a HDInsight Cluster (Default)</span></span>
```
Get-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] [-IgnoreSslErrors <Boolean>]
 [-JobId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e6e68-106">Ottenere la cronologia jobDetails di un cluster HDInsight (con credenziali di sottoscrizione specifiche)</span><span class="sxs-lookup"><span data-stu-id="e6e68-106">Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Get-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] [-JobId <String>] [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e6e68-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6e68-107">DESCRIPTION</span></span>
<span data-ttu-id="e6e68-108">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="e6e68-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="e6e68-109">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="e6e68-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="e6e68-110">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e6e68-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="e6e68-111">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="e6e68-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="e6e68-112">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="e6e68-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="e6e68-113">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e6e68-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="e6e68-114">Il cmdlet **Get-AzureHDInsightJob** ottiene i processi di HDInsight di Azure recenti per un cluster specificato e li visualizza in ordine cronologico inverso.</span><span class="sxs-lookup"><span data-stu-id="e6e68-114">The **Get-AzureHDInsightJob** cmdlet gets recent Azure HDInsight jobs for a specified cluster and displays them in reverse chronological order.</span></span>

## <span data-ttu-id="e6e68-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6e68-115">EXAMPLES</span></span>

## <span data-ttu-id="e6e68-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6e68-116">PARAMETERS</span></span>

### <span data-ttu-id="e6e68-117">-Certificato</span><span class="sxs-lookup"><span data-stu-id="e6e68-117">-Certificate</span></span>
<span data-ttu-id="e6e68-118">Specifica il certificato di gestione per un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="e6e68-118">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="e6e68-119">-Cluster</span><span class="sxs-lookup"><span data-stu-id="e6e68-119">-Cluster</span></span>
<span data-ttu-id="e6e68-120">Specifica un cluster.</span><span class="sxs-lookup"><span data-stu-id="e6e68-120">Specifies a cluster.</span></span>
<span data-ttu-id="e6e68-121">Questo cmdlet ottiene i processi di HDInsight eseguiti nel cluster specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e6e68-121">This cmdlet gets HDInsight jobs that run on the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="e6e68-122">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="e6e68-122">-Credential</span></span>
<span data-ttu-id="e6e68-123">Specifica le credenziali da usare per l'accesso diretto tramite HTTP a un cluster.</span><span class="sxs-lookup"><span data-stu-id="e6e68-123">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="e6e68-124">Puoi specificare questo parametro anziché il parametro *Subscription* per autenticare l'accesso a un cluster.</span><span class="sxs-lookup"><span data-stu-id="e6e68-124">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Get jobDetails History of a HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e68-125">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="e6e68-125">-Endpoint</span></span>
<span data-ttu-id="e6e68-126">Specifica l'endpoint da usare per la connessione a Azure.</span><span class="sxs-lookup"><span data-stu-id="e6e68-126">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="e6e68-127">Se non specifichi questo parametro, questo cmdlet usa l'endpoint predefinito.</span><span class="sxs-lookup"><span data-stu-id="e6e68-127">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="e6e68-128">-HostedService</span><span class="sxs-lookup"><span data-stu-id="e6e68-128">-HostedService</span></span>
<span data-ttu-id="e6e68-129">Specifica lo spazio dei nomi di un servizio HDInsight se non si vuole usare lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="e6e68-129">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="e6e68-130">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="e6e68-130">-IgnoreSslErrors</span></span>
<span data-ttu-id="e6e68-131">Indica se gli errori SSL (Secure Sockets Layer) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="e6e68-131">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="e6e68-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="e6e68-132">-JobId</span></span>
<span data-ttu-id="e6e68-133">Specifica l'ID di un processo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="e6e68-133">Specifies the ID of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6e68-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="e6e68-134">-Profile</span></span>
<span data-ttu-id="e6e68-135">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6e68-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e6e68-136">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="e6e68-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e6e68-137">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="e6e68-137">-Subscription</span></span>
<span data-ttu-id="e6e68-138">Specifica l'abbonamento che contiene i processi di HDInsight da ottenere.</span><span class="sxs-lookup"><span data-stu-id="e6e68-138">Specifies the subscription that contains the HDInsight jobs to get.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e68-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6e68-139">CommonParameters</span></span>
<span data-ttu-id="e6e68-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6e68-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6e68-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6e68-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6e68-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6e68-142">INPUTS</span></span>

## <span data-ttu-id="e6e68-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6e68-143">OUTPUTS</span></span>

## <span data-ttu-id="e6e68-144">Note</span><span class="sxs-lookup"><span data-stu-id="e6e68-144">NOTES</span></span>

## <span data-ttu-id="e6e68-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6e68-145">RELATED LINKS</span></span>

[<span data-ttu-id="e6e68-146">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e6e68-146">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="e6e68-147">Stop-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e6e68-147">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)

[<span data-ttu-id="e6e68-148">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e6e68-148">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


