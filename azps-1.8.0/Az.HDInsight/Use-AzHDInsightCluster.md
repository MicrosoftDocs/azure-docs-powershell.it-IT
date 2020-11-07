---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: 7e9df747becd5e2bd49b865b61f963d1db585e17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835952"
---
# <span data-ttu-id="1bf47-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="1bf47-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="1bf47-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1bf47-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf47-103">Seleziona un cluster da usare con il cmdlet Invoke-RmAzureHDInsightHiveJob.</span><span class="sxs-lookup"><span data-stu-id="1bf47-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="1bf47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1bf47-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bf47-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1bf47-105">DESCRIPTION</span></span>
<span data-ttu-id="1bf47-106">Il cmdlet **use-AzHDInsightCluster** seleziona il cluster Azure HDInsight per il cmdlet Invoke-AzHDInsightHiveJob da usare per inviare processi hive.</span><span class="sxs-lookup"><span data-stu-id="1bf47-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="1bf47-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1bf47-107">EXAMPLES</span></span>

### <span data-ttu-id="1bf47-108">Esempio 1: selezionare un cluster per l'invio di query hive</span><span class="sxs-lookup"><span data-stu-id="1bf47-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="1bf47-109">Questo comando consente di selezionare un cluster per un invio di query hive.</span><span class="sxs-lookup"><span data-stu-id="1bf47-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="1bf47-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1bf47-110">PARAMETERS</span></span>

### <span data-ttu-id="1bf47-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="1bf47-111">-ClusterName</span></span>
<span data-ttu-id="1bf47-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="1bf47-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="1bf47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf47-113">-DefaultProfile</span></span>
<span data-ttu-id="1bf47-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1bf47-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1bf47-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="1bf47-115">-HttpCredential</span></span>
<span data-ttu-id="1bf47-116">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="1bf47-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="1bf47-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bf47-117">-ResourceGroupName</span></span>
<span data-ttu-id="1bf47-118">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1bf47-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1bf47-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf47-119">CommonParameters</span></span>
<span data-ttu-id="1bf47-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bf47-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf47-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bf47-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf47-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1bf47-122">INPUTS</span></span>

### <span data-ttu-id="1bf47-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1bf47-123">None</span></span>

## <span data-ttu-id="1bf47-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1bf47-124">OUTPUTS</span></span>

### <span data-ttu-id="1bf47-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1bf47-125">System.String</span></span>

## <span data-ttu-id="1bf47-126">Note</span><span class="sxs-lookup"><span data-stu-id="1bf47-126">NOTES</span></span>

## <span data-ttu-id="1bf47-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1bf47-127">RELATED LINKS</span></span>

[<span data-ttu-id="1bf47-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="1bf47-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="1bf47-129">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="1bf47-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)


