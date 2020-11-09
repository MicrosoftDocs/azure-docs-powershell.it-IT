---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/start-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
ms.openlocfilehash: 6eab5c80fa8c21d5b592f0e194a5aba50c4d3002
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296292"
---
# <span data-ttu-id="4dc50-101">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4dc50-101">Start-AzHDInsightJob</span></span>

## <span data-ttu-id="4dc50-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4dc50-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc50-103">Avvia un processo di Azure HDInsight definito in un cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="4dc50-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

## <span data-ttu-id="4dc50-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4dc50-104">SYNTAX</span></span>

```
Start-AzHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4dc50-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4dc50-105">DESCRIPTION</span></span>
<span data-ttu-id="4dc50-106">Il cmdlet **Start-AzHDInsightJob** avvia un processo di Azure HDInsight definito in un cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="4dc50-106">The **Start-AzHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="4dc50-107">Può trattarsi di un processo MapReduce, di un processo di MapReduce in streaming, di un processo hive o di un processo di maiale.</span><span class="sxs-lookup"><span data-stu-id="4dc50-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="4dc50-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4dc50-108">EXAMPLES</span></span>

### <span data-ttu-id="4dc50-109">Esempio 1: avviare un processo nel cluster specificato</span><span class="sxs-lookup"><span data-stu-id="4dc50-109">Example 1: Start a job on the specified cluster</span></span>
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

<span data-ttu-id="4dc50-110">Questo comando avvia un processo nel cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="4dc50-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="4dc50-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4dc50-111">PARAMETERS</span></span>

### <span data-ttu-id="4dc50-112">-Clustername</span><span class="sxs-lookup"><span data-stu-id="4dc50-112">-ClusterName</span></span>
<span data-ttu-id="4dc50-113">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="4dc50-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="4dc50-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dc50-114">-DefaultProfile</span></span>
<span data-ttu-id="4dc50-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4dc50-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4dc50-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="4dc50-116">-HttpCredential</span></span>
<span data-ttu-id="4dc50-117">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="4dc50-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="4dc50-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="4dc50-118">-JobDefinition</span></span>
<span data-ttu-id="4dc50-119">Specifica il processo da avviare nel cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4dc50-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="4dc50-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dc50-120">-ResourceGroupName</span></span>
<span data-ttu-id="4dc50-121">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4dc50-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4dc50-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc50-122">CommonParameters</span></span>
<span data-ttu-id="4dc50-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dc50-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc50-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dc50-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc50-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4dc50-125">INPUTS</span></span>

### <span data-ttu-id="4dc50-126">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="4dc50-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>

## <span data-ttu-id="4dc50-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4dc50-127">OUTPUTS</span></span>

### <span data-ttu-id="4dc50-128">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4dc50-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="4dc50-129">Note</span><span class="sxs-lookup"><span data-stu-id="4dc50-129">NOTES</span></span>

## <span data-ttu-id="4dc50-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4dc50-130">RELATED LINKS</span></span>

[<span data-ttu-id="4dc50-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4dc50-131">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="4dc50-132">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="4dc50-132">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="4dc50-133">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4dc50-133">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="4dc50-134">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4dc50-134">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


