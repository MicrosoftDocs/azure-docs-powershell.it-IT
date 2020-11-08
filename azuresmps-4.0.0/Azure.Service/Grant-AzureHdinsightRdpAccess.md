---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 95CCEB79-EAC4-4F56-B289-5401F976E5F5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92b2c005f855ccf99e8bae4d8db8445ba7e63dad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029724"
---
# <span data-ttu-id="122d0-101">Grant-AzureHDInsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="122d0-101">Grant-AzureHDInsightRdpAccess</span></span>

## <span data-ttu-id="122d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="122d0-102">SYNOPSIS</span></span>
<span data-ttu-id="122d0-103">Concede l'accesso RDP a un cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="122d0-103">Grants RDP access to an HDInsight cluster.</span></span>

## <span data-ttu-id="122d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="122d0-104">SYNTAX</span></span>

```
Grant-AzureHDInsightRdpAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 -RdpCredential <PSCredential> -RdpAccessExpiry <DateTime> [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="122d0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="122d0-105">DESCRIPTION</span></span>
<span data-ttu-id="122d0-106">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="122d0-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="122d0-107">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="122d0-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="122d0-108">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="122d0-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="122d0-109">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="122d0-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="122d0-110">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="122d0-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="122d0-111">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="122d0-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="122d0-112">Il cmdlet **Grant-AzureHDInsightRdpAccess** concede l'accesso RDP (Remote Desktop Protocol) a un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="122d0-112">The **Grant-AzureHDInsightRdpAccess** cmdlet grants Remote Desktop Protocol (RDP) access to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="122d0-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="122d0-113">EXAMPLES</span></span>

## <span data-ttu-id="122d0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="122d0-114">PARAMETERS</span></span>

### <span data-ttu-id="122d0-115">-Certificato</span><span class="sxs-lookup"><span data-stu-id="122d0-115">-Certificate</span></span>
<span data-ttu-id="122d0-116">Specifica il certificato di gestione per un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="122d0-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="122d0-117">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="122d0-117">-Endpoint</span></span>
<span data-ttu-id="122d0-118">Specifica l'endpoint da usare per la connessione a Azure.</span><span class="sxs-lookup"><span data-stu-id="122d0-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="122d0-119">Se non specifichi questo parametro, questo cmdlet usa l'endpoint predefinito.</span><span class="sxs-lookup"><span data-stu-id="122d0-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="122d0-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="122d0-120">-HostedService</span></span>
<span data-ttu-id="122d0-121">Specifica lo spazio dei nomi di un servizio HDInsight.</span><span class="sxs-lookup"><span data-stu-id="122d0-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="122d0-122">Se non specifichi questo parametro, questo cmdlet usa lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="122d0-122">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="122d0-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="122d0-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="122d0-124">Indica se gli errori SSL (Secure Sockets Layer) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="122d0-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="122d0-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="122d0-125">-Location</span></span>
<span data-ttu-id="122d0-126">Specifica l'area di Azure in cui si trova un cluster.</span><span class="sxs-lookup"><span data-stu-id="122d0-126">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="122d0-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="122d0-127">-Name</span></span>
<span data-ttu-id="122d0-128">Specifica il nome di un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="122d0-128">Specifies the name of an Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="122d0-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="122d0-129">-Profile</span></span>
<span data-ttu-id="122d0-130">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="122d0-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="122d0-131">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="122d0-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="122d0-132">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="122d0-132">-RdpAccessExpiry</span></span>
<span data-ttu-id="122d0-133">Specifica la scadenza, come oggetto **DateTime** , per l'accesso RDP (Remote Desktop Protocol) a un cluster.</span><span class="sxs-lookup"><span data-stu-id="122d0-133">Specifies the expiration, as a **DateTime** object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="122d0-134">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="122d0-134">-RdpCredential</span></span>
<span data-ttu-id="122d0-135">Specifica le credenziali per l'accesso RDP a un cluster.</span><span class="sxs-lookup"><span data-stu-id="122d0-135">Specifies the credentials for RDP access to a cluster.</span></span>

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

### <span data-ttu-id="122d0-136">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="122d0-136">-Subscription</span></span>
<span data-ttu-id="122d0-137">Specifica l'abbonamento che contiene il cluster HDInsight a cui concedere l'accesso.</span><span class="sxs-lookup"><span data-stu-id="122d0-137">Specifies the subscription that contains the HDInsight cluster to which to grant access.</span></span>

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

### <span data-ttu-id="122d0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="122d0-138">CommonParameters</span></span>
<span data-ttu-id="122d0-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="122d0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="122d0-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="122d0-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="122d0-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="122d0-141">INPUTS</span></span>

## <span data-ttu-id="122d0-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="122d0-142">OUTPUTS</span></span>

## <span data-ttu-id="122d0-143">Note</span><span class="sxs-lookup"><span data-stu-id="122d0-143">NOTES</span></span>

## <span data-ttu-id="122d0-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="122d0-144">RELATED LINKS</span></span>

[<span data-ttu-id="122d0-145">Revoke-AzureHdinsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="122d0-145">Revoke-AzureHdinsightRdpAccess</span></span>](./Revoke-AzureHdinsightRdpAccess.md)


