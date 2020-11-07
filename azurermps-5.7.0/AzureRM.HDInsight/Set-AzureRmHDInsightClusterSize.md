---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
ms.openlocfilehash: eda9032cde317f418132e28917f7543d60ea0bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686741"
---
# <span data-ttu-id="d1443-101">Set-AzureRmHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="d1443-101">Set-AzureRmHDInsightClusterSize</span></span>

## <span data-ttu-id="d1443-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1443-102">SYNOPSIS</span></span>
<span data-ttu-id="d1443-103">Imposta il numero di nodi di lavoro in un cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="d1443-103">Sets the number of Worker nodes in a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1443-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1443-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1443-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1443-105">DESCRIPTION</span></span>
<span data-ttu-id="d1443-106">Il cmdlet **set-AzureRmHDInsightClusterSize** imposta il numero di nodi di lavoro in un cluster di Azure HDInsight specificato.</span><span class="sxs-lookup"><span data-stu-id="d1443-106">The **Set-AzureRmHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="d1443-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1443-107">EXAMPLES</span></span>

### <span data-ttu-id="d1443-108">Esempio 1: impostare le dimensioni di un cluster specificato</span><span class="sxs-lookup"><span data-stu-id="d1443-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzureRmHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="d1443-109">Questo comando imposta le dimensioni del cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="d1443-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="d1443-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1443-110">PARAMETERS</span></span>

### <span data-ttu-id="d1443-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="d1443-111">-ClusterName</span></span>
<span data-ttu-id="d1443-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="d1443-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="d1443-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1443-113">-DefaultProfile</span></span>
<span data-ttu-id="d1443-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d1443-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1443-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1443-115">-ResourceGroupName</span></span>
<span data-ttu-id="d1443-116">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d1443-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d1443-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="d1443-117">-TargetInstanceCount</span></span>
<span data-ttu-id="d1443-118">Specifica il numero desiderato di nodi di lavoro nel cluster.</span><span class="sxs-lookup"><span data-stu-id="d1443-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1443-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1443-119">CommonParameters</span></span>
<span data-ttu-id="d1443-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1443-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1443-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1443-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1443-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1443-122">INPUTS</span></span>

### <span data-ttu-id="d1443-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d1443-123">None</span></span>
<span data-ttu-id="d1443-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d1443-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d1443-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1443-125">OUTPUTS</span></span>

### <span data-ttu-id="d1443-126">Microsoft. Azure. Management. HDInsight. Models. cluster</span><span class="sxs-lookup"><span data-stu-id="d1443-126">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="d1443-127">Note</span><span class="sxs-lookup"><span data-stu-id="d1443-127">NOTES</span></span>

## <span data-ttu-id="d1443-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1443-128">RELATED LINKS</span></span>

