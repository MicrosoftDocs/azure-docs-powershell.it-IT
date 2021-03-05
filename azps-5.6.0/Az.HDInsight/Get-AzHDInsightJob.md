---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
ms.openlocfilehash: 87a5b306619bd3d16b9a7c4e76256f2d0e74d568
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998310"
---
# <span data-ttu-id="67f2f-101">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="67f2f-101">Get-AzHDInsightJob</span></span>

## <span data-ttu-id="67f2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67f2f-102">SYNOPSIS</span></span>
<span data-ttu-id="67f2f-103">Recupera l'elenco dei processi da un cluster ed elenca i processi in ordine cronologico inverso oppure recupera un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="67f2f-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

## <span data-ttu-id="67f2f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67f2f-104">SYNTAX</span></span>

```
Get-AzHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67f2f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="67f2f-105">DESCRIPTION</span></span>
<span data-ttu-id="67f2f-106">Il cmdlet **Get-AzHDInsightJob** ottiene i processi recenti per un cluster Azure HDInsight specificato in ordine cronologico inverso, con il processo più recente all'inizio dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="67f2f-106">The **Get-AzHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="67f2f-107">Ottenere un processo specifico fornendo il *parametro JobId.*</span><span class="sxs-lookup"><span data-stu-id="67f2f-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="67f2f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67f2f-108">EXAMPLES</span></span>

### <span data-ttu-id="67f2f-109">Esempio 1: Ottenere processi recenti per un cluster Azure HDInsight specificato</span><span class="sxs-lookup"><span data-stu-id="67f2f-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
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

<span data-ttu-id="67f2f-110">Questo comando recupera tutti i processi recenti per il cluster denominato your-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="67f2f-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="67f2f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67f2f-111">PARAMETERS</span></span>

### <span data-ttu-id="67f2f-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="67f2f-112">-ClusterName</span></span>
<span data-ttu-id="67f2f-113">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="67f2f-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="67f2f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67f2f-114">-DefaultProfile</span></span>
<span data-ttu-id="67f2f-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="67f2f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67f2f-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="67f2f-116">-HttpCredential</span></span>
<span data-ttu-id="67f2f-117">Specifica le credenziali di accesso del cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="67f2f-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="67f2f-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="67f2f-118">-JobId</span></span>
<span data-ttu-id="67f2f-119">Specifica l'ID processo del processo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="67f2f-119">Specifies the job ID of the job to get.</span></span>

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

### <span data-ttu-id="67f2f-120">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="67f2f-120">-NumOfJobs</span></span>
<span data-ttu-id="67f2f-121">Specifica il numero di processi da recuperare.</span><span class="sxs-lookup"><span data-stu-id="67f2f-121">Specifies the number of jobs to retrieve.</span></span>

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

### <span data-ttu-id="67f2f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67f2f-122">-ResourceGroupName</span></span>
<span data-ttu-id="67f2f-123">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="67f2f-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="67f2f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f2f-124">CommonParameters</span></span>
<span data-ttu-id="67f2f-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67f2f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f2f-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="67f2f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f2f-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="67f2f-127">INPUTS</span></span>

### <span data-ttu-id="67f2f-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="67f2f-128">None</span></span>

## <span data-ttu-id="67f2f-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67f2f-129">OUTPUTS</span></span>

### <span data-ttu-id="67f2f-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="67f2f-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="67f2f-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="67f2f-131">NOTES</span></span>

## <span data-ttu-id="67f2f-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67f2f-132">RELATED LINKS</span></span>

[<span data-ttu-id="67f2f-133">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="67f2f-133">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="67f2f-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="67f2f-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="67f2f-135">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="67f2f-135">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="67f2f-136">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="67f2f-136">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


