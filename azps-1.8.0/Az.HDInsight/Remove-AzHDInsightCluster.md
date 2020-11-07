---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: e52d838f0aa7ce901b8099710b38f570d4285a4c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835991"
---
# <span data-ttu-id="ac51d-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ac51d-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="ac51d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac51d-102">SYNOPSIS</span></span>
<span data-ttu-id="ac51d-103">Rimuove il cluster HDInsight specificato dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="ac51d-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="ac51d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac51d-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac51d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac51d-105">DESCRIPTION</span></span>
<span data-ttu-id="ac51d-106">Il cmdlet **Remove-AzHDInsightCluster** rimuove il cluster di servizi HDInsight specificato da un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ac51d-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="ac51d-107">Questa operazione elimina anche tutti i dati archiviati nel file System distribuito Hadoop (HDFS) nel cluster.</span><span class="sxs-lookup"><span data-stu-id="ac51d-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="ac51d-108">I dati archiviati nell'account di archiviazione di Azure associato non vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="ac51d-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="ac51d-109">I dati archiviati in Metastore esterni non vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="ac51d-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="ac51d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac51d-110">EXAMPLES</span></span>

### <span data-ttu-id="ac51d-111">Esempio 1: eliminare un cluster di Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="ac51d-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="ac51d-112">Questo comando rimuove il cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="ac51d-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="ac51d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac51d-113">PARAMETERS</span></span>

### <span data-ttu-id="ac51d-114">-Clustername</span><span class="sxs-lookup"><span data-stu-id="ac51d-114">-ClusterName</span></span>
<span data-ttu-id="ac51d-115">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="ac51d-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="ac51d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac51d-116">-DefaultProfile</span></span>
<span data-ttu-id="ac51d-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ac51d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac51d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac51d-118">-ResourceGroupName</span></span>
<span data-ttu-id="ac51d-119">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ac51d-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ac51d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac51d-120">CommonParameters</span></span>
<span data-ttu-id="ac51d-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac51d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac51d-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac51d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac51d-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac51d-123">INPUTS</span></span>

### <span data-ttu-id="ac51d-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ac51d-124">None</span></span>

## <span data-ttu-id="ac51d-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac51d-125">OUTPUTS</span></span>

### <span data-ttu-id="ac51d-126">Microsoft. Azure. Management. HDInsight. Models. ClusterGetResponse</span><span class="sxs-lookup"><span data-stu-id="ac51d-126">Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse</span></span>

## <span data-ttu-id="ac51d-127">Note</span><span class="sxs-lookup"><span data-stu-id="ac51d-127">NOTES</span></span>

## <span data-ttu-id="ac51d-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac51d-128">RELATED LINKS</span></span>

[<span data-ttu-id="ac51d-129">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ac51d-129">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="ac51d-130">Usare-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ac51d-130">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


