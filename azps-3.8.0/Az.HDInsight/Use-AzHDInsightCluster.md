---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: 15d93d6dbdc7b231d47d5372864883f915e66ae9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864900"
---
# <span data-ttu-id="0f128-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0f128-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="0f128-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f128-102">SYNOPSIS</span></span>
<span data-ttu-id="0f128-103">Seleziona un cluster da usare con il cmdlet Invoke-RmAzureHDInsightHiveJob.</span><span class="sxs-lookup"><span data-stu-id="0f128-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="0f128-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f128-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f128-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f128-105">DESCRIPTION</span></span>
<span data-ttu-id="0f128-106">Il cmdlet **use-AzHDInsightCluster** seleziona il cluster Azure HDInsight per il cmdlet Invoke-AzHDInsightHiveJob da usare per inviare processi hive.</span><span class="sxs-lookup"><span data-stu-id="0f128-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="0f128-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f128-107">EXAMPLES</span></span>

### <span data-ttu-id="0f128-108">Esempio 1: selezionare un cluster per l'invio di query hive</span><span class="sxs-lookup"><span data-stu-id="0f128-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="0f128-109">Questo comando consente di selezionare un cluster per un invio di query hive.</span><span class="sxs-lookup"><span data-stu-id="0f128-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="0f128-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f128-110">PARAMETERS</span></span>

### <span data-ttu-id="0f128-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="0f128-111">-ClusterName</span></span>
<span data-ttu-id="0f128-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="0f128-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="0f128-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f128-113">-DefaultProfile</span></span>
<span data-ttu-id="0f128-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0f128-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f128-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="0f128-115">-HttpCredential</span></span>
<span data-ttu-id="0f128-116">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="0f128-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="0f128-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f128-117">-ResourceGroupName</span></span>
<span data-ttu-id="0f128-118">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0f128-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0f128-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f128-119">CommonParameters</span></span>
<span data-ttu-id="0f128-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f128-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f128-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f128-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f128-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f128-122">INPUTS</span></span>

### <span data-ttu-id="0f128-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0f128-123">None</span></span>

## <span data-ttu-id="0f128-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f128-124">OUTPUTS</span></span>

### <span data-ttu-id="0f128-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0f128-125">System.String</span></span>

## <span data-ttu-id="0f128-126">Note</span><span class="sxs-lookup"><span data-stu-id="0f128-126">NOTES</span></span>

## <span data-ttu-id="0f128-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f128-127">RELATED LINKS</span></span>

[<span data-ttu-id="0f128-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0f128-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="0f128-129">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0f128-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)


