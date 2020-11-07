---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/use-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
ms.openlocfilehash: a129f882779d3c855efbc0ae83c3d1da9a7e002d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687867"
---
# <span data-ttu-id="eff4f-101">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="eff4f-101">Use-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="eff4f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eff4f-102">SYNOPSIS</span></span>
<span data-ttu-id="eff4f-103">Seleziona un cluster da usare con il cmdlet Invoke-RmAzureHDInsightHiveJob.</span><span class="sxs-lookup"><span data-stu-id="eff4f-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eff4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eff4f-104">SYNTAX</span></span>

```
Use-AzureRmHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eff4f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eff4f-105">DESCRIPTION</span></span>
<span data-ttu-id="eff4f-106">Il cmdlet **use-AzureRmHDInsightCluster** seleziona il cluster Azure HDInsight per il cmdlet Invoke-AzureRmHDInsightHiveJob da usare per inviare processi hive.</span><span class="sxs-lookup"><span data-stu-id="eff4f-106">The **Use-AzureRmHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzureRmHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="eff4f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eff4f-107">EXAMPLES</span></span>

### <span data-ttu-id="eff4f-108">Esempio 1: selezionare un cluster per l'invio di query hive</span><span class="sxs-lookup"><span data-stu-id="eff4f-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzureRmHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="eff4f-109">Questo comando consente di selezionare un cluster per un invio di query hive.</span><span class="sxs-lookup"><span data-stu-id="eff4f-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="eff4f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eff4f-110">PARAMETERS</span></span>

### <span data-ttu-id="eff4f-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="eff4f-111">-ClusterName</span></span>
<span data-ttu-id="eff4f-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="eff4f-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="eff4f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eff4f-113">-DefaultProfile</span></span>
<span data-ttu-id="eff4f-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="eff4f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eff4f-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="eff4f-115">-HttpCredential</span></span>
<span data-ttu-id="eff4f-116">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="eff4f-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="eff4f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eff4f-117">-ResourceGroupName</span></span>
<span data-ttu-id="eff4f-118">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eff4f-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="eff4f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eff4f-119">CommonParameters</span></span>
<span data-ttu-id="eff4f-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eff4f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eff4f-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eff4f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eff4f-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eff4f-122">INPUTS</span></span>

### <span data-ttu-id="eff4f-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="eff4f-123">None</span></span>

## <span data-ttu-id="eff4f-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eff4f-124">OUTPUTS</span></span>

### <span data-ttu-id="eff4f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="eff4f-125">System.String</span></span>

## <span data-ttu-id="eff4f-126">Note</span><span class="sxs-lookup"><span data-stu-id="eff4f-126">NOTES</span></span>

## <span data-ttu-id="eff4f-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eff4f-127">RELATED LINKS</span></span>

[<span data-ttu-id="eff4f-128">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="eff4f-128">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="eff4f-129">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="eff4f-129">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)


