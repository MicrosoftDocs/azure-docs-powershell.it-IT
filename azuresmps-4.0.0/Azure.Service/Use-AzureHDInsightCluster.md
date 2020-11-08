---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0BF58D9C-814E-4276-823F-D566DC99391C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 773af58d0ae9b4ca940240875b5cf9a8d3a0ffe7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023795"
---
# <span data-ttu-id="036de-101">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="036de-101">Use-AzureHDInsightCluster</span></span>

## <span data-ttu-id="036de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="036de-102">SYNOPSIS</span></span>
<span data-ttu-id="036de-103">Seleziona un cluster HDInsight per il cmdlet Invoke-AzureHDInsightHiveJob da usare per inviare i processi.</span><span class="sxs-lookup"><span data-stu-id="036de-103">Selects an HDInsight cluster for the Invoke-AzureHDInsightHiveJob cmdlet to use to submit jobs.</span></span>

## <span data-ttu-id="036de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="036de-104">SYNTAX</span></span>

```
Use-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="036de-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="036de-105">DESCRIPTION</span></span>
<span data-ttu-id="036de-106">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="036de-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="036de-107">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="036de-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="036de-108">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="036de-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="036de-109">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="036de-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="036de-110">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="036de-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="036de-111">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="036de-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="036de-112">Il cmdlet **use-AzureHDInsightCluster** seleziona il cluster Azure HDInsight per il cmdlet **Invoke-AzureHDInsightHiveJob** da usare per inviare i processi.</span><span class="sxs-lookup"><span data-stu-id="036de-112">The **Use-AzureHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the **Invoke-AzureHDInsightHiveJob** cmdlet to use to submit jobs.</span></span>

## <span data-ttu-id="036de-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="036de-113">EXAMPLES</span></span>

## <span data-ttu-id="036de-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="036de-114">PARAMETERS</span></span>

### <span data-ttu-id="036de-115">-Certificato</span><span class="sxs-lookup"><span data-stu-id="036de-115">-Certificate</span></span>
<span data-ttu-id="036de-116">Specifica il certificato di gestione per un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="036de-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="036de-117">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="036de-117">-Endpoint</span></span>
<span data-ttu-id="036de-118">Specifica l'endpoint da usare per la connessione a Azure.</span><span class="sxs-lookup"><span data-stu-id="036de-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="036de-119">Se non specifichi questo parametro, questo cmdlet usa l'endpoint predefinito.</span><span class="sxs-lookup"><span data-stu-id="036de-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="036de-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="036de-120">-HostedService</span></span>
<span data-ttu-id="036de-121">Specifica lo spazio dei nomi di un servizio HDInsight.</span><span class="sxs-lookup"><span data-stu-id="036de-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="036de-122">Se non specifichi questo parametro, viene usato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="036de-122">If you do not specify this parameter, the default namespace is used.</span></span>

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

### <span data-ttu-id="036de-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="036de-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="036de-124">Indica se gli errori SSL (Secure Sockets Layer) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="036de-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="036de-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="036de-125">-Name</span></span>
<span data-ttu-id="036de-126">Specifica il nome del cluster usato dal cmdlet **Invoke-AzureHDInsightHiveJob** .</span><span class="sxs-lookup"><span data-stu-id="036de-126">Specifies the name of the cluster that is used by the **Invoke-AzureHDInsightHiveJob** cmdlet.</span></span>

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

### <span data-ttu-id="036de-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="036de-127">-Profile</span></span>
<span data-ttu-id="036de-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="036de-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="036de-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="036de-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="036de-130">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="036de-130">-Subscription</span></span>
<span data-ttu-id="036de-131">Specifica l'abbonamento che contiene i cluster HDInsight da usare.</span><span class="sxs-lookup"><span data-stu-id="036de-131">Specifies the subscription that contains the HDInsight clusters to use.</span></span>

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

### <span data-ttu-id="036de-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="036de-132">CommonParameters</span></span>
<span data-ttu-id="036de-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="036de-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="036de-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="036de-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="036de-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="036de-135">INPUTS</span></span>

## <span data-ttu-id="036de-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="036de-136">OUTPUTS</span></span>

## <span data-ttu-id="036de-137">Note</span><span class="sxs-lookup"><span data-stu-id="036de-137">NOTES</span></span>

## <span data-ttu-id="036de-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="036de-138">RELATED LINKS</span></span>

[<span data-ttu-id="036de-139">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="036de-139">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="036de-140">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="036de-140">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="036de-141">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="036de-141">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)


