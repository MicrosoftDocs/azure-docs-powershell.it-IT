---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: c89293ee071aba3fcec2d58d071714193cc44a0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010478"
---
# <span data-ttu-id="d83f4-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d83f4-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="d83f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d83f4-102">SYNOPSIS</span></span>
<span data-ttu-id="d83f4-103">Ottiene ed elenca tutti i cluster Azure HDInsight associati alla sottoscrizione corrente o a un gruppo di risorse specificato oppure recupera uno specifico cluster.</span><span class="sxs-lookup"><span data-stu-id="d83f4-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="d83f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d83f4-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d83f4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d83f4-105">DESCRIPTION</span></span>
<span data-ttu-id="d83f4-106">Il cmdlet **Get-AzHDInsightCluster** elenca i cluster di servizi Azure HDInsight per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="d83f4-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="d83f4-107">Usare il *parametro ClusterName* per ottenere i dettagli per un cluster specifico.</span><span class="sxs-lookup"><span data-stu-id="d83f4-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="d83f4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d83f4-108">EXAMPLES</span></span>

### <span data-ttu-id="d83f4-109">Esempio 1: Elencare tutti i cluster Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="d83f4-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="d83f4-110">Questo comando elenca tutti i cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d83f4-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="d83f4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d83f4-111">PARAMETERS</span></span>

### <span data-ttu-id="d83f4-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d83f4-112">-ClusterName</span></span>
<span data-ttu-id="d83f4-113">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="d83f4-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d83f4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d83f4-114">-DefaultProfile</span></span>
<span data-ttu-id="d83f4-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d83f4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d83f4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d83f4-116">-ResourceGroupName</span></span>
<span data-ttu-id="d83f4-117">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d83f4-117">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d83f4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d83f4-118">CommonParameters</span></span>
<span data-ttu-id="d83f4-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d83f4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d83f4-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d83f4-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d83f4-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="d83f4-121">INPUTS</span></span>

### <span data-ttu-id="d83f4-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d83f4-122">None</span></span>

## <span data-ttu-id="d83f4-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d83f4-123">OUTPUTS</span></span>

### <span data-ttu-id="d83f4-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d83f4-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="d83f4-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="d83f4-125">NOTES</span></span>

## <span data-ttu-id="d83f4-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d83f4-126">RELATED LINKS</span></span>

[<span data-ttu-id="d83f4-127">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d83f4-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="d83f4-128">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d83f4-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


