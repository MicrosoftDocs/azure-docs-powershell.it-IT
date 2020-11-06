---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
ms.openlocfilehash: 5e3ee9de0adf511407013ef346a2867cb43fb11c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521656"
---
# <span data-ttu-id="0e51e-101">Get-AzureRmHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="0e51e-101">Get-AzureRmHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="0e51e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0e51e-102">SYNOPSIS</span></span>
<span data-ttu-id="0e51e-103">Ottiene la cronologia delle azioni di script per un cluster e la elenca in ordine cronologico inverso o ottiene i dettagli di un'azione di script eseguita in precedenza.</span><span class="sxs-lookup"><span data-stu-id="0e51e-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e51e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0e51e-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e51e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e51e-105">DESCRIPTION</span></span>
<span data-ttu-id="0e51e-106">Il cmdlet **Get-AzureRmHDInsightScriptActionHistory** ottiene la cronologia delle azioni di script per un cluster HDInsight di Azure e la elenca in ordine cronologico inverso o ottiene i dettagli di un'azione di script eseguita in precedenza.</span><span class="sxs-lookup"><span data-stu-id="0e51e-106">The **Get-AzureRmHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="0e51e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0e51e-107">EXAMPLES</span></span>

### <span data-ttu-id="0e51e-108">Esempio 1: ottenere la cronologia delle esecuzioni di azioni di script per un cluster</span><span class="sxs-lookup"><span data-stu-id="0e51e-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="0e51e-109">Questo comando consente di ottenere la cronologia delle azioni di script per il cluster ur-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="0e51e-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="0e51e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0e51e-110">PARAMETERS</span></span>

### <span data-ttu-id="0e51e-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="0e51e-111">-ClusterName</span></span>
<span data-ttu-id="0e51e-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="0e51e-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="0e51e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e51e-113">-ResourceGroupName</span></span>
<span data-ttu-id="0e51e-114">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0e51e-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0e51e-115">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="0e51e-115">-ScriptExecutionId</span></span>
<span data-ttu-id="0e51e-116">Specifica l'ID di esecuzione dell'azione di script eseguito.</span><span class="sxs-lookup"><span data-stu-id="0e51e-116">Specifies the execution ID of the executed script action.</span></span>

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

### <span data-ttu-id="0e51e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e51e-117">-DefaultProfile</span></span>
<span data-ttu-id="0e51e-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0e51e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e51e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e51e-119">CommonParameters</span></span>
<span data-ttu-id="0e51e-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e51e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e51e-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e51e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e51e-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0e51e-122">INPUTS</span></span>

## <span data-ttu-id="0e51e-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0e51e-123">OUTPUTS</span></span>

### <span data-ttu-id="0e51e-124">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionDetail]</span><span class="sxs-lookup"><span data-stu-id="0e51e-124">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail]</span></span>

## <span data-ttu-id="0e51e-125">Note</span><span class="sxs-lookup"><span data-stu-id="0e51e-125">NOTES</span></span>

## <span data-ttu-id="0e51e-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0e51e-126">RELATED LINKS</span></span>

