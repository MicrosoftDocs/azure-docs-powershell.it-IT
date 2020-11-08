---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3B39F43D-E74A-441D-91BC-26C324C1EDF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d0ea12e873604360114b02bb89d9bde12c9e70e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023602"
---
# <span data-ttu-id="c93d8-101">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c93d8-101">Get-AzureHDInsightCluster</span></span>

## <span data-ttu-id="c93d8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c93d8-102">SYNOPSIS</span></span>
<span data-ttu-id="c93d8-103">Ottiene un cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c93d8-103">Gets an HDInsight cluster.</span></span>

## <span data-ttu-id="c93d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c93d8-104">SYNTAX</span></span>

```
Get-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Name <String>] [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c93d8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c93d8-105">DESCRIPTION</span></span>
<span data-ttu-id="c93d8-106">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="c93d8-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="c93d8-107">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="c93d8-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="c93d8-108">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c93d8-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="c93d8-109">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="c93d8-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="c93d8-110">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="c93d8-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="c93d8-111">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c93d8-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="c93d8-112">Il cmdlet **Get-AzureHDInsightCluster** ottiene i cluster di servizi di Azure HDInsight per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="c93d8-112">The **Get-AzureHDInsightCluster** cmdlet gets the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="c93d8-113">Puoi usare il parametro *Name* per ottenere un cluster specifico.</span><span class="sxs-lookup"><span data-stu-id="c93d8-113">You can use the *Name* parameter to get a specific cluster.</span></span>

## <span data-ttu-id="c93d8-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c93d8-114">EXAMPLES</span></span>

### <span data-ttu-id="c93d8-115">Esempio 1: ottenere i cluster in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="c93d8-115">Example 1: Get the clusters in a subscription</span></span>
```
PS C:\> Get-AzureHDInsightCluster
```

<span data-ttu-id="c93d8-116">Questo comando consente di ottenere informazioni sui cluster HDInsight nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="c93d8-116">This command gets information about the HDInsight clusters in the current subscription.</span></span>

## <span data-ttu-id="c93d8-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c93d8-117">PARAMETERS</span></span>

### <span data-ttu-id="c93d8-118">-Certificato</span><span class="sxs-lookup"><span data-stu-id="c93d8-118">-Certificate</span></span>
<span data-ttu-id="c93d8-119">Specifica il certificato di gestione per un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="c93d8-119">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="c93d8-120">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="c93d8-120">-Endpoint</span></span>
<span data-ttu-id="c93d8-121">Specifica l'endpoint da usare per la connessione a Azure.</span><span class="sxs-lookup"><span data-stu-id="c93d8-121">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="c93d8-122">Se non specifichi questo parametro, questo cmdlet usa l'endpoint predefinito.</span><span class="sxs-lookup"><span data-stu-id="c93d8-122">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="c93d8-123">-HostedService</span><span class="sxs-lookup"><span data-stu-id="c93d8-123">-HostedService</span></span>
<span data-ttu-id="c93d8-124">Specifica lo spazio dei nomi di un servizio HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c93d8-124">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="c93d8-125">Se non specifichi questo parametro, questo cmdlet usa lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="c93d8-125">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="c93d8-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="c93d8-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="c93d8-127">Indica se gli errori SSL (Secure Sockets Layer) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="c93d8-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="c93d8-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="c93d8-128">-Name</span></span>
<span data-ttu-id="c93d8-129">Specifica il nome di un cluster HDInsight da ottenere.</span><span class="sxs-lookup"><span data-stu-id="c93d8-129">Specifies the name of an HDInsight cluster to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c93d8-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="c93d8-130">-Profile</span></span>
<span data-ttu-id="c93d8-131">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c93d8-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c93d8-132">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c93d8-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c93d8-133">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="c93d8-133">-Subscription</span></span>
<span data-ttu-id="c93d8-134">Specifica l'abbonamento che contiene il cluster HDInsight per ottenere.</span><span class="sxs-lookup"><span data-stu-id="c93d8-134">Specifies the subscription that contains the HDInsight cluster to get.</span></span>

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

### <span data-ttu-id="c93d8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c93d8-135">CommonParameters</span></span>
<span data-ttu-id="c93d8-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c93d8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c93d8-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c93d8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c93d8-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c93d8-138">INPUTS</span></span>

## <span data-ttu-id="c93d8-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c93d8-139">OUTPUTS</span></span>

## <span data-ttu-id="c93d8-140">Note</span><span class="sxs-lookup"><span data-stu-id="c93d8-140">NOTES</span></span>

## <span data-ttu-id="c93d8-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c93d8-141">RELATED LINKS</span></span>

[<span data-ttu-id="c93d8-142">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c93d8-142">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="c93d8-143">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c93d8-143">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)

[<span data-ttu-id="c93d8-144">Usare-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c93d8-144">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


