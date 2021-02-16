---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: 4c1d991d3236c8e631b2b5c7f0026e91af2f8cf2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185847"
---
# <span data-ttu-id="2e9fa-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2e9fa-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="2e9fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e9fa-102">SYNOPSIS</span></span>
<span data-ttu-id="2e9fa-103">Attende il completamento o l'errore di un processo specificato.</span><span class="sxs-lookup"><span data-stu-id="2e9fa-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="2e9fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e9fa-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e9fa-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2e9fa-105">DESCRIPTION</span></span>
<span data-ttu-id="2e9fa-106">Il cmdlet **Wait-AzHDInsightJob** attende il completamento o l'errore di un processo di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2e9fa-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="2e9fa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e9fa-107">EXAMPLES</span></span>

### <span data-ttu-id="2e9fa-108">Esempio 1: Attendere il completamento o l'esito negativo di un processo</span><span class="sxs-lookup"><span data-stu-id="2e9fa-108">Example 1: Wait for the completion or failure of a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Wait-AzHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="2e9fa-109">Questo comando attende il completamento o l'errore di un processo.</span><span class="sxs-lookup"><span data-stu-id="2e9fa-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="2e9fa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e9fa-110">PARAMETERS</span></span>

### <span data-ttu-id="2e9fa-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2e9fa-111">-ClusterName</span></span>
<span data-ttu-id="2e9fa-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="2e9fa-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2e9fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e9fa-113">-DefaultProfile</span></span>
<span data-ttu-id="2e9fa-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="2e9fa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e9fa-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="2e9fa-115">-HttpCredential</span></span>
<span data-ttu-id="2e9fa-116">Specifica le credenziali di accesso del cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="2e9fa-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="2e9fa-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="2e9fa-117">-JobId</span></span>
<span data-ttu-id="2e9fa-118">Specifica l'ID processo del processo.</span><span class="sxs-lookup"><span data-stu-id="2e9fa-118">Specifies the job ID of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e9fa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e9fa-119">-ResourceGroupName</span></span>
<span data-ttu-id="2e9fa-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2e9fa-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2e9fa-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="2e9fa-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="2e9fa-122">Il tempo totale di attesa del completamento del processo, in secondi.</span><span class="sxs-lookup"><span data-stu-id="2e9fa-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="2e9fa-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="2e9fa-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="2e9fa-124">Il tempo di attesa tra i controlli dello stato del processo, in secondi.</span><span class="sxs-lookup"><span data-stu-id="2e9fa-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="2e9fa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e9fa-125">CommonParameters</span></span>
<span data-ttu-id="2e9fa-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e9fa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e9fa-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2e9fa-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e9fa-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="2e9fa-128">INPUTS</span></span>

### <span data-ttu-id="2e9fa-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2e9fa-129">System.String</span></span>

## <span data-ttu-id="2e9fa-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e9fa-130">OUTPUTS</span></span>

### <span data-ttu-id="2e9fa-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2e9fa-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="2e9fa-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="2e9fa-132">NOTES</span></span>

## <span data-ttu-id="2e9fa-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e9fa-133">RELATED LINKS</span></span>

[<span data-ttu-id="2e9fa-134">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2e9fa-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="2e9fa-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2e9fa-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="2e9fa-136">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2e9fa-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)


