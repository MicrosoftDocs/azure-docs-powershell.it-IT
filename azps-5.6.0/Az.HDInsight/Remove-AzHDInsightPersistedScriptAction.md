---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: a7c5c9c2008839d4e90dd5f393fbe4acea0f78a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965886"
---
# <span data-ttu-id="79ba4-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="79ba4-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="79ba4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79ba4-102">SYNOPSIS</span></span>
<span data-ttu-id="79ba4-103">Rimuove un'azione di script persistente da un cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="79ba4-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="79ba4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79ba4-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79ba4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="79ba4-105">DESCRIPTION</span></span>
<span data-ttu-id="79ba4-106">Il cmdlet **Remove-AzHDInsightPersistedScriptAction** rimuove un'azione script persistente dall'elenco di azioni degli script persistenti del cluster Azure HDInsight specificato.</span><span class="sxs-lookup"><span data-stu-id="79ba4-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="79ba4-107">Lo script rimosso non verrà più eseguito quando il cluster viene ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="79ba4-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="79ba4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79ba4-108">EXAMPLES</span></span>

### <span data-ttu-id="79ba4-109">Esempio 1: Rimuovere un'azione script dall'elenco di azioni di script persistenti in un cluster</span><span class="sxs-lookup"><span data-stu-id="79ba4-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="79ba4-110">Questo comando rimuove l'azione script denominata Scriptaction dall'elenco di azioni di script persistenti nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="79ba4-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="79ba4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79ba4-111">PARAMETERS</span></span>

### <span data-ttu-id="79ba4-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="79ba4-112">-ClusterName</span></span>
<span data-ttu-id="79ba4-113">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="79ba4-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="79ba4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79ba4-114">-DefaultProfile</span></span>
<span data-ttu-id="79ba4-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="79ba4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79ba4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="79ba4-116">-Name</span></span>
<span data-ttu-id="79ba4-117">Specifica il nome dell'azione script persistente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="79ba4-117">Specifies the name of the persisted script action to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79ba4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79ba4-118">-ResourceGroupName</span></span>
<span data-ttu-id="79ba4-119">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="79ba4-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="79ba4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79ba4-120">CommonParameters</span></span>
<span data-ttu-id="79ba4-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79ba4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79ba4-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="79ba4-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79ba4-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="79ba4-123">INPUTS</span></span>

### <span data-ttu-id="79ba4-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="79ba4-124">None</span></span>

## <span data-ttu-id="79ba4-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79ba4-125">OUTPUTS</span></span>

### <span data-ttu-id="79ba4-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="79ba4-126">System.Void</span></span>

## <span data-ttu-id="79ba4-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="79ba4-127">NOTES</span></span>

## <span data-ttu-id="79ba4-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79ba4-128">RELATED LINKS</span></span>

[<span data-ttu-id="79ba4-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="79ba4-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="79ba4-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="79ba4-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


