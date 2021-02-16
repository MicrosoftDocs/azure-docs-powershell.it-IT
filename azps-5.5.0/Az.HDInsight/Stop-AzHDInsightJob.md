---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/stop-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
ms.openlocfilehash: bff9b9d44d8afcbc315293dc07be3592172f1a4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185863"
---
# <span data-ttu-id="677ce-101">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="677ce-101">Stop-AzHDInsightJob</span></span>

## <span data-ttu-id="677ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="677ce-102">SYNOPSIS</span></span>
<span data-ttu-id="677ce-103">Interrompe un processo in esecuzione specificato in un cluster.</span><span class="sxs-lookup"><span data-stu-id="677ce-103">Stops a specified running job on a cluster.</span></span>

## <span data-ttu-id="677ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="677ce-104">SYNTAX</span></span>

```
Stop-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="677ce-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="677ce-105">DESCRIPTION</span></span>
<span data-ttu-id="677ce-106">Il cmdlet **Stop-AzHDInsightJob** interrompe un processo specificato in esecuzione in un cluster Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="677ce-106">The **Stop-AzHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="677ce-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="677ce-107">EXAMPLES</span></span>

### <span data-ttu-id="677ce-108">Esempio 1: Arrestare un processo nel cluster specificato</span><span class="sxs-lookup"><span data-stu-id="677ce-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="677ce-109">Questo comando interrompe un processo nel cluster denominato your-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="677ce-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="677ce-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="677ce-110">PARAMETERS</span></span>

### <span data-ttu-id="677ce-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="677ce-111">-ClusterName</span></span>
<span data-ttu-id="677ce-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="677ce-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="677ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="677ce-113">-DefaultProfile</span></span>
<span data-ttu-id="677ce-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="677ce-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="677ce-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="677ce-115">-HttpCredential</span></span>
<span data-ttu-id="677ce-116">Specifica le credenziali di accesso del cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="677ce-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="677ce-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="677ce-117">-JobId</span></span>
<span data-ttu-id="677ce-118">Specifica l'ID processo del processo.</span><span class="sxs-lookup"><span data-stu-id="677ce-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="677ce-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="677ce-119">-ResourceGroupName</span></span>
<span data-ttu-id="677ce-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="677ce-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="677ce-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="677ce-121">CommonParameters</span></span>
<span data-ttu-id="677ce-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="677ce-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="677ce-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="677ce-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="677ce-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="677ce-124">INPUTS</span></span>

### <span data-ttu-id="677ce-125">System.String</span><span class="sxs-lookup"><span data-stu-id="677ce-125">System.String</span></span>

## <span data-ttu-id="677ce-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="677ce-126">OUTPUTS</span></span>

### <span data-ttu-id="677ce-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="677ce-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="677ce-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="677ce-128">NOTES</span></span>

## <span data-ttu-id="677ce-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="677ce-129">RELATED LINKS</span></span>

[<span data-ttu-id="677ce-130">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="677ce-130">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="677ce-131">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="677ce-131">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="677ce-132">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="677ce-132">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


