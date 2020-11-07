---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
ms.openlocfilehash: 5512482b6b8edc0d9c336c8879eb43072143ff53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688299"
---
# <span data-ttu-id="14321-101">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="14321-101">Start-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="14321-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="14321-102">SYNOPSIS</span></span>
<span data-ttu-id="14321-103">Avvia un processo di Azure HDInsight definito in un cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="14321-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14321-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14321-104">SYNTAX</span></span>

```
Start-AzureRmHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14321-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14321-105">DESCRIPTION</span></span>
<span data-ttu-id="14321-106">Il cmdlet **Start-AzureRMHDInsightJob** avvia un processo di Azure HDInsight definito in un cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="14321-106">The **Start-AzureRMHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="14321-107">Può trattarsi di un processo MapReduce, di un processo di MapReduce in streaming, di un processo hive o di un processo di maiale.</span><span class="sxs-lookup"><span data-stu-id="14321-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="14321-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14321-108">EXAMPLES</span></span>

### <span data-ttu-id="14321-109">Esempio 1: avviare un processo nel cluster specificato</span><span class="sxs-lookup"><span data-stu-id="14321-109">Example 1: Start a job on the specified cluster</span></span>
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

<span data-ttu-id="14321-110">Questo comando avvia un processo nel cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="14321-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="14321-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14321-111">PARAMETERS</span></span>

### <span data-ttu-id="14321-112">-Clustername</span><span class="sxs-lookup"><span data-stu-id="14321-112">-ClusterName</span></span>
<span data-ttu-id="14321-113">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="14321-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14321-114">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="14321-114">-HttpCredential</span></span>
<span data-ttu-id="14321-115">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="14321-115">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14321-116">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="14321-116">-JobDefinition</span></span>
<span data-ttu-id="14321-117">Specifica il processo da avviare nel cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="14321-117">Specifies the job to start on the Azure HDInsight cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14321-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14321-118">-ResourceGroupName</span></span>
<span data-ttu-id="14321-119">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="14321-119">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14321-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14321-120">-DefaultProfile</span></span>
<span data-ttu-id="14321-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14321-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14321-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14321-122">CommonParameters</span></span>
<span data-ttu-id="14321-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14321-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14321-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14321-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14321-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="14321-125">INPUTS</span></span>

### <span data-ttu-id="14321-126">AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="14321-126">AzureHDInsightJobDefinition</span></span>
<span data-ttu-id="14321-127">Il parametro ' JobDefinition ' accetta il valore di tipo ' AzureHDInsightJobDefinition ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="14321-127">Parameter 'JobDefinition' accepts value of type 'AzureHDInsightJobDefinition' from the pipeline</span></span>

## <span data-ttu-id="14321-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14321-128">OUTPUTS</span></span>

### <span data-ttu-id="14321-129">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="14321-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="14321-130">Note</span><span class="sxs-lookup"><span data-stu-id="14321-130">NOTES</span></span>

## <span data-ttu-id="14321-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14321-131">RELATED LINKS</span></span>

[<span data-ttu-id="14321-132">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="14321-132">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="14321-133">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="14321-133">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="14321-134">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="14321-134">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="14321-135">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="14321-135">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


