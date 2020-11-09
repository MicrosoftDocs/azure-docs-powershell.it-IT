---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/stop-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
ms.openlocfilehash: d5e38cf3edb89801b630735dee1ce0dbd1d62d41
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296287"
---
# <span data-ttu-id="2dddf-101">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2dddf-101">Stop-AzHDInsightJob</span></span>

## <span data-ttu-id="2dddf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2dddf-102">SYNOPSIS</span></span>
<span data-ttu-id="2dddf-103">Interrompe un processo in uso specificato in un cluster.</span><span class="sxs-lookup"><span data-stu-id="2dddf-103">Stops a specified running job on a cluster.</span></span>

## <span data-ttu-id="2dddf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2dddf-104">SYNTAX</span></span>

```
Stop-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dddf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2dddf-105">DESCRIPTION</span></span>
<span data-ttu-id="2dddf-106">Il cmdlet **Stop-AzHDInsightJob** interrompe un processo in uso specificato in un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2dddf-106">The **Stop-AzHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="2dddf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2dddf-107">EXAMPLES</span></span>

### <span data-ttu-id="2dddf-108">Esempio 1: arrestare un processo nel cluster specificato</span><span class="sxs-lookup"><span data-stu-id="2dddf-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="2dddf-109">Questo comando Arresta un processo nel cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="2dddf-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="2dddf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2dddf-110">PARAMETERS</span></span>

### <span data-ttu-id="2dddf-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="2dddf-111">-ClusterName</span></span>
<span data-ttu-id="2dddf-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="2dddf-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2dddf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dddf-113">-DefaultProfile</span></span>
<span data-ttu-id="2dddf-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2dddf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2dddf-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="2dddf-115">-HttpCredential</span></span>
<span data-ttu-id="2dddf-116">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="2dddf-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="2dddf-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="2dddf-117">-JobId</span></span>
<span data-ttu-id="2dddf-118">Specifica l'ID processo del processo.</span><span class="sxs-lookup"><span data-stu-id="2dddf-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="2dddf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dddf-119">-ResourceGroupName</span></span>
<span data-ttu-id="2dddf-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2dddf-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2dddf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dddf-121">CommonParameters</span></span>
<span data-ttu-id="2dddf-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dddf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dddf-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dddf-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dddf-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2dddf-124">INPUTS</span></span>

### <span data-ttu-id="2dddf-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2dddf-125">System.String</span></span>

## <span data-ttu-id="2dddf-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2dddf-126">OUTPUTS</span></span>

### <span data-ttu-id="2dddf-127">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2dddf-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="2dddf-128">Note</span><span class="sxs-lookup"><span data-stu-id="2dddf-128">NOTES</span></span>

## <span data-ttu-id="2dddf-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2dddf-129">RELATED LINKS</span></span>

[<span data-ttu-id="2dddf-130">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2dddf-130">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="2dddf-131">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2dddf-131">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="2dddf-132">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2dddf-132">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


