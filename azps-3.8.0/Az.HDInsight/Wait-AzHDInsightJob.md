---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: 6b87b7f6e3482aad974c5f7d334724f5d2f99e7c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018397"
---
# <span data-ttu-id="2c085-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2c085-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="2c085-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c085-102">SYNOPSIS</span></span>
<span data-ttu-id="2c085-103">Attende il completamento o l'errore di un processo specificato.</span><span class="sxs-lookup"><span data-stu-id="2c085-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="2c085-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c085-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c085-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c085-105">DESCRIPTION</span></span>
<span data-ttu-id="2c085-106">Il cmdlet **wait-AzHDInsightJob** attende il completamento o l'errore di un processo di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2c085-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="2c085-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c085-107">EXAMPLES</span></span>

### <span data-ttu-id="2c085-108">Esempio 1: attendere il completamento o l'errore di un processo</span><span class="sxs-lookup"><span data-stu-id="2c085-108">Example 1: Wait for the completion or failure of a job</span></span>
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

<span data-ttu-id="2c085-109">Questo comando attende il completamento o l'errore di un processo.</span><span class="sxs-lookup"><span data-stu-id="2c085-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="2c085-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c085-110">PARAMETERS</span></span>

### <span data-ttu-id="2c085-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="2c085-111">-ClusterName</span></span>
<span data-ttu-id="2c085-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="2c085-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2c085-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c085-113">-DefaultProfile</span></span>
<span data-ttu-id="2c085-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2c085-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c085-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="2c085-115">-HttpCredential</span></span>
<span data-ttu-id="2c085-116">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="2c085-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="2c085-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="2c085-117">-JobId</span></span>
<span data-ttu-id="2c085-118">Specifica l'ID processo del processo.</span><span class="sxs-lookup"><span data-stu-id="2c085-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="2c085-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c085-119">-ResourceGroupName</span></span>
<span data-ttu-id="2c085-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2c085-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2c085-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="2c085-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="2c085-122">Il tempo totale di attesa per il completamento del processo, in secondi.</span><span class="sxs-lookup"><span data-stu-id="2c085-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="2c085-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="2c085-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="2c085-124">Il tempo di attesa tra i controlli dello stato dei processi, in secondi.</span><span class="sxs-lookup"><span data-stu-id="2c085-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="2c085-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c085-125">CommonParameters</span></span>
<span data-ttu-id="2c085-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c085-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c085-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c085-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c085-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c085-128">INPUTS</span></span>

### <span data-ttu-id="2c085-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2c085-129">System.String</span></span>

## <span data-ttu-id="2c085-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c085-130">OUTPUTS</span></span>

### <span data-ttu-id="2c085-131">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2c085-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="2c085-132">Note</span><span class="sxs-lookup"><span data-stu-id="2c085-132">NOTES</span></span>

## <span data-ttu-id="2c085-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c085-133">RELATED LINKS</span></span>

[<span data-ttu-id="2c085-134">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2c085-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="2c085-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2c085-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="2c085-136">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2c085-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)


