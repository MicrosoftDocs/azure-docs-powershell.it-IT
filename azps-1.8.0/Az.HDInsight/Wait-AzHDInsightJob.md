---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: b603be88ffa89f730cfaaa2f67738cdadc2d4d25
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835943"
---
# <span data-ttu-id="24452-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="24452-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="24452-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24452-102">SYNOPSIS</span></span>
<span data-ttu-id="24452-103">Attende il completamento o l'errore di un processo specificato.</span><span class="sxs-lookup"><span data-stu-id="24452-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="24452-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24452-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24452-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24452-105">DESCRIPTION</span></span>
<span data-ttu-id="24452-106">Il cmdlet **wait-AzHDInsightJob** attende il completamento o l'errore di un processo di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="24452-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="24452-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24452-107">EXAMPLES</span></span>

### <span data-ttu-id="24452-108">Esempio 1: attendere il completamento o l'errore di un processo</span><span class="sxs-lookup"><span data-stu-id="24452-108">Example 1: Wait for the completion or failure of a job</span></span>
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

<span data-ttu-id="24452-109">Questo comando attende il completamento o l'errore di un processo.</span><span class="sxs-lookup"><span data-stu-id="24452-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="24452-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24452-110">PARAMETERS</span></span>

### <span data-ttu-id="24452-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="24452-111">-ClusterName</span></span>
<span data-ttu-id="24452-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="24452-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="24452-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24452-113">-DefaultProfile</span></span>
<span data-ttu-id="24452-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="24452-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24452-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="24452-115">-HttpCredential</span></span>
<span data-ttu-id="24452-116">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="24452-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="24452-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="24452-117">-JobId</span></span>
<span data-ttu-id="24452-118">Specifica l'ID processo del processo.</span><span class="sxs-lookup"><span data-stu-id="24452-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="24452-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24452-119">-ResourceGroupName</span></span>
<span data-ttu-id="24452-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="24452-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="24452-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="24452-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="24452-122">Il tempo totale di attesa per il completamento del processo, in secondi.</span><span class="sxs-lookup"><span data-stu-id="24452-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="24452-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="24452-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="24452-124">Il tempo di attesa tra i controlli dello stato dei processi, in secondi.</span><span class="sxs-lookup"><span data-stu-id="24452-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="24452-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24452-125">CommonParameters</span></span>
<span data-ttu-id="24452-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24452-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24452-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24452-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24452-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24452-128">INPUTS</span></span>

### <span data-ttu-id="24452-129">System. String</span><span class="sxs-lookup"><span data-stu-id="24452-129">System.String</span></span>

## <span data-ttu-id="24452-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24452-130">OUTPUTS</span></span>

### <span data-ttu-id="24452-131">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="24452-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="24452-132">Note</span><span class="sxs-lookup"><span data-stu-id="24452-132">NOTES</span></span>

## <span data-ttu-id="24452-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24452-133">RELATED LINKS</span></span>

[<span data-ttu-id="24452-134">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="24452-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="24452-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="24452-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="24452-136">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="24452-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)


