---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: 7dae5bd29877097b7d0df60feff8bf44977e61f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207315"
---
# <span data-ttu-id="2137c-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="2137c-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="2137c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2137c-102">SYNOPSIS</span></span>
<span data-ttu-id="2137c-103">Imposta il numero di nodi di lavoro in un cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="2137c-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="2137c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2137c-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2137c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2137c-105">DESCRIPTION</span></span>
<span data-ttu-id="2137c-106">Il cmdlet **Set-AzHDInsightClusterSize** imposta il numero di nodi worker in un cluster HDInsight di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="2137c-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="2137c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2137c-107">EXAMPLES</span></span>

### <span data-ttu-id="2137c-108">Esempio 1: Impostare le dimensioni di un cluster specificato</span><span class="sxs-lookup"><span data-stu-id="2137c-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="2137c-109">Questo comando imposta le dimensioni del cluster denominato your-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="2137c-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="2137c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2137c-110">PARAMETERS</span></span>

### <span data-ttu-id="2137c-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2137c-111">-ClusterName</span></span>
<span data-ttu-id="2137c-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="2137c-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2137c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2137c-113">-DefaultProfile</span></span>
<span data-ttu-id="2137c-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="2137c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2137c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2137c-115">-ResourceGroupName</span></span>
<span data-ttu-id="2137c-116">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2137c-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2137c-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="2137c-117">-TargetInstanceCount</span></span>
<span data-ttu-id="2137c-118">Specifica il numero desiderato di nodi di lavoro nel cluster.</span><span class="sxs-lookup"><span data-stu-id="2137c-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

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

### <span data-ttu-id="2137c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2137c-119">CommonParameters</span></span>
<span data-ttu-id="2137c-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2137c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2137c-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2137c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2137c-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="2137c-122">INPUTS</span></span>

### <span data-ttu-id="2137c-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2137c-123">None</span></span>

## <span data-ttu-id="2137c-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2137c-124">OUTPUTS</span></span>

### <span data-ttu-id="2137c-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span><span class="sxs-lookup"><span data-stu-id="2137c-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="2137c-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="2137c-126">NOTES</span></span>

## <span data-ttu-id="2137c-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2137c-127">RELATED LINKS</span></span>
