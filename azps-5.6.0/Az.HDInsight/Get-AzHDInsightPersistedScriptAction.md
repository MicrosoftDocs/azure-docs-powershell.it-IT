---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 136099b4fb37952825afbf82ba99a11695b901a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009102"
---
# <span data-ttu-id="b6cb7-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="b6cb7-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="b6cb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="b6cb7-103">Recupera le azioni degli script persistenti per un cluster ed elencale in ordine cronologico oppure recupera i dettagli per un'azione di script persistente specificata.</span><span class="sxs-lookup"><span data-stu-id="b6cb7-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="b6cb7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6cb7-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6cb7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b6cb7-105">DESCRIPTION</span></span>
<span data-ttu-id="b6cb7-106">Il cmdlet **Get-AzHDInsightPersistedScriptAction** ottiene le azioni dello script persistente per un cluster Azure HDInsight ed elenca le azioni in ordine cronologico oppure recupera i dettagli per un'azione di script persistente specificata.</span><span class="sxs-lookup"><span data-stu-id="b6cb7-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="b6cb7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6cb7-107">EXAMPLES</span></span>

### <span data-ttu-id="b6cb7-108">Esempio 1: Ottenere le azioni dello script persistente in un cluster</span><span class="sxs-lookup"><span data-stu-id="b6cb7-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="b6cb7-109">Questo comando recupera le azioni degli script persistenti nel cluster denominato your-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="b6cb7-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="b6cb7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6cb7-110">PARAMETERS</span></span>

### <span data-ttu-id="b6cb7-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b6cb7-111">-ClusterName</span></span>
<span data-ttu-id="b6cb7-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="b6cb7-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="b6cb7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6cb7-113">-DefaultProfile</span></span>
<span data-ttu-id="b6cb7-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="b6cb7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6cb7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b6cb7-115">-Name</span></span>
<span data-ttu-id="b6cb7-116">Specifica il nome dell'azione script persistente.</span><span class="sxs-lookup"><span data-stu-id="b6cb7-116">Specifies the name of the persisted script action.</span></span>

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

### <span data-ttu-id="b6cb7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6cb7-117">-ResourceGroupName</span></span>
<span data-ttu-id="b6cb7-118">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b6cb7-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b6cb7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6cb7-119">CommonParameters</span></span>
<span data-ttu-id="b6cb7-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6cb7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6cb7-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b6cb7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6cb7-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="b6cb7-122">INPUTS</span></span>

### <span data-ttu-id="b6cb7-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b6cb7-123">None</span></span>

## <span data-ttu-id="b6cb7-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6cb7-124">OUTPUTS</span></span>

### <span data-ttu-id="b6cb7-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="b6cb7-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="b6cb7-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="b6cb7-126">NOTES</span></span>

## <span data-ttu-id="b6cb7-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6cb7-127">RELATED LINKS</span></span>

[<span data-ttu-id="b6cb7-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="b6cb7-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="b6cb7-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="b6cb7-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


