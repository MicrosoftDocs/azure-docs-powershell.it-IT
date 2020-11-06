---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/wait-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
ms.openlocfilehash: de7df9417e617f88c61e75c64dd42f32b83fc66b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516619"
---
# <span data-ttu-id="37d41-101">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="37d41-101">Wait-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="37d41-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37d41-102">SYNOPSIS</span></span>
<span data-ttu-id="37d41-103">Attende il completamento o l'errore di un processo specificato.</span><span class="sxs-lookup"><span data-stu-id="37d41-103">Waits for the completion or failure of a specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37d41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37d41-104">SYNTAX</span></span>

```
Wait-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37d41-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37d41-105">DESCRIPTION</span></span>
<span data-ttu-id="37d41-106">Il cmdlet **wait-AzureRmHDInsightJob** attende il completamento o l'errore di un processo di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="37d41-106">The **Wait-AzureRmHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="37d41-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37d41-107">EXAMPLES</span></span>

### <span data-ttu-id="37d41-108">Esempio 1: attendere il completamento o l'errore di un processo</span><span class="sxs-lookup"><span data-stu-id="37d41-108">Example 1: Wait for the completion or failure of a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Wait-AzureRmHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="37d41-109">Questo comando attende il completamento o l'errore di un processo.</span><span class="sxs-lookup"><span data-stu-id="37d41-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="37d41-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37d41-110">PARAMETERS</span></span>

### <span data-ttu-id="37d41-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="37d41-111">-ClusterName</span></span>
<span data-ttu-id="37d41-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="37d41-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="37d41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37d41-113">-DefaultProfile</span></span>
<span data-ttu-id="37d41-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="37d41-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37d41-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="37d41-115">-HttpCredential</span></span>
<span data-ttu-id="37d41-116">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="37d41-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="37d41-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="37d41-117">-JobId</span></span>
<span data-ttu-id="37d41-118">Specifica l'ID processo del processo.</span><span class="sxs-lookup"><span data-stu-id="37d41-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="37d41-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37d41-119">-ResourceGroupName</span></span>
<span data-ttu-id="37d41-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="37d41-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="37d41-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="37d41-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="37d41-122">Il tempo totale di attesa per il completamento del processo, in secondi.</span><span class="sxs-lookup"><span data-stu-id="37d41-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="37d41-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="37d41-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="37d41-124">Il tempo di attesa tra i controlli dello stato dei processi, in secondi.</span><span class="sxs-lookup"><span data-stu-id="37d41-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="37d41-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37d41-125">CommonParameters</span></span>
<span data-ttu-id="37d41-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37d41-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37d41-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37d41-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37d41-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37d41-128">INPUTS</span></span>

### <span data-ttu-id="37d41-129">System. String</span><span class="sxs-lookup"><span data-stu-id="37d41-129">System.String</span></span>
<span data-ttu-id="37d41-130">Parametri: JobId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="37d41-130">Parameters: JobId (ByValue)</span></span>

## <span data-ttu-id="37d41-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37d41-131">OUTPUTS</span></span>

### <span data-ttu-id="37d41-132">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="37d41-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="37d41-133">Note</span><span class="sxs-lookup"><span data-stu-id="37d41-133">NOTES</span></span>

## <span data-ttu-id="37d41-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37d41-134">RELATED LINKS</span></span>

[<span data-ttu-id="37d41-135">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="37d41-135">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="37d41-136">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="37d41-136">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="37d41-137">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="37d41-137">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)


