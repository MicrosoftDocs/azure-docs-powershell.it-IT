---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
ms.openlocfilehash: 8273ad77091d008bead41e568f6c9d2de0e0d6f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983118"
---
# <span data-ttu-id="56613-101">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="56613-101">Get-AzHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="56613-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56613-102">SYNOPSIS</span></span>
<span data-ttu-id="56613-103">Recupera la cronologia delle azioni dello script per un cluster e la elenca in ordine cronologico inverso oppure recupera i dettagli di un'azione di script eseguita in precedenza.</span><span class="sxs-lookup"><span data-stu-id="56613-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="56613-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56613-104">SYNTAX</span></span>

```
Get-AzHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56613-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="56613-105">DESCRIPTION</span></span>
<span data-ttu-id="56613-106">Il cmdlet **Get-AzHDInsightScriptActionHistory** ottiene la cronologia delle azioni dello script per un cluster Azure HDInsight ed elenca i dati in ordine cronologico inverso oppure recupera i dettagli di un'azione script eseguita in precedenza.</span><span class="sxs-lookup"><span data-stu-id="56613-106">The **Get-AzHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="56613-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56613-107">EXAMPLES</span></span>

### <span data-ttu-id="56613-108">Esempio 1: Ottenere la cronologia delle esecuzioni delle azioni degli script per un cluster</span><span class="sxs-lookup"><span data-stu-id="56613-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="56613-109">Questo comando recupera la cronologia delle azioni degli script per il cluster your-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="56613-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="56613-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56613-110">PARAMETERS</span></span>

### <span data-ttu-id="56613-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="56613-111">-ClusterName</span></span>
<span data-ttu-id="56613-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="56613-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="56613-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56613-113">-DefaultProfile</span></span>
<span data-ttu-id="56613-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="56613-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56613-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56613-115">-ResourceGroupName</span></span>
<span data-ttu-id="56613-116">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="56613-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="56613-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="56613-117">-ScriptExecutionId</span></span>
<span data-ttu-id="56613-118">Specifica l'ID di esecuzione dell'azione di script eseguita.</span><span class="sxs-lookup"><span data-stu-id="56613-118">Specifies the execution ID of the executed script action.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56613-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56613-119">CommonParameters</span></span>
<span data-ttu-id="56613-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56613-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56613-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="56613-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56613-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="56613-122">INPUTS</span></span>

### <span data-ttu-id="56613-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="56613-123">None</span></span>

## <span data-ttu-id="56613-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56613-124">OUTPUTS</span></span>

### <span data-ttu-id="56613-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span><span class="sxs-lookup"><span data-stu-id="56613-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span></span>

## <span data-ttu-id="56613-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="56613-126">NOTES</span></span>

## <span data-ttu-id="56613-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56613-127">RELATED LINKS</span></span>
