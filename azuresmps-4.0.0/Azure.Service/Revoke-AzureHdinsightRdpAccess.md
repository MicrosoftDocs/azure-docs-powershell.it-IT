---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 6818F49E-0A51-4D99-BC3D-5A90F1F30C33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 78caed4ac43f21a1afe21a8901bdcd77ba29e482
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023434"
---
# <span data-ttu-id="25e54-101">Revoke-AzureHDInsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="25e54-101">Revoke-AzureHDInsightRdpAccess</span></span>

## <span data-ttu-id="25e54-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="25e54-102">SYNOPSIS</span></span>
<span data-ttu-id="25e54-103">Disabilita l'accesso RDP a un cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="25e54-103">Disables RDP access to an HDInsight cluster.</span></span>

## <span data-ttu-id="25e54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25e54-104">SYNTAX</span></span>

```
Revoke-AzureHDInsightRdpAccess [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="25e54-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25e54-105">DESCRIPTION</span></span>
<span data-ttu-id="25e54-106">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="25e54-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="25e54-107">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="25e54-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="25e54-108">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="25e54-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="25e54-109">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="25e54-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="25e54-110">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="25e54-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="25e54-111">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="25e54-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="25e54-112">Il cmdlet **Revoke-AzureHDInsightRdpAccess** Disabilita l'accesso RDP (Remote Desktop Protocol) a un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="25e54-112">The **Revoke-AzureHDInsightRdpAccess** cmdlet disables Remote Desktop Protocol (RDP) access to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="25e54-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25e54-113">EXAMPLES</span></span>

## <span data-ttu-id="25e54-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="25e54-114">PARAMETERS</span></span>

### <span data-ttu-id="25e54-115">-Certificato</span><span class="sxs-lookup"><span data-stu-id="25e54-115">-Certificate</span></span>
<span data-ttu-id="25e54-116">Specifica il certificato di gestione per un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="25e54-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="25e54-117">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="25e54-117">-Endpoint</span></span>
<span data-ttu-id="25e54-118">Specifica l'endpoint da usare per la connessione a Azure.</span><span class="sxs-lookup"><span data-stu-id="25e54-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="25e54-119">Se non specifichi questo parametro, questo cmdlet usa l'endpoint predefinito.</span><span class="sxs-lookup"><span data-stu-id="25e54-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="25e54-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="25e54-120">-HostedService</span></span>
<span data-ttu-id="25e54-121">Specifica lo spazio dei nomi di un servizio HDInsight.</span><span class="sxs-lookup"><span data-stu-id="25e54-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="25e54-122">Se non specifichi questo parametro, questo cmdlet usa lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="25e54-122">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="25e54-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="25e54-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="25e54-124">Indica se gli errori SSL (Secure Sockets Layer) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="25e54-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="25e54-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="25e54-125">-Location</span></span>
<span data-ttu-id="25e54-126">Specifica l'area di Azure in cui si trova un cluster.</span><span class="sxs-lookup"><span data-stu-id="25e54-126">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="25e54-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="25e54-127">-Name</span></span>
<span data-ttu-id="25e54-128">Specifica il nome di un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="25e54-128">Specifies the name of an Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="25e54-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="25e54-129">-Profile</span></span>
<span data-ttu-id="25e54-130">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25e54-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="25e54-131">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="25e54-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="25e54-132">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="25e54-132">-Subscription</span></span>
<span data-ttu-id="25e54-133">Specifica un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="25e54-133">Specifies a subscription.</span></span>
<span data-ttu-id="25e54-134">Questo cmdlet revoca l'accesso RDP (Remote Desktop Protocol) per l'abbonamento specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="25e54-134">This cmdlet revokes Remote Desktop Protocol (RDP) access for the subscription that this parameter specifies.</span></span>

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

### <span data-ttu-id="25e54-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e54-135">CommonParameters</span></span>
<span data-ttu-id="25e54-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25e54-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e54-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25e54-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e54-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="25e54-138">INPUTS</span></span>

## <span data-ttu-id="25e54-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25e54-139">OUTPUTS</span></span>

## <span data-ttu-id="25e54-140">Note</span><span class="sxs-lookup"><span data-stu-id="25e54-140">NOTES</span></span>

## <span data-ttu-id="25e54-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25e54-141">RELATED LINKS</span></span>

[<span data-ttu-id="25e54-142">Grant-AzureHdinsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="25e54-142">Grant-AzureHdinsightRdpAccess</span></span>](./Grant-AzureHdinsightRdpAccess.md)


