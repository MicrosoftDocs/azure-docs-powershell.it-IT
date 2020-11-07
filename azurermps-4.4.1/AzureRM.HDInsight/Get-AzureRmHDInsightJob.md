---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
ms.openlocfilehash: e3cfd7978ecd7f8395a0c499d3d194f133960a7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686577"
---
# <span data-ttu-id="f67ae-101">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f67ae-101">Get-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="f67ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f67ae-102">SYNOPSIS</span></span>
<span data-ttu-id="f67ae-103">Ottiene l'elenco dei processi da un cluster e li elenca in ordine cronologico inverso o recupera un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="f67ae-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f67ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f67ae-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f67ae-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f67ae-105">DESCRIPTION</span></span>
<span data-ttu-id="f67ae-106">Il cmdlet **Get-AzureRmHDInsightJob** ottiene i processi recenti per un cluster di Azure HDInsight specificato in ordine cronologico inverso, con il processo più recente nella parte superiore dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="f67ae-106">The **Get-AzureRmHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="f67ae-107">Ottenere un processo specifico fornendo il parametro *JobID* .</span><span class="sxs-lookup"><span data-stu-id="f67ae-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="f67ae-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f67ae-108">EXAMPLES</span></span>

### <span data-ttu-id="f67ae-109">Esempio 1: ottenere processi recenti per un cluster di Azure HDInsight specificato</span><span class="sxs-lookup"><span data-stu-id="f67ae-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="f67ae-110">Questo comando ottiene tutti i processi recenti per il cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="f67ae-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="f67ae-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f67ae-111">PARAMETERS</span></span>

### <span data-ttu-id="f67ae-112">-Clustername</span><span class="sxs-lookup"><span data-stu-id="f67ae-112">-ClusterName</span></span>
<span data-ttu-id="f67ae-113">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="f67ae-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f67ae-114">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="f67ae-114">-HttpCredential</span></span>
<span data-ttu-id="f67ae-115">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="f67ae-115">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="f67ae-116">-JobId</span><span class="sxs-lookup"><span data-stu-id="f67ae-116">-JobId</span></span>
<span data-ttu-id="f67ae-117">Specifica l'ID lavoro del processo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="f67ae-117">Specifies the job ID of the job to get.</span></span>

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

### <span data-ttu-id="f67ae-118">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="f67ae-118">-NumOfJobs</span></span>
<span data-ttu-id="f67ae-119">Specifica il numero di processi da recuperare.</span><span class="sxs-lookup"><span data-stu-id="f67ae-119">Specifies the number of jobs to retrieve.</span></span>

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

### <span data-ttu-id="f67ae-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f67ae-120">-ResourceGroupName</span></span>
<span data-ttu-id="f67ae-121">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f67ae-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f67ae-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f67ae-122">-DefaultProfile</span></span>
<span data-ttu-id="f67ae-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f67ae-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f67ae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f67ae-124">CommonParameters</span></span>
<span data-ttu-id="f67ae-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f67ae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f67ae-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f67ae-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f67ae-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f67ae-127">INPUTS</span></span>

## <span data-ttu-id="f67ae-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f67ae-128">OUTPUTS</span></span>

### <span data-ttu-id="f67ae-129">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f67ae-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="f67ae-130">Note</span><span class="sxs-lookup"><span data-stu-id="f67ae-130">NOTES</span></span>

## <span data-ttu-id="f67ae-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f67ae-131">RELATED LINKS</span></span>

[<span data-ttu-id="f67ae-132">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f67ae-132">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="f67ae-133">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f67ae-133">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="f67ae-134">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f67ae-134">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="f67ae-135">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f67ae-135">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


