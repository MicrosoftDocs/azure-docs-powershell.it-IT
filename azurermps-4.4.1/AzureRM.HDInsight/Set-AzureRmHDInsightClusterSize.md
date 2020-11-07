---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
ms.openlocfilehash: 180cf2082b17e16fe5efcf1ee3009256b7c4703c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688022"
---
# <span data-ttu-id="b2bcd-101">Set-AzureRmHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="b2bcd-101">Set-AzureRmHDInsightClusterSize</span></span>

## <span data-ttu-id="b2bcd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2bcd-102">SYNOPSIS</span></span>
<span data-ttu-id="b2bcd-103">Imposta il numero di nodi di lavoro in un cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="b2bcd-103">Sets the number of Worker nodes in a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2bcd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2bcd-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2bcd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2bcd-105">DESCRIPTION</span></span>
<span data-ttu-id="b2bcd-106">Il cmdlet **set-AzureRmHDInsightClusterSize** imposta il numero di nodi di lavoro in un cluster di Azure HDInsight specificato.</span><span class="sxs-lookup"><span data-stu-id="b2bcd-106">The **Set-AzureRmHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b2bcd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2bcd-107">EXAMPLES</span></span>

### <span data-ttu-id="b2bcd-108">Esempio 1: impostare le dimensioni di un cluster specificato</span><span class="sxs-lookup"><span data-stu-id="b2bcd-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzureRmHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="b2bcd-109">Questo comando imposta le dimensioni del cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="b2bcd-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="b2bcd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2bcd-110">PARAMETERS</span></span>

### <span data-ttu-id="b2bcd-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="b2bcd-111">-ClusterName</span></span>
<span data-ttu-id="b2bcd-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="b2bcd-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="b2bcd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2bcd-113">-ResourceGroupName</span></span>
<span data-ttu-id="b2bcd-114">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b2bcd-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b2bcd-115">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="b2bcd-115">-TargetInstanceCount</span></span>
<span data-ttu-id="b2bcd-116">Specifica il numero desiderato di nodi di lavoro nel cluster.</span><span class="sxs-lookup"><span data-stu-id="b2bcd-116">Specifies the desired number of Worker nodes in the cluster.</span></span>

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

### <span data-ttu-id="b2bcd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2bcd-117">-DefaultProfile</span></span>
<span data-ttu-id="b2bcd-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2bcd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2bcd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2bcd-119">CommonParameters</span></span>
<span data-ttu-id="b2bcd-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2bcd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2bcd-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2bcd-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2bcd-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2bcd-122">INPUTS</span></span>

## <span data-ttu-id="b2bcd-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2bcd-123">OUTPUTS</span></span>

### <span data-ttu-id="b2bcd-124">Microsoft. Azure. Management. HDInsight. Models. cluster</span><span class="sxs-lookup"><span data-stu-id="b2bcd-124">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="b2bcd-125">Note</span><span class="sxs-lookup"><span data-stu-id="b2bcd-125">NOTES</span></span>

## <span data-ttu-id="b2bcd-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2bcd-126">RELATED LINKS</span></span>

