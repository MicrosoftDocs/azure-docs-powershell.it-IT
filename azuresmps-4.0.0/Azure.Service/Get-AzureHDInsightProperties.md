---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 325DE85D-B9CB-4584-8C61-DA417736ABBF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55992408c1376c9456157387456b114c292b44c2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029813"
---
# <span data-ttu-id="29788-101">Get-AzureHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="29788-101">Get-AzureHDInsightProperties</span></span>

## <span data-ttu-id="29788-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="29788-102">SYNOPSIS</span></span>
<span data-ttu-id="29788-103">Ottiene le proprietà specifiche di un servizio HDInsight.</span><span class="sxs-lookup"><span data-stu-id="29788-103">Gets properties specific to an HDInsight service.</span></span>

## <span data-ttu-id="29788-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29788-104">SYNTAX</span></span>

```
Get-AzureHDInsightProperties [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Locations] [-Subscription <String>] [-Versions] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="29788-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29788-105">DESCRIPTION</span></span>
<span data-ttu-id="29788-106">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="29788-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="29788-107">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="29788-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="29788-108">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="29788-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="29788-109">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="29788-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="29788-110">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="29788-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="29788-111">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="29788-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="29788-112">Il cmdlet **Get-AzureHDInsightProperties** ottiene le proprietà specifiche di un servizio HDInsight di Azure, ad esempio un elenco delle aree di Azure disponibili, le versioni di cluster HDInsight e la capacità di calcolo disponibile.</span><span class="sxs-lookup"><span data-stu-id="29788-112">The **Get-AzureHDInsightProperties** cmdlet gets properties specific to an Azure HDInsight service, such as a list of available Azure regions, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="29788-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29788-113">EXAMPLES</span></span>

### <span data-ttu-id="29788-114">Esempio 1: ottenere le proprietà di HDInsight per un abbonamento</span><span class="sxs-lookup"><span data-stu-id="29788-114">Example 1: Get HDInsight properties for a subscription</span></span>
```
PS C:\>$SubName = Get-AzureSubscription -Current | %{ $_.SubscriptionName }
PS C:\> Get-AzureHDInsightProperties -Subscription $SubName
```

<span data-ttu-id="29788-115">Il primo comando ottiene il nome dell'abbonamento Azure corrente e lo archivia nella variabile $SubName.</span><span class="sxs-lookup"><span data-stu-id="29788-115">The first command gets the name of the current Azure subscription, and then stores it in the $SubName variable.</span></span>

<span data-ttu-id="29788-116">Il secondo comando ottiene le proprietà HDInsight per l'abbonamento in $SubName.</span><span class="sxs-lookup"><span data-stu-id="29788-116">The second command gets the HDInsight properties for the subscription in $SubName.</span></span>

## <span data-ttu-id="29788-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="29788-117">PARAMETERS</span></span>

### <span data-ttu-id="29788-118">-Certificato</span><span class="sxs-lookup"><span data-stu-id="29788-118">-Certificate</span></span>
<span data-ttu-id="29788-119">Specifica il certificato di gestione per un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="29788-119">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="29788-120">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="29788-120">-Endpoint</span></span>
<span data-ttu-id="29788-121">Specifica l'endpoint da usare per la connessione a Azure.</span><span class="sxs-lookup"><span data-stu-id="29788-121">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="29788-122">Se non specifichi questo parametro, questo cmdlet usa l'endpoint predefinito.</span><span class="sxs-lookup"><span data-stu-id="29788-122">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="29788-123">-HostedService</span><span class="sxs-lookup"><span data-stu-id="29788-123">-HostedService</span></span>
<span data-ttu-id="29788-124">Specifica lo spazio dei nomi di un servizio HDInsight.</span><span class="sxs-lookup"><span data-stu-id="29788-124">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="29788-125">Se non specifichi questo parametro, questo cmdlet usa lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="29788-125">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="29788-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="29788-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="29788-127">Indica se gli errori SSL (Secure Sockets Layer) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="29788-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="29788-128">-Locations</span><span class="sxs-lookup"><span data-stu-id="29788-128">-Locations</span></span>
<span data-ttu-id="29788-129">Indica che questo cmdlet ottiene l'elenco delle aree di Azure in cui è disponibile il servizio HDInsight.</span><span class="sxs-lookup"><span data-stu-id="29788-129">Indicates that this cmdlet gets the list of Azure regions where the HDInsight service is available.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29788-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="29788-130">-Profile</span></span>
<span data-ttu-id="29788-131">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29788-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="29788-132">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="29788-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="29788-133">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="29788-133">-Subscription</span></span>
<span data-ttu-id="29788-134">Specifica l'abbonamento che contiene le proprietà HDInsight da ottenere.</span><span class="sxs-lookup"><span data-stu-id="29788-134">Specifies the subscription that contains the HDInsight properties to get.</span></span>

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

### <span data-ttu-id="29788-135">-Versioni</span><span class="sxs-lookup"><span data-stu-id="29788-135">-Versions</span></span>
<span data-ttu-id="29788-136">Indica che questo cmdlet ottiene l'elenco delle versioni del cluster HDInsight disponibili nel servizio per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="29788-136">Indicates that this cmdlet gets the list of HDInsight cluster versions that are available in the service for a subscription.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29788-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29788-137">CommonParameters</span></span>
<span data-ttu-id="29788-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29788-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29788-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29788-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29788-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="29788-140">INPUTS</span></span>

## <span data-ttu-id="29788-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29788-141">OUTPUTS</span></span>

## <span data-ttu-id="29788-142">Note</span><span class="sxs-lookup"><span data-stu-id="29788-142">NOTES</span></span>

## <span data-ttu-id="29788-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29788-143">RELATED LINKS</span></span>

