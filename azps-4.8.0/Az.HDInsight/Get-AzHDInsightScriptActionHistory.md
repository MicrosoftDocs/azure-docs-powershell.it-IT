---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
ms.openlocfilehash: 4f73c58ee709e53e1337c161b698aa31cc38ca43
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031202"
---
# <span data-ttu-id="d1c25-101">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="d1c25-101">Get-AzHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="d1c25-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1c25-102">SYNOPSIS</span></span>
<span data-ttu-id="d1c25-103">Ottiene la cronologia delle azioni di script per un cluster e la elenca in ordine cronologico inverso o ottiene i dettagli di un'azione di script eseguita in precedenza.</span><span class="sxs-lookup"><span data-stu-id="d1c25-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="d1c25-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1c25-104">SYNTAX</span></span>

```
Get-AzHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1c25-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1c25-105">DESCRIPTION</span></span>
<span data-ttu-id="d1c25-106">Il cmdlet **Get-AzHDInsightScriptActionHistory** ottiene la cronologia delle azioni di script per un cluster HDInsight di Azure e la elenca in ordine cronologico inverso o ottiene i dettagli di un'azione di script eseguita in precedenza.</span><span class="sxs-lookup"><span data-stu-id="d1c25-106">The **Get-AzHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="d1c25-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1c25-107">EXAMPLES</span></span>

### <span data-ttu-id="d1c25-108">Esempio 1: ottenere la cronologia delle esecuzioni di azioni di script per un cluster</span><span class="sxs-lookup"><span data-stu-id="d1c25-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="d1c25-109">Questo comando consente di ottenere la cronologia delle azioni di script per il cluster ur-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="d1c25-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="d1c25-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1c25-110">PARAMETERS</span></span>

### <span data-ttu-id="d1c25-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="d1c25-111">-ClusterName</span></span>
<span data-ttu-id="d1c25-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="d1c25-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="d1c25-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1c25-113">-DefaultProfile</span></span>
<span data-ttu-id="d1c25-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d1c25-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1c25-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1c25-115">-ResourceGroupName</span></span>
<span data-ttu-id="d1c25-116">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d1c25-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d1c25-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="d1c25-117">-ScriptExecutionId</span></span>
<span data-ttu-id="d1c25-118">Specifica l'ID di esecuzione dell'azione di script eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1c25-118">Specifies the execution ID of the executed script action.</span></span>

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

### <span data-ttu-id="d1c25-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1c25-119">CommonParameters</span></span>
<span data-ttu-id="d1c25-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1c25-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1c25-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1c25-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1c25-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1c25-122">INPUTS</span></span>

### <span data-ttu-id="d1c25-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d1c25-123">None</span></span>

## <span data-ttu-id="d1c25-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1c25-124">OUTPUTS</span></span>

### <span data-ttu-id="d1c25-125">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionDetail</span><span class="sxs-lookup"><span data-stu-id="d1c25-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span></span>

## <span data-ttu-id="d1c25-126">Note</span><span class="sxs-lookup"><span data-stu-id="d1c25-126">NOTES</span></span>

## <span data-ttu-id="d1c25-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1c25-127">RELATED LINKS</span></span>
