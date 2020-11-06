---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/start-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
ms.openlocfilehash: 8c3e0f01472469be856d69c1a87f8eb5185f2012
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521447"
---
# <span data-ttu-id="9fcc3-101">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9fcc3-101">Start-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="9fcc3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9fcc3-102">SYNOPSIS</span></span>
<span data-ttu-id="9fcc3-103">Avvia un processo di Azure HDInsight definito in un cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="9fcc3-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fcc3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9fcc3-104">SYNTAX</span></span>

```
Start-AzureRmHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9fcc3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9fcc3-105">DESCRIPTION</span></span>
<span data-ttu-id="9fcc3-106">Il cmdlet **Start-AzureRMHDInsightJob** avvia un processo di Azure HDInsight definito in un cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="9fcc3-106">The **Start-AzureRMHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="9fcc3-107">Può trattarsi di un processo MapReduce, di un processo di MapReduce in streaming, di un processo hive o di un processo di maiale.</span><span class="sxs-lookup"><span data-stu-id="9fcc3-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="9fcc3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9fcc3-108">EXAMPLES</span></span>

### <span data-ttu-id="9fcc3-109">Esempio 1: avviare un processo nel cluster specificato</span><span class="sxs-lookup"><span data-stu-id="9fcc3-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="9fcc3-110">Questo comando avvia un processo nel cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="9fcc3-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="9fcc3-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9fcc3-111">PARAMETERS</span></span>

### <span data-ttu-id="9fcc3-112">-Clustername</span><span class="sxs-lookup"><span data-stu-id="9fcc3-112">-ClusterName</span></span>
<span data-ttu-id="9fcc3-113">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="9fcc3-113">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fcc3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fcc3-114">-DefaultProfile</span></span>
<span data-ttu-id="9fcc3-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9fcc3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fcc3-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="9fcc3-116">-HttpCredential</span></span>
<span data-ttu-id="9fcc3-117">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="9fcc3-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fcc3-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="9fcc3-118">-JobDefinition</span></span>
<span data-ttu-id="9fcc3-119">Specifica il processo da avviare nel cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9fcc3-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

```yaml
Type: AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fcc3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fcc3-120">-ResourceGroupName</span></span>
<span data-ttu-id="9fcc3-121">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9fcc3-121">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fcc3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fcc3-122">CommonParameters</span></span>
<span data-ttu-id="9fcc3-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fcc3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fcc3-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fcc3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fcc3-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9fcc3-125">INPUTS</span></span>

### <span data-ttu-id="9fcc3-126">AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9fcc3-126">AzureHDInsightJobDefinition</span></span>
<span data-ttu-id="9fcc3-127">Il parametro ' JobDefinition ' accetta il valore di tipo ' AzureHDInsightJobDefinition ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="9fcc3-127">Parameter 'JobDefinition' accepts value of type 'AzureHDInsightJobDefinition' from the pipeline</span></span>

## <span data-ttu-id="9fcc3-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9fcc3-128">OUTPUTS</span></span>

### <span data-ttu-id="9fcc3-129">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9fcc3-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="9fcc3-130">Note</span><span class="sxs-lookup"><span data-stu-id="9fcc3-130">NOTES</span></span>

## <span data-ttu-id="9fcc3-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9fcc3-131">RELATED LINKS</span></span>

[<span data-ttu-id="9fcc3-132">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9fcc3-132">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="9fcc3-133">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9fcc3-133">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="9fcc3-134">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9fcc3-134">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="9fcc3-135">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9fcc3-135">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


