---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 7D73D37B-17EE-4FF8-9A21-D2014D5417D6
online version: ''
schema: 2.0.0
ms.openlocfilehash: fa779907648ca8e8e1288394d562c86b6102d9ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029938"
---
# <span data-ttu-id="2fce0-101">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2fce0-101">Remove-AzureHDInsightCluster</span></span>

## <span data-ttu-id="2fce0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2fce0-102">SYNOPSIS</span></span>
<span data-ttu-id="2fce0-103">Elimina un cluster HDInsight da un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2fce0-103">Deletes an HDInsight cluster from a subscription.</span></span>

## <span data-ttu-id="2fce0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fce0-104">SYNTAX</span></span>

```
Remove-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="2fce0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fce0-105">DESCRIPTION</span></span>
<span data-ttu-id="2fce0-106">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="2fce0-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="2fce0-107">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="2fce0-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="2fce0-108">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2fce0-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="2fce0-109">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="2fce0-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="2fce0-110">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="2fce0-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="2fce0-111">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2fce0-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="2fce0-112">Il cmdlet **Remove-AzureHDInsightCluster** Elimina il cluster di servizi HDInsight specificato da un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2fce0-112">The **Remove-AzureHDInsightCluster** cmdlet deletes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="2fce0-113">Questa operazione elimina anche tutti i dati archiviati nel file System distribuito Hadoop (HDFS) nel cluster.</span><span class="sxs-lookup"><span data-stu-id="2fce0-113">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="2fce0-114">I dati archiviati nell'account di archiviazione di Azure associato non vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="2fce0-114">Data stored in the associated Azure Storage account is not deleted.</span></span>

## <span data-ttu-id="2fce0-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fce0-115">EXAMPLES</span></span>

### <span data-ttu-id="2fce0-116">Esempio 1: rimuovere un cluster</span><span class="sxs-lookup"><span data-stu-id="2fce0-116">Example 1: Remove a cluster</span></span>
```
PS C:\>Remove-AzureHDInsightCluster -Name "HDICluster"
```

<span data-ttu-id="2fce0-117">Questo comando Elimina il cluster HDInsight denominato HDICluster.</span><span class="sxs-lookup"><span data-stu-id="2fce0-117">This command deletes the HDInsight cluster named HDICluster.</span></span>

## <span data-ttu-id="2fce0-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2fce0-118">PARAMETERS</span></span>

### <span data-ttu-id="2fce0-119">-Certificato</span><span class="sxs-lookup"><span data-stu-id="2fce0-119">-Certificate</span></span>
<span data-ttu-id="2fce0-120">Specifica il certificato di gestione per un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="2fce0-120">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="2fce0-121">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="2fce0-121">-Endpoint</span></span>
<span data-ttu-id="2fce0-122">Specifica l'endpoint da usare per la connessione a Azure.</span><span class="sxs-lookup"><span data-stu-id="2fce0-122">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="2fce0-123">Se non specifichi questo parametro, questo cmdlet usa l'endpoint predefinito.</span><span class="sxs-lookup"><span data-stu-id="2fce0-123">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="2fce0-124">-HostedService</span><span class="sxs-lookup"><span data-stu-id="2fce0-124">-HostedService</span></span>
<span data-ttu-id="2fce0-125">Specifica lo spazio dei nomi di un servizio HDInsight se non si vuole usare lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="2fce0-125">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="2fce0-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="2fce0-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="2fce0-127">Indica se gli errori SSL (Secure Sockets Layer) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="2fce0-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="2fce0-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="2fce0-128">-Name</span></span>
<span data-ttu-id="2fce0-129">Specifica il nome del cluster HDInsight da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2fce0-129">Specifies the name of the HDInsight cluster to remove.</span></span>

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

### <span data-ttu-id="2fce0-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="2fce0-130">-Profile</span></span>
<span data-ttu-id="2fce0-131">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fce0-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2fce0-132">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="2fce0-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2fce0-133">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="2fce0-133">-Subscription</span></span>
<span data-ttu-id="2fce0-134">Specifica l'account di sottoscrizione che contiene il cluster HDInsight da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2fce0-134">Specifies the subscription account that contains the HDInsight cluster to remove.</span></span>

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

### <span data-ttu-id="2fce0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fce0-135">CommonParameters</span></span>
<span data-ttu-id="2fce0-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fce0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fce0-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fce0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fce0-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2fce0-138">INPUTS</span></span>

## <span data-ttu-id="2fce0-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fce0-139">OUTPUTS</span></span>

## <span data-ttu-id="2fce0-140">Note</span><span class="sxs-lookup"><span data-stu-id="2fce0-140">NOTES</span></span>

## <span data-ttu-id="2fce0-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fce0-141">RELATED LINKS</span></span>

[<span data-ttu-id="2fce0-142">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2fce0-142">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="2fce0-143">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2fce0-143">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="2fce0-144">Usare-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2fce0-144">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


