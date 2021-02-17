---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: 289f7b4bf397384b1420af02a5517e57bf51675d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188358"
---
# <span data-ttu-id="63948-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="63948-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="63948-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63948-102">SYNOPSIS</span></span>
<span data-ttu-id="63948-103">Ottiene ed elenca tutti i cluster Azure HDInsight associati alla sottoscrizione corrente o a un gruppo di risorse specificato oppure recupera uno specifico cluster.</span><span class="sxs-lookup"><span data-stu-id="63948-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="63948-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63948-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63948-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="63948-105">DESCRIPTION</span></span>
<span data-ttu-id="63948-106">Il cmdlet **Get-AzHDInsightCluster** elenca i cluster di servizi Azure HDInsight per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="63948-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="63948-107">Usare il *parametro ClusterName* per ottenere i dettagli per un cluster specifico.</span><span class="sxs-lookup"><span data-stu-id="63948-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="63948-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63948-108">EXAMPLES</span></span>

### <span data-ttu-id="63948-109">Esempio 1: Elencare tutti i cluster Di Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="63948-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="63948-110">Questo comando elenca tutti i cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="63948-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="63948-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63948-111">PARAMETERS</span></span>

### <span data-ttu-id="63948-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="63948-112">-ClusterName</span></span>
<span data-ttu-id="63948-113">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="63948-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="63948-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63948-114">-DefaultProfile</span></span>
<span data-ttu-id="63948-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="63948-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63948-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63948-116">-ResourceGroupName</span></span>
<span data-ttu-id="63948-117">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="63948-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="63948-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63948-118">CommonParameters</span></span>
<span data-ttu-id="63948-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63948-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63948-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="63948-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63948-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="63948-121">INPUTS</span></span>

### <span data-ttu-id="63948-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="63948-122">None</span></span>

## <span data-ttu-id="63948-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63948-123">OUTPUTS</span></span>

### <span data-ttu-id="63948-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="63948-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="63948-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="63948-125">NOTES</span></span>

## <span data-ttu-id="63948-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63948-126">RELATED LINKS</span></span>

[<span data-ttu-id="63948-127">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="63948-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="63948-128">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="63948-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


