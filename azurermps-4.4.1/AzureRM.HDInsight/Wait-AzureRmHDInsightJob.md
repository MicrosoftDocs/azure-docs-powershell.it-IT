---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
ms.openlocfilehash: 6e19594cfcd79c6be82373af6245ea2154296b48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688638"
---
# <span data-ttu-id="64b27-101">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="64b27-101">Wait-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="64b27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64b27-102">SYNOPSIS</span></span>
<span data-ttu-id="64b27-103">Attende il completamento o l'errore di un processo specificato.</span><span class="sxs-lookup"><span data-stu-id="64b27-103">Waits for the completion or failure of a specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64b27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64b27-104">SYNTAX</span></span>

```
Wait-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64b27-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64b27-105">DESCRIPTION</span></span>
<span data-ttu-id="64b27-106">Il cmdlet **wait-AzureRmHDInsightJob** attende il completamento o l'errore di un processo di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="64b27-106">The **Wait-AzureRmHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="64b27-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64b27-107">EXAMPLES</span></span>

### <span data-ttu-id="64b27-108">Esempio 1: attendere il completamento o l'errore di un processo</span><span class="sxs-lookup"><span data-stu-id="64b27-108">Example 1: Wait for the completion or failure of a job</span></span>
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

<span data-ttu-id="64b27-109">Questo comando attende il completamento o l'errore di un processo.</span><span class="sxs-lookup"><span data-stu-id="64b27-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="64b27-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64b27-110">PARAMETERS</span></span>

### <span data-ttu-id="64b27-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="64b27-111">-ClusterName</span></span>
<span data-ttu-id="64b27-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="64b27-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="64b27-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="64b27-113">-HttpCredential</span></span>
<span data-ttu-id="64b27-114">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="64b27-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="64b27-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="64b27-115">-JobId</span></span>
<span data-ttu-id="64b27-116">Specifica l'ID processo del processo.</span><span class="sxs-lookup"><span data-stu-id="64b27-116">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="64b27-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64b27-117">-ResourceGroupName</span></span>
<span data-ttu-id="64b27-118">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="64b27-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="64b27-119">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="64b27-119">-TimeoutInSeconds</span></span>
<span data-ttu-id="64b27-120">Il tempo totale di attesa per il completamento del processo, in secondi.</span><span class="sxs-lookup"><span data-stu-id="64b27-120">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="64b27-121">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="64b27-121">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="64b27-122">Il tempo di attesa tra i controlli dello stato dei processi, in secondi.</span><span class="sxs-lookup"><span data-stu-id="64b27-122">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="64b27-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64b27-123">-DefaultProfile</span></span>
<span data-ttu-id="64b27-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64b27-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64b27-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64b27-125">CommonParameters</span></span>
<span data-ttu-id="64b27-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64b27-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64b27-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64b27-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64b27-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64b27-128">INPUTS</span></span>

### <span data-ttu-id="64b27-129">Stringa</span><span class="sxs-lookup"><span data-stu-id="64b27-129">String</span></span>
<span data-ttu-id="64b27-130">Il parametro ' JobId ' accetta il valore di tipo ' String ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="64b27-130">Parameter 'JobId' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="64b27-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64b27-131">OUTPUTS</span></span>

### <span data-ttu-id="64b27-132">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="64b27-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="64b27-133">Note</span><span class="sxs-lookup"><span data-stu-id="64b27-133">NOTES</span></span>

## <span data-ttu-id="64b27-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64b27-134">RELATED LINKS</span></span>

[<span data-ttu-id="64b27-135">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="64b27-135">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="64b27-136">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="64b27-136">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="64b27-137">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="64b27-137">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)


