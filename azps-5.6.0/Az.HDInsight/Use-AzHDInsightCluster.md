---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: c9b95a1f16c90eb3c6e057707dbf63d431b9a1ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013550"
---
# <span data-ttu-id="c80b4-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c80b4-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="c80b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c80b4-102">SYNOPSIS</span></span>
<span data-ttu-id="c80b4-103">Seleziona un cluster da usare con il cmdlet Invoke-RmAzureHDInsightHiveJob cluster.</span><span class="sxs-lookup"><span data-stu-id="c80b4-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="c80b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c80b4-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c80b4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c80b4-105">DESCRIPTION</span></span>
<span data-ttu-id="c80b4-106">Il cmdlet **Use-AzHDInsightCluster** seleziona il cluster Azure HDInsight per il cmdlet Invoke-AzHDInsightHiveJob da usare per inviare i processi Hive.</span><span class="sxs-lookup"><span data-stu-id="c80b4-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="c80b4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c80b4-107">EXAMPLES</span></span>

### <span data-ttu-id="c80b4-108">Esempio 1: Selezionare un cluster per l'invio di query hive</span><span class="sxs-lookup"><span data-stu-id="c80b4-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="c80b4-109">Questo comando seleziona un cluster per l'invio di una query Hive.</span><span class="sxs-lookup"><span data-stu-id="c80b4-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="c80b4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c80b4-110">PARAMETERS</span></span>

### <span data-ttu-id="c80b4-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c80b4-111">-ClusterName</span></span>
<span data-ttu-id="c80b4-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="c80b4-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="c80b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c80b4-113">-DefaultProfile</span></span>
<span data-ttu-id="c80b4-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c80b4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c80b4-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="c80b4-115">-HttpCredential</span></span>
<span data-ttu-id="c80b4-116">Specifica le credenziali di accesso del cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="c80b4-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c80b4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c80b4-117">-ResourceGroupName</span></span>
<span data-ttu-id="c80b4-118">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c80b4-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c80b4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c80b4-119">CommonParameters</span></span>
<span data-ttu-id="c80b4-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c80b4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c80b4-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c80b4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c80b4-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="c80b4-122">INPUTS</span></span>

### <span data-ttu-id="c80b4-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c80b4-123">None</span></span>

## <span data-ttu-id="c80b4-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c80b4-124">OUTPUTS</span></span>

### <span data-ttu-id="c80b4-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c80b4-125">System.String</span></span>

## <span data-ttu-id="c80b4-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="c80b4-126">NOTES</span></span>

## <span data-ttu-id="c80b4-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c80b4-127">RELATED LINKS</span></span>

[<span data-ttu-id="c80b4-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c80b4-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="c80b4-129">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c80b4-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)


