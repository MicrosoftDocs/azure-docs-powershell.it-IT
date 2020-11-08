---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
ms.openlocfilehash: 2489da10ebf1d346b147e252d6d347635efb1aff
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193325"
---
# <span data-ttu-id="a47aa-101">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="a47aa-101">Get-AzHDInsightJobOutput</span></span>

## <span data-ttu-id="a47aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a47aa-102">SYNOPSIS</span></span>
<span data-ttu-id="a47aa-103">Ottiene l'output del log per un processo dall'account di archiviazione associato a un cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="a47aa-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

## <span data-ttu-id="a47aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a47aa-104">SYNTAX</span></span>

```
Get-AzHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a47aa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a47aa-105">DESCRIPTION</span></span>
<span data-ttu-id="a47aa-106">Il cmdlet **Get-AzHDInsightJobOutput** Ottiene l'output del log per un processo dall'account di archiviazione associato a un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a47aa-106">The **Get-AzHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="a47aa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a47aa-107">EXAMPLES</span></span>

### <span data-ttu-id="a47aa-108">Esempio 1: ottenere l'output del log per un processo</span><span class="sxs-lookup"><span data-stu-id="a47aa-108">Example 1: Get the log output for a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "<status folder>"
PS C:\> $query = "<query here>"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzHDInsightJobOutput `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="a47aa-109">Questo comando consente di ottenere l'output del log dal cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="a47aa-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="a47aa-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a47aa-110">PARAMETERS</span></span>

### <span data-ttu-id="a47aa-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="a47aa-111">-ClusterName</span></span>
<span data-ttu-id="a47aa-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="a47aa-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a47aa-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="a47aa-113">-DefaultContainer</span></span>
<span data-ttu-id="a47aa-114">Specifica il nome del contenitore predefinito.</span><span class="sxs-lookup"><span data-stu-id="a47aa-114">Specifies the default container name.</span></span>

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

### <span data-ttu-id="a47aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a47aa-115">-DefaultProfile</span></span>
<span data-ttu-id="a47aa-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a47aa-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a47aa-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a47aa-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="a47aa-118">Specifica la chiave dell'account di archiviazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a47aa-118">Specifies the default Storage account key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47aa-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a47aa-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="a47aa-120">Specifica il nome dell'account di archiviazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="a47aa-120">Specifies the default Storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47aa-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="a47aa-121">-DisplayOutputType</span></span>
<span data-ttu-id="a47aa-122">Specifica il tipo di output del processo richiesto.</span><span class="sxs-lookup"><span data-stu-id="a47aa-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="a47aa-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a47aa-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a47aa-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="a47aa-124">StandardOutput</span></span>
- <span data-ttu-id="a47aa-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="a47aa-125">StandardError</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Job.JobDisplayOutputType
Parameter Sets: (All)
Aliases:
Accepted values: StandardOutput, StandardError

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47aa-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="a47aa-126">-HttpCredential</span></span>
<span data-ttu-id="a47aa-127">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="a47aa-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47aa-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="a47aa-128">-JobId</span></span>
<span data-ttu-id="a47aa-129">Specifica l'ID processo del processo di cui viene recuperato l'output.</span><span class="sxs-lookup"><span data-stu-id="a47aa-129">Specifies the job ID of the job whose output will be fetched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47aa-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a47aa-130">-ResourceGroupName</span></span>
<span data-ttu-id="a47aa-131">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a47aa-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a47aa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a47aa-132">CommonParameters</span></span>
<span data-ttu-id="a47aa-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a47aa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a47aa-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a47aa-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a47aa-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a47aa-135">INPUTS</span></span>

### <span data-ttu-id="a47aa-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a47aa-136">None</span></span>

## <span data-ttu-id="a47aa-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a47aa-137">OUTPUTS</span></span>

### <span data-ttu-id="a47aa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a47aa-138">System.String</span></span>

## <span data-ttu-id="a47aa-139">Note</span><span class="sxs-lookup"><span data-stu-id="a47aa-139">NOTES</span></span>

## <span data-ttu-id="a47aa-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a47aa-140">RELATED LINKS</span></span>

[<span data-ttu-id="a47aa-141">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a47aa-141">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="a47aa-142">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a47aa-142">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

