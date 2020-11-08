---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
ms.openlocfilehash: b2ba2144eccd3069453daa1ada15527539400c22
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193327"
---
# <span data-ttu-id="237e7-101">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="237e7-101">Get-AzHDInsightJob</span></span>

## <span data-ttu-id="237e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="237e7-102">SYNOPSIS</span></span>
<span data-ttu-id="237e7-103">Ottiene l'elenco dei processi da un cluster e li elenca in ordine cronologico inverso o recupera un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="237e7-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

## <span data-ttu-id="237e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="237e7-104">SYNTAX</span></span>

```
Get-AzHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="237e7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="237e7-105">DESCRIPTION</span></span>
<span data-ttu-id="237e7-106">Il cmdlet **Get-AzHDInsightJob** ottiene i processi recenti per un cluster di Azure HDInsight specificato in ordine cronologico inverso, con il processo più recente nella parte superiore dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="237e7-106">The **Get-AzHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="237e7-107">Ottenere un processo specifico fornendo il parametro *JobID* .</span><span class="sxs-lookup"><span data-stu-id="237e7-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="237e7-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="237e7-108">EXAMPLES</span></span>

### <span data-ttu-id="237e7-109">Esempio 1: ottenere processi recenti per un cluster di Azure HDInsight specificato</span><span class="sxs-lookup"><span data-stu-id="237e7-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="237e7-110">Questo comando ottiene tutti i processi recenti per il cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="237e7-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="237e7-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="237e7-111">PARAMETERS</span></span>

### <span data-ttu-id="237e7-112">-Clustername</span><span class="sxs-lookup"><span data-stu-id="237e7-112">-ClusterName</span></span>
<span data-ttu-id="237e7-113">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="237e7-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="237e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="237e7-114">-DefaultProfile</span></span>
<span data-ttu-id="237e7-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="237e7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="237e7-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="237e7-116">-HttpCredential</span></span>
<span data-ttu-id="237e7-117">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="237e7-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="237e7-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="237e7-118">-JobId</span></span>
<span data-ttu-id="237e7-119">Specifica l'ID lavoro del processo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="237e7-119">Specifies the job ID of the job to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="237e7-120">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="237e7-120">-NumOfJobs</span></span>
<span data-ttu-id="237e7-121">Specifica il numero di processi da recuperare.</span><span class="sxs-lookup"><span data-stu-id="237e7-121">Specifies the number of jobs to retrieve.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="237e7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="237e7-122">-ResourceGroupName</span></span>
<span data-ttu-id="237e7-123">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="237e7-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="237e7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="237e7-124">CommonParameters</span></span>
<span data-ttu-id="237e7-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="237e7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="237e7-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="237e7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="237e7-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="237e7-127">INPUTS</span></span>

### <span data-ttu-id="237e7-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="237e7-128">None</span></span>

## <span data-ttu-id="237e7-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="237e7-129">OUTPUTS</span></span>

### <span data-ttu-id="237e7-130">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="237e7-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="237e7-131">Note</span><span class="sxs-lookup"><span data-stu-id="237e7-131">NOTES</span></span>

## <span data-ttu-id="237e7-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="237e7-132">RELATED LINKS</span></span>

[<span data-ttu-id="237e7-133">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="237e7-133">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="237e7-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="237e7-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="237e7-135">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="237e7-135">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="237e7-136">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="237e7-136">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


