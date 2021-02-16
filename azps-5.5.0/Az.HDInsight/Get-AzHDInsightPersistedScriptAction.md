---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: b5d62e963bdd2f30ab0c5b821854ee46b391376b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207346"
---
# <span data-ttu-id="63d13-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="63d13-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="63d13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63d13-102">SYNOPSIS</span></span>
<span data-ttu-id="63d13-103">Recupera le azioni degli script persistenti per un cluster ed elencale in ordine cronologico oppure recupera i dettagli per un'azione di script persistente specificata.</span><span class="sxs-lookup"><span data-stu-id="63d13-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="63d13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63d13-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63d13-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="63d13-105">DESCRIPTION</span></span>
<span data-ttu-id="63d13-106">Il cmdlet **Get-AzHDInsightPersistedScriptAction** ottiene le azioni dello script persistente per un cluster HDInsight di Azure ed elenca le azioni in ordine cronologico oppure ottiene i dettagli per un'azione di script persistente specificata.</span><span class="sxs-lookup"><span data-stu-id="63d13-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="63d13-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63d13-107">EXAMPLES</span></span>

### <span data-ttu-id="63d13-108">Esempio 1: Ottenere le azioni dello script persistente in un cluster</span><span class="sxs-lookup"><span data-stu-id="63d13-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="63d13-109">Questo comando recupera le azioni degli script persistenti nel cluster denominato your-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="63d13-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="63d13-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63d13-110">PARAMETERS</span></span>

### <span data-ttu-id="63d13-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="63d13-111">-ClusterName</span></span>
<span data-ttu-id="63d13-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="63d13-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="63d13-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63d13-113">-DefaultProfile</span></span>
<span data-ttu-id="63d13-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="63d13-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63d13-115">-Name</span><span class="sxs-lookup"><span data-stu-id="63d13-115">-Name</span></span>
<span data-ttu-id="63d13-116">Specifica il nome dell'azione script persistente.</span><span class="sxs-lookup"><span data-stu-id="63d13-116">Specifies the name of the persisted script action.</span></span>

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

### <span data-ttu-id="63d13-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63d13-117">-ResourceGroupName</span></span>
<span data-ttu-id="63d13-118">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="63d13-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="63d13-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63d13-119">CommonParameters</span></span>
<span data-ttu-id="63d13-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63d13-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63d13-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="63d13-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63d13-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="63d13-122">INPUTS</span></span>

### <span data-ttu-id="63d13-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="63d13-123">None</span></span>

## <span data-ttu-id="63d13-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63d13-124">OUTPUTS</span></span>

### <span data-ttu-id="63d13-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="63d13-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="63d13-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="63d13-126">NOTES</span></span>

## <span data-ttu-id="63d13-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63d13-127">RELATED LINKS</span></span>

[<span data-ttu-id="63d13-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="63d13-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="63d13-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="63d13-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


