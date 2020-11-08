---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: 6b87b7f6e3482aad974c5f7d334724f5d2f99e7c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201286"
---
# <span data-ttu-id="c9294-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c9294-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="c9294-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9294-102">SYNOPSIS</span></span>
<span data-ttu-id="c9294-103">Attende il completamento o l'errore di un processo specificato.</span><span class="sxs-lookup"><span data-stu-id="c9294-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="c9294-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9294-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9294-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9294-105">DESCRIPTION</span></span>
<span data-ttu-id="c9294-106">Il cmdlet **wait-AzHDInsightJob** attende il completamento o l'errore di un processo di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c9294-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="c9294-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9294-107">EXAMPLES</span></span>

### <span data-ttu-id="c9294-108">Esempio 1: attendere il completamento o l'errore di un processo</span><span class="sxs-lookup"><span data-stu-id="c9294-108">Example 1: Wait for the completion or failure of a job</span></span>
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

<span data-ttu-id="c9294-109">Questo comando attende il completamento o l'errore di un processo.</span><span class="sxs-lookup"><span data-stu-id="c9294-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="c9294-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9294-110">PARAMETERS</span></span>

### <span data-ttu-id="c9294-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="c9294-111">-ClusterName</span></span>
<span data-ttu-id="c9294-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="c9294-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="c9294-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9294-113">-DefaultProfile</span></span>
<span data-ttu-id="c9294-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c9294-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9294-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="c9294-115">-HttpCredential</span></span>
<span data-ttu-id="c9294-116">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="c9294-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="c9294-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="c9294-117">-JobId</span></span>
<span data-ttu-id="c9294-118">Specifica l'ID processo del processo.</span><span class="sxs-lookup"><span data-stu-id="c9294-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="c9294-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9294-119">-ResourceGroupName</span></span>
<span data-ttu-id="c9294-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c9294-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c9294-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="c9294-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="c9294-122">Il tempo totale di attesa per il completamento del processo, in secondi.</span><span class="sxs-lookup"><span data-stu-id="c9294-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="c9294-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="c9294-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="c9294-124">Il tempo di attesa tra i controlli dello stato dei processi, in secondi.</span><span class="sxs-lookup"><span data-stu-id="c9294-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="c9294-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9294-125">CommonParameters</span></span>
<span data-ttu-id="c9294-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9294-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9294-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9294-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9294-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9294-128">INPUTS</span></span>

### <span data-ttu-id="c9294-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c9294-129">System.String</span></span>

## <span data-ttu-id="c9294-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9294-130">OUTPUTS</span></span>

### <span data-ttu-id="c9294-131">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c9294-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="c9294-132">Note</span><span class="sxs-lookup"><span data-stu-id="c9294-132">NOTES</span></span>

## <span data-ttu-id="c9294-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9294-133">RELATED LINKS</span></span>

[<span data-ttu-id="c9294-134">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c9294-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="c9294-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c9294-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="c9294-136">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c9294-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)


