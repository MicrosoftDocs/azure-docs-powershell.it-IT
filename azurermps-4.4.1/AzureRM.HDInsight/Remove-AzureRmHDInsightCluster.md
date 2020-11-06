---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
ms.openlocfilehash: a09da5122403d971d8b5d1abde79c8a9a95c3ecd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521242"
---
# <span data-ttu-id="da406-101">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="da406-101">Remove-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="da406-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="da406-102">SYNOPSIS</span></span>
<span data-ttu-id="da406-103">Rimuove il cluster HDInsight specificato dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="da406-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da406-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da406-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da406-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da406-105">DESCRIPTION</span></span>
<span data-ttu-id="da406-106">Il cmdlet **Remove-AzureRmHDInsightCluster** rimuove il cluster di servizi HDInsight specificato da un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="da406-106">The **Remove-AzureRmHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="da406-107">Questa operazione elimina anche tutti i dati archiviati nel file System distribuito Hadoop (HDFS) nel cluster.</span><span class="sxs-lookup"><span data-stu-id="da406-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="da406-108">I dati archiviati nell'account di archiviazione di Azure associato non vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="da406-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="da406-109">I dati archiviati in Metastore esterni non vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="da406-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="da406-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da406-110">EXAMPLES</span></span>

### <span data-ttu-id="da406-111">Esempio 1: eliminare un cluster di Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="da406-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="da406-112">Questo comando rimuove il cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="da406-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="da406-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="da406-113">PARAMETERS</span></span>

### <span data-ttu-id="da406-114">-Clustername</span><span class="sxs-lookup"><span data-stu-id="da406-114">-ClusterName</span></span>
<span data-ttu-id="da406-115">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="da406-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="da406-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da406-116">-ResourceGroupName</span></span>
<span data-ttu-id="da406-117">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="da406-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="da406-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da406-118">-DefaultProfile</span></span>
<span data-ttu-id="da406-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da406-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da406-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da406-120">CommonParameters</span></span>
<span data-ttu-id="da406-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da406-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da406-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da406-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da406-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="da406-123">INPUTS</span></span>

## <span data-ttu-id="da406-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da406-124">OUTPUTS</span></span>

### <span data-ttu-id="da406-125">Microsoft. Azure. Management. HDInsight. Models. ClusterGetResponse</span><span class="sxs-lookup"><span data-stu-id="da406-125">Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse</span></span>

## <span data-ttu-id="da406-126">Note</span><span class="sxs-lookup"><span data-stu-id="da406-126">NOTES</span></span>

## <span data-ttu-id="da406-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da406-127">RELATED LINKS</span></span>

[<span data-ttu-id="da406-128">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="da406-128">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="da406-129">Usare-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="da406-129">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


