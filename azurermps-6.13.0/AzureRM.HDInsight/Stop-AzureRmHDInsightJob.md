---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/stop-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
ms.openlocfilehash: 7247a4f5e23bc4f0f3c520f909cec221ee03e1ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513836"
---
# <span data-ttu-id="84b29-101">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="84b29-101">Stop-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="84b29-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84b29-102">SYNOPSIS</span></span>
<span data-ttu-id="84b29-103">Interrompe un processo in uso specificato in un cluster.</span><span class="sxs-lookup"><span data-stu-id="84b29-103">Stops a specified running job on a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84b29-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84b29-104">SYNTAX</span></span>

```
Stop-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84b29-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84b29-105">DESCRIPTION</span></span>
<span data-ttu-id="84b29-106">Il cmdlet **Stop-AzureRmHDInsightJob** interrompe un processo in uso specificato in un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="84b29-106">The **Stop-AzureRmHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="84b29-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84b29-107">EXAMPLES</span></span>

### <span data-ttu-id="84b29-108">Esempio 1: arrestare un processo nel cluster specificato</span><span class="sxs-lookup"><span data-stu-id="84b29-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="84b29-109">Questo comando Arresta un processo nel cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="84b29-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="84b29-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84b29-110">PARAMETERS</span></span>

### <span data-ttu-id="84b29-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="84b29-111">-ClusterName</span></span>
<span data-ttu-id="84b29-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="84b29-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="84b29-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84b29-113">-DefaultProfile</span></span>
<span data-ttu-id="84b29-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="84b29-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84b29-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="84b29-115">-HttpCredential</span></span>
<span data-ttu-id="84b29-116">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="84b29-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="84b29-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="84b29-117">-JobId</span></span>
<span data-ttu-id="84b29-118">Specifica l'ID processo del processo.</span><span class="sxs-lookup"><span data-stu-id="84b29-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="84b29-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84b29-119">-ResourceGroupName</span></span>
<span data-ttu-id="84b29-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="84b29-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="84b29-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b29-121">CommonParameters</span></span>
<span data-ttu-id="84b29-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84b29-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b29-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84b29-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b29-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84b29-124">INPUTS</span></span>

### <span data-ttu-id="84b29-125">System. String</span><span class="sxs-lookup"><span data-stu-id="84b29-125">System.String</span></span>
<span data-ttu-id="84b29-126">Parametri: JobId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="84b29-126">Parameters: JobId (ByValue)</span></span>

## <span data-ttu-id="84b29-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84b29-127">OUTPUTS</span></span>

### <span data-ttu-id="84b29-128">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="84b29-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="84b29-129">Note</span><span class="sxs-lookup"><span data-stu-id="84b29-129">NOTES</span></span>

## <span data-ttu-id="84b29-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84b29-130">RELATED LINKS</span></span>

[<span data-ttu-id="84b29-131">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="84b29-131">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="84b29-132">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="84b29-132">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="84b29-133">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="84b29-133">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


