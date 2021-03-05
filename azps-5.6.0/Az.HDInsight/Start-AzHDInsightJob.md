---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/start-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
ms.openlocfilehash: 316ac2671fe60271ad0d994855189071e3da2b95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964717"
---
# <span data-ttu-id="392e8-101">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="392e8-101">Start-AzHDInsightJob</span></span>

## <span data-ttu-id="392e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="392e8-102">SYNOPSIS</span></span>
<span data-ttu-id="392e8-103">Avvia un processo definito di Azure HDInsight in un cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="392e8-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

## <span data-ttu-id="392e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="392e8-104">SYNTAX</span></span>

```
Start-AzHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="392e8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="392e8-105">DESCRIPTION</span></span>
<span data-ttu-id="392e8-106">Il cmdlet **Start-AzHDInsightJob** avvia un processo definito di Azure HDInsight in un cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="392e8-106">The **Start-AzHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="392e8-107">Può trattarsi di un processo di MapReduce, di un processo di Streaming MapReduce, di un processo di hive o di maiali.</span><span class="sxs-lookup"><span data-stu-id="392e8-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="392e8-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="392e8-108">EXAMPLES</span></span>

### <span data-ttu-id="392e8-109">Esempio 1: Avviare un processo nel cluster specificato</span><span class="sxs-lookup"><span data-stu-id="392e8-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="392e8-110">Questo comando avvia un processo nel cluster denominato your-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="392e8-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="392e8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="392e8-111">PARAMETERS</span></span>

### <span data-ttu-id="392e8-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="392e8-112">-ClusterName</span></span>
<span data-ttu-id="392e8-113">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="392e8-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="392e8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="392e8-114">-DefaultProfile</span></span>
<span data-ttu-id="392e8-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="392e8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="392e8-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="392e8-116">-HttpCredential</span></span>
<span data-ttu-id="392e8-117">Specifica le credenziali di accesso del cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="392e8-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="392e8-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="392e8-118">-JobDefinition</span></span>
<span data-ttu-id="392e8-119">Specifica il processo da avviare nel cluster Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="392e8-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="392e8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="392e8-120">-ResourceGroupName</span></span>
<span data-ttu-id="392e8-121">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="392e8-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="392e8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="392e8-122">CommonParameters</span></span>
<span data-ttu-id="392e8-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="392e8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="392e8-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="392e8-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="392e8-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="392e8-125">INPUTS</span></span>

### <span data-ttu-id="392e8-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="392e8-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>

## <span data-ttu-id="392e8-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="392e8-127">OUTPUTS</span></span>

### <span data-ttu-id="392e8-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="392e8-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="392e8-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="392e8-129">NOTES</span></span>

## <span data-ttu-id="392e8-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="392e8-130">RELATED LINKS</span></span>

[<span data-ttu-id="392e8-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="392e8-131">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="392e8-132">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="392e8-132">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="392e8-133">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="392e8-133">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="392e8-134">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="392e8-134">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


