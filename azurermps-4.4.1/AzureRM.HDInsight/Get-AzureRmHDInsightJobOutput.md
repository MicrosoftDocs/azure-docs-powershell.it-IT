---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
ms.openlocfilehash: eebbe6fb233b0d6117411973e841cf39f2ae377d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519172"
---
# <span data-ttu-id="cdc09-101">Get-AzureRmHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="cdc09-101">Get-AzureRmHDInsightJobOutput</span></span>

## <span data-ttu-id="cdc09-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cdc09-102">SYNOPSIS</span></span>
<span data-ttu-id="cdc09-103">Ottiene l'output del log per un processo dall'account di archiviazione associato a un cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="cdc09-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdc09-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cdc09-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdc09-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cdc09-105">DESCRIPTION</span></span>
<span data-ttu-id="cdc09-106">Il cmdlet **Get-AzureRmHDInsightJobOutput** Ottiene l'output del log per un processo dall'account di archiviazione associato a un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cdc09-106">The **Get-AzureRmHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="cdc09-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cdc09-107">EXAMPLES</span></span>

### <span data-ttu-id="cdc09-108">Esempio 1: ottenere l'output del log per un processo</span><span class="sxs-lookup"><span data-stu-id="cdc09-108">Example 1: Get the log output for a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "<status folder>"
PS C:\> $query = "<query here>"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzureRmHDInsightJobOutput `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="cdc09-109">Questo comando consente di ottenere l'output del log dal cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="cdc09-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="cdc09-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cdc09-110">PARAMETERS</span></span>

### <span data-ttu-id="cdc09-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="cdc09-111">-ClusterName</span></span>
<span data-ttu-id="cdc09-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="cdc09-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="cdc09-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="cdc09-113">-DefaultContainer</span></span>
<span data-ttu-id="cdc09-114">Specifica il nome del contenitore predefinito.</span><span class="sxs-lookup"><span data-stu-id="cdc09-114">Specifies the default container name.</span></span>

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

### <span data-ttu-id="cdc09-115">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="cdc09-115">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="cdc09-116">Specifica la chiave dell'account di archiviazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="cdc09-116">Specifies the default Storage account key.</span></span>

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

### <span data-ttu-id="cdc09-117">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cdc09-117">-DefaultStorageAccountName</span></span>
<span data-ttu-id="cdc09-118">Specifica il nome dell'account di archiviazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="cdc09-118">Specifies the default Storage account name.</span></span>

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

### <span data-ttu-id="cdc09-119">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="cdc09-119">-DisplayOutputType</span></span>
<span data-ttu-id="cdc09-120">Specifica il tipo di output del processo richiesto.</span><span class="sxs-lookup"><span data-stu-id="cdc09-120">Specifies the job output type being requested.</span></span>
<span data-ttu-id="cdc09-121">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="cdc09-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cdc09-122">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="cdc09-122">StandardOutput</span></span>
- <span data-ttu-id="cdc09-123">StandardError</span><span class="sxs-lookup"><span data-stu-id="cdc09-123">StandardError</span></span>

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

### <span data-ttu-id="cdc09-124">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="cdc09-124">-HttpCredential</span></span>
<span data-ttu-id="cdc09-125">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="cdc09-125">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="cdc09-126">-JobId</span><span class="sxs-lookup"><span data-stu-id="cdc09-126">-JobId</span></span>
<span data-ttu-id="cdc09-127">Specifica l'ID processo del processo di cui viene recuperato l'output.</span><span class="sxs-lookup"><span data-stu-id="cdc09-127">Specifies the job ID of the job whose output will be fetched.</span></span>

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

### <span data-ttu-id="cdc09-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdc09-128">-ResourceGroupName</span></span>
<span data-ttu-id="cdc09-129">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cdc09-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cdc09-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdc09-130">-DefaultProfile</span></span>
<span data-ttu-id="cdc09-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cdc09-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdc09-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdc09-132">CommonParameters</span></span>
<span data-ttu-id="cdc09-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdc09-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdc09-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdc09-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdc09-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cdc09-135">INPUTS</span></span>

## <span data-ttu-id="cdc09-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cdc09-136">OUTPUTS</span></span>

### <span data-ttu-id="cdc09-137">System. String</span><span class="sxs-lookup"><span data-stu-id="cdc09-137">System.String</span></span>

## <span data-ttu-id="cdc09-138">Note</span><span class="sxs-lookup"><span data-stu-id="cdc09-138">NOTES</span></span>

## <span data-ttu-id="cdc09-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cdc09-139">RELATED LINKS</span></span>

[<span data-ttu-id="cdc09-140">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="cdc09-140">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="cdc09-141">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="cdc09-141">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


