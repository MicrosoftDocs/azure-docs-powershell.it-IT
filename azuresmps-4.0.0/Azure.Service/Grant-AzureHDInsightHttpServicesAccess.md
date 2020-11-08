---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: E3D22B03-2997-4F2C-895E-AE0993FD7C92
online version: ''
schema: 2.0.0
ms.openlocfilehash: bfd3e1f2bb5d057dec8a7bee5929ba5c67c8d53d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029960"
---
# <span data-ttu-id="575f9-101">Grant-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="575f9-101">Grant-AzureHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="575f9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="575f9-102">SYNOPSIS</span></span>
<span data-ttu-id="575f9-103">Concede l'accesso HTTP a un cluster.</span><span class="sxs-lookup"><span data-stu-id="575f9-103">Grants HTTP access to a cluster.</span></span>

## <span data-ttu-id="575f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="575f9-104">SYNTAX</span></span>

```
Grant-AzureHDInsightHttpServicesAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Credential <PSCredential> [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String>
 [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="575f9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="575f9-105">DESCRIPTION</span></span>
<span data-ttu-id="575f9-106">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="575f9-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="575f9-107">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="575f9-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="575f9-108">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="575f9-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="575f9-109">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="575f9-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="575f9-110">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="575f9-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="575f9-111">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="575f9-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="575f9-112">Il cmdlet **Grant-AzureHDInsightHttpServicesAccess** concede l'accesso HTTP a un cluster HDInsight di Azure usando i servizi ODBC, Ambari, oozie e Web.</span><span class="sxs-lookup"><span data-stu-id="575f9-112">The **Grant-AzureHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie, and web services.</span></span>

## <span data-ttu-id="575f9-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="575f9-113">EXAMPLES</span></span>

## <span data-ttu-id="575f9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="575f9-114">PARAMETERS</span></span>

### <span data-ttu-id="575f9-115">-Certificato</span><span class="sxs-lookup"><span data-stu-id="575f9-115">-Certificate</span></span>
<span data-ttu-id="575f9-116">Specifica il certificato di gestione per un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="575f9-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="575f9-117">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="575f9-117">-Credential</span></span>
<span data-ttu-id="575f9-118">Specifica un nome utente e una password per l'accesso HTTP.</span><span class="sxs-lookup"><span data-stu-id="575f9-118">Specifies a user name and password for HTTP access.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="575f9-119">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="575f9-119">-Endpoint</span></span>
<span data-ttu-id="575f9-120">Specifica l'endpoint da usare per la connessione a Azure.</span><span class="sxs-lookup"><span data-stu-id="575f9-120">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="575f9-121">Se non specifichi questo parametro, questo cmdlet usa l'endpoint predefinito.</span><span class="sxs-lookup"><span data-stu-id="575f9-121">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="575f9-122">-HostedService</span><span class="sxs-lookup"><span data-stu-id="575f9-122">-HostedService</span></span>
<span data-ttu-id="575f9-123">Specifica lo spazio dei nomi di un servizio HDInsight.</span><span class="sxs-lookup"><span data-stu-id="575f9-123">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="575f9-124">Se non specifichi questo parametro, questo cmdlet usa lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="575f9-124">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="575f9-125">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="575f9-125">-IgnoreSslErrors</span></span>
<span data-ttu-id="575f9-126">Indica se gli errori SSL (Secure Sockets Layer) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="575f9-126">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="575f9-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="575f9-127">-Location</span></span>
<span data-ttu-id="575f9-128">Specifica l'area di Azure in cui si trova un cluster.</span><span class="sxs-lookup"><span data-stu-id="575f9-128">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="575f9-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="575f9-129">-Name</span></span>
<span data-ttu-id="575f9-130">Specifica il nome di un cluster.</span><span class="sxs-lookup"><span data-stu-id="575f9-130">Specifies the name of a cluster.</span></span>
<span data-ttu-id="575f9-131">Questo cmdlet concede l'accesso HTTP al cluster specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="575f9-131">This cmdlet grants HTTP access to the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="575f9-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="575f9-132">-Profile</span></span>
<span data-ttu-id="575f9-133">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="575f9-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="575f9-134">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="575f9-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="575f9-135">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="575f9-135">-Subscription</span></span>
<span data-ttu-id="575f9-136">Specifica l'abbonamento che contiene il cluster HDInsight a cui concedere l'accesso.</span><span class="sxs-lookup"><span data-stu-id="575f9-136">Specifies the subscription that contains the HDInsight cluster to which to grant access.</span></span>

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

### <span data-ttu-id="575f9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="575f9-137">CommonParameters</span></span>
<span data-ttu-id="575f9-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="575f9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="575f9-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="575f9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="575f9-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="575f9-140">INPUTS</span></span>

## <span data-ttu-id="575f9-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="575f9-141">OUTPUTS</span></span>

## <span data-ttu-id="575f9-142">Note</span><span class="sxs-lookup"><span data-stu-id="575f9-142">NOTES</span></span>

## <span data-ttu-id="575f9-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="575f9-143">RELATED LINKS</span></span>

[<span data-ttu-id="575f9-144">Revoke-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="575f9-144">Revoke-AzureHDInsightHttpServicesAccess</span></span>](./Revoke-AzureHDInsightHttpServicesAccess.md)


