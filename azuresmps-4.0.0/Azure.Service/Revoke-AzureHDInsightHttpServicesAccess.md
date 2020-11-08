---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A1DFA523-B532-4902-838D-74C8CA97A335
online version: ''
schema: 2.0.0
ms.openlocfilehash: f85d12100eb5b2b093eea252ac308e8a45cf1c53
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029896"
---
# <span data-ttu-id="d2f8b-101">Revoke-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d2f8b-101">Revoke-AzureHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="d2f8b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="d2f8b-103">Disabilita l'accesso HTTP a un cluster.</span><span class="sxs-lookup"><span data-stu-id="d2f8b-103">Disables HTTP access to a cluster.</span></span>

## <span data-ttu-id="d2f8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2f8b-104">SYNTAX</span></span>

```
Revoke-AzureHDInsightHttpServicesAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 [-IgnoreSslErrors <Boolean>] [-Endpoint <Uri>] -Location <String> -Name <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d2f8b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2f8b-105">DESCRIPTION</span></span>
<span data-ttu-id="d2f8b-106">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="d2f8b-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="d2f8b-107">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="d2f8b-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="d2f8b-108">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d2f8b-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="d2f8b-109">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="d2f8b-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="d2f8b-110">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="d2f8b-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="d2f8b-111">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d2f8b-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="d2f8b-112">Il cmdlet **Revoke-AzureHDInsightHttpServicesAccess** Disabilita l'accesso HTTP a un cluster per i servizi Web ODBC, Ambari, oozie e WebHCatalog.</span><span class="sxs-lookup"><span data-stu-id="d2f8b-112">The **Revoke-AzureHDInsightHttpServicesAccess** cmdlet disables HTTP access to a cluster for ODBC, Ambari, Oozie and WebHCatalog web services.</span></span>

## <span data-ttu-id="d2f8b-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2f8b-113">EXAMPLES</span></span>

## <span data-ttu-id="d2f8b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2f8b-114">PARAMETERS</span></span>

### <span data-ttu-id="d2f8b-115">-Certificato</span><span class="sxs-lookup"><span data-stu-id="d2f8b-115">-Certificate</span></span>
<span data-ttu-id="d2f8b-116">Specifica il certificato di gestione per un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="d2f8b-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="d2f8b-117">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="d2f8b-117">-Endpoint</span></span>
<span data-ttu-id="d2f8b-118">Specifica l'endpoint da usare per la connessione a Azure.</span><span class="sxs-lookup"><span data-stu-id="d2f8b-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="d2f8b-119">Se non specifichi questo parametro, questo cmdlet usa l'endpoint predefinito.</span><span class="sxs-lookup"><span data-stu-id="d2f8b-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="d2f8b-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="d2f8b-120">-HostedService</span></span>
<span data-ttu-id="d2f8b-121">Specifica lo spazio dei nomi di un servizio HDInsight se non si vuole usare lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="d2f8b-121">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="d2f8b-122">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="d2f8b-122">-IgnoreSslErrors</span></span>
<span data-ttu-id="d2f8b-123">Indica se gli errori SSL (Secure Sockets Layer) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="d2f8b-123">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="d2f8b-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d2f8b-124">-Location</span></span>
<span data-ttu-id="d2f8b-125">Specifica l'area geografica in cui si trova un cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d2f8b-125">Specifies the region in which an HDInsight cluster is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2f8b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2f8b-126">-Name</span></span>
<span data-ttu-id="d2f8b-127">Specifica il nome di un cluster.</span><span class="sxs-lookup"><span data-stu-id="d2f8b-127">Specifies the name of a cluster.</span></span>
<span data-ttu-id="d2f8b-128">Questo cmdlet disabilita l'accesso HTTP al cluster specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d2f8b-128">This cmdlet disables HTTP access to the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2f8b-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="d2f8b-129">-Profile</span></span>
<span data-ttu-id="d2f8b-130">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2f8b-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d2f8b-131">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d2f8b-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d2f8b-132">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="d2f8b-132">-Subscription</span></span>
<span data-ttu-id="d2f8b-133">Specifica l'account di sottoscrizione che contiene il cluster HDInsight da revocare.</span><span class="sxs-lookup"><span data-stu-id="d2f8b-133">Specifies the subscription account that contains the HDInsight cluster to revoke.</span></span>

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

### <span data-ttu-id="d2f8b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2f8b-134">CommonParameters</span></span>
<span data-ttu-id="d2f8b-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2f8b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2f8b-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2f8b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2f8b-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2f8b-137">INPUTS</span></span>

## <span data-ttu-id="d2f8b-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2f8b-138">OUTPUTS</span></span>

## <span data-ttu-id="d2f8b-139">Note</span><span class="sxs-lookup"><span data-stu-id="d2f8b-139">NOTES</span></span>

## <span data-ttu-id="d2f8b-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2f8b-140">RELATED LINKS</span></span>

[<span data-ttu-id="d2f8b-141">Grant-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d2f8b-141">Grant-AzureHDInsightHttpServicesAccess</span></span>](./Grant-AzureHDInsightHttpServicesAccess.md)


