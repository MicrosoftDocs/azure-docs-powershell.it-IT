---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: 8f34e9233da61bb2381c99c33922fa4332b588fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296329"
---
# <span data-ttu-id="34b0b-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="34b0b-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="34b0b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34b0b-102">SYNOPSIS</span></span>
<span data-ttu-id="34b0b-103">Imposta il numero di nodi di lavoro in un cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="34b0b-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="34b0b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34b0b-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34b0b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34b0b-105">DESCRIPTION</span></span>
<span data-ttu-id="34b0b-106">Il cmdlet **set-AzHDInsightClusterSize** imposta il numero di nodi di lavoro in un cluster di Azure HDInsight specificato.</span><span class="sxs-lookup"><span data-stu-id="34b0b-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="34b0b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34b0b-107">EXAMPLES</span></span>

### <span data-ttu-id="34b0b-108">Esempio 1: impostare le dimensioni di un cluster specificato</span><span class="sxs-lookup"><span data-stu-id="34b0b-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="34b0b-109">Questo comando imposta le dimensioni del cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="34b0b-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="34b0b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34b0b-110">PARAMETERS</span></span>

### <span data-ttu-id="34b0b-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="34b0b-111">-ClusterName</span></span>
<span data-ttu-id="34b0b-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="34b0b-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="34b0b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34b0b-113">-DefaultProfile</span></span>
<span data-ttu-id="34b0b-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="34b0b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34b0b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34b0b-115">-ResourceGroupName</span></span>
<span data-ttu-id="34b0b-116">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="34b0b-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="34b0b-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="34b0b-117">-TargetInstanceCount</span></span>
<span data-ttu-id="34b0b-118">Specifica il numero desiderato di nodi di lavoro nel cluster.</span><span class="sxs-lookup"><span data-stu-id="34b0b-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34b0b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34b0b-119">CommonParameters</span></span>
<span data-ttu-id="34b0b-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34b0b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34b0b-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34b0b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34b0b-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34b0b-122">INPUTS</span></span>

### <span data-ttu-id="34b0b-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="34b0b-123">None</span></span>

## <span data-ttu-id="34b0b-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34b0b-124">OUTPUTS</span></span>

### <span data-ttu-id="34b0b-125">Microsoft. Azure. Management. HDInsight. Models. cluster</span><span class="sxs-lookup"><span data-stu-id="34b0b-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="34b0b-126">Note</span><span class="sxs-lookup"><span data-stu-id="34b0b-126">NOTES</span></span>

## <span data-ttu-id="34b0b-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34b0b-127">RELATED LINKS</span></span>
