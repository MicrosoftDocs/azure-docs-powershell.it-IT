---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 771B7CB2-88F6-4FC5-9DB0-E623D231E51A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bdbf7778ca2d7498d7f33586f7e9e50e0955c521
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023920"
---
# <span data-ttu-id="2e7b2-101">Set-AzureHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="2e7b2-101">Set-AzureHDInsightClusterSize</span></span>

## <span data-ttu-id="2e7b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2e7b2-102">SYNOPSIS</span></span>
<span data-ttu-id="2e7b2-103">Imposta il numero di nodi dati per un cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2e7b2-103">Sets the number of data nodes for an HDInsight cluster.</span></span>

## <span data-ttu-id="2e7b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e7b2-104">SYNTAX</span></span>

### <span data-ttu-id="2e7b2-105">Impostare le dimensioni del cluster in nodi con nome.</span><span class="sxs-lookup"><span data-stu-id="2e7b2-105">Set cluster size in nodes with name.</span></span>
```
Set-AzureHDInsightClusterSize -ClusterSizeInNodes <Int32> -Name <String> [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e7b2-106">Impostare le dimensioni del cluster in nodi con il cluster dalla pipeline.</span><span class="sxs-lookup"><span data-stu-id="2e7b2-106">Set cluster size in nodes with cluster from pipeline.</span></span>
```
Set-AzureHDInsightClusterSize -ClusterSizeInNodes <Int32> [-Force] -Cluster <AzureHDInsightCluster>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2e7b2-107">Cluster per nome (con credenziali di sottoscrizione specifiche)</span><span class="sxs-lookup"><span data-stu-id="2e7b2-107">Cluster By Name (with Specific Subscription Credential)</span></span>
```
Set-AzureHDInsightClusterSize [-Certificate <X509Certificate2>] [-Subscription <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2e7b2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e7b2-108">DESCRIPTION</span></span>
<span data-ttu-id="2e7b2-109">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="2e7b2-109">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="2e7b2-110">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="2e7b2-110">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="2e7b2-111">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2e7b2-111">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="2e7b2-112">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="2e7b2-112">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="2e7b2-113">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="2e7b2-113">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="2e7b2-114">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2e7b2-114">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="2e7b2-115">Il cmdlet **set-AzureHDInsightClusterSize** imposta il numero di nodi dati per un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2e7b2-115">The **Set-AzureHDInsightClusterSize** cmdlet sets the number of data nodes for an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="2e7b2-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e7b2-116">EXAMPLES</span></span>

## <span data-ttu-id="2e7b2-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2e7b2-117">PARAMETERS</span></span>

### <span data-ttu-id="2e7b2-118">-Certificato</span><span class="sxs-lookup"><span data-stu-id="2e7b2-118">-Certificate</span></span>
<span data-ttu-id="2e7b2-119">Specifica il certificato di gestione per un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="2e7b2-119">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e7b2-120">-Cluster</span><span class="sxs-lookup"><span data-stu-id="2e7b2-120">-Cluster</span></span>
<span data-ttu-id="2e7b2-121">Specifica il cluster da ridimensionare.</span><span class="sxs-lookup"><span data-stu-id="2e7b2-121">Specifies the cluster to resize.</span></span>

```yaml
Type: AzureHDInsightCluster
Parameter Sets: Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e7b2-122">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="2e7b2-122">-ClusterSizeInNodes</span></span>
<span data-ttu-id="2e7b2-123">Specifica il numero di nodi dati da creare per un cluster.</span><span class="sxs-lookup"><span data-stu-id="2e7b2-123">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Set cluster size in nodes with name.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Int32
Parameter Sets: Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e7b2-124">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="2e7b2-124">-Endpoint</span></span>
<span data-ttu-id="2e7b2-125">Specifica l'endpoint da usare per la connessione a Azure.</span><span class="sxs-lookup"><span data-stu-id="2e7b2-125">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="2e7b2-126">Se non specifichi questo parametro, questo cmdlet usa l'endpoint predefinito.</span><span class="sxs-lookup"><span data-stu-id="2e7b2-126">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e7b2-127">-Force</span><span class="sxs-lookup"><span data-stu-id="2e7b2-127">-Force</span></span>
<span data-ttu-id="2e7b2-128">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2e7b2-128">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Set cluster size in nodes with name., Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e7b2-129">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="2e7b2-129">-IgnoreSslErrors</span></span>
<span data-ttu-id="2e7b2-130">Indica se gli errori SSL (Secure Sockets Layer) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="2e7b2-130">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e7b2-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e7b2-131">-Name</span></span>
<span data-ttu-id="2e7b2-132">Specifica il nome del cluster HDInsight da ridimensionare.</span><span class="sxs-lookup"><span data-stu-id="2e7b2-132">Specifies the name of the HDInsight cluster to resize.</span></span>

```yaml
Type: String
Parameter Sets: Set cluster size in nodes with name.
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e7b2-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="2e7b2-133">-Profile</span></span>
<span data-ttu-id="2e7b2-134">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e7b2-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2e7b2-135">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="2e7b2-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2e7b2-136">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="2e7b2-136">-Subscription</span></span>
<span data-ttu-id="2e7b2-137">Specifica un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2e7b2-137">Specifies a subscription.</span></span>
<span data-ttu-id="2e7b2-138">Questo cmdlet imposta le dimensioni del cluster per l'abbonamento specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2e7b2-138">This cmdlet sets the cluster size for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e7b2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e7b2-139">CommonParameters</span></span>
<span data-ttu-id="2e7b2-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e7b2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e7b2-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e7b2-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e7b2-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2e7b2-142">INPUTS</span></span>

## <span data-ttu-id="2e7b2-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e7b2-143">OUTPUTS</span></span>

## <span data-ttu-id="2e7b2-144">Note</span><span class="sxs-lookup"><span data-stu-id="2e7b2-144">NOTES</span></span>

## <span data-ttu-id="2e7b2-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e7b2-145">RELATED LINKS</span></span>

