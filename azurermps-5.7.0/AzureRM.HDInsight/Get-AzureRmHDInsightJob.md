---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
ms.openlocfilehash: 2fa3ae6cd48887f377ea4bdb6ce36001afe29b5d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685988"
---
# <span data-ttu-id="567fa-101">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="567fa-101">Get-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="567fa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="567fa-102">SYNOPSIS</span></span>
<span data-ttu-id="567fa-103">Ottiene l'elenco dei processi da un cluster e li elenca in ordine cronologico inverso o recupera un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="567fa-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="567fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="567fa-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="567fa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="567fa-105">DESCRIPTION</span></span>
<span data-ttu-id="567fa-106">Il cmdlet **Get-AzureRmHDInsightJob** ottiene i processi recenti per un cluster di Azure HDInsight specificato in ordine cronologico inverso, con il processo più recente nella parte superiore dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="567fa-106">The **Get-AzureRmHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="567fa-107">Ottenere un processo specifico fornendo il parametro *JobID* .</span><span class="sxs-lookup"><span data-stu-id="567fa-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="567fa-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="567fa-108">EXAMPLES</span></span>

### <span data-ttu-id="567fa-109">Esempio 1: ottenere processi recenti per un cluster di Azure HDInsight specificato</span><span class="sxs-lookup"><span data-stu-id="567fa-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
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

<span data-ttu-id="567fa-110">Questo comando ottiene tutti i processi recenti per il cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="567fa-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="567fa-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="567fa-111">PARAMETERS</span></span>

### <span data-ttu-id="567fa-112">-Clustername</span><span class="sxs-lookup"><span data-stu-id="567fa-112">-ClusterName</span></span>
<span data-ttu-id="567fa-113">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="567fa-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="567fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="567fa-114">-DefaultProfile</span></span>
<span data-ttu-id="567fa-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="567fa-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="567fa-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="567fa-116">-HttpCredential</span></span>
<span data-ttu-id="567fa-117">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="567fa-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567fa-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="567fa-118">-JobId</span></span>
<span data-ttu-id="567fa-119">Specifica l'ID lavoro del processo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="567fa-119">Specifies the job ID of the job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567fa-120">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="567fa-120">-NumOfJobs</span></span>
<span data-ttu-id="567fa-121">Specifica il numero di processi da recuperare.</span><span class="sxs-lookup"><span data-stu-id="567fa-121">Specifies the number of jobs to retrieve.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567fa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="567fa-122">-ResourceGroupName</span></span>
<span data-ttu-id="567fa-123">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="567fa-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="567fa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="567fa-124">CommonParameters</span></span>
<span data-ttu-id="567fa-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="567fa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="567fa-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="567fa-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="567fa-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="567fa-127">INPUTS</span></span>

### <span data-ttu-id="567fa-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="567fa-128">None</span></span>
<span data-ttu-id="567fa-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="567fa-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="567fa-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="567fa-130">OUTPUTS</span></span>

### <span data-ttu-id="567fa-131">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="567fa-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="567fa-132">Note</span><span class="sxs-lookup"><span data-stu-id="567fa-132">NOTES</span></span>

## <span data-ttu-id="567fa-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="567fa-133">RELATED LINKS</span></span>

[<span data-ttu-id="567fa-134">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="567fa-134">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="567fa-135">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="567fa-135">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="567fa-136">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="567fa-136">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="567fa-137">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="567fa-137">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


