---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/remove-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
ms.openlocfilehash: 1029871a2125668c732f7ff541582f06dbd790c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686517"
---
# <span data-ttu-id="a7f8c-101">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a7f8c-101">Remove-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="a7f8c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7f8c-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f8c-103">Rimuove il cluster HDInsight specificato dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="a7f8c-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7f8c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7f8c-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7f8c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7f8c-105">DESCRIPTION</span></span>
<span data-ttu-id="a7f8c-106">Il cmdlet **Remove-AzureRmHDInsightCluster** rimuove il cluster di servizi HDInsight specificato da un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a7f8c-106">The **Remove-AzureRmHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="a7f8c-107">Questa operazione elimina anche tutti i dati archiviati nel file System distribuito Hadoop (HDFS) nel cluster.</span><span class="sxs-lookup"><span data-stu-id="a7f8c-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="a7f8c-108">I dati archiviati nell'account di archiviazione di Azure associato non vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="a7f8c-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="a7f8c-109">I dati archiviati in Metastore esterni non vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="a7f8c-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="a7f8c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7f8c-110">EXAMPLES</span></span>

### <span data-ttu-id="a7f8c-111">Esempio 1: eliminare un cluster di Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="a7f8c-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="a7f8c-112">Questo comando rimuove il cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="a7f8c-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="a7f8c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7f8c-113">PARAMETERS</span></span>

### <span data-ttu-id="a7f8c-114">-Clustername</span><span class="sxs-lookup"><span data-stu-id="a7f8c-114">-ClusterName</span></span>
<span data-ttu-id="a7f8c-115">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="a7f8c-115">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f8c-116">-DefaultProfile</span></span>
<span data-ttu-id="a7f8c-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a7f8c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f8c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f8c-118">-ResourceGroupName</span></span>
<span data-ttu-id="a7f8c-119">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a7f8c-119">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f8c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f8c-120">CommonParameters</span></span>
<span data-ttu-id="a7f8c-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7f8c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f8c-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7f8c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f8c-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7f8c-123">INPUTS</span></span>

### <span data-ttu-id="a7f8c-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a7f8c-124">None</span></span>
<span data-ttu-id="a7f8c-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a7f8c-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a7f8c-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7f8c-126">OUTPUTS</span></span>

### <span data-ttu-id="a7f8c-127">Microsoft. Azure. Management. HDInsight. Models. ClusterGetResponse</span><span class="sxs-lookup"><span data-stu-id="a7f8c-127">Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse</span></span>

## <span data-ttu-id="a7f8c-128">Note</span><span class="sxs-lookup"><span data-stu-id="a7f8c-128">NOTES</span></span>

## <span data-ttu-id="a7f8c-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7f8c-129">RELATED LINKS</span></span>

[<span data-ttu-id="a7f8c-130">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a7f8c-130">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="a7f8c-131">Usare-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a7f8c-131">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)

