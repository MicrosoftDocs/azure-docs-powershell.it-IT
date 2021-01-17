---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: b5d62e963bdd2f30ab0c5b821854ee46b391376b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473814"
---
# <span data-ttu-id="e7fe3-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="e7fe3-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="e7fe3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e7fe3-102">SYNOPSIS</span></span>
<span data-ttu-id="e7fe3-103">Ottiene le azioni di script permanenti per un cluster e le elenca in ordine cronologico oppure restituisce i dettagli per un'azione di script persistente specificata.</span><span class="sxs-lookup"><span data-stu-id="e7fe3-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="e7fe3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7fe3-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7fe3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7fe3-105">DESCRIPTION</span></span>
<span data-ttu-id="e7fe3-106">Il cmdlet **Get-AzHDInsightPersistedScriptAction** ottiene le azioni di script permanenti per un cluster HDInsight di Azure e le elenca in ordine cronologico oppure restituisce i dettagli per un'azione di script persistente specificata.</span><span class="sxs-lookup"><span data-stu-id="e7fe3-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="e7fe3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7fe3-107">EXAMPLES</span></span>

### <span data-ttu-id="e7fe3-108">Esempio 1: ottenere le azioni di script permanenti in un cluster</span><span class="sxs-lookup"><span data-stu-id="e7fe3-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="e7fe3-109">Questo comando ottiene le azioni di script permanenti nel cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="e7fe3-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="e7fe3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e7fe3-110">PARAMETERS</span></span>

### <span data-ttu-id="e7fe3-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="e7fe3-111">-ClusterName</span></span>
<span data-ttu-id="e7fe3-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="e7fe3-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e7fe3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7fe3-113">-DefaultProfile</span></span>
<span data-ttu-id="e7fe3-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e7fe3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7fe3-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e7fe3-115">-Name</span></span>
<span data-ttu-id="e7fe3-116">Specifica il nome dell'azione di script persistente.</span><span class="sxs-lookup"><span data-stu-id="e7fe3-116">Specifies the name of the persisted script action.</span></span>

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

### <span data-ttu-id="e7fe3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7fe3-117">-ResourceGroupName</span></span>
<span data-ttu-id="e7fe3-118">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e7fe3-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e7fe3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7fe3-119">CommonParameters</span></span>
<span data-ttu-id="e7fe3-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7fe3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7fe3-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7fe3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7fe3-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e7fe3-122">INPUTS</span></span>

### <span data-ttu-id="e7fe3-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e7fe3-123">None</span></span>

## <span data-ttu-id="e7fe3-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7fe3-124">OUTPUTS</span></span>

### <span data-ttu-id="e7fe3-125">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="e7fe3-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="e7fe3-126">Note</span><span class="sxs-lookup"><span data-stu-id="e7fe3-126">NOTES</span></span>

## <span data-ttu-id="e7fe3-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7fe3-127">RELATED LINKS</span></span>

[<span data-ttu-id="e7fe3-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="e7fe3-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="e7fe3-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="e7fe3-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


