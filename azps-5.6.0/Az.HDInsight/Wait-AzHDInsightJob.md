---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: 4d4b3ff71142540ff5c5635938d31a16e3fd9603
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975790"
---
# <span data-ttu-id="56ea8-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="56ea8-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="56ea8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="56ea8-103">Attende il completamento o l'errore di un processo specificato.</span><span class="sxs-lookup"><span data-stu-id="56ea8-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="56ea8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56ea8-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56ea8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="56ea8-105">DESCRIPTION</span></span>
<span data-ttu-id="56ea8-106">Il cmdlet **Wait-AzHDInsightJob** attende il completamento o l'errore di un processo di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="56ea8-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="56ea8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56ea8-107">EXAMPLES</span></span>

### <span data-ttu-id="56ea8-108">Esempio 1: Attendere il completamento o l'esito negativo di un processo</span><span class="sxs-lookup"><span data-stu-id="56ea8-108">Example 1: Wait for the completion or failure of a job</span></span>
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

<span data-ttu-id="56ea8-109">Questo comando attende il completamento o l'errore di un processo.</span><span class="sxs-lookup"><span data-stu-id="56ea8-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="56ea8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56ea8-110">PARAMETERS</span></span>

### <span data-ttu-id="56ea8-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="56ea8-111">-ClusterName</span></span>
<span data-ttu-id="56ea8-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="56ea8-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="56ea8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56ea8-113">-DefaultProfile</span></span>
<span data-ttu-id="56ea8-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="56ea8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56ea8-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="56ea8-115">-HttpCredential</span></span>
<span data-ttu-id="56ea8-116">Specifica le credenziali di accesso del cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="56ea8-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="56ea8-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="56ea8-117">-JobId</span></span>
<span data-ttu-id="56ea8-118">Specifica l'ID processo del processo.</span><span class="sxs-lookup"><span data-stu-id="56ea8-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="56ea8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56ea8-119">-ResourceGroupName</span></span>
<span data-ttu-id="56ea8-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="56ea8-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="56ea8-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="56ea8-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="56ea8-122">Il tempo totale di attesa, in secondi, del completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="56ea8-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="56ea8-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="56ea8-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="56ea8-124">Il tempo di attesa tra i controlli dello stato del processo, in secondi.</span><span class="sxs-lookup"><span data-stu-id="56ea8-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="56ea8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56ea8-125">CommonParameters</span></span>
<span data-ttu-id="56ea8-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56ea8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56ea8-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="56ea8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56ea8-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="56ea8-128">INPUTS</span></span>

### <span data-ttu-id="56ea8-129">System.String</span><span class="sxs-lookup"><span data-stu-id="56ea8-129">System.String</span></span>

## <span data-ttu-id="56ea8-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56ea8-130">OUTPUTS</span></span>

### <span data-ttu-id="56ea8-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="56ea8-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="56ea8-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="56ea8-132">NOTES</span></span>

## <span data-ttu-id="56ea8-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56ea8-133">RELATED LINKS</span></span>

[<span data-ttu-id="56ea8-134">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="56ea8-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="56ea8-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="56ea8-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="56ea8-136">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="56ea8-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)


